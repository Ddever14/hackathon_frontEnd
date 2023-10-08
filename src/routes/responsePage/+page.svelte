<script>
  let formData = {
    compname: "",
    industry: "",
    motoSlogan: "",
    filename: "",
    design: "",
    color: "",
    goalAd: "",
    tone: "",
    keyWords: "",
    finalIdea: ""
  };
  const handleSubmit = async () => {
    try {
      const response = await fetch('http://localhost:3000/submit-form', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify(formData),
      });

      const result = await response.json();
      console.log(result);  // log the result for now, handle it as you need
    } catch (error) {
      console.error('Error:', error);
    }
  };



</script>

<div class="topnav">
  <a class="logo" href="/"><img src="logo.png" alt="" class="image" /></a>
  <a class="getStarted" href="/responsePage.svelte"><button>Start Generating</button></a>
</div>

<body>
<div class="container">
  <div class="input">
    <h2 style="color:white">Advertisement Information</h2>
    <br/>
    <p style="color:white">The user will receive a prompt to input a comprehensive description for 
      their intended advertisement, along with the option to upload accompanying images. Additionally, 
      there is an optional provision to upload logos and/or prior advertisements for enhancement purposes.</p>
    <br/>
    <h1 style="color: #2f999d9e"><a href="#topOfDescription"><button class="descriptButton">Begin Description!</button></a></h1>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
  </div>

  <form on:submit|preventDefault={handleSubmit}>
    <div class="header">
      <a id=topOfDescription> <h1>Business Description</h1></a>
    </div>
    <div class="row">
      <div class="col-25">
        <label for="cname" style="color:white">Company Name</label>
      </div>
      <div class="col-75">
        <input type="text" id="cname" bind:value={formData.compname} placeholder="Your company name.." />
      </div>
    </div>
    <div class="row">
      <div class="col-25">
        <label for="industry" style="color:white">Industry</label>
      </div>
      <div class="col-75">
        <input type="text" id="industry" bind:value={formData.industry} placeholder="Your company's industry.." />
      </div>
    </div>
    <div class="row">
      <div class="col-25">
        <label for="moto" style="color:white">Moto/Slogan</label>
      </div>
      <div class="col-75">
        <input type="text" id="moto" bind:value={formData.motoSlogan} placeholder="Your company's moto.." />
      </div>
    </div>

    <div class="header">
      <h1>Visual Description</h1>
    </div>
    <div class="container2">
      <div class="row">
        <div class="col-25">
          <label for="cname" style="color:white">Advertisement Image</label>
        </div>
        <div class="col-75">
          <input type="file" id="myFile" bind:value={formData.filename} />
        </div>
      </div>
      <div class="row">
        <div class="col-25">
          <label for="design" style="color:white">Description of Image</label>
        </div>
        <div class="col-75">
          <textarea id="design" bind:value={formData.design} placeholder="Write a detailed description of the image submitted.." style="height:150px"></textarea>
        </div>
      </div>
      <div class="row">
        <div class="col-25">
          <label for="colors" style="color:white">Colors</label>
        </div>
        <div class="col-75">
          <input type="text" id="colors" bind:value={formData.color} placeholder="Your company's color scheme.." />
        </div>
      </div>
    </div>

    <div class="header">
      <h1>Objective Description</h1>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-25">
          <label for="goals" style="color:white">Goals</label>
        </div>
        <div class="col-75">
          <input type="text" id="goals" bind:value={formData.goalAd} placeholder="Goals of the advertisement.." />
        </div>
      </div>
      <div class="row">
        <div class="col-25">
          <label for="tone" style="color:white">Tone</label>
        </div>
        <div class="col-75">
          <input type="text" id="tone" bind:value={formData.tone} placeholder="Desired tone of your advertisement.." />
        </div>
      </div>
      <div class="row">
        <div class="col-25">
          <label for="words" style="color:white">Key Words/Phrases</label>
        </div>
        <div class="col-75">
          <input type="text" id="words" bind:value={formData.keyWords} placeholder="Key words you would like included.." />
        </div>
      </div>
    </div>

    <div class="header">
      <h1>Other Specifications/Ideas</h1>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-25">
          <label for="ideas" style="color:white">Final Ideas</label>
        </div>
        <div class="col-75">
          <textarea id="ideas" bind:value={formData.finalIdea} placeholder="Put any final or additional specifications about the ad you would like generated.." style="height:150px"></textarea>
        </div>
      </div>
      <div>
        <input style="font-size:larger" type="submit" value="Submit" />
      </div>
    </div>
  </form>
</div>
</body>

<style>

body, html {
background-color: black;
margin: -20px;
padding: 0;
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

/* Style inputs, select elements and textareas */
input[type=text], select, textarea{
width: 100%;
padding: 12px;
border: 1px solid #ccc;
border-radius: 4px;
box-sizing: border-box;
resize: vertical;
}

/* Style the label to display next to the inputs */
label {
display: inline-block;
float: right;
margin-right: 20px;
font-size: 25px;
}

/* Style the submit button */
input[type=submit] {
background-color: black;
color: white;
padding: 12px 20px;
border: none;
border-radius: 4px;
cursor: pointer;
float: right;
}

/* Style the container */
.container {
border-radius: 5px;
background-color: black;
padding: 20px;
}

.header {

color: #2f999d9e;
text-align: center;
float: center;
font-family:Verdana, Geneva, Tahoma, sans-serif;
}
/* Floating column for labels: 25% width */
.col-25 {
float: left;
width: 22%;
margin-top: 6px;
font-size: 20px;
}

/* Floating column for inputs: 75% width */
.col-75 {
float: left;
width: 75%;
margin-top: 6px;
}

/* Clear floats after the columns */
.row:after {
content: "";
display: table;
clear: both;
}

.input{
  color: white;
  font-size: 30px;
  text-align: center;
  margin-left: 35px;
  margin-right: 35px;
}

.descriptButton{
  font-size: 40px;
  width: 375px;  /* adjust based on your requirement */
  height: 115px; /* to maintain the aspect ratio */
  background-color: #2f999d9e;
  color: white;
  border: none;
  border-radius: 10px;
}

/* Responsive layout - when the screen is less than 600px wide, make the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
.col-25, .col-75, input[type=submit] {
  width: 100%;
  margin-top: 0;
}
}

</style>