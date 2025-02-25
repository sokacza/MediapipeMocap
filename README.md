<h1>Mediapipe Mocap</h1>
<h2>About</h2>
<p>This project hopes to overcome some barriers that exist in similar projects. The goals of this project are: </p>
<ul>
<li>Performing motion capture on a live video feed using an accessible software package like Mediapipe</li>
<li>Live retargeting of point cloud data to an pre-defined armature</li>
<li>Transmission of armature pose to Unreal Engine using their LiveLink standard</li>
</ul>

<h2> Project Progress</h2>
<h3>This project can be broken into some distinct components:</h3>
<ul>
<li>Mediapipe pose capture script [Progress: COMPLETE]</li>
<li>Retargeting script [Progress: INCOMPLETE]</li>
<li>Armature model [Progress: ALMOST COMPLETE]</li>
<li>LiveLink script [Progress: COMPLETE]</li>
<li>CLI inteface [Progress: UP-TO-DATE]</li>
<li>Documentation [Progress: UP-TO-DATE]</li>
</ul>
 
 <h2> Pose Capture Script</h2>
 <p>This is a script that assigns each step of the motion capture process to its own queued thread. These threads can run in parallel. This will improve speed when multiple video feeds are implemented in the future.</p>
 
<h2>Retargeting Script</h2>
<p>The role of this script is to take the point data provided by Mediapipe and modify an armature model to match those landmark points. This script also has to mathematically extrapolate orientation and global position from the landmark points provided.</p>

<h2>Armature Model</h2>
<p>The role of these classes are to represent the hierarchy of bones in the armature model. It is implemented as a tree, where each element points to its parent and children, beginning at the ROOT component.</p>

<h2>LiveLink Script</h2>
<p>Publishes the bone coordinate and quaternion orientation to Unreal Engine using UDP LiveLink.</p>

<h2>CLI Interface</h2>
<p>Provides a convenient way to run test scripts.</p>

<h2>Documentation</h2>
<p>Currently, just ensuring that this markdown document is up-to-date. </p>
