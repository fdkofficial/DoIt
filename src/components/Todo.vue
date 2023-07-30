<template>
    <div class="wrapper">
        <div class="custom-header">
            <h2 class="h1">Todo</h2>
        </div>
        <div class="todo-block" style="margin-top: 2rem;">
            <div class="card">
                <div class="card-header">
                    <h2 class="h1">30th July 2023</h2>
                </div>
                <div class="card-body" v-for="i in cards" :key="i">
                    <div class="time-task">
                        <div style="margin-top: 10px;opacity: 0.7;">
                            9:30 AM
                        </div>
                        <div>
                            <b>
                                {{ i }}
                            </b>
                        </div>
                    </div>
                    <div class="pic">
                        <Image alt="Image" class="p-image-preview-icon" preview>
                            <template #image>
                                <img class="circle" src="https://primefaces.org/cdn/primevue/images/galleria/galleria12s.jpg"
                                    alt="image" />
                            </template>
                            <template #preview="slotProps">
                                <img src="https://primefaces.org/cdn/primevue/images/galleria/galleria12.jpg" alt="preview"
                                    :style="slotProps.style" @click="slotProps.onClick" />
                            </template>
                        </Image>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup >
let cards = ["Go To Gym, Yo!","Start The Dieting,Yup","Learn More And More"]
</script>
<style lang="css">
.custom-header {
    border-radius: 25px;
    padding: 1rem;
    background: rgb(41, 75, 158);
    background: linear-gradient(90deg, rgba(41, 75, 158, 1) 0%, rgba(165, 0, 255, 1) 97%);
    font-family: 'Courier New', Courier, monospace;
    color: antiquewhite;
}
.card-body{
    display: flex;
    justify-content: space-around;
    border: 2px solid dodgerblue;
    border-radius: 25px;
    padding: 1rem;
    margin-top: 5px;
}

.circle{
    border-radius: 50%;
}
</style>