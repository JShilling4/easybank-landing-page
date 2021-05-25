<template>
	<header class="header">
		<div class="outer-container">
			<img
				src="@/assets/images/logo.svg"
				alt="Manage logo"
				class="logo"
			/>

			<nav
				v-if="showMobileMenu"
				class="nav"
			>
				<a
					href="#"
					class="nav-item"
				>Home</a>
				<a
					href="#"
					class="nav-item"
				>About</a>
				<a
					href="#"
					class="nav-item"
				>Blog</a>
				<a
					href="#"
					class="nav-item"
				>Contact</a>
				<a
					href="#"
					class="nav-item"
				>Careers</a>
			</nav>

			<img
				v-if="showMobileMenu"
				src="@/assets/images/icon-close.svg"
				alt="close mobile menu icon"
				@click="$emit('close')"
				class="mobileClose"
			>
			<img
				v-else
				src="@/assets/images/icon-hamburger.svg"
				alt="mobile menu icon"
				@click="$emit('open')"
				class="hamburger"
			>

			<AppButton>Request Invite</AppButton>
		</div>
	</header>
</template>

<script>
export default {
	name: "TheNavbar",
	props: {
		showMobileMenu: {
			type: Boolean,
		},
	},
};
</script>

<style lang="scss" scoped>
.header {
	position: relative;
	z-index: 999;
	background-color: #fff;
	width: 100%;
    height: 10rem;
	@include breakpoint(mobile) {
		height: 7rem;
	}
	.outer-container {
		display: flex;
		align-items: center;
		justify-content: space-between;
        height: 100%;
	}
	.logo {
		width: 15rem;
	}
	.nav {
		@include breakpoint(tablet-land) {
			position: absolute;
			display: flex;
			flex-direction: column;
			background-color: #fff;
			width: 85%;
			top: 12rem;
			padding: 4rem 2rem;
			left: 50%;
			transform: translateX(-50%);
			box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.3);
			text-align: center;
		}
		@include breakpoint(mobile) {
			top: 10rem;
		}
		.nav-item {
			margin: 0 1.85rem;
			font-size: 1.8rem;
			font-weight: 700;
			color: $blue-dark;
			transition: color 0.3s;
			@include breakpoint(tablet-land) {
				margin: 0;
				padding: 3rem 0;
				font-weight: 600;
				font-size: 2.3rem;
			}
			@include breakpoint(mobile) {
				font-size: 1.8rem;
			}
			&:hover {
				color: lighten(#333, 40%);
			}
		}
	}
	button {
		@include breakpoint(laptop) {
			display: none;
		}
	}
	.hamburger {
		display: none;
		@include breakpoint(ipadPro) {
			display: block;
		}
	}
	.mobileClose {
		@media screen and (min-width: 769px) {
			display: none;
		}
	}
}
</style>