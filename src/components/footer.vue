<template>
    <footer>
        <div class="container text-center">
            by Mr.Spider | made with {{vuejs}}
        </div>
    </footer>
</template>

<script>
export default {
    name: "myFooter",
    data(){
        return{
            vuejs: "{{ Vuejs }}"
        }
    }
}
</script>

<style scoped>
    footer{
        bottom: 0px;
        background-color: rgb(35, 35, 36);
        color: white;
        font-size: 24px;
        position: absolute;
        width: 100%;
    }
</style>