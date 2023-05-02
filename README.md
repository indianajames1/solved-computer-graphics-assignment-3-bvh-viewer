Download Link: https://assignmentchef.com/product/solved-computer-graphics-assignment-3-bvh-viewer
<br>
<strong></strong>



<ul>

 <li>Only accept answers submitted via git push to this course project for you at <a href="https://hconnect.hanyang.ac.kr/">https://hconnect.hanyang.ac.kr</a> (&lt;Year&gt;_&lt;Course no.&gt;_&lt;Class code&gt;/&lt;Year&gt;_&lt;Course</li>

</ul>

no.&gt;_&lt;Student ID&gt;.git).

<ul>

 <li>Place your files under the directory structure <strong>&lt;Assignment name&gt;/&lt;your files&gt;</strong> just like</li>

</ul>

the following example.

<table width="234">

 <tbody>

  <tr>

   <td width="234">+ 2020_ITE0000_2019000001+ ClassAssignment1/–  main.py–  report.docx</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>The submission time is determined not when the commit is made but when the git push</li>

</ul>

is made.




<ol>

 <li>Implement your own bvh file viewer.

  <ol>

   <li>You have to implement all requirements in a single program. This assignment DOES NOT require each requirement to be a separate program</li>

   <li>The window size doesn’t need to be (480, 480). Use the larger window that is enough to</li>

  </ol></li>

</ol>

see the details of the viewer.




<ol start="2">

 <li><strong>Requirements </strong>

  <ol>

   <li><strong>Manipulate the camera in the same way as in ClassAssignment1 using your </strong></li>

  </ol></li>

</ol>

<strong>ClassAssignment1 code (10 pts). </strong>

<ol>

 <li>Also draw the reference grid plane.</li>

</ol>




<ol>

 <li><strong>Load a bvh file and render it (80 pts) </strong>

  <ol>

   <li>Open a bvh file by drag-and-drop to your bvh viewer window <strong>(10 pts)</strong></li>

  </ol></li>

 <li>Google glfwSetDropCallback to see how to do it</li>

 <li>The viewer should render only one bvh file at a time. If a bvh file B is drag-anddropped to the viewer while it is rendering another bvh file A, the viewer should</li>

</ol>

only render the new bvh file B.

<ol start="3">

 <li><strong>This feature is essential for scoring your assignment, so if not implemented, </strong></li>

</ol>

<strong>you won’t get any score for “Load a bvh file and render it (80 pts)” </strong>

<ol>

 <li>Read the bvh file and <strong>render the “skeleton” (t-pose) of the motion when you load the file by drag-and-drop</strong> <strong>(30 pts).</strong>

  <ol>

   <li><strong>Do not automatically animate the character.</strong> Just draw its skeleton (t-pose) when</li>

  </ol></li>

</ol>

you open a file.

<ol start="2">

 <li>Just draw joints with offsets between them only using the HIERARCHY section of</li>

</ol>

the bvh file.

<ol start="3">

 <li>In other words, draw a pose of the motion with zero translation (0,0,0) and no rotation (identity matrix) being applied to transitional joints and rotational joints,</li>

</ol>

respectively.

<ol start="4">

 <li>Draw the skeleton by line segments. Each line segment should connect each pair</li>

</ol>

of parent-child joints.

<ol start="5">

 <li>For end-effector joints such as foot, a line segmented should connect the end-</li>

</ol>

effector joint and the “end site”.

<ol start="6">

 <li>An example screenshot for sample-walk.bvh</li>

 <li></li>

</ol>

<ul>

 <li><strong>Animate the loaded motion if you press the &lt;spacebar&gt; key</strong> <strong>(30 pts)</strong>.

  <ol>

   <li>As time goes by, draw each pose of the motion using each line of frame data in</li>

  </ol></li>

</ul>

the MOTION of the bvh file, from the start frame to the end frame.

<ol start="2">

 <li>Calling glfw.swap_interval(1) in your main function, then just drawing the pose of each frame for each iteration of the main loop (the while loop in the main function)</li>

</ol>

would be enough for timing of rendering each pose.

<ol start="3">

 <li>After drawing the last frame, just <strong>replay</strong> the motion again (draw from the first</li>

</ol>

frame to the last frame again).

<ol start="4">

 <li>Example screenshots for sample-walk.bvh</li>

</ol>




<ol>

 <li>When open a bvh file, print out the following information of the bvh file to stdout</li>

</ol>

(console) <strong>(10 pts)</strong>

<ol>

 <li>File name</li>

 <li>Number of frames</li>

 <li>FPS (which is 1/FrameTime)</li>

 <li>Number of joints (including root)</li>

 <li>List of all joint names</li>

