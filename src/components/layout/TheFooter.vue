<template>
    <footer>
        <article class="logo">
            <img src="../../assets/footerLogo.png" alt="logo">
        </article>
        <article class="lang">
            <div>
                <ul>
                    <li v-for="(elem,i) in lang" :key="i+elem">{{ elem }}</li>
                </ul>
            </div>
        </article>
        <article class="block">
            <p>© 2022 ARHITECH</p>
            <div class="btn">
                <p>I WANT TO STAY TUNED</p>
                <button>
                    <img src="../../assets/footerArrow.png" alt="rigthArrow">
                </button>
            </div>
        </article>
    </footer>

</template>

<script>

export default {
    name:'TheFooter',
    data(){
        return {
            lang:['RU','EN']
        }
    }
}

</script>

<style scoped>

footer{
    max-width: 1440px;
    width:100%;
    margin: 0 auto 115px;
    padding: 0 113px 0 169px;
}

footer .logo{
    max-width: 103px;
    margin: 0 auto 13px;
}

footer .block{
    display: flex;
    justify-content: space-between;
    align-items: center;
}

footer .block p{
    font-family: "Roboto", sans-serif;
    font-size: 16px;
    font-weight: 700;
    font-style: normal;
    line-height: 18.75px;
}

footer .lang div{
    display: flex;
    justify-content: center;
}

footer .lang ul{
    display: flex;
    align-items: center;
    column-gap: 35px;
}

footer .lang ul li{
    font-family: "Roboto", sans-serif;
    font-size: 16px;
    font-weight: 400;
    font-style: normal;
    line-height: 18.75px;
}

footer .lang ul li .active{
    font-weight: 700;
}


footer .block .btn{
    display: flex;
    align-items: flex-end;
    column-gap: 14px;
}

footer .block .btn p{
    font-size: 16px;
    font-weight: 700;
    font-style: normal;
    line-height: 18.75px;
}

footer .block .btn button{
    border: none;
    background-color: transparent;
    cursor: pointer;
}

footer .block .btn button img{
    width: 32px;
    height: 32px;
}


</style>