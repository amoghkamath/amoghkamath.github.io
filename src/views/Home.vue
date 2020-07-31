<template>
  <div class="home_parent">
    <div class="home">
        <section class="banner" id="sec">
          <div class="content">
            <h2>Hello World, <br> I'm <span>Amogh Kamath</span></h2>
            <p>Welcome to my website.</p>
            <a @click="scrollDown" href="#">Know More</a>
            <div class="sci">
              <i class="fab fa-facebook"></i>
              <i class="fab fa-linkedin"></i>
            </div>
          </div>
        </section>
      <!-- <p @click="scrollDown"><u>MEET <strong>ME</strong></u></p> -->
    </div>

    <div class="about">
      <section id="aboutme">

        <div class="container">
          <div class="row">
            <div class="col-md-5">
              <div class="about-img">
                  <img src="https://media.giphy.com/media/SkbtmgU7vDCHC/giphy.gif" alt="">
              </div>
            </div>
            <br>
            <div class="col-md-7 about-right">
                <h2 class="color-3"><b>About Me</b>
                </h2>
                    <p class="p_first">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco labor is nisi ut aliquip ex ea commodo consequat.</p>

                    <p class="text-white">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. </p>

                    <h3 class="color-3 social-link-text">
                        <button class="btn btn-info">Let's Talk</button>
                    </h3>

                    <ul class="about-link">
                      <li><a href=" "><i class="fa fa-fonticons"></i></a></li>
                      <li><a href=" "><i class="fa fa-envira"></i></a></li>
                      <li><a href=" "><i class="fa fa-reddit-alien"></i></a></li>
                      <li><a href=" "><i class="fa fa-youtube-play" aria-hidden="true"></i></a></li>
                    </ul>
            </div>

          </div>

        </div>

      </section>


    </div>
    <div class="work">
      <div class="tile is-ancestor">
        <div class="tile is-vertical" style="width: 50%">
          <div @click="toggle($event)" class="tile is-child is-primary food">
            <p>Food</p>
          </div>
          <div class="tile is-child is-primary landscape">
            <p>Landscapes</p>
          </div>
        </div>
        <div class="tile is-secondary wildlife" style="width: 50%">
          <p>Wildlife</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script type="text/javascript">
import $ from 'jquery'
export default {
  name: 'Home',
  methods: {
    scrollDown: function () {
      window.scrollBy({
        top: document.body.scrollHeight,
        behavior: 'smooth'
      })
    },
    toggle: function (ev) {
      $(ev.target).toggleClass('active')
    }
  }
}
</script>

<style lang="scss">
  .home {
    background: #333;
    background: url('bg.jpg');
    // background:  linear-gradient(to bottom, rgba(50, 50, 50, 0.9), rgba(90, 90, 90, 0.8));
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  .content {
    max-width: 600px;
  }
  .content h2{
    color: #fff;
    font-size: 2.5em;
  }
  .content h2 span {
    color: #40c3ff;
    font-size: 1.2em;
  }
  .content p {
    font-size: 1.2em;
    color: #fff;
    font-weight: 300;
  }
  .content a {
    position: relative;
    display: inline-block;
    margin-top: 20px;
    background: #fff;
    color: #000;
    padding: 10px 30px;
    text-decoration: none;
    font-size: 1.2em;
    font-weight: 300;
  }
  .sci {
    bottom: 50px;
    right: initial;
    display: flex;
    flex-direction: row;
    width: 100%;
    left: 0px;
    top: 80vh;
    justify-content: center;
    li {list-style: none}
  }
  .sci i {
    color: white;
    font-size: 28px;
    margin: 24px 10px 0px 4px;
  }
  @media (max-width: 767px) {
    .home {
      background: #000;
    }
    .banner {
      padding: 100px 50px 150px;
    }
    .banner h2 {
      font-size: 1.8em;
    }
    .banner .content p {
      font-size: 1em;
    }
    .banner .content a {
      font-size: 1em;
    }
  }

  .about {
    background: #fff;
    font-family: sans-serif;
    text-align: justify;
    display: flex;
    overflow: hidden;
  }
  #aboutme{
    padding-top: 50px;
    padding-bottom: 101px;
  }
  #aboutme .col-md-7{
    margin-top: 55px;
  }
  #aboutme .about-img{
    position: absolute;
    left: -1px;
    top: 60px;
    width: 90%;
  }
  #aboutme .p_first{
      margin-bottom: 30px;
  }

  #aboutme h2{
    margin-bottom: 27px;
    margin-top: 12px;
    font-size: x-large;
  }

  #aboutme .social-link-text {
    margin-top: 20px;
    margin-bottom: 25px;
  }
  #aboutme .about-link{
    padding-left: 0px;
  }
  #aboutme .about-link li{
    display: inline-block;
  }
  #aboutme .about-link li a i{
    width: 35px;
    height: 35px;
    border-radius: 50%;
    text-align: center;
    margin-right: 10px;
    font-size: 22px;
    color: #d6c6b2
  }
  #aboutme .about-link li a i:hover {
    color: #222222;
    background: #d6c6b2;
    border-color: #d6c6b2;
  }

  #aboutme .about-img {
    position: relative;
  }

  .color-3 {
    color: #d6c6b2;
  }
  .text_white{
    color: black;
  }

  #aboutme p {
    margin-bottom: 0;
    font-size: 16px;
    line-height: 24px;
  }

  .btn-info {
    border-radius: 0;
    padding: 10px 20px;
  }

  @media (max-width: 767px) {
    #aboutme {
      padding: 100px 50px 150px;
    }
    #aboutme h2 {
      font-size: 1.8em;
    }
    #aboutme p {
      font-size: 1em;
    }
    #aboutme a {
      font-size: 1em;
    }
  }


  .food {
    background: url('https://images.unsplash.com/photo-1511690656952-34342bb7c2f2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1000&q=80');
    background-size: cover;
    background-position: center;
    border-radius: 4px;
    margin: 8px;
  }
  .landscape {
    background: url('https://images.unsplash.com/photo-1500964757637-c85e8a162699?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1978&q=80');
    background-size: cover;
    background-position: center;
    border-radius: 4px;
    margin: 8px;

  }
  .wildlife {
    background: url('https://images.unsplash.com/photo-1564712564108-981afa2bc79a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=975&q=80');
    background-size: cover;
    background-position: center;
    margin-left: 16px;
    border-radius: 4px;
    p {color: #333;}

  }
  .home, .about, .work {
    width: 100%;
    min-height: 100vh;
    height: 100vh;
    padding: 100px;
    display: flex;
    padding: 80px;
    flex-direction: column;
    justify-content: center;
    // h1 {
    //   font-size: calc(32px + 28*(100vw - 320px)/1120);
    //   color: white;
    //   margin: 20px auto 0px 0px;
    //   letter-spacing: 0.5px;
    //   font-weight: bold;
    // }
//     p {
//       color: white;
//       // color: #988e9f;
//       margin: 50px auto 0px 0px;
//       font-size: 18px;
//       cursor: pointer;
//       &:hover {color: lighten(#988e9f, 10%) }
//     }
//     p strong {
//       color: white;
//     }
// //     h2 {
// //       font-size: 28px;
// //       font-weight: 200;
// //       display: flex;
// //       flex-direction: column;
// //       span {
// // margin-bottom: 20px;
// //       }
// //     }
  }
  .food, .landscape, .wildlife {
    p {color: white; font-size: 40px; font-weight: 300;}
    transition: .4s;
  }
  .wildlife p, .landscape p {
    color: #333;
    margin: 20px auto;
  }
</style>
