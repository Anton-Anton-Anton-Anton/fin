<script>
    import Snippet from "./Snippet.svelte";
</script>

<h2>Installation Instructions</h2>

<h3>Svelte</h3>

<p>NodeJS and npm are required to install Svelte. The instructions for that installation are provided below</p>

<p>After that is done, we need a few other tools to install Svelte. Run the following commands from the project folder</p>

<Snippet text="npm install -g npx"/>
<Snippet text="npm install -g degit"/>

<p>Now we can clone the template project to be able to start modifying it afterwards. The following command clones it in the current working directory. </p>

<Snippet text="npx degit sveltejs/template ."/>

<p>The following command will install all the dependencies which are specified in the package.json file. This will also create the 'node-modules' folder, which is full of the programs/projects that are needed to run all this.</p>
<Snippet text="npm install"/>

<p>To start the app and see it in the broswer at http://localhost:8080, run the following command. Ctrol-C to end this process</p>
<Snippet text="npm run dev"/>


<h3>NodeJS</h3>

<p>These instructions are for installing NodeJS for an Ubuntu Operating System. One will need the `apt` package manager first. Then we run the following commands</p>

<Snippet text="sudo apt update"/>
<Snippet text="sudo apt install nodejs"/>
<Snippet text="node -v"/>

<p>If all is successful you should get a version printed out, of the Node you just installed.</p>

<p>Then to get the npm package manager, run the following command</p>
<Snippet text="sudo apt install npm"/>

<p></p>
