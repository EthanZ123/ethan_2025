---
layout: page
title: About me
permalink: /about/
comments: true
---


Hi, My name is Ethan. I'm a sophomore at Del Norte High School. &#128513; &#128513;


Here are the states that I have lived in...
<style>
    /* Style looks pretty compact, trace grid-container and grid-item in the code */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }
</style>

<!-- This grid_container class is for the CSS styling, the id is for JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "f/f7/Flag_of_Texas.svg", "greeting": "Howdy", "description": "Texas - Five years"},
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hi", "description": "California - Current"},
  
    ]; 
    
    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description


        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

<h1>Culture and Hobbies</h1>




I'm Chinese, but my parents and I speak a regional dialect of mandarin at home. &#x1F44D;

My main hobby is playing the violin and viola, and listening to music overall

Over the summer, I went to a national youth orchestra, where I met a lot of people who are now some of my closest friends 

Here are some pictures of me from over the summer:

<img src= "{{site.baseurl}}/images/notebooks/image copy 9.png" alt="Me">
<img src= "{{site.baseurl}}/images/notebooks/image copy 13.png" alt = "Me">

<body style="background-color:Pink;">


<script src="https://utteranc.es/client.js"
        repo="EthanZ123/ethan_2025"
        issue-term="title"
        label="utterances"
        theme="github-light"
        crossorigin="anonymous"
        async> 
</script>



