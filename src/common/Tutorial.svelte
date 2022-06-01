<script>
    import Snippet from "./Snippet.svelte";
</script>

<h2>Installation Instructions</h2>

<h3>Svelte Tutorial</h3>

<p>Once everything is installed and the template project is runnable, we can start editing and/or creating files with the .svelte extension. These are the components which serve the function of separation of concerns and code reusability.</p>

<p>The entry point is the main.js file. It instantiates and calls the App.svelte, and we don't need to modify main.js, we can go and start working on App.svelte. We will also be creating our own components.</p>

<p>In our app, we will have a left sidebar which won't change, and the content section which will present a different component based on which sidebar item is selected.</p>

<p>In the script section create a variable to hold the state of what the user clicked, and that will determine what will appear in the content section.</p>


<p>Make your sections for the sidebar and set them to display flex and set flex direction to column, so they appear vertically. On each section add an on:click property and pass them all a separate reacting function, which you don't call, but just wrap its name with curly brackets. All those functions will do is set the global variable of what to appear in the content. this is just like a button, but on a div.</p>


<p>The function itself is defined up in the scripts sections and all it does is set the whatsClicked variable to numbers 1-5</p>

<p>Then in the content div, we set up some template logic to determine which component to put into it, based on the value of that variable</p>

<p>And now we just need to create those components in their own separate file each. But we want make a folder for all of them to be in one place </p>

    
<p>Then for each ComponentX make a ComponentX.svelte file in that folder.</p>
<p>Import the components in the place where they need to be used, ie App.svelete in this or inside the components themselves (when they need to use other components).</p>
<p>Let's make a Snippet component which will let us quickly add a line of code into any of the components. This component needs to receive its text from the component that used it. The way it works is that we simply need to in the component that calls our Snippet, we just need to set the text like a property </p>

<p>In our Snippet component we can use the text that was sent to us if we wrap it in curly brackets</p>

<p>We set the styling in the Snippet component itself. I set the font family to monospace, put a little bottom border to delianate the lines -- as each snippet is strictly a line of code, but that can wrap, and the border will let us know that it's still one line</p>

<Snippet text="this is meant to be code"/>
<Snippet text="nice and easy to create, and reuse this component"/>

<p>I am very short on time, otherwise I'd try to make this tutorial more detailed.</p>
