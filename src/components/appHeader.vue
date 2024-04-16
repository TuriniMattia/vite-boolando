<template>
	<div>
		<header class="page-header">
			<nav class="container">
				<div class="row">
					<ul class="row">
						<li v-for="(link, i) in menu " ::key="i">{{ link.text }}</li>

					</ul>

					<a class="logo" href="#">
						<img src="/boolean-logo.png" alt="" />
					</a>

					<ul class="row">
						<li><a href=""><i class="fa-regular fa-user"></i></a></li>
						<li><a href=""><i class="fa-regular fa-heart"></i></a></li>
						<li><a href=""><i class="fa-solid fa-bag-shopping"></i></a></li>
					</ul>
				</div>
			</nav>
		</header>

	</div>
</template>

<script>
export default {
	data() {
		return {
			menu: [
				{
					text: 'Donna',
					href: '#',

				},
				{
					text: 'Uomo',
					href: '#',

				},
				{
					text: 'Bambini',
					href: '#',

				},
			],
		}
	}
}
</script>

<style lang="scss" scoped>
.page-header {
	background-color: #FF6900;
	color: white;
	padding: 12px 0;
}


.logo img {
	height: 36px;
}
</style>