<template>
  <head>
    <link href="https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:wght@300;700&display=swap" rel="stylesheet">
  </head>
  <div class="hello">
    <div class="div">
      <a @click="handleClick"><h1 class="latest">ALL THE LATEST FROM AEG</h1></a>
      <div class="recipes">
        <div class="card">
          <a @click="handleClick"><img alt="Vue logo" src="./img2/Image-01.jpg"></a>
          <div class="info1">
            <a @click="handleClick"><h2 class="subtitles">Summer Lunch Menu Mark Best</h2></a>
            <a @click="handleClick"><p>AEG ambassador Mark Best's summer eats are guaranteed to help you make the most of the warmer months and entertain at home. Make the most of your cooking with these tips.</p></a>
            <a @click="handleClick">READ MORE</a>
          </div>
        </div>
        <div class="card">
          <a @click="handleClick"><img alt="Vue logo" src="./img2/Image-02.jpg"></a>
          <div class="info">
            <a @click="handleClick"><h2 class="subtitles">A Traditional Christmas Eve, Mark Best Style</h2></a>
            <a @click="handleClick"><p>AEG ambassador Mark Best's summer eats are guaranteed to help you make the most of the warmer months and entertain at home. Make the most of your cooking with these tips.</p></a>
            <a @click="handleClick">READ MORE</a>
          </div>
        </div>
        <div class="card">
          <a @click="handleClick"><img alt="Vue logo" src="./img2/Image-03.jpg"></a>
          <div class="info">
            <a @click="handleClick"><h2 class="subtitles">Taking Taste Further</h2></a>
            <a @click="handleClick"><p>AEG ambassador Mark Best's summer eats are guaranteed to help you make the most of the warmer months and entertain at home. Make the most of your cooking with these tips.</p></a>
            <a @click="handleClick">READ MORE</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    // function that output a consol.log() everytime an anchor tag is clicked
    handleClick(event) {
      event.preventDefault();
      console.log('Link clicked:', event.target.innerText);
    }
  }
}
</script>

<style scoped>
.hello {
  background-color: #0e0e0e;
  padding: 130px 100px 100px 140px;
}

h1 {
  font-size: 38px;
  color: white; /* Ensure the heading text is visible */
}

.recipes {
  display: flex;
  flex-wrap: wrap; /* Allow cards to wrap on smaller screens */
  gap: 20px;
  margin-top: 55px;
}

.card {
  flex: 1 1 calc(33.333% - 20px); /* Three columns with space for gaps */
  box-sizing: border-box;
}

.card img {
  width: 100%;
  height: auto; /* Maintain aspect ratio */
}

h2 {
  font-size: 18px;
  color: white; /* Ensure the text is visible */
}

.info1, .info {
  text-align: left;
  margin-left: 9px;
}

p {
  color: gray;
  line-height: 1.5;
  font-family: 'Open Sans Condensed', sans-serif;
  font-size: 20px;
}

a {
  color: white;
  text-decoration: none; /* Remove underline */
  border-bottom: 2px solid red; /* Red line below the link */
  padding-bottom: 2px;
  font-family: 'Open Sans Condensed', sans-serif;
  font-size: 17px;
}

.latest{
  width: 100%;
  font-family: 'Open Sans Condensed', sans-serif;
  font-weight: 400;
  letter-spacing: 0.08em;
  font-size: 50px;
}

a:hover {
  text-decoration: underline; /* Add underline on hover */
}

/* Responsive Design */
@media (max-width: 1024px) {
  .hello {
    padding: 100px 50px 50px 50px;
  }

  h1 {
    font-size: 32px;
  }

  .card {
    flex: 1 1 calc(50% - 20px); /* Two columns on medium screens */
  }

  h2 {
    font-size: 16px;
  }
  .subtitles{
    font-family: 'Open Sans Condensed', sans-serif;
  }
}

@media (max-width: 768px) {
  .hello {
    padding: 70px 20px 20px 20px;
  }

  h1 {
    font-size: 28px;
  }

  .card {
    flex: 1 1 100%; /* Full width cards on small screens */
  }

  h2 {
    font-size: 14px;
  }

  p {
    font-size: 14px;
  }
}

@media (max-width: 480px) {
  .hello {
    padding: 50px 10px 10px 10px;
  }

  h1 {
    font-size: 24px;
  }

  h2 {
    font-size: 12px;
  }

  p {
    font-size: 12px;
  }
}
</style>
