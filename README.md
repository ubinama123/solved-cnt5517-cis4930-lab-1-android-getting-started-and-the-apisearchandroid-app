Download Link: https://assignmentchef.com/product/solved-cnt5517-cis4930-lab-1-android-getting-started-and-the-apisearchandroid-app
<br>
<strong>INTRODUCTION</strong>

In this lab, you will learn how to setup the Android development environment and install all necessary developer tools on your computer in preparation for writing applications for Android. You will also learn how to use basic development tools to develop Android applications, from project creation to installation.




<strong>GOALS</strong>

<ul>

 <li>Setup the Android development environment (Install Android Studio).</li>

 <li>Create a <em>“Hello World”</em> Android application and run it on the Android Virtual Device (emulator).</li>

 <li>Understand the basic components of an Android project.</li>

 <li>Download and import the <em>APISearchAndroid</em> application and run it on the emulator.</li>

 <li>Make specific changes to the <em>APISearchAndroid</em></li>

</ul>




<h1>1.    Setting Up the Android Development Environment</h1>




To set up the development environment for Android, you first need to install Android

Studio, which can be found at <u>https://developer.android.com/studio/index.html</u>The download page also features the steps needed to install Android Studio. What follows is a quick summary of the steps.




<strong>Windows </strong>




<ul>

 <li>Download the executable from the official page.</li>

 <li>Run the installer</li>

 <li>Follow the prompts. You can leave all of the options as their defaults.</li>

 <li>Run Android Studio and follow the prompts. You can leave all of the options as their defaults. <strong>Notice:</strong> Make sure that you select the <em>Android Emulator Image</em> option when installing the SDK.</li>

</ul>




<strong>Mac</strong>




<ul>

 <li>Download the dmg from the official page.</li>

 <li>Mount the image and drag Android Studio into the Applications Folder</li>

 <li>Run Android Studio and follow the prompts. You can leave all of the options as their defaults. <strong>Notice:</strong> Make sure that you select the <em>Android Emulator Image</em> option when installing the SDK.</li>

</ul>




<strong>Linux</strong>




<ul>

 <li>Download the Android Studio archive from the official page.</li>

 <li>Depending on your distro, use your package manager to install Android Studio’s needed dependencies (libc6 libncurses5 libstdc++6 lib32z1 libbz2-1.0). <strong>Notice:</strong> If your machine is 64-bit, you must install the 32-bit versions of the aforementioned libraries</li>

 <li>Unarchive Android Studio to your installation folder of choice (Google recommends /opt) and run android-studio/bin/studio.sh. You can leave all of the options as their defaults. <strong>Notice:</strong> Make sure that you select the <em>Android Emulator Image</em> option when installing the SDK.</li>

</ul>




<h1>2.    Creating and Running <em>Hello World</em> Application</h1>




In this lab, we only require you to be able to run your app on a device emulator (Android Virtual Device or AVD). Of course, you should be able to run your app on an actual Android device if you have access to one, but you are not required to. To set up an AVD:

<ul>

 <li>Select the menu <strong>Tools</strong> =&gt; <strong>Android</strong> =&gt; <strong>AVD Manager</strong>, or click on the phone shaped icon in the toolbar. (<strong>Notice:</strong> If you have followed the installation steps, then a device should already be listed as <em>Nexus 5X API 25 x86, or later devices</em>)</li>

</ul>







If you do not see any devices, then follow these steps to create an Android Emulator.

<ul>

 <li>Open the <strong>Android</strong> <strong>Virtual Devices</strong></li>

 <li>Click the <strong>Create Virtual Device</strong> button (located in the bottom left).</li>

 <li>Select <strong>Nexus 5X</strong>.</li>

 <li>On the next screen, select the target build that you would like to run the application on, e.g., “<strong>Nougat</strong>“.</li>

 <li>Click <strong>Next </strong>and then <strong>Finish</strong> to terminate the SDK/AVD Manager Window.</li>

</ul>




