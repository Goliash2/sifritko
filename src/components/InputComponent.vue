<template>
    <ion-grid>
        <form>
            <ion-col>
                <ion-item>
                    <ion-label>
                        Zadani:
                    </ion-label>
                    <ion-input name="input"></ion-input>
                </ion-item>
            </ion-col>
            <ion-col>
                <ion-button type="submit" color="primary" expand="block">Lustit</ion-button>
            </ion-col>
        </form>
    </ion-grid>
</template>

<script>
    export default {
        name: "input.component"
    }
</script>
