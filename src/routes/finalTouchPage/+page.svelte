<div class="topnav">
    <a class="logo" href="/"><img src = "logo.png" alt = "" class = "image"/></a>
    <a class="getStarted" href="/responsePage.svelte"><button>Start Generating</button></a>
</div>

<body>
<div>
<h1 class="heading">Congratulations! Your Post Has Been Made!</h1>
<p style="color:white">You can now see your advertisement post on Twitter. Is this post not to your liking? No problem!
    please enter in the box below any specific changes you would like to make about the text of your generated
    advertisement. 
</p>

<br/>
<br/>

<p style="color:white">However, if you are pleased with the posted advertisement, come back to make more here at AdVantage!</p>
</div>







</body>
<style>

.body {
    background-color: black;
    width: 100%;
    height:100%;
}

.heading {
    text-align: center;
    color: white;
    font-size: 40px;
}

.topnav {
  background-color: #000000;
  overflow: hidden;
  margin-top: -10px;
  margin-left: -10px;
  margin-right: -19px;
}

/* Style the links inside the navigation bar */
.topnav a {
float: left;
color: #f2f2f2;
text-align: center;
padding: 25px 30px;
text-decoration: none;
font-size: 17px;
}

.topnav a.logo .image {
  width: 160px;  /* adjust based on your requirement */
  height: 50px; /* to maintain the aspect ratio */
  float: right; /* to push it to the right */
  margin-top: 10px;
  margin-right: 0px;
}

/* Change the color of links on hover */
.topnav a:hover {
background-color: #ddd;
color: black;
}

/* Add a color to the active/current link */
.topnav a.getStarted {
background-color: #000000;
color: white;
float: right;
}

.topnav a.getStarted button{
  font-size: 13px;
  width: 160px;  /* adjust based on your requirement */
  height: 50px; /* to maintain the aspect ratio */
  background-color: #2f999d9e;
  color: white;
  border: none;
  border-radius: 10px;
}


</style>
