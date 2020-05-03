<p><strong># glfw-set</strong></p>
<p><span style="color: #ff0000;">the target of this work is to fix error faces you when tring to create a new empty project in vs 2017 and run glfw code in it.</span></p>
<p><br />if you tried this video: <a href="https://www.youtube.com/watch?v=k9LDF016_1A&amp;feature=share">https://www.youtube.com/watch?v=k9LDF016_1A&amp;feature=share</a></p>
<p><span style="color: #ff0000;">and it's not working try the following</span></p>
<p><span style="color: #333399;">if you tried to add a glfw work before delete all glfw files in this directory </span><br />C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Auxiliary\VS\include</p>
<p><span style="color: #333399;">then take this link to download glfw precompiled binary for win 32 </span><br />https://github.com/glfw/glfw/releases/download/3.2.1/glfw-3.2.1.bin.WIN32.zip</p>
<p>the file will download library and include files</p>

<img src="images/1.png">
<p>&nbsp;</p>
<p>add include file in vs include directory&nbsp;</p>

<p>add lib file in vs lib directory&nbsp;</p>
<p>add glfw3.dll in system32</p>

the same for glad except you have to download your own version depending on your graphic card opengl value 
https://glad.dav1d.de/

you can check this on your graphic card vendor website 
<p>&nbsp;</p>
<p>in the new created empty project do the following :</p>
<p>1- create new .cpp file and copy the following file code in&nbsp;</p>
<p><a href="https://learnopengl.com/code_viewer_gh.php?code=src/1.getting_started/2.1.hello_triangle/hello_triangle.cpp">https://learnopengl.com/code_viewer_gh.php?code=src/1.getting_started/2.1.hello_triangle/hello_triangle.cpp</a></p>
<p>2- add glad.c file to your project directory&nbsp;</p>
<p>// to get project directory RC the project in vs2017 and choose open folder in file explorer&nbsp;</p>
<p>3- RC project source in vs2017 project ---&gt; add --&gt; exiciting item ---&gt; will open navigation window ---&gt; glad.c</p>
<p>4- in project properties :</p>
<p>linker --&gt; input --&gt; additional depedencies ---&gt; glfw3.lib , opengl32.lib</p>
<p>5- tools ---&gt; options ---&gt; depugging --&gt; symbols -- &gt; check "microsoft symbol server"</p>
<img src="images/2.png">

<p>try to run</p>
<p>&nbsp;</p>
<p><br /><span style="color: #339966;">Errors fix visual studio 2017</span></p>
<p><br /> <br />1- Can&rsquo;t open pdb file </p>
<p>Go to Tools-&gt;Options-&gt;Debugging-&gt;Symbols</p>
<img src="images/2.png">

<p><br />2- Screen disappears <br />Right click on your project-&gt; Properties-&gt;Configuration Properties-&gt; Linker-&gt; System, select Console (/SUBSYSTEM:CONSOLE) in SubSystem option.
  
  <img src="images/3.png">
<img src="images/4.png">

  After this, press Ctrl+F5 then by default it prompts your to press return to close the window. If you want to use the debugger, you should put a breakpoint on the last line.<br /> </p>
<p>Configuration ----- release or ctrl + f5</p>
