<template>
	<div class="about">
		<div class="profile">
			<img
				class="headshot"
				src="/pictures/profilepic.jpg"
				alt="Professional headshot"
			/>
			<div class="bio">
				<h1>Zavyer Weller</h1>
				<p>
					Brief professional summary. Replace this text with your own headline
					and short bio.
				</p>
			</div>
		</div>
	</div>
</template>

<style scoped>
.about {
	max-width: 900px;
	margin: 40px auto;
	padding: 20px;
}
.profile {
	display: flex;
	align-items: center;
	gap: 20px;
}
.headshot {
	width: 140px;
	height: 140px;
	object-fit: cover;
	border-radius: 50%;
	border: 3px solid #e6e6e6;
}
.bio h1 {
	margin: 0 0 8px 0;
	font-size: 1.6rem;
}
.bio p {
	margin: 0;
	color: #555;
}

@media (max-width: 600px) {
	.profile {
		flex-direction: column;
		text-align: center;
	}
}
</style>
