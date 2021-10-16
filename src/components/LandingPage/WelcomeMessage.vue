<template>
    <section :style="welcome" class="position-relative m-auto" id="home">
        <div class="darknet justify-content-center align-content-center">
            <div class="container position-relative m-auto row">
                <div class="col-lg-9">
                    <h1 class="h1 text-light fw-bold pb-5">WELCOME TO MY PERSONAL SITE</h1>
                    <p class="h6 text-light">My Name is Ichinomiya Mori | 壱のみや森, Currently as Student at Paradi Island</p>
                    <p class="h6 text-light">I'm NodeJS Developer {Vue, Express}</p>
                    <p class="h6 text-light">And Also Core Team of Google Developer Student Clubs Chapter Paradi Island</p>
                    <button type="button" class="btn btn-dark mt-3 p-3"><a href="#about" class="link-light text-decoration-none">Know More ....</a></button>
                </div>
                <div class="col-lg-3">
                    <img :src="profpic" class="img-fluid">
                </div>
            </div>
        </div>
    </section>
</template>
<style>
    .darknet{
        position: relative; 
        height: 100vh;
        width: 100%;
        display: flex;

    }
    .darknet::before{
        content: "";
        background-color: #111;
        position: absolute;
        top: 0px;
        right: 0px;
        bottom: 0px;
        left: 0px;
        opacity: 0.65;
    }
</style>
<script>
export default {
    name: 'WelcomeMesage',
    setup(){
        const profpic = './assets/14.webp'
        return {profpic}
    },
    computed:{
        welcome(){
            return{            
                'background': `url('assets/james-harrison-vpOeXr5wmR4-unsplash.webp')`,
                'background-repeat': 'no-repeat',
                'background-size': 'cover',
                'background-attachment': 'fixed',
                'min-height' : '100vh'
            }
        },
        darken(){
            return{
                'background-color': '#333',
                'display': 'flex',
                'opacity': '0.6',
                'height': '100vh',
                'width': '100%'
            }
        }
    }
}
</script>