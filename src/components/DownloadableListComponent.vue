<template>
    <div>
        <div class="row justify-content-center">
            <div class="col-md-8 col-12">
                <div class="py-5">
                    <p class="mc-text">These are the available versions of <b>Minecraft PE</b>.</p>
                    <p class="mc-text">Click on any of these to start <b>downloading!</b></p>
                </div>

                <ul class="downloadable-list">
                    <li v-for="(item, index) in state.downloadables" :key="index">
                        <button class="mc-button" @click="testDownload(item)">{{ item.text }}</button>
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
            downloadables: [
                {
                    text: "Minecraft PE 1.19.0.28",
                    link: "https://mega.nz/file/TPJh2LIB#g7dHRdah2awuWBfFMyFSKiINKPpAE9Y7P5FP_-RTVRE",
                },
                {
                    text: "Minecraft PE 1.18.31",
                    link: "https://mega.nz/file/SHY3lRYB#47ihQSzIudHFuY7UV0giD2kXpQNfqz3W90b8PlCkhms",
                },
                {
                    text: "Minecraft PE 1.18.20.27",
                    link: "https://mega.nz/file/WKBRmTIR#sYxMc-X638zSl7aSXwD_mcqxSXBmZF8PIoV0HKN10Qo",
                },
                {
                    text: "Minecraft PE 1.18.12",
                    link: "https://mega.nz/file/rGR1yRiL#fJjPiJ3odJc37R_Roz0dkTdfIdl9bq7w-ulwoqL1EHo",
                },
                {
                    text: "Minecraft PE 1.18.0.27",
                    link: "https://mega.nz/file/yDgBQLyT#y-fAHck4MB7bfAA9Avgv8NpTcmvOnD4S9s8rR_7Binw",
                },
                {
                    text: "Minecraft PE 1.17.41",
                    link: "https://mega.nz/file/ybAhEYzZ#2ymPV8i4UeMoWz39trJCq0iCbE4jdC54fPjXpnCCBYs",
                },
                {
                    text: "Minecraft PE 1.17.40",
                    link: "https://mega.nz/file/6PpUlLDT#K3SNxoO5NjLyKHf59BTd44U4h_Pdv6-8_N85rppn49E",
                },
                {
                    text: "Minecraft PE 1.17.2",
                    link: "https://mega.nz/file/yfgShQzC#iBvGUNwhdK8KuwSqy9JvOhS2cx2j5D8a8UrhaAHN3Lo",
                },
                {
                    text: "Minecraft PE 1.17.0.58",
                    link: "https://mega.nz/file/jagnBLJS#7xx2eXEx33pBd0Aq-hSV9IN5Hqp-9r6Uo2-ODEjXXTE",
                },
            ]
        });

        const testDownload = (item) => {
            window.open(item.link, "_blank");
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
    letter-spacing: 2px;
}

@media only screen and (max-width: 450px) {
    .mc-button {
        letter-spacing: 1px;
        font-size: 12px;
    }
}

.mc-button:hover {
    background: #3b8526;
    color: #fff;
}

.downloadable-list {
    list-style: none;
    padding-left: 0;
}
</style>

