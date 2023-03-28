<script>
export default {
    name: "AppNav",
    data() {
        return {
            imgLogo: `/img/dc-logo.png`,
            links: [
                `characters`,
                `comics`,
                `movies`,
                `tv`,
                `games`,
                `collectibles`,
                `videos`,
                `fans`,
                `news`,
                `shop`,
            ],
        }
    },
}
</script>


<template>
    <nav>
        <div id="logo">
            <img :src="imgLogo" alt="">
        </div>

        <div id="links">
            <ul>
                <li v-for="link in links"> <strong>{{ link }}</strong></li>
            </ul>
        </div>
    </nav>
</template>


<style lang="scss" scoped>
nav {
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-around;
    align-items: center;
    height: 80px;
    background-color: #FFFFFF;

    #logo {
        height: 80%;

        img {
            max-height: 100%;
        }
    }

    #links {
        ul {
            display: flex;
            gap: 20px;
            font-size: .8em;
            text-transform: uppercase;
            color: #46464C;

            li:hover {
                color: #0281F8;
                cursor: pointer;
            }
        }
    }
}
</style>