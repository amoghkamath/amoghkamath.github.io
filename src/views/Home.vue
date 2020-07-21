<template>
  <div class="home_parent">
    <div class="home">
      <h1>Hello. My name is <span style="color: #6928ef">Amogh Bozcni#k.</span></h1>
      <h1>I take useless photography</h1>
      <p @click="scrollDown">Let me show you...</p>
    </div>
    <div class="about">
      <h2>
        <span>
          <span style="color: purple">Ameeeeegh</span> is an international photographer specialised in people, food, hotel, home and commercial objects photography as well as book productions.
        </span>
        <br>
        <span>
          He together with his team works on full-scale photo productions, covering all – from planning a shoot to post-production.
        </span>
        <br>
        <span>
          His work spans from special commissions for global clients to for international magazines and numerous books.
        </span>
      </h2>
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
    background: linear-gradient(to bottom, rgba(50, 50, 50, 0.9), rgba(90, 90, 90, 0.8)), url('https://images.unsplash.com/photo-1562813733-b31f71025d54?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2698&q=80');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  .about {
    background: white;
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
    height: 100vh;
    display: flex;
    padding: 80px;
    flex-direction: column;
    justify-content: center;
    h1 {
      font-size: 40px;
      color: white;
      margin: 20px auto 0px 0px;
      letter-spacing: 0.5px;
      font-weight: bold;
    }
    p {
      color: #988e9f;
      margin: 32px auto 0px 0px;
      font-size: 18px;
      cursor: pointer;
      &:hover {color: lighten(#988e9f, 10%) }
    }
    h2 {
      font-size: 28px;
      font-weight: 200;
      display: flex;
      flex-direction: column;
      span {
margin-bottom: 20px;
      }
    }
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
