<template>
    <div class="container">
        <HeaderComponent />

        <DownloadableListComponent />
    </div>
</template>

<script>
import { reactive } from 'vue';
import HeaderComponent from './components/HeaderComponent.vue';
import DownloadableListComponent from './components/DownloadableListComponent.vue';

export default {
    components: {
        HeaderComponent,
        DownloadableListComponent,
    },
    setup() {
        const state = reactive({
            downloadables: [
                {
                    text: "Hello",
                },
                {
                    text: "Hello",
                },
                {
                    text: "Hello",
                },
                {
                    text: "Hello",
                },
                {
                    text: "Hello",
                },
                {
                    text: "Hello",
                }
            ],
        })

        return {
            state,
        }
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
