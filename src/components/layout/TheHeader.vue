<template>
    <header>
        <article class="log-media">
            <div>            
                <h1>ARCH - architectual company. Architectual with care</h1>
            </div>
            <section>
                <p>Watch, listen, read, speak, find.</p>
                <h3>Follow the noise.</h3>   
            </section>
            <div class="media">
                <div class="img-wrapper"
                     v-for="(item,i) in media" 
                     :key="i+item.alt">
                    <img :src="item.link" 
                         :alt="item.alt">
                </div>
            </div>
        </article>
        <article class="search-log">
            <div class="search">
                <p>SEARCH</p>
                <div>
                    <input />
                    <img src="../../assets/loupe.png" alt="">
                </div>
            </div>
            <div class="log">
                <button>SIGN IN</button>
                <p>|</p>
                <button>REGISTRATION</button>   
            </div>
        </article>
        <article class="pre-nav">
            <nav>
                <ul>
                    <li v-for='(item,i) in preNav' :key="i+item.text"><a :href="item.link">{{ item.text }}</a></li>
                </ul>  
            </nav>
        </article>
        <article class="main-nav">
            <div class="logo">
                <img src="../../assets/logo.png" alt="ARCH">
            </div>
            <nav>
                <ul>
                    <li v-for='(item,i) in mainNav' :key="i+item.text" >
                        <div class="nav-active"></div>
                        <a :href="item.link">{{ item.text }}</a>
                    </li>
                </ul>        
            </nav>
        </article>
    </header>
</template>

<script>
export default {
  name: 'TheHeader',
  data(){
    return{
        preNav: [
            {text:'COMPANIES', link: ''},
            {text:'VACANCIES', link: ''},
            {text:'RESUME', link: ''},
            {text:'ADVERTISING', link: ''},
        ],
        mainNav:[
            {text:'ABOUT', link: ''},
            {text:'REVIEWS', link: ''},
            {text:'EVENTS', link: ''},
            {text:'FAQ', link: ''},
            {text:'CONTACT', link: ''},
        ],
        media:[
            {alt:'facebook',link:'facebook.png'},
            {alt:'telegram',link:'telegram.png'}
        ],
    }
  }
}
</script>

<style scoped>

header{
    max-width: 1440px;
    width: 100%;
    margin: 31px auto 0;
    padding-left: 169px;
    padding-right: 146px;
}

header .log-media{
    margin-bottom: 34px;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
}

header .log-media section p{
    font-family: "Roboto", sans-serif;
    font-size: 16px;
    font-weight: 400;
    font-style: normal;
    line-height: 18.75px;
}

header .log-media section h3{
    max-width: 330px;
    font-family: "Roboto", sans-serif;
    font-size: 48px;
    font-weight: 700;
    font-style: normal;
    line-height: 56.25px;
}

header .log-media .media{
    display: flex;
    flex-direction: column;
    row-gap: 22px;
    margin-bottom: 13px;
}

header .log-media .media .img-wrapper{
    max-width: 32px;
    cursor: pointer;
}

header .search-log{
    margin-bottom: 83px;
    display: flex;
    justify-content: space-between;
}

header .search-log .search{
    display: flex;
    align-items: center;
}

header .search-log .search p{
    font-family: "Roboto", sans-serif;
    font-size: 16px;
    font-weight: 700;
    font-style: normal;
    line-height: 18.75px;
}


header .search-log .search div{
    position: relative;
}

header .search-log .search div input {
    margin-left: 8px;
    padding-right: 25px;
    padding-bottom: 3px;
    border: none;
    border-bottom: 1px solid black;
    font-family: "Roboto", sans-serif;
    font-size: 16px;
    font-weight: 400;
    font-style: normal;
    line-height: 18.75px;
    background-color: transparent;
}

header .search-log .search div img{
    max-width: 22px;
    position: absolute;
    right: 0;
    bottom: 10px;
    cursor: pointer;
}

header .search-log .log{
    display: flex;
    justify-content: center;
    column-gap: 3px;
    font-family: "Roboto", sans-serif;
    font-size: 16px;
    font-weight: 700;
    font-style: normal;
}

header .search-log .log button{
    padding: 0;
    background-color: transparent;
    border:none;
    border-radius: none;
    cursor: pointer;
}

header .pre-nav{
    margin-bottom: 57px;
}

header .pre-nav nav ul{
    display: flex;
    justify-content: space-between;
}

header .pre-nav nav ul li{
    max-width: 230px;
    width: 100%;
    border-bottom: 3px solid black;
    font-family: "Roboto", sans-serif;
    font-size: 16px;
    font-weight: 700;
    font-style: normal;
}

header .main-nav{
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header .main-nav .logo{
    max-width: 174px;
}

header .main-nav nav{
    max-width: 787px;
    width: 100%;
}

header .main-nav nav ul{
    display: flex;
    justify-content: space-between;
    font-family: "Roboto", sans-serif;
    font-size: 16px;
    font-weight: 700;
    font-style: normal;
}

.nav-active{
    margin: 0 auto 12px;
    width: 25px;
    height: 25px;
    border-radius: 50%;
    background-color: black;
    opacity: 0;
}

</style>