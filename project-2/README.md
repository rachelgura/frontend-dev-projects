This project is an interactive resume detailing the projects I have completed, my education, work experience and places I have lived. To view this resume select the index.html file to run. In this project I was given a template which looked something like this:
![](http://i.imgur.com/pWU1Xbl.png)
The end was result was this:
"images/resume.png"

The project contains the following files:

* **index.html**: The main HTML document. Contains links to all of the CSS and JS resources needed to render the resume, including resumeBuilder.js.
* **js/helper.js**: Contains helper code needed to format the resume and build the map. It also has a few function shells for additional functionality. More on helper.js further down.
* **js/resumeBuilder.js**: This file is empty. You should write your code here.
* **js/jQuery.js**: The jQuery library.
* **css/style.css**: Contains all of the CSS needed to style the page.
* **README.md**: 
The GitHub readme file.
* and some images in the images directory.


The resume has four distinct sections: work, education, projects and a header with biographical information. For this project I:

1. Built four JSON objects, each one representing a different resume section. The objects created need to follow the schema below exactly. Property names are case-sensitive. 

* `bio` contains:
        
            name : string
            role : string
            contacts : an object with
                  mobile: string
                  email: string 
                  github: string
                  twitter: string 
                  location: string
            welcomeMessage: string 
            skills: array of strings
            biopic: url
            display: function taking no parameters

* `education` contains:
      
            schools: array of objects with
                 name: string
                 location: string
                 degree: string
                 majors: array of strings
                 dates: integer (graduation date)
                 url: string
            onlineCourses: array with
                 title: string
                 school: string
                 date: integer (date finished)
                 url: string
            display: function taking no parameters

* `work` contains
          
            jobs: array of objects with
                 employer: string 
                 title: string 
                 location: string 
                 dates: string (works with a hyphen between them)
                 description: string 
            display: function taking no parameters

* `projects` contains:

            projects: array of objects with
                  title: string 
                  dates: string (works with a hyphen between them)
                  description: string
                  images: array with string urls
            display: function taking no parameters

2. Iterated through each JSON object and append its information to index.html in the correct section.
 * Used jQuery’s `selector.append()` and `selector.prepend()` functions to modify index.html. `selector.append()` made an element appear at the end of a selected section. `selector.prepend()` makes an element appear at the beginning of a selected section.
   * Used the JavaScript method `string.replace(old, new)` to swap out all the placeholder text (e.g. `%data%`) for data from your resume JSON objects.
  * Used the mockup at the top of the page as a guide for the order in which you should append elements to the page.
3. The resume includes an interactive map which was added by 
 * In resumeBuilder.js, appended the googleMap string to `<div id=”mapDiv”>`.
 * In helper.js, at the bottom of the file, uncomment code to initialize map and set fitBounds.
4. All code for adding elements to the resume is written within functions. All functions encapsulated within the same objects containing your resume data. 
5. Your resume should also `console.log()` information about click locations. On line 90 in helper.js, you’ll find a jQuery onclick handler that was modified to work with the `logClicks(x,y)` function above it.