Now, you have created an Android emulator. Next, create the <em>Hello World</em> app:

<ul>

 <li>Click the menu <strong>File </strong>-&gt; <strong>New </strong>-&gt; <strong>Android Application Project</strong>.</li>

 <li>Name the project “Hello World” and set location of project, or use default location</li>

 <li>Check the latest release/API level from the Build Target SDK list, and leave other settings as default.</li>

 <li>On the next screen, you can select an activity template from which to begin building your app. For this project, select <strong>Empty Activity</strong> and click <strong>Next</strong>.</li>

</ul>

<em>By selecting <strong>Empty Activity</strong>, a Hello World app is automatically generated.</em><sub>&#x263a;</sub> <em>How convenient!! The ADK is doing the assignment for you </em><em>  </em>

<ul>

 <li>Both the activity and its associated layout must be named. Leave the default selections and click <strong>Finish</strong>.</li>

</ul>

Now, run Hello World App on the Emulator:

<ul>

 <li>Select <strong>Run</strong> =&gt; <strong>Run App</strong> in the toolbar, then select your AVD and click <strong>OK</strong>.</li>

 <li>Select or make sure you are under <strong>Android Application.</strong> Then type in or browse and select your project in the <strong>Android</strong> Then in <strong>Target</strong> tab, choose the emulator you just created. Click <strong>Run</strong>.</li>

</ul>

The emulator will be launched (after some delays, so be patient). If all goes well, you should see the following result.







<strong><em>Congratulations, you’ve just created and ran your first Android Application! </em></strong> <strong><em>(Buy yourself an Oatmeal cookie)</em></strong>

<h1>3.    Directories and Files in an Android Project</h1>




Now let us look at the workspace of the <em>Hello World </em>app and get to know the useful directories and files in an Android project. Double click your <em>HelloWorld</em> project in the Package Explorer to expand it, if it is not already expanded. You should see the following directories:

<ul>

 <li>src/: directory for app’s main source code (includes Activity class)</li>

 <li>xml: describes all metadata about the app that the Android OS will need to run the app properly.

  <ul>

   <li>Package name used to identify the application.</li>

   <li>List of Activities, Services, Broadcast Receivers, and Content Provider classes and all of their necessary information, including permissions.o Libraries and API levels that the application will use.</li>

  </ul></li>

 <li>res/: directory for app resources. The main content categories include drawables, layouts, and values.

  <ul>

   <li>drawable/: directory that holds image and animation files designed for screens with different densities.</li>

   <li>layout/: directory for files that define your app’s user interface. It already contains a file called xml which defines the user interface for your HelloWorld Activity class. Double clicking on this file will open up the Android UI Editor that you can use to help generate the xml layout files.</li>

   <li>values/: directory where you define (in XML) your globally used colors, dimensions, strings and styles.</li>

  </ul></li>

 <li>gen/: directory where code is generated for all the resources defined in your res folder. It already contains one file called “R.java” which is a special static class that is used for referencing the data contained in your resource files.</li>

 <li>assets/:directory where stores miscellaneous files you need to access in your code as raw data. Unlike files in the res folder, the only way to load something from assets is to programmatically open it as a file.</li>

</ul>




<h1>4.    Activities</h1>

An <u>Activity</u> is an application component that provides a screen with which the user and the application can interact. For instance the user may interact with the application by dialing a phone number, taking a photo shot, sending an email, or viewing a map. Each activity has an associated <strong>Activity Layout</strong> (in XML) that is provided as a window with user interface widgets.

An application usually consists of multiple activities that are loosely bound to each other. Typically, one activity in an application is specified as the “main” activity, which is presented to the user when launching the application for the first time. Each activity can then start another activity using <u>Intent</u> in order to perform different actions. Each time a new activity starts, the previous activity is stopped, but the system preserves the activities in a stack (the “back stack”). Activities must be declared in the manifest file in order for them to be accessible to the system. Creating an activity in a project through <strong>File</strong> =&gt; <strong>New</strong> =&gt; <strong>Activity</strong>, which will automatically create a declaration for that activity in the manifest file. However, an activity can also be declared (or a declaration edited) by opening the manifest file and adding or editing an &lt;activity&gt; element as a child of the &lt;application&gt; element.

