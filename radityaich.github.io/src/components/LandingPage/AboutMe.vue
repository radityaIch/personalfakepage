<template>
  <div class="container m-auto pt-4 pb-4">
    <div class="title text-center mt-4 d-flex justify-content-center">
      <h1 class="display-4 lh-lg border-bottom w-50">About Me</h1>
    </div>
    <div class="card-layout row">
      <div class="col-lg-12">
        <figure class="text-center">
          <blockquote class="blockquote">
            <p>A Simple Man who likes about programming especialy web tech like NodeJS {Vue, Express, Adonis, etc}</p>
            <p class="h6">My Favorite Things To-Do</p>
          </blockquote>
        </figure>
      </div>

      <div class="col-lg-12">
        <div class="row m-auto">

          <div class="col-lg-4" v-for="todo in favoritesThing" :key="todo.activity">
            <div class="card" style="width: 100%;">
              <img :src="todo.thumbnail" class="card-img-top fit" alt="Item" style="height: 14rem">
              <div class="card-body">
                <h5 class="card-title">{{todo.activity}}</h5>
                <p class="card-text">{{todo.description}}</p>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'AboutMe',
    setup(){
      const favoritesThing = [
        {
          activity: 'Coding',
          thumbnail: 'assets/alvaro-reyes-fSWOVc3e06w-unsplash.webp',
          description: 'Yeah, Coding is my passion. Everytime and everywhere i always do a lot solving problem challenge. Sometimes i invite my friend to join for solving the challenge'
        },
        {
          activity: 'Badminton',
          thumbnail: 'assets/frame-harirak-UR_mNYmpwco-unsplash.webp',
          description: 'Not only coding. Sometimes I invite my friend to play badminton together. That\'s so fun because it can relieve stress after study & coding everyday'
        },
        {
          activity: 'OSU!',
          thumbnail: 'assets/wallpaperflare.com_wallpaper.webp',
          description: 'This rhythm game always accompany me when I got stuck at my task or coding challenge. And OSU! can make me typing so fast'
        }
      ]
      return{favoritesThing}
    }
}
</script>

<style>

</style>