<template>
    <nav class="text-center pt-2 pb-2 text-light fixed-top" :class="{change_color: (scrollPosition.value > 50)}">
        <!-- <p class="h3">{{scrollPosition.value}}</p> -->
        <ul class="nav justify-content-center">
            <li v-for="navItem in navigation" :key="navItem.name" class="nav-item nav-hoverable ms-3 me-3">
                <a class="nav-link text-light fw-bold fs-5" :href="navItem.link">{{navItem.name}}</a>
            </li>
        </ul>
    </nav>
</template>
<style scoped>
    .nav-hoverable:hover{
        background-color: rgb(137, 145, 255);
        transition: .7s;
    }
    .change_color {
       background-color:#333;
       transition: .7s;
   }
</style>
<script>
import { onMounted, reactive } from 'vue'
export default {
  name: 'NavigationComponent',
  props: {
    msg: String,
  },
  setup(){
    const navigation = [
        {
            name: 'Home',
            link: '#home'
        },
        {
            name: 'About',
            link: '#about'
        },
        {
            name: 'Projects',
            link: '#projects'
        },
        {
            name: 'Socials',
            link: '#socials'
        }
    ]
    const logo = './assets/logo.png'

    const scrollPosition = reactive({
        value: 0,
    })
    function updateScroll() {
        scrollPosition.value = window.scrollY
    }
    onMounted(()=>{
        window.addEventListener('scroll', updateScroll);
    })

    return {navigation, logo, scrollPosition}
  },
}
</script>
