<!-- PROJECT LOGO -->
<p align="center">
  <a href="https://devondoyle.com/"><img src="images/devon_suit.png" alt="Logo" width="150" height="150" style="border-radius:50%"></a>
  <h1 align="center">Motion Profile Mapper (2018)</h1>
  <p align="center">
    <a href="https://github.com/DevonRD/Motion-Profile-Mapper-2018/network/members"><img src="https://img.shields.io/github/forks/DevonRD/Motion-Profile-Mapper-2018?style=for-the-badge"/></a>
    <a href="https://github.com/DevonRD/Motion-Profile-Mapper-2018/stargazers"><img src="https://img.shields.io/github/stars/DevonRD/Motion-Profile-Mapper-2018?style=for-the-badge"/></a>
    <a href="https://github.com/DevonRD/Motion-Profile-Mapper-2018/issues"><img src="https://img.shields.io/github/issues/DevonRD/Motion-Profile-Mapper-2018?style=for-the-badge"/></a>
    <a href="https://github.com/DevonRD/Motion-Profile-Mapper-2018/blob/master/LICENSE"><img src="https://img.shields.io/github/license/DevonRD/Motion-Profile-Mapper-2018?style=for-the-badge"/></a>
  </p>
  <p align="center">
    <a href="https://github.com/DevonRD/Motion-Profile-Mapper-2018/issues">Report Bug</a>
    ·
    <a href="https://devondoyle.com/">My Portfolio</a>
	<br><br>
    <a href="https://linkedin.com/in/devon-doyle/"><img src="https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555"/></a>
  </p>
</p>

<!-- TABLE OF CONTENTS -->
<h2 style="display: inline-block">Table of Contents</h2>
<details open="open">
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
		<li><a href="#the-user-interface">The User Interface</a></li>
		<li><a href="#velocity-calculation">Velocity Calculation</a></li>
		<li><a href="#competition-versatility">Competition Versatility</a></li>
		<li><a href="#proper-programming">Proper Programming</a></li>
      </ul>
    </li>
    <li><a href="#try-it-out">Try it Out</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

In my final year of high school, as lead programmer of FRC Team 3539, my main goal was to develop an 
application that creates paths on the field that the robot could read and follow based solely on user 
input. In the first 15 seconds of every game the robot needed to move by itself, and instead of 
hard-coding motor speeds and times manually and spending hours testing each resulting path, we created 
this application to quickly design a specific path and automatically generate motor velocity and time 
data in Java for the robot to follow that path. This was much easier to use and allowed us to be 
more versatile during competitions, where the ability to change based on your teammates' needs was 
essential. I am extremely grateful to our mentor, Mr. VanCamp, who provided framework and guidance 
and was absolutely essential in our journey to reaching the end product.

### Built With

* [Windows Forms](https://docs.microsoft.com/en-us/dotnet/desktop/winforms/?view=netdesktop-5.0)
* [C#](https://docs.microsoft.com/en-us/dotnet/csharp/)
* [Java](https://www.java.com/en/)

### The User Interface

In the game for 2018, there were obstacles on the field (shown as green, red, and yellow boxes) that 
needed to be traversed autonomously. We could only stand back and watch as the robot moved on its own, 
without any human input. All robot movement was guided by the paths generated in this program, as seen 
in the demonstration.

[![Product Name Screen Shot][demo-image]]()

The user creates points on the chart that the robot should follow, and the program uses those points to 
create two separate paths, one for each side of the robot.

### Velocity Calculation

After two splines are generated for the left and right sides of the robot, the application then creates 
a complete guide of velocity values that the robot should apply to its motors in order to accurately 
follow the path. This was an especially difficult task, since the motors have physical limitations beyond 
what might be mathematically possible.

[![Product Name Screen Shot][profile-marked-image]]()

Shown here are the corresponding velocity maps for the left (blue) and right (red) sides of the robot. 
This data was generated from the demonstrated path above! Turns are indicated by an increase in velocity 
for one side and a decrease in velocity for the other side.

<br>

Some issues that we had to work around were the minor physical differences between motors, the need to 
ramp-up and ramp-down velocities for optimal performance (including battery saving), and possible 
variations in actual field measurements from competition to competition.

### Competition Versatility

During competition, we were often paired with teammates that had autonomous plans that conflicted with 
ours. For example, both of our robot paths could end up colliding during the game, which could break the 
robots. In those cases, instead of having to re-code, debug, and test new plans (which was impossible 
given competition time constraints), we simply opened up the motion profile mapper, drew a new path 
according to their needs, and had everything ready to go within minutes. This proved to be critical to 
our success in many matches.

### Proper Programming

One major difference between this project and my other projects at the time was the necessity of 
programming professionally. Upon graduation, this application was going to be passed down to future 
programmers on the team to improve and maintain for years to come. Because of that, I needed to make sure 
that all code that I wrote was clean, easy to follow, and properly documented. This, of course, is much 
easier said than done. However, this was where I developed most of my good programming practices, which 
have influenced the structures of my future projects. This application is still used by team programmers 
today!

<!-- GETTING STARTED -->
## Try it Out

This GitHub repository contains an archived version of this mapper from when I graduated in 2018. Feel 
free to download it and try it out! You can watch [this video](https://www.youtube.com/watch?v=NRdkGwCWpzM) 
of our robot following a motion profile path live at the FRC State Championship in Michigan. Watch team 
3539 for the first 15 seconds!

<!-- USAGE EXAMPLES -->
## Usage

Click on the map to create points for the robot to follow. The "Apply" button creates splines along this 
point path and generates the motion profile. After creating a path, click the "Data" tab to view the 
distance and velocity calculations that will be sent to the robot.

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.

<!-- CONTACT -->
## Contact

Devon Doyle - [Portfolio](https://devondoyle.com/) - devonrd@umich.edu

Project Link: [https://github.com/DevonRD/Motion-Profile-Mapper-2018](https://github.com/DevonRD/Motion-Profile-Mapper-2018)

<!-- MARKDOWN LINKS & IMAGES -->
[forks-shield]: https://img.shields.io/github/forks/DevonRD/Motion-Profile-Mapper-2018
[forks-url]: https://github.com/DevonRD/Motion-Profile-Mapper-2018/network/members
[stars-shield]: https://img.shields.io/github/stars/DevonRD/Motion-Profile-Mapper-2018?style=for-the-badge
[stars-url]: https://github.com/DevonRD/Motion-Profile-Mapper-2018/stargazers
[issues-shield]: https://img.shields.io/github/issues/DevonRD/Motion-Profile-Mapper-2018
[issues-url]: https://github.com/DevonRD/Motion-Profile-Mapper-2018/issues
[license-shield]: https://img.shields.io/github/license/DevonRD/Motion-Profile-Mapper-2018
[license-url]: https://github.com/DevonRD/Motion-Profile-Mapper-2018/blob/master/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/devon-doyle/
[demo-image]: images/profile_demo.gif
[profile-marked-image]: images/profile_velocity.PNG
[profile-image]: images/profile_velocity_nomarks.png
[download-exe]: https://github.com/DevonRD/Motion-Profile-Mapper-2018
