<template>
    <div class="container m-auto">
        <div class="title text-center mt-4 mb-3 d-flex justify-content-center" >
            <h1 class="display-4 lh-lg border-bottom w-75">Socials</h1>
        </div>
        <div class="row">
            <div class="col-lg-12 text-center">
                <figure class="text-center">
                    <blockquote class="blockquote">
                        <p class="lead">I'M NOT HIKIKOMORI, I have social media too.</p>
                        <p class="lead">You can add me as friend or follow my account below</p>
                    </blockquote>
                </figure>
            </div>
            <div class="col-lg-12 row">
                <div class="col-lg-4 mt-2 mb-2"  v-for="social in topSocials" :key="social.name">
                    <div class="card bg-dark text-white">
											<img :src="social.thumbnail" class="card-img  opacity-50 fit" :alt="social.socialMedia" style="height: 200px">
											<div class="card-img-overlay">
													<h4 class="card-title text-decoration-underline">{{social.socialMedia}}</h4>
													<p class="h6">{{social.name}}</p>
													<p>{{social.accountId}}</p>
													<button v-if="social.link" type="button" class="btn btn-outline-light" @click="gotoLink('https://discordapp.com/users/470781596912451585')">Add Me</button>
													<button v-else type="button" class="btn btn-outline-light" data-bs-toggle="modal" data-bs-target="#exampleModal">Add Me</button>
											</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
	setup(){
		const topSocials = [
			{
				socialMedia: 'Discord',
        name: 'Ichinomiya Mori',
				accountId : 'ichinomiyamori#9166',
        thumbnail: 'assets/discord.webp',
				link: 'https://discordapp.com/users/470781596912451585'
      },
      {
				socialMedia: 'LINE',
        name: 'Ichinomiya Mori',
				accountId : '@1nomiyaMori26',
        thumbnail: 'assets/line.webp',
				link: null
      },
      {
				socialMedia: 'CryptoGram',
        name: 'Ichinomiya Mori',
				accountId: '@ichinomiya.mori',
        thumbnail: 'assets/radu-marcusu-mbKApJz6RSU-unsplash.webp',
				link: null
      },
		]

		const gotoLink = (link) =>{
			window.location.href = link
		}
		return {topSocials, gotoLink}
	}
}
</script>

<style>

</style>