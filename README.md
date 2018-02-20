CS 4331-002 – Virtual Reality Project 1
Due: February 20, 2018
Video demonstration link
Project link
https://gar37012.github.io/VR-project-1/
Report
What I learned
•	How to use google cardboard
•	The basics of Aframe and HTML
•	Add, commit, and push to GitHub
•	Where the link to my GitHub account is for each repositories
 General issues
•	Iphone 6 devices do not work well when testing virtual reality scene on google cardboard
•	Downloading models such as .obj and .gtlf can have good and bad models 
•	Low frame rate depending on models/ how much memory taken up
Contributors	
        Eddie Garcia
Key features
Living Room
The living room has different features, the most noticeable ones are the 3D models as you can see below. In the screen shot you can see a dog, cat, couch, and statue that shows the many possibilities with Virtual Reality. There is a mix of GLTF and OBJ models that is interesting how html and Aframe allows you to do that.
 

Another feature that I added was a light switch. This was a difficult feature for me to add at first. I like that on a click of a mouse the user can change the lighting. In my picture the lighting is not complete dark, however you can change the light intensity based on user preference. 
 
Here is the code that helped me create this feature:

      <!-- Lighting -->
      <a-light type="ambient" color="#ccc" position="0 0 0" rotation="0 0 0" scale="1 1 1" visible="true" light="type:ambient;color:#ccc"></a-light>
      <a-light color="#ddf" distance="100" intensity="0.4" type="point" position="0 0 0" rotation="0 0 0" scale="1 1 1" visible="true" light="color:#ddf;distance:100;intensity:0.4;type:point"></a-light>
      <a-light color="#ddf" position="3 10 -10" distance="50" intensity="0.4" type="point" rotation="0 0 0" scale="1 1 1" visible="true" light="color:#ddf;distance:50;intensity:0.4;type:point"></a-light>

	 
		 <a-entity id = "light" = static-body geometry="primitive: sphere; radius:0.2" position="79.27 9.757 -8.16" rotation="0 0 0" material="shader: standard;
		roughness: 1; src: url(images/TV.png)" light="type:ambient; intensity:0.8; color:white; distance:10;" class="intersectable">
            <a-animation begin="click" attribute="light.intensity" from="0.8" to="0.1" direction="alternate"></a-animation>
			
			<a-box color= "blue" depth="2" height="4" width="0.5" position="0.336 0.009 -.02" rotation="0 0 0" scale="1 .4 .3" visible="true" material="color:#7AD2F7" geometry="primitive:box;depth:2;height:4;width:0.5"></a-box>
        </a-entity>
	  
