<template>
	<div class="home">
		<section class="hero">
			<div class="hero__outer-container outer-container">
				<div class="col-1">
					<h1 class="hero__heading">
						Next generation digital banking
					</h1>
					<p class="hero__copy copy">
						Take your financial life online. Your Easybank account will be a one-stop-shop for spending, saving, budgeting, investing, and much more.
					</p>
					<AppButton class="hero__cta">Request Invite</AppButton>
				</div>

				<div class="col-2">
					<div class="overlay"></div>
					<img
						src="@/assets/images/image-mockups.png"
						class="mockups"
						alt=""
					>
				</div>
			</div>
		</section>

		<section class="whyEasybank">
			<div class="outer-container">
				<div class="top">
					<h2 class="section-heading">
						Why choose Easybank?
					</h2>
					<p class="whyEasybank__copy copy">
						We leverage Open Banking to turn your bank account into your financial hub.
						Control your finances like never before.
					</p>
				</div>

				<div class="feature-container">
					<div class="feature">
						<img
							src="@/assets/images/icon-online.svg"
							class="feature__icon"
							alt=""
						>
						<h3 class="feature__heading">
							Online Banking
						</h3>
						<p class="feature__copy copy">
							Our modern web and mobile applications allow you to keep track of your
							finances wherever you are in the world.
						</p>
					</div>
					<div class="feature">
						<img
							src="@/assets/images/icon-budgeting.svg"
							class="feature__icon"
							alt=""
						>
						<h3 class="feature__heading">
							Simple Budgeting
						</h3>
						<p class="feature__copy copy">
							See exactly where your money goes each month. Receive notifications when
							you're close to hitting your limits.
						</p>
					</div>
					<div class="feature">
						<img
							src="@/assets/images/icon-onboarding.svg"
							class="feature__icon"
							alt=""
						>
						<h3 class="feature__heading">
							Fast Onboarding
						</h3>
						<p class="feature__copy copy">
							We don’t do branches. Open your account in minutes online and start taking control
							of your finances right away.
						</p>
					</div>
					<div class="feature">
						<img
							src="@/assets/images/icon-api.svg"
							class="feature__icon"
							alt=""
						>
						<h3 class="feature__heading">
							Open API
						</h3>
						<p class="feature__copy copy">
							Manage your savings, investments, pension, and much more from one account. Tracking
							your money has never been easier.
						</p>
					</div>
				</div>
			</div>
		</section>

		<section class="articles">
			<div class="outer-container">
				<h2 class="section-heading">
					Latest Articles
				</h2>
				<div class="articles-container">
					<div class="article">
						<img
							src="@/assets/images/image-currency.jpg"
							alt=""
						>

						<div class="details">
							<span class="details__author">
								By Claire Robinson
							</span>
							<h3 class="details__heading">
								Receive money in any currency with no fees
							</h3>
							<p class="details__copy copy">
								The world is getting smaller and we’re becoming more mobile. So why should you be
								forced to only receive money in a single …
							</p>
						</div>
					</div>
					<div class="article">
						<img
							src="@/assets/images/image-restaurant.jpg"
							alt=""
						>

						<div class="details">
							<span class="details__author">
								By Wilson Hunter
							</span>
							<h3 class="details__heading">
								Treat yourself without worrying about money
							</h3>
							<p class="details__copy copy">
								Our simple budgeting feature allows you to separate out your spending and set
								realistic limits each month. That means you …
							</p>
						</div>
					</div>
					<div class="article">
						<img
							src="@/assets/images/image-plane.jpg"
							alt=""
						>

						<div class="details">
							<span class="details__author">
								By Wilson Hunter
							</span>
							<h3 class="details__heading">
								Take your Easybank card wherever you go
							</h3>
							<p class="details__copy copy">
								We want you to enjoy your travels. This is why we don’t charge any fees on purchases
								while you’re abroad. We’ll even show you …
							</p>
						</div>
					</div>
					<div class="article">
						<img
							src="@/assets/images/image-confetti.jpg"
							alt=""
						>

						<div class="details">
							<span class="details__author">
								By Claire Robinson
							</span>
							<h3 class="details__heading">
								Our invite-only Beta accounts are now live!
							</h3>
							<p class="details__copy copy">
								After a lot of hard work by the whole team, we’re excited to launch our closed beta.
								It’s easy to request an invite through the site ...
							</p>
						</div>
					</div>
				</div>
			</div>
		</section>
	</div>
</template>

<script>
export default {
	name: "Home",
	components: {},
};
</script>

