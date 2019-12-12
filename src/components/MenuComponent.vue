<template>
    <!-- Listen to before and after tab change events -->
    <ion-tabs>
        <ion-tab tab="schedule">
            <Schedule />
        </ion-tab>

        <!-- Match by "app.speakers" route name -->
        <ion-tab tab="speakers">
            <Speakers />
        </ion-tab>

        <!-- Match by an array of route names -->
        <ion-tab tab="map">
            <Map />
        </ion-tab>

        <!-- Get matched routes with a helper method -->
        <ion-tab tab="about">
            <About />
        </ion-tab>

        <!-- Match by "app.speakers" route name -->
        <ion-tab tab="speakers">
            <Test1 />
        </ion-tab>

        <!-- Match by an array of route names -->
        <ion-tab tab="map">
            <Test2 />
        </ion-tab>

        <!-- Get matched routes with a helper method -->
        <ion-tab tab="about">
            <Test3 />
        </ion-tab>

        <!-- Use v-slot:bottom with Vue ^2.6.0 -->
        <template slot="bottom">
            <ion-tab-bar>
                <ion-tab-button tab="schedule">
                    <ion-icon name="swap"></ion-icon>
                    <ion-label>Caesar</ion-label>
                </ion-tab-button>

                <!-- Provide a custom route to navigate to -->
                <ion-tab-button tab="speakers">
                    <ion-icon name="key"></ion-icon>
                    <ion-label>Heslo</ion-label>
                </ion-tab-button>

                <!-- Provide extra data to route -->
                <ion-tab-button tab="map">
                    <ion-icon name="sync"></ion-icon>
                    <ion-label>Otoč abec</ion-label>
                </ion-tab-button>

                <!-- Provide custom click handler -->
                <ion-tab-button tab="about">
                    <ion-icon name="information-circle"></ion-icon>
                    <ion-label>About</ion-label>
                </ion-tab-button>

                <!-- Provide custom click handler -->
                <ion-tab-button tab="Test1">
                    <ion-icon name="information-circle"></ion-icon>
                    <ion-label>About</ion-label>
                </ion-tab-button>

                <!-- Provide custom click handler -->
                <ion-tab-button tab="Test2">
                    <ion-icon name="information-circle"></ion-icon>
                    <ion-label>About</ion-label>
                </ion-tab-button>

                <!-- Provide custom click handler -->
                <ion-tab-button tab="Test3">
                    <ion-icon name="information-circle"></ion-icon>
                    <ion-label>About</ion-label>
                </ion-tab-button>
            </ion-tab-bar>
        </template>
    </ion-tabs>
</template>

<script>
    export default {
        name: "MenuComponent"
    }
</script>

<style scoped>

</style>