</ol>




<ol start="3">

 <li><strong>Report (10 pts) </strong>

  <ol>

   <li>Submit a report of <strong>at most 2 pages</strong> in docx file format (MS Word). Do not exceed the</li>

  </ol></li>

</ol>

limit.

<ol>

 <li>The report should include:

  <ol>

   <li>Which requirements you implemented (5 pts) ii.A few screenshot images of your program with downloaded bvh files (5 pts)

    <ol>

     <li>Download bvh files from the Internet and open them with your viewer. You may download bvh files from

      <ol>

       <li><a href="http://motion.hahasoha.net/">http://motion.hahasoha.net/</a></li>

       <li><a href="http://mocap.cs.sfu.ca/">http://mocap.cs.sfu.ca/</a></li>

       <li><a href="http://dancedb.eu/main/performances">http://dancedb.eu/main/performances</a></li>

      </ol></li>

     <li>Choose some of the best looking screenshot images of your viewer.</li>

     <li><strong>Do not use the sample bvh files for this requirement. </strong>You must use other bvh files downloaded from internet to get score for this requirement.</li>

    </ol></li>

   <li>You do not need to try to write a long report. Just write down the required information.</li>

  </ol></li>

</ol>

Use either English or Korean.




<ol start="4">

 <li><strong>Extra credits (Only one of two items A, B will be reflected in the score) </strong>

  <ol>

   <li>Use a box to draw each body part instead of a line segment <strong>(+10 pts).</strong>

    <ol>

     <li>The boxes should be rendered with proper shading and lighting settings.</li>

     <li>If you render the body parts without lighting and shading, you cannot get the score</li>

    </ol></li>

  </ol></li>

</ol>

for this item.

<ul>

 <li>You can implement this requirement for only one of the sample bvh files provided.</li>

</ul>

<ol>

 <li>An example screenshot for sample-walk.bvh

  <ol>

   <li></li>

   <li>(You don’t need to draw the shadow and shaded ground plane)</li>

  </ol></li>

 <li>Use different obj files to draw each body part instead of a line segment <strong>(+20 pts).</strong>

  <ol>

   <li>The meshes should be rendered with proper shading and lighting settings.</li>

   <li>If you render the body parts without lighting and shading, you cannot get the score</li>

  </ol></li>

</ol>

for this item.

<ul>

 <li>You can implement this requirement for only one of the sample bvh files provided.</li>

</ul>

<ol>

 <li>Example screenshots (not for sample-walk.bvh)

  <ol>

   <li></li>

   <li>(You don’t need to draw the shadow and shaded ground plane)</li>

   <li>Search and download cool obj files from the internet and use them.

    <ol>

     <li>If you use simple obj files like box shapes, you’ll only get 10 pts.</li>

    </ol></li>

  </ol></li>

</ol>




<ol start="5">

 <li><strong>Runtime Environment </strong>

  <ol start="3">

   <li><strong>Your program should be able to run on systems only with Python 3.7 or later, NumPy, </strong></li>

  </ol></li>

</ol>

<strong>PyOpenGL, glfw. Do not use any other additional python modules. </strong>

<ol>

 <li>Only <strong>glfw</strong> is allowed for event processing and window &amp; OpenGL context management. <strong>Do not use glut functions for this purpose.</strong></li>

 <li><strong>If your program does not meet this requirement, it will not run on TA’s computer </strong><strong>so </strong></li>

</ol>

<strong>you will not get any score for this assignment (except report). </strong>

<strong> </strong>

<ol start="6">

 <li><strong>Test your viewer with sample bvh files. </strong> sample-walk.bvh: A walking motion file</li>

 <li>sample-spin.bvh: A walking while spinning around a vertical axis</li>

</ol>

<strong> </strong>

<ol start="7">

 <li><strong>What you have to submit: </strong>

  <ol>

   <li><strong>.py files</strong>

    <ol>

     <li>You can use multiple .py files for this assignment. In this case, explain how to run the</li>

    </ol></li>

  </ol></li>

</ol>

program in the report.

<ol>

 <li><strong>.docx report file</strong></li>

</ol>




<ol start="8">

 <li>Additional information

  <ol>

   <li>drop_callback in glfw python binding is slightly different from that of original glfw written in C. drop_callback in python takes only two parameters, window and paths. paths is a list</li>

  </ol></li>

</ol>

of dropped file paths.

<ol>

 <li>Python provides powerful string methods helpful for parsing a bvh file. Among them, split() will be most useful.</li>

</ol>