<style lang="scss" scoped>
.home {
    overflow-x: hidden;
}
.section-heading {
	margin-bottom: 3rem;
	font-size: 4.8rem;
	font-weight: 400;
	color: #333;
}
.copy {
	color: $gray-blue;
	font-weight: 400;
	font-size: 2.2rem;
	line-height: 1.5;
}

.hero {
	position: relative;
	height: 80rem;
	max-width: 100%;
	background-color: $gray-extra-light;
	@include breakpoint(ipadPro) {
		height: 55rem;
	}
	@include breakpoint(tablet-land) {
		height: 55rem;
	}

	&__outer-container {
		display: flex;
		align-items: center;
		height: 100%;
	}
	&__heading {
		margin-bottom: 3.7rem;
		font-weight: 300;
		font-size: 6.6rem;
		color: #333;
		@include breakpoint(desktop) {
			font-size: 6rem;
		}
		@include breakpoint(ipadPro) {
			font-size: 5.5rem;
		}
	}
	&__copy {
		margin-bottom: 4.5rem;
	}
	.col-1 {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
		width: 40%;
        height: 100%;
        @include breakpoint(desktop) {
            width: 50%;
        }
	}
	.col-2 {
		position: absolute;
        right: 0;
        width: 60%;
        height: 100%;
		.overlay {
			width: 100%;
			height: 100%;
			background-image: url("~@/assets/images/bg-intro-desktop.svg");
			background-size: cover;
			background-position: 100px -225px;
			background-size: 112%;
			background-repeat: no-repeat;
			@include breakpoint(ipadPro) {
				background-position: 75px -50px;
                background-size: 120%;
			}
		}
		img.mockups {
			position: absolute;
			top: -20%;
			right: -10%;
			width: 85%;
			z-index: 2;
			@include breakpoint(desktop) {
				top: -5%;
			}
		}
	}
}

.whyEasybank {
	padding: 12rem 0 6rem;
	background-color: $gray-blue-light;
	.top {
		width: 60%;
		@include breakpoint(ipadPro) {
			margin: 0 auto;
			width: 80%;
			text-align: center;
		}
	}
	.copy {
		margin-bottom: 8rem;
	}
	.feature-container {
		display: flex;
		@include breakpoint(ipadPro) {
			flex-wrap: wrap;
			justify-content: center;
		}
		.feature {
			width: 25%;
			@include breakpoint(ipadPro) {
				width: 40%;
				text-align: center;
				padding: 0 3rem;
			}
			&:not(:last-child) {
				margin-right: 2rem;
			}
			&__icon {
				margin-bottom: 3rem;
				width: 9rem;
			}
			&__heading {
				margin-bottom: 3rem;
				font-size: 2.8rem;
				font-weight: 400;
				color: #333;
			}
			&__copy {
				font-size: 2rem;
				@include breakpoint(desktop) {
					font-size: 1.6rem;
				}
			}
		}
	}
}

.articles {
	padding: 12rem 0;
	background-color: $gray-extra-light;
	.articles-container {
		display: flex;
		@include breakpoint(ipadPro) {
			flex-wrap: wrap;
			justify-content: center;
		}
	}
	.section-heading {
		margin-bottom: 6rem;
		@include breakpoint(ipadPro) {
			text-align: center;
		}
	}
	.article {
		width: 25%;
		background-color: #fff;
		box-shadow: 0 1rem 1.25rem rgba(0, 0, 0, 0.3);
		border-radius: 3px;
		transform: scale(0.95);
		transition: transform 0.5s, box-shadow 0.5s;
		backface-visibility: hidden;
		will-change: transform, box-shadow;
		cursor: pointer;
		@include breakpoint(ipadPro) {
			width: 40%;
			margin: 0 2rem 4rem;
		}
		&:hover {
			transform: scale(1) translateY(-1rem);
			box-shadow: 0 1.5rem 2.25rem rgba(0, 0, 0, 0.25);
		}
		&:not(:last-child) {
			margin-right: 2rem;
		}
		img {
			object-fit: cover;
			width: 100%;
			height: 20rem;
			border-top-right-radius: 3px;
			border-top-left-radius: 3px;
		}
		.details {
			padding: 3rem;
			&__author {
				display: inline-block;
				margin-bottom: 2rem;
				font-size: 1.4rem;
				color: $gray-blue;
			}
			&__heading {
				margin-bottom: 1.5rem;
				font-weight: 400;
			}
			&__copy {
				font-size: 1.6rem;
			}
		}
	}
}
</style>
