<template>
  <div class="container m-auto">
    <div class="title text-center mt-4 d-flex justify-content-center" >
      <h1 class="display-4 lh-lg border-bottom w-75">My Projects (With Team Too..)</h1>
    </div>
    <div class="card-layout row">
      <div class="col-lg-12">
        <figure class="text-center">
          <blockquote class="blockquote">
            <p>All of the project made by myself or working with team</p>
            <p class="h6">Here's top 4 of My Projects</p>
          </blockquote>
        </figure>
      </div>

      <div class="col-lg-12">
        <div class="row m-auto">

          <div class="col-lg-6 mt-2 mb-2"  v-for="project in topProjects" :key="project.name">
            <div class="card bg-dark text-white">
              <img :src="project.thumbnail" class="card-img  opacity-50 fit" alt="..." style="height: 240px">
              <div class="card-img-overlay">
                <h5 class="card-title">{{project.name}}</h5>
                <p class="card-text">{{project.description}}</p>
                <p class="card-text">Last updated 3 mins ago</p>
                <button type="button" class="btn btn-outline-light" data-bs-toggle="modal" data-bs-target="#exampleModal">Details</button>
              </div>
              <div class="card-footer">
                {{project.works}}
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
  name: 'MyProjects',
  setup(){
    const topProjects = [
      {
        name: 'Discord Bot JS',
        thumbnail: 'assets/discord.webp',
        description: 'This Project is Discord Bot, where it can do some moderation command',
        works: 'Individual Project'
      },
      {
        name: 'Bookshelf API',
        thumbnail: 'assets/radu-marcusu-mbKApJz6RSU-unsplash.webp',
        description: 'Simple Bookshelf API using hapiJS server',
        works: 'Individual Project'
      },
      {
        name: 'Simple Calculator JS',
        thumbnail: 'assets/kelly-sikkema-3-Tc_5LROrM-unsplash.webp',
        description: 'Calculator built in Javascript + DOM. It has some features like history calculate & dark theme',
        works: 'Community Project | Prime Developers'
      },
      {
        name: 'Simple To-Do List JS',
        thumbnail: 'assets/glenn-carstens-peters-RLw-UC03Gwc-unsplash.webp',
        description: 'To-Do List built in Javascript + DOM. It has some features like save activty list in local storage & dark theme',
        works: 'Community Project | Prime Developers'
      }
    ]
    return{topProjects}
  }
}
</script>

<style>
  .fit{
    object-fit: cover;
  }
  .cursor-pointer{
    cursor: pointer;
  }
</style>