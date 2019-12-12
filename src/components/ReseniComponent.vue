<template>
    <ion-card v-if="reseni">
        <ion-card-header>
            <ion-card-title>Řešení:</ion-card-title>
        </ion-card-header>
        <ion-card-content>
            <ion-list>
                <ion-item>
                    <pre>{{ reseni }}</pre>
                </ion-item>
            </ion-list>
        </ion-card-content>
    </ion-card>
</template>

<script>
    export default {
        name: "ReseniComponent",
        props: ["reseni"]
    }
</script>