For more information about how to implement an Activity, how to create and use Intent, how to implement user interface layout for an Activity, how to declare the Activity in the Manifest file and so forth, read <u>Android developer webpage</u>.

<h1>5.    Download and Import the <em>APISearchAndroid</em> App</h1>




<ul>

 <li>Download the source code of the <em>APISearchAndroid</em> app covered in the Android lecture from <u>http://www.cise.ufl.edu/~helal/classes/s17/APISearchAndroid.zip</u></li>

 <li>Unpack the ZIP file and copy/paste the <em>APISearchAndroid</em> folder to your Android Studio workspace (i.e., the folder where your<em> Hello World</em> app is located).</li>

 <li>Next, to open the <em>APISearchAndroid</em> project into your Android Studio project, click the menu <strong>File</strong> =&gt; <strong>Open</strong></li>

 <li>In this screen, browse and select the directory where you just saved your <em>APISearchAndroid</em> Click <strong>OK</strong>, then <strong>Next</strong>, and then<strong> Finish</strong>.</li>

</ul>




Now you have opened the <em>APISearchAndroid</em> App in your Android Studio.

<h1>6.    Making Changes to <em>APISearchAndroid</em> App</h1>




In this project, you are required to make following two changes to the APISearchAndroid application you just imported.




<ol>

 <li>A user can choose any result from the list of the returned results by clicking on it. When the user clicks a particular result, it will navigate to a new screen which displays the user selected result information (title, text, image).</li>

</ol>

To achieve 1, you will need to create a new Empty Activity (name it

ResultDisplayActivity) to display the information about the user selected result. Then you will need to add new function to the APISearchActivity class to be able to parse the user selected item from the user interface and initiate the ResultDisplayActivity (So now you are doing Java programming). Finally, you will have to reconfigure the application Manifest to use your new name retrieval Activity on startup.

<ol start="2">

 <li>Add back button functionality to the layout of the result display (result.xml). This button allows the user to finish the current activity and load the previous screen view (i.e., from result to the main layout) by clicking on it. Note that, at any screen (e.g., main layout) that is loaded by pressing back button, it should still be able to perform its function properly (e.g, in the main view, user is still able to click on any result from the list to navigate to a new screen where its info is displayed).</li>

</ol>

<strong>Extra Credit.   </strong>

For extra credit, implement a way to add a result as a “favorite” result. The storage of those marked as favorites should be on the local device (not on the API endpoint). Feel free to use an ImageButton with the image of a star as the button to mark a result as a favorite. <strong>Make sure that the ID of the button is starButton</strong>. This will allow for our grading scripts to be able to interface with those buttons. Now your modified app should look like.




<em>APISearchActivity                                                                     ResultDisplayActivity</em>




<h1>7.    Exporting Android Application and Deliverables</h1>




The Android system requires that all installed applications be digitally signed with a certificate. The system will not install an application on an emulator or a device if it is not signed. However, Android Studio has been automatically signing your application with its own “debug” certificate and compile your source code as .apk file under res/ folder. Although signing with the “debug” certificate is not acceptable for release to the general public, an application with “debug” certificate can be installed on an emulator or personal Android device. As of now, you’ve only been executing your application on an emulator by launching it through Android Studio’s AVD or your personal Android device. So debug certificate should be sufficient for our use. For more information (e.g., signing your application in release mode), read

<u>http://developer.android.com/tools/publishing/app-signing.html</u>




To complete this lab you are required to submit your source code through Canvas.

Pack the folder of your project into a .zip file and submit the compressed file to Canvas. For example, if you have not changed the project name, you should compress the folder “APISearchAndroid” into APISearchAndroid.zip. Make sure your folder can be successfully imported and run in the Android Studio before submitting your code.