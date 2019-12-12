<template>
    <ion-grid>
        <form @submit.prevent="onSubmit">
            <ion-col>
                <ion-item>
                    <ion-label>Zadání:</ion-label>
                    <ion-input
                            :value="zadani"
                            @input="zadani = $event.target.value"
                            name="zadani"
                    ></ion-input>
                </ion-item>
            </ion-col>
            <ion-col>
                <ion-button type="submit" color="primary" expand="block">Luštit</ion-button>
            </ion-col>
        </form>
    </ion-grid>
</template>

<script>
    export default {
        name: "InputComponent",
        data() {
            return {
                zadani: ""
            }
        },
        methods: {
            onSubmit() {
                this.$emit("get-zadani", this.zadani);
            }
        }
    }
</script>
