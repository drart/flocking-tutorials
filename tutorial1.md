# Getting Started

This tutorial will show you how to take the examples from the Flocking Playground and run them on your own computer, without the need for an internet connection. 

## Step 1: Make sure the examples work for you

Go to the Flocking Playground and run the examples: https://flockingjs.org/demos/playground/

## Step: 2: Copy the sine example and work it into a simple HTML page

Open up your favourite text editor and type out a basic webpage. Put the example in a script tag. Open it up in a web browser. If you are lucky this won't work. 

    flock.synth({
        synthDef: {
            ugen: "flock.ugen.sinOsc",
            freq: 440,
            mul: 0.25
        }
    });

## Step 3: Add the Flocking.js library to your sketch

There are many ways to add Flocking.js to your project. We are going to start with the simplest method of downloading the file and having it in the same folder as our html file and then using the script tag to link it into our page. 

You can get a copy of Flocking.js by going to the github page and looking in the dist/ folder for various builds of the Flocking.js library. We are going to use the flocking-all.min.js file (it is included in this tutorial to make your life easier) as our Flocking.js build, it includes a few other libraries like Infusion and jQuery. 

Once you have a copy of the Flocking.js library you can include it in the head section of your webpage. Be sure to include the library before you try to call any of the code that might depend on it, otherwise you will get an error along the lines of unknown variable flock, which makes sense since Javascript isn't yet aware of how Flocking.js is going to work with audio. 

At this point your sketch will also not work. 

## Step 4: Putting it all together

We have Flocking.js and we have a demo. We have two more problems to solve: we need to tell Flocking.js to start playing and we need to create a user action in order for the browser to allow our program access to the sound on our webpage. 
