<template>
  <main>
    <article class="events">
      <h2>ARCH EVENTS SEASON - 2022</h2>
      <div class="events-wrapper">
        <div class="event" v-for="(elem,i) in events" :key="i+elem.text">
          <h4>{{ elem.title }}</h4>
          <p class="text">{{ elem.text }}</p>
          <p class="date">{{ elem.date.start }}-<br>{{ elem.date.end }}</p>
        </div>
      </div>
    </article>
    <article class="about">
      <div class="title">
      <h3>ABOUT</h3>
      <div class="background"></div>
      </div>
      <div class="content">
        <div class="text-block-wrapper">
          <div class="text-block">
              <div class="circle"></div>
              <div class="text bold">
                <div class="first-line"></div>
                <p>We are an architectural company that has brought together the same burning professionals in the field of architecture on one site. Here you will find useful and up-to-date information and events in the field of architecture.
                </p>
              </div>            
          </div>
          <div class="text-block">
            <div class="circle"></div>
            <div class="text">
              <p>Architectural studio ARCH always intends to use in its projects the newest achievements of architecture and design. Designing for exact people we materialize their version of ideal space, their dreams and desires. Our studio’s projects- the result of creative architects' and clients' alliance, the result of joint thought. That is why you will not find two identical buildings or interiors among our works. Designing for people, we change their lives for the better.
              </p>
            </div>
          </div>
        </div>
        <div class="founders-block">
          <h3>PROJECT<br>FOUNDERS</h3>
          <div class="line"></div>
          <div class="imgs">
            <img src="../assets/foto0.png" alt="Jessica foto">
            <img src="../assets/foto1.png" alt="Andrus foto">
          </div>
          <div class="names">
            <p>JESSICA SMITH -<br>EXCUTIVE DIRECTOR</p>
            <p>ANDRUS BEZSDAR -<br>ARTISTIC DIRECTOR</p>
          </div>
        </div>
      </div>
    </article>
  </main>
</template>

<script>

export default {
  name:'AboutView',
  data(){
    return{
      events: [
        {title:'event', text:'DESCRIPTION, PLACE, TIME', date:{start:'23.FEB',end:'17.MAR.22'}},
        {title:'event', text:'DESCRIPTION, PLACE, TIME', date:{start:'23.FEB',end:'17.MAR.22'}},
        {title:'event', text:'DESCRIPTION, PLACE, TIME', date:{start:'23.FEB',end:'17.MAR.22'}},
        {title:'event', text:'DESCRIPTION, PLACE, TIME', date:{start:'23.FEB',end:'17.MAR.22'}},
      ],
    }
  }
}
</script>

<style scoped>
 main{
    max-width: 1440px;
    width: 100%;
    margin: 0 auto;
    padding-left: 169px;
    padding-right: 146px;
}

main .events{
  display: flex;
  flex-direction: column;
  row-gap: 51px;
  margin-bottom: 72px;
}

main .events h2{
  display: flex;
  justify-content: flex-end;
  font-family: "Roboto", sans-serif;
  font-size: 64px;
  font-weight: 400;
  font-style: normal;
  line-height: 75px;
}

main .events .events-wrapper{
  display: flex;
  column-gap: 123px;
} 

main .events .events-wrapper .event{
  display: flex;
  flex-direction: column;
  row-gap: 13px;
}

main .events .events-wrapper .event:nth-child(2){
 margin-right: auto;
}

main .events .events-wrapper .event h4{
  padding-bottom: 13px;
  font-family: "Roboto", sans-serif;
  font-size: 16px;
  font-weight: 700;
  font-style: normal;
  line-height: 18.75px;
  text-transform: uppercase;
  border-bottom: 1px solid black;
}

main .events .events-wrapper .event .text{
  font-family: "Roboto", sans-serif;
  font-size: 16px;
  font-weight: 400;
  font-style: normal;
  line-height: 18.75px;
  text-transform: uppercase;
}

main .events .events-wrapper .event .date{
  font-family: "Roboto", sans-serif;
  font-size: 16px;
  font-weight: 700;
  font-style: normal;
  line-height: 18.75px;
  text-transform: uppercase;
}

main .about .title h3{
  position: relative;
  font-family: "Roboto", sans-serif;
  font-size: 144px;
  font-weight: 800;
  font-style: normal;
  line-height: 168.75px;
  text-transform: uppercase;
  z-index: 2;
}

main .about .title{
  position: relative;
}

main .about .title .background{
  position: absolute;
  top: 0px;
  left: -10px;
  width: 500px;
  height: 90px;
  background-color: #DFB41B;
  z-index: 1;
}

main .about .content{
  position: relative;
  margin-top: 57px;
  padding-bottom: 180px;
}

main .about .content .text-block-wrapper{
  display: flex;
  flex-direction: column;
  row-gap: 10px;
}

main .about .content .text-block-wrapper .text-block{
  display: flex;
  column-gap: 84px;
}

main .about .content .text-block-wrapper .text-block .first-line{
  position: absolute;
  top:0;
  width: 160px;
  height: 1px;
  background-color: black;
}


main .about .content .text-block-wrapper .text-block .circle{
  margin-top: 40px;
  width: 96px;
  height: 96px;
  border-radius: 50%;
  background-color: black;
}

main .about .content .text-block-wrapper .text-block .text{
  max-width: 500px;
  font-family: "Roboto", sans-serif;
  font-size: 24px;
  font-weight: 400;
  font-style: normal;
  line-height: 28.13px;
}

main .about .content .text-block-wrapper .text-block .text.bold{
  position: relative;
  padding-top: 28px;
  font-weight: 700;
}

main .about .content .founders-block{
  position: absolute;
  bottom: 0;
  right: 0;
  display: flex;
  flex-direction: column;
  row-gap: 20px;
}

main .about .content .founders-block h3{
  font-family: "Roboto", sans-serif;
  font-size: 48px;
  font-weight: 700;
  font-style: normal;
  line-height: 56.24px;
} 

main .about .content .founders-block .imgs{
  display: flex;
  column-gap: 25px;
}

main .about .content .founders-block .line{
  width: 160px;
  height: 1px;
  background-color: black;
}


main .about .content .founders-block .imgs img{
  max-width: 137px;
}

main .about .content .founders-block .names{
  display: flex;
  flex-direction: column;
  row-gap: 13px;
  font-family: "Roboto", sans-serif;
  font-size: 18px;
  font-weight: 700;
  font-style: normal;
  line-height: 21.09px;
}

</style>