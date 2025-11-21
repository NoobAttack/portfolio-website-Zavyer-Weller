<template>
	<div class="portfolio">
		<h1>My Portfolio</h1>
		<p class="subtitle">A collection of my GitHub repositories</p>

		<!-- Loading State -->
		<div v-if="loading" class="loading">
			<div class="spinner"></div>
			<p>Loading repositories...</p>
		</div>

		<!-- Error State -->
		<div v-else-if="error" class="error">
			<h2>Oops! Something went wrong</h2>
			<p>{{ error }}</p>
			<button @click="fetchRepositories" class="retry-btn">Try Again</button>
		</div>

		<!-- Repository List -->
		<div v-else-if="repositories.length > 0" class="repositories">
			<div v-for="repo in repositories" :key="repo.id" class="repo-card">
				<h2 class="repo-name">
					<a :href="repo.html_url" target="_blank" rel="noopener noreferrer">
						{{ repo.name }}
					</a>
				</h2>
				<p class="repo-description">
					{{ repo.description || 'No description available' }}
				</p>
				<div class="repo-meta">
					<span v-if="repo.language" class="repo-language">
						<span class="language-dot"></span>
						{{ repo.language }}
					</span>
					<span class="repo-updated">
						Updated: {{ formatDate(repo.updated_at) }}
					</span>
				</div>
			</div>
		</div>

		<!-- Empty State -->
		<div v-else class="empty">
			<p>No repositories found.</p>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Portfolio',
	data() {
		return {
			repositories: [],
			loading: true,
			error: null,
			// IMPORTANT: Update this with your actual GitHub username
			// Example: githubUsername: 'your-github-username'
			githubUsername: 'zwell',
		};
	},
	mounted() {
		this.fetchRepositories();
	},
	methods: {
		async fetchRepositories() {
			this.loading = true;
			this.error = null;
			try {
				const response = await fetch(
					`https://api.github.com/users/${this.githubUsername}/repos`
				);
				if (!response.ok) {
					throw new Error(
						`Failed to fetch repositories: ${response.statusText}`
					);
				}
				const data = await response.json();
				this.repositories = data.sort(
					(a, b) => new Date(b.updated_at) - new Date(a.updated_at)
				);
			} catch (err) {
				this.error =
					err.message || 'Unable to load repositories. Please try again later.';
				console.error('Error fetching repositories:', err);
			} finally {
				this.loading = false;
			}
		},
		formatDate(dateString) {
			const date = new Date(dateString);
			return date.toLocaleDateString('en-US', {
				year: 'numeric',
				month: 'long',
				day: 'numeric',
			});
		},
	},
};
</script>

<style scoped>
.portfolio {
	max-width: 1200px;
	margin: 0 auto;
	padding: 40px 20px;
	min-height: calc(100vh - 200px);
}

h1 {
	font-size: 2.5rem;
	margin-bottom: 10px;
	color: #2c3e50;
}

.subtitle {
	font-size: 1.1rem;
	color: #666;
	margin-bottom: 40px;
}

/* Loading State */
.loading {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	padding: 60px 20px;
}

.spinner {
	border: 4px solid #f3f3f3;
	border-top: 4px solid #42b983;
	border-radius: 50%;
	width: 50px;
	height: 50px;
	animation: spin 1s linear infinite;
	margin-bottom: 20px;
}

@keyframes spin {
	0% {
		transform: rotate(0deg);
	}
	100% {
		transform: rotate(360deg);
	}
}

/* Error State */
.error {
	text-align: center;
	padding: 60px 20px;
	color: #e74c3c;
}

.error h2 {
	margin-bottom: 15px;
}

.retry-btn {
	margin-top: 20px;
	padding: 10px 20px;
	background-color: #42b983;
	color: white;
	border: none;
	border-radius: 5px;
	cursor: pointer;
	font-size: 1rem;
	transition: background-color 0.3s;
}

.retry-btn:hover {
	background-color: #35a372;
}

/* Repository List */
.repositories {
	display: grid;
	grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
	gap: 30px;
	margin-top: 30px;
}

.repo-card {
	background: white;
	border: 1px solid #e1e8ed;
	border-radius: 8px;
	padding: 25px;
	transition: transform 0.2s, box-shadow 0.2s;
	text-align: left;
}

.repo-card:hover {
	transform: translateY(-5px);
	box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.repo-name {
	margin: 0 0 15px 0;
	font-size: 1.5rem;
}

.repo-name a {
	color: #42b983;
	text-decoration: none;
	transition: color 0.2s;
}

.repo-name a:hover {
	color: #35a372;
	text-decoration: underline;
}

.repo-description {
	color: #666;
	margin-bottom: 20px;
	line-height: 1.6;
	min-height: 48px;
}

.repo-meta {
	display: flex;
	justify-content: space-between;
	align-items: center;
	flex-wrap: wrap;
	gap: 10px;
	font-size: 0.9rem;
	color: #888;
}

.repo-language {
	display: flex;
	align-items: center;
	gap: 6px;
}

.language-dot {
	width: 12px;
	height: 12px;
	border-radius: 50%;
	background-color: #42b983;
	display: inline-block;
}

.repo-updated {
	font-size: 0.85rem;
}

/* Empty State */
.empty {
	text-align: center;
	padding: 60px 20px;
	color: #888;
}

/* Responsive Design */
@media (max-width: 768px) {
	.portfolio {
		padding: 20px 15px;
	}

	h1 {
		font-size: 2rem;
	}

	.repositories {
		grid-template-columns: 1fr;
		gap: 20px;
	}

	.repo-card {
		padding: 20px;
	}

	.repo-meta {
		flex-direction: column;
		align-items: flex-start;
	}
}

@media (max-width: 480px) {
	h1 {
		font-size: 1.75rem;
	}

	.subtitle {
		font-size: 1rem;
	}
}
</style>
