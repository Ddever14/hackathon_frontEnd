<body>
<div class="topnav">
    <a class="logo" href="#home" style="margin-left:-60px"><img src = "logo.png" alt = "" class = "image"/></a>
    <a class="getStarted" href=/responsePage><button>Start Generating</button></a>
</div>

<div class="container">
  <div class="mainPage" >
    <div class="listMain" >
    <ol>
        
        <li><b>Input Product Description </b></li>
        <li><b>Prototype Advertisement </b></li>
        <li><b>Make Final Adjustments</b> </li>
        <li><b>Select Upload to Socials</b> </li>
    </ol>
    </div>
    <img src = "mainPic.jpg" alt = "" class = "image"/>
  <div class="middle">
    
    <div><a href=/responsePage ><button class="text">Get Started</button></a></div>
    
  </div>
  <div class="bottom">
    Create. Inspire. Entice.
  </div>
  
</div>

<div class="mainPage2" >
    
  
</div>
</div>
</body>

<style>
body {
  background-color: black;
  margin: 0;
  padding: 0;
}
.container {
    display: flex;
    flex-direction: column; /* This will stack children vertically */
    align-items: center; /* Center children horizontally */
    margin-right: -50px;
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


.mainPage {
  display: flex;
    flex-wrap: wrap; 
    width: 90%; /* Modify this to ensure it doesn't exceed viewport width */
    
    
}

.image {
  opacity: 1;
  display: block;
  height: 100%;
  transition: .5s ease;
  backface-visibility: hidden;
  margin-left: 60px;    
  width: 60%;
  border-radius: 15px;
  flex-shrink: 0;
}

.middle {
  transition: .5s ease;
  opacity: 0;
  position: absolute;
  top:45%;
  left: 60%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  text-align: center;
}

.mainPage:hover .image {
  opacity: 0.3;
}

.mainPage:hover .middle {
  opacity: 1;
}

.text {
  background-color: #2f999d9e;
  color: white;
  font-size: 16px;
  padding: 16px 32px;
}


.listMain {
    text-align: left;
    font-size: 24px;
    color: white;
    margin-right: 0px;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}

.listMain li {
    margin-top: 60px; /* Adds space to the top of each list item */
    margin-bottom: 60px; /* Adds space to the bottom of each list item */
}

.mainPage2 {
  position: relative;
  width: 102%;
  height: 100%;
  margin-top: 0px;
  margin-left: -9.5px;
  margin-right: -25px;
  background-color: black;
  display: flex;           /* Make this a flex container */
  justify-content: center; /* Center the children horizontally */
  align-items: center;  
}

.bottom {
    background-color: black;
    color: white;
    font-size: 40px;
    text-align: center;
    padding: 4%;
    margin-bottom: -20px;
    margin-left: -20px;
    width: 100%; 
    /* Removed the position: absolute; and other related properties */
}

</style>
