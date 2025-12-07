<template>
  <div class="home-view">
    <div class="container hero-section">
      <div class="text-center">
        <img
          src="../assets/profilepic.jpg"
          alt="A professional headshot of Zavyer Weller"
          class="profile-image mb-4"
        />
        <h1 class="hero-title">
          Hello, my name is <span class="accent-text">Zavyer</span> <br />
          Weller and I am learning coding everyday
        </h1>
        <p class="hero-description mx-auto">
          I hope to improve my coding abilities each day
        </p>
        <div class="hero-buttons mt-4">
          <router-link to="/about" class="btn-primary">Learn More</router-link>
          <router-link to="/portfolio" class="btn-secondary">View Portfolio</router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView'
}
</script>

<style scoped>
.home-view {
	min-height: calc(100vh - 100px);
	display: flex;
	align-items: center;
	justify-content: center;
	padding: 2rem 0;
}

:root {
	--primary-bg: #0a192f;
	--secondary-text: #8892b0;
	--tea-green: hsla(75, 83%, 84%, 1);
	--accent-color: var(--tea-green);
	--main-text: #e6f1ff;
	--mindaro: hsla(75, 68%, 70%, 1);
	--shadow-md: 0 4px 16px rgba(0, 0, 0, 0.2);
	--shadow-lg: 0 8px 32px rgba(0, 0, 0, 0.3);
	--shadow-accent: 0 0 20px rgba(204, 214, 161, 0.3);
	--transition-normal: 0.3s ease;
}

.hero-section {
	min-height: 100vh;
	display: flex;
	align-items: center;
	justify-content: center;
	position: relative;
	padding: 2rem 0;
}

.profile-image {
	width: 180px;
	height: 180px;
	border-radius: 50%;
	border: 4px solid var(--accent-color);
	object-fit: cover;
	box-shadow: var(--shadow-accent), var(--shadow-lg);
	transition: all 0.5s ease;
	animation: float 3s ease-in-out infinite;
}

@keyframes float {
	0%, 100% {
		transform: translateY(0px);
	}
	50% {
		transform: translateY(-10px);
	}
}

.profile-image:hover {
	transform: translateY(-10px) scale(1.05);
	box-shadow: 0 0 30px rgba(204, 214, 161, 0.5), var(--shadow-lg);
}

.hero-title {
	color: var(--main-text);
	font-weight: 800;
	font-size: 3.5rem;
	margin-bottom: 1.5rem;
	line-height: 1.2;
	letter-spacing: -1px;
}

.accent-text {
	color: var(--accent-color);
	background: linear-gradient(135deg, var(--accent-color) 0%, var(--mindaro) 100%);
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
	background-clip: text;
}

.hero-description {
	font-size: 1.25rem;
	color: var(--secondary-text);
	margin-top: 1rem;
	max-width: 600px;
}

.hero-buttons {
	display: flex;
	gap: 1rem;
	justify-content: center;
	flex-wrap: wrap;
}

.btn-primary,
.btn-secondary {
	padding: 0.75rem 2rem;
	border-radius: 8px;
	font-weight: 600;
	font-size: 1rem;
	text-decoration: none;
	transition: all var(--transition-normal);
	display: inline-block;
	border: 2px solid transparent;
}

.btn-primary {
	background: linear-gradient(135deg, var(--accent-color) 0%, var(--mindaro) 100%);
	color: var(--primary-bg);
	border: 2px solid var(--accent-color);
	box-shadow: var(--shadow-md);
}

.btn-primary:hover {
	transform: translateY(-3px);
	box-shadow: var(--shadow-lg), var(--shadow-accent);
	color: var(--primary-bg);
}

.btn-secondary {
	background: transparent;
	color: var(--accent-color);
	border: 2px solid var(--accent-color);
}

.btn-secondary:hover {
	background: rgba(204, 214, 161, 0.1);
	transform: translateY(-3px);
	box-shadow: var(--shadow-md);
}

@media (max-width: 768px) {
	.hero-title {
		font-size: 2rem;
	}

	.profile-image {
		width: 150px;
		height: 150px;
	}

	.hero-buttons {
		flex-direction: column;
		align-items: center;
	}

	.btn-primary,
	.btn-secondary {
		width: 100%;
		max-width: 250px;
		text-align: center;
	}
}
</style>
