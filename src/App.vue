<template>
    <div class="grid-container">
        <app-Header></app-Header>
        <app-Navbar></app-Navbar>
        <transition name="flip" mode="out-in">
            <router-view></router-view>
        </transition>
        <hr>
        <app-footer></app-footer>
    </div>
</template>

<script>
    import Header from './components/Header.vue'
    import Navbar from './components/Navbar.vue'
    import Footer from './components/Footer.vue'

    export default {
        components: {
          appHeader: Header,
          appNavbar: Navbar,
          appFooter: Footer,
        }
    }

    // TODO: change css for .grid-container>.test {
</script>

<style>


header { grid-area: header; }
nav { grid-area: nav; }
main { grid-area: main; }
footer { grid-area: footer; }

.grid-container {
  display: grid;
  grid-template-areas:
    'header'
    'nav'
    'main'
    'footer';
    grid-gap: 1rem;
    grid-column-gap: 1rem;
    background-color: rgb(255, 255, 255);
    padding: 30px;

}

.grid-container>.test {
  background-color: rgb(255, 255, 255);
  text-align: center;
  align-items: center;
  align-self: center;
  padding:20px 0;
  font-size: 30px;
}


.flip-enter-active {
    animation: flip-in  0.8s ease-out forwards;
}

.flip-leave-active {
    animation: flip-out 0.5s ease-out forwards;
}

@keyframes flip-out {
    from {
        transform: rotateY(0deg);
    }
    to {
        transform: rotateY(90deg);
    }
}

@keyframes flip-in {
    from {
        transform: rotateY(90deg);
    }
    to {
        transform: rotateY(0deg);
    }
}
</style>
