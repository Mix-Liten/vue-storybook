<template>
  <div class="wrap">
    <ul class="timeline">
      <li>
        <a href="#">
          <h2>標題一</h2>
          <p>內文一...</p>
        </a>
      </li>
      <li>
        <a href="#">
          <h2>標題二</h2>
          <p>內文二...</p>
        </a>
      </li>
      <li>
        <a href="#">
          <h2>標題三</h2>
          <p>內文三...</p>
        </a>
      </li>
      <li>
        <a href="#">
          <h2>標題四</h2>
          <p>內文四...</p>
        </a>
      </li>
      <li>
        <a href="#">
          <h2>標題五</h2>
          <p>內文五...</p>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "TimeLine"
  };
</script>

<style scoped>
  @import url("https://fonts.googleapis.com/css?family=Noto+Sans+TC:100,300,400,500,700,900&display=swap");
  * {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  body {
    background-color: #edece1;
  }
  .wrap {
    width: 960px;
    margin: auto;
    font-family: "Noto Sans TC", sans-serif;
  }
  h1 {
    font-size: 32px;
    margin-bottom: 10px;
  }
  h1 ~ p {
    line-height: 1.7;
  }
  .wrap:after {
    content: "";
    display: block;
    width: 100%;
    height: 0px;
    clear: both;
  }
  .timeline {
    padding: 100px 0 200px;
  }
  .timeline li {
    width: 50%;
    box-sizing: border-box;
    padding: 20px 0;
    position: relative;
  }
  .timeline li:nth-child(odd) {
    float: left;
    padding-right: 100px;
  }
  .timeline li:nth-child(even) {
    float: right;
    padding-left: 100px;
    transform: translateY(50%);
  }
  .timeline li:nth-child(odd)::after {
    content: "";
    position: absolute;
    z-index: -1;
    width: 1px;
    top: 0;
    height: 100%;
    background-color: #ccc;
    right: 0;
  }
  .timeline li:last-child::after {
    height: 50%;
  }

  .timeline li:before {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    margin: auto;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background-color: #aaa;
    z-index: 2;
  }
  .timeline li:nth-child(odd)::before {
    right: -10px;
  }
  .timeline li:nth-child(even)::before {
    left: -10px;
  }
  .timeline a {
    display: block;
    text-decoration: none;
    background-color: #fff;
    border: 1px solid #aaa;
    box-sizing: border-box;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 3px 3px 5px #888;
  }
  .timeline a:hover {
    background-color: #6fa5f6;
  }
  .timeline a:hover h2,
  .timeline a:hover p {
    color: #fff;
  }
  .timeline h2 {
    color: #333;
    font-family: "Noto Sans TC", sans-serif;
    font-weight: 700;
    margin-bottom: 1em;
  }
  .timeline p {
    color: #666;
    font-family: "Noto Sans TC", sans-serif;
    font-weight: 100;
    line-height: 1.5;
  }

  .timeline h2::after {
    content: "";
    position: absolute;
    height: 1px;
    width: 100px;
    background-color: #aaa;
    top: 0;
    bottom: 0;
    margin: auto;
  }
  .timeline li:nth-child(odd) h2::after {
    right: 0;
  }
  .timeline li:nth-child(even) h2::after {
    left: 0;
  }
</style>