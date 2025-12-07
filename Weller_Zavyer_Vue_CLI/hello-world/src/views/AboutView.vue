<template>
	<div class="about-view">
		<div class="container about-section py-5">
			<div class="row">
				<div class="col-12 text-center mb-4">
					<h2 class="main-title">About Me</h2>
				</div>
			</div>
			<div class="row g-4 mt-2">
				<div class="col-md-4">
					<div class="about-card">
						<div class="about-card-icon">👨‍🎓</div>
						<h3 class="about-card-title">Student & Learner</h3>
						<p class="about-card-text">
							I'm Zavyer Weller, a student learning new skills every day.
						</p>
					</div>
				</div>
				<div class="col-md-4">
					<div class="about-card">
						<div class="about-card-icon">🚀</div>
						<h3 class="about-card-title">Building Projects</h3>
						<p class="about-card-text">
							I enjoy building small projects to improve my skills.
						</p>
					</div>
				</div>
				<div class="col-md-4">
					<div class="about-card">
						<div class="about-card-icon">💻</div>
						<h3 class="about-card-title">Technologies</h3>
						<p class="about-card-text">
							Learning HTML, CSS, JavaScript, Vue.js, Git, GitHub, and Bootstrap.
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<style scoped>
.about-view {
	min-height: calc(100vh - 100px);
	padding: 2rem 0;
}

:root {
	--primary-bg: #0a192f;
	--secondary-bg: #112240;
	--secondary-text: #8892b0;
	--tea-green: hsla(75, 83%, 84%, 1);
	--accent-color: var(--tea-green);
	--accent-hover: hsla(75, 83%, 74%, 1);
	--main-text: #e6f1ff;
	--card-bg: rgba(17, 34, 64, 0.5);
	--shadow-lg: 0 8px 32px rgba(0, 0, 0, 0.3);
	--shadow-accent: 0 0 20px rgba(204, 214, 161, 0.3);
	--transition-normal: 0.3s ease;
}

.about-section {
	background: var(--card-bg);
	backdrop-filter: blur(10px);
	border-radius: 16px;
	margin: 2rem auto;
	max-width: 1200px;
	color: var(--main-text);
	border: 1px solid rgba(136, 146, 176, 0.1);
	box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
	padding: 3rem 2rem !important;
	position: relative;
	overflow: hidden;
}

.about-section::before {
	content: '';
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 4px;
	background: linear-gradient(90deg, var(--accent-color) 0%, hsla(75, 68%, 70%, 1) 100%);
}

.main-title {
	color: var(--main-text);
	font-weight: 700;
	font-size: 2.5rem;
	margin-bottom: 1.5rem;
	position: relative;
	display: inline-block;
}

.main-title::after {
	content: '';
	position: absolute;
	bottom: -10px;
	left: 50%;
	transform: translateX(-50%);
	width: 60px;
	height: 3px;
	background: linear-gradient(90deg, var(--accent-color) 0%, hsla(75, 68%, 70%, 1) 100%);
	border-radius: 2px;
}

.about-card {
	background: rgba(17, 34, 64, 0.6);
	backdrop-filter: blur(10px);
	border: 1px solid rgba(136, 146, 176, 0.15);
	border-radius: 12px;
	padding: 2rem 1.5rem;
	height: 100%;
	transition: all var(--transition-normal);
	text-align: center;
	position: relative;
	overflow: hidden;
}

.about-card::before {
	content: '';
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 3px;
	background: linear-gradient(90deg, var(--accent-color) 0%, hsla(75, 68%, 70%, 1) 100%);
	transform: scaleX(0);
	transition: transform var(--transition-normal);
}

.about-card:hover {
	transform: translateY(-8px);
	box-shadow: var(--shadow-lg), var(--shadow-accent);
	border-color: rgba(204, 214, 161, 0.3);
	background: rgba(17, 34, 64, 0.8);
}

.about-card:hover::before {
	transform: scaleX(1);
}

.about-card-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
	display: block;
	transition: transform var(--transition-normal);
}

.about-card:hover .about-card-icon {
	transform: scale(1.1) rotate(5deg);
}

.about-card-title {
	color: var(--main-text);
	font-size: 1.25rem;
	font-weight: 600;
	margin-bottom: 1rem;
	letter-spacing: -0.3px;
}

.about-card-text {
	color: var(--secondary-text);
	font-size: 0.95rem;
	line-height: 1.6;
	margin: 0;
}

@media (max-width: 768px) {
	.about-section {
		padding: 2rem 1.5rem !important;
	}

	.main-title {
		font-size: 2rem;
	}

	.about-card {
		padding: 1.5rem 1.25rem;
		margin-bottom: 1rem;
	}
}
</style>
