<template>
    <div>
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="py-5">
                    <p class="mc-text">These are the available versions of <b>Minecraft PE</b>.</p>
                    <p class="mc-text">Click on any of these to start <b>downloading!</b></p>
                </div>

                <ul class="downloadable-list">
                    <li v-for="(item, index) in state.downloadables" :key="index">
                        <button class="mc-button" @click="testDownload(index)">{{ item.text }}</button>
                        <a :href="item.link" :id="'download_btn_' + index" download hidden></a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
import { reactive } from 'vue';

export default {
    setup() {
        const state = reactive({
            downloadables: [{
                text: "Minecraft PE 1.18",
                link: "/downloadables/test.txt",
            }]
        });

        const testDownload = (index) => {
            document.getElementById("download_btn_" + index).click();
        }

        return {
            state,
            testDownload,
        };
    }
}
</script>

<style type="text/css">
.mc-btn {
    background-image: url('../assets/img/button_bg.png');
    padding: 39px 0;
    background-size: cover;
}

.mc-button {
    background: #D0D1D5;
    border: 2px solid #1A2116;
    color: #1A2116;
    font-family: "Minecraft";
    width: 100%; 
    padding: 13px 0px 16px 0;
    font-weight: bold;
    text-space: 4px;
    letter-spacing: 2px;
}

.mc-button:hover {
    background: #3b8526;
    color: #fff;
}

.downloadable-list {
    list-style: none;
}
</style>

