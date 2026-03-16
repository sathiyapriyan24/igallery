# Ex.07 Design of Interactive Image Gallery
## Date:16.03.2026

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM:
~~~
<html>
    <head>
        <title>Intractive Image Gallery</title>
    </head>
    <style>
        body
        {
            background:black;
            text-align: center;
        }
        .header
        {
            background:green;
            padding:15px;
            font-size:20px;
        }
        .container
        {
            display:flex;
            justify-content:center;
            align-items:center;
            height:80vh;
        }
        .card img
        {
            width:300px;
            height:250px;
            border: 4px dotted pink;
            border-radius:10px;
        }
        .caption
        {
            margin-top:10px;
            font-size:20px;
            color:red;
        }
        button
        {
            padding:8px 18px;
            margin:5px;
            border:4px solid pink;
            background:blue;
            color:black;
        }
        .footer
        {
            background:white;
            padding:10px;
            position:fixed;
            bottom:50;
            width:100%;
            font-size:20px;
        }
    </style>
    <body>
        <div class="header">
            Electronic items
        </div>
        <div class="container">
            <div class="card">
                <img id="galleryImage" src="smart watch.jpg">
                <div class="caption" id="caption">
                    Smart Watch
                </div>
                <div class="buttons">
                    <button onclick="previous()">Previous</button>
                    <button onclick="next()">Next</button>
                </div>
            </div>
            <div class="footer">
                SATHIYA PRIYAN G(25018768)
            </div>
        </div>
        <script>
            let images=[
            {src:"watch.jpeg",caption:"Smart Watch"},
            {src:"headphone.jpeg",caption:"Headset"},
            {src:"tab.jpeg",caption:"Tablet"},
            {src:"mobile.jpeg",caption:"Mobile"},
            {src:"lap.jpeg",caption:"Laptop"},
            ];
            let index=0;

            function showImage()
            {
                document.getElementById("galleryImage").src = images[index].src;
                document.getElementById("caption").innerText = images[index].caption;
            }
            function next()
            {
                index++;
                if(index >= images.length)
                {
                    index = 0;
                }
                showImage();
            }
            function previous()
            {
                index--;
                if(index < 0)
                {
                index=images.length-1;
                }
                showImage();
            }
        </script>
    </body>
</html>
~~~
## OUTPUT:
![alt text](<Screenshot (41).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
