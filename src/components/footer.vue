<template>
    <footer>
        <div class="container text-center">
          Made with &#128150; by Mr.Spider | Using {{vuejs}}
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
        width: 100%;
        padding: 8px 0px 5px 0px;
    }
</style>