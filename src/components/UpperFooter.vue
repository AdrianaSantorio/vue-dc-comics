<template>
    <div class="upper-footer">
        <div class="container">
            <nav>
                <ul>
                   <li v-for="(menu, index) in footerMenus" :key="index">
                       <Menu :menu="menu"/>
                   </li>
               </ul>
            </nav>
        </div>
    </div>
</template>

<script>
import Menu from "./Menu.vue"

export default {
    name: "upper-footer",
    components: {
        Menu,
    },
    data() {
        return {
            footerMenus: [
                {
                    title: "DC COMICS",
                    links: [
                        {link:"Characters" , url:"#"},
                        {link:"Comics" , url:"#"},
                        {link:"Movies" , url:"#"},
                        {link:"TV" , url:"#"},
                        {link:"Games" , url:"#"},
                        {link:"Videos" , url:"#"},
                        {link:"News" , url:"#"},
                    ],
                },
                {   
                    title: "SHOP",
                    links: [
                        {link:"Shop DC" , url:"#"},
                        {link:"Shop DC Collectibles" , url:"#"},
                    ],
                },
                {   
                    title: "DC",
                    links: [
                        {link:"Term Of Use" , url:"#"},
                        {link:"Privacy policy(New)" , url:"#"},
                        {link:"Ad Choices" , url:"#"},
                        {link:"Advertising" , url:"#"},
                        {link:"Jobs" , url:"#"},
                        {link:"Subscritions" , url:"#"},
                        {link:"Talent Workshops" , url:"#"},
                        {link:"CPSC Certificates" , url:"#"},
                        {link:"Ratings" , url:"#"},
                        {link:"Shop Help" , url:"#"},
                        {link:"Contact Us" , url:"#"},
                    ],
                },
                {   
                    title: "SITES",            
                    links: [
                        {link:"DC" , url:"#"},
                        {link:"MAD Magazine" , url:"#"},
                        {link:"DC Kids" , url:"#"},
                        {link:"DC Universe" , url:"#"},
                        {link:"DC Power Visa" , url:"#"},
                    ]
                }
            ]

        }
    }

}
</script>

<style scoped lang="scss">
    
    .upper-footer {
        background-image: url(../assets/img/footer-bg.jpg);
        padding: 30px;
        

        ul {
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            justify-content: flex-start;
            height: 270px;
            align-content: flex-start; 
        }
    }

    
</style>