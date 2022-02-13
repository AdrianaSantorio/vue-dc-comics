<template>
    <div class="upper-footer">
        <div class="container">
            <nav>
                <div>
                    <!-- dc comics -->
                    <h3>DC COMICS</h3>
                    <ul>
                        <li v-for="(link,index) in comicsLinks" :key="index">
                            <a href="link.url">{{link.link}}</a>
                        </li>
                    </ul>
                    <!-- shop -->
                    <h3>SHOP</h3>
                    <ul>
                        <li v-for="(link,index) in shopLinks" :key="index">
                            <a href="link.url">{{link.link}}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <!-- DC -->
                    <h3>DC</h3>
                    <ul>
                        <li v-for="(link,index) in dcLinks" :key="index">
                            <a href="link.url">{{link.link}}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <!-- SITES -->
                    <h3>SITES</h3>
                    <ul>
                        <li v-for="(link,index) in sitesLinks" :key="index">
                            <a href="link.url">{{link.link}}</a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
    </div>
</template>

<script>
export default {
    name: "upper-footer",
    data() {
        return {
            comicsLinks: [
                {link:"Characters" , url:"#"},
                {link:"Comics" , url:"#"},
                {link:"Movies" , url:"#"},
                {link:"TV" , url:"#"},
                {link:"Games" , url:"#"},
                {link:"Videos" , url:"#"},
                {link:"News" , url:"#"},
            ],
            shopLinks: [
                {link:"Shop DC" , url:"#"},
                {link:"Shop DC Collectibles" , url:"#"},
            ],
            dcLinks: [
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
            sitesLinks: [
                {link:"DC" , url:"#"},
                {link:"MAD Magazine" , url:"#"},
                {link:"DC Kids" , url:"#"},
                {link:"DC Universe" , url:"#"},
                {link:"DC Power Visa" , url:"#"},
            ]

        }
    }

}
</script>

<style scoped lang="scss">
    
    .upper-footer {
        background-image: url(../assets/img/footer-bg.jpg);
        padding: 30px;
    }

    nav {
        display: flex;
        justify-content: flex-start;

        h3 {
            color: white;
        }

        ul {
            list-style-type: none;
            margin: 5px 15px 5px 0;
           a {
               font-size: 0.8rem;
               color: #959595;
           }

        }

    }
</style>