<template>
   <div class="menu">
       <h3>{{menu.title}}</h3>
            <ul>
                <li v-for="(link,index) in menu.links" :key="index">
                    <a href="link.url">{{link.link}}</a>
                </li>
            </ul>
   </div>
</template>

<script>
export default {
    name: "Menu",
    props: ["menu"]

}
</script>

<style scoped lang="scss">
    h3 {
        color: white;
        margin: 10px 0;
        }

        ul {
            list-style-type: none;
            margin: 5px 15px 5px 0;
           a {
               font-size: 0.8rem;
               color: #959595;
           }

        }
</style>