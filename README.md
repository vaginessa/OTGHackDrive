# OTGHackDrive
OTG Hack Drive is a HID , Works as a Keyboard &amp; Mouse on the go. Usually used as a Penetration OR Hacking Device.

# Ref
<a href="http://otghackdrive.dishantrathi.tk">OTG Hack Drive</a>

<p><b>Note :</b><b>Open Source And For Educational Purpose Only.</b><br>Also Rights To Thier Respective Owners.<br>For New Payloads Or Suggestions mail me @ <a href="mailto:dishantrathi@engineer.com">dishantrathi@engineer.com</a></p>

		<br>

	<p><b>References :</b></p>

<p>1 : <a href="http://usbrubberducky.com/#!index.md">USB Rubber Ducky[Official Page]</a></p>

<p>2 : <a href="https://github.com/hak5darren/USB-Rubber-Ducky/wiki">USB Rubber Ducky[Github Page]</a></p>

<p>3 : <a href="https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payloads">USB Rubber Ducky[PayLoads]</a></p>

<p>4 : <a href="https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payloads">USBDriveBy[<a href="https://Samy.pl/"><b>Samy</a></b>]</a></p>

<p>5 : <a href="https://ducktoolkit.com/">DuckyScript Generator</a></p>

<p>5 : <a href="../PCDoA/index.html">DuckyScript To Arduino Script Convertor - PCDoA v2.0</a></p>

<p>For More <a href="http://www.dishantrathi.tk/">Dishant Rathi</a></p>

		

		<hr>

		<hr>

		

		<h2 id="toc" class="alt"><center>Contents</center></h2>

		<ol class="alpha">

			<li><a href="#introarduino">Introduction To Arduino</a></li>

            <li><a href="#introdevice">Introduction To Chipset MT32u4</a></li>

            <li><a href="#introotghackdrive">Introduction To OnTheGo Hack Drive</a></li>
				
			<li><a href="#Buy">Where To Get ?</a></li>
			
			<li><a href="#environments">Working Environments</a></li>
			
			<li><a href="#Usage">Where $ How To Use ?</a></li>
			
			<li><a href="#prevention">Prevention</a></li>
			
			<li><a href="#others">Guides</a></li>

		</ol>

			

		

		

<ol class="content alpha" style="padding:0;">

<hr>

<hr>

		<center><h2 id="introarduino"><strong><img src="https://www.arduino.cc/favicon.ico">Introduction To Arduino</strong> <a href="#toc">Top</a></h2></center>

			<p>Arduino is an open-source project that created micro-controller based kits for building digital devices and interactive objects that can sense and control physical devices.</p>
			<p>Arduino boards are available commercially in preassembled form, or as do-it-yourself kits. Some of them are really small and have a built-in USB connector which makes sketch upload easier.Some of you may be thinking, how can Arduino be used to hack something?</p><p> Well, since Arduino supports keyboard emulation we can build sketch which contains keyboard instruction to type command and executes it just like the popular USB Rubber Ducky (http://usbrubberducky.com/).</p>



<hr>

<hr>

		<center><h2 id="introdevice"><strong>Introduction To Chipset MT32u4</strong> <a href="#toc">Top</a></h2></center>
				
			<p>This Chipset can work as a HID - Human Interface Device. Which means ... you can do anything that you want to do in seconds.</p>
			<p>You can execute almost anything using keyboard emulation and autorun, even with antivirus installed and updated. From just typing simple commands to coding an executable from scratch.All of it will be done automatically, starting right after Arduino is installed on the target computer. This typically takes about 3 – 5 seconds.</p>
			<p>This device isn't recognized as a USB Device but a Keyboard Or Mouse, depending upon the programming done by you.</p>			
			<p>Get More Details Form Here <a href="https://github.com/hokim72/ATmega32U4">Arduino MT32u4</a></p>
			<P>Devices can be used are : </p>
			<p><center><a href="https://www.arduino.cc/en/Main/ArduinoBoardLeonardo"><img Src="https://www.arduino.cc/en/uploads/Main/Leonardo.jpg">Arduino Leonardo</a><br><p>_______________________________________________________________________________________________</p><a href="https://www.arduino.cc/en/Main/ArduinoBoardMicro"><img Src="https://www.arduino.cc/en/uploads/Main/A000053_iso_both1.jpg">Arduino Pro Micro/Leonardo Micro</a></center><p>


<hr>

<hr>

		<center><h2 id="Buy"><strong>Where To Get ?</strong> <a href="#toc">Top</a></h2></center>

			<p>Well, You can get the links to buy this !  </p>
			<p>> <a href="https://www.amazon.com/s/ref=sr_gnr_fkmr0?rh=i%3Acomputers%2Ck%3Aarduino+micro+pro&keywords=arduino+micro+pro&ie=UTF8&qid=1481090741">Click Here To Buy [Valid WorldWide]</a>
			<p>> <a href="http://www.amazon.in/OSOYOO-ATmega32U4-arduino-Leonardo-ATmega328/dp/B012FOV17O?tag=googinhydr18418-21&tag=googinkenshoo-21&ascsubtag=cbf3bdf6-ba1b-49ee-9cf6-b1f80c0a4f8a">Click Here To Buy [Valid India]</a>	
			<p>> <a href="https://www.arduino.cc/en/Main/Software">Arduino Software</a></p>
<hr>

<hr>

		<center><h2 id="#environments"><strong>Working Environments</strong> <a href="#toc">Top</a></h2></center>

			<p>Well, You this can work under Any Version of Windows, Flavors of Linux, Under Mac OS, Android [Any Version]</p>
			
<hr>

<hr>
		<center><h2 id="Usage"><strong>Where $ How To Use ?</strong> <a href="#toc">Top</a></h2></center>

			<p><b>Tools you’ll need:</b> </p><p>Arduino Pro Micro ATMega32U4 5V/16MHz (or any Arduino with ATMega32U4 chip) <br> USB Micro Adapter Cable (you don’t need this one if the Arduino you use comes with builtin USB A male connector).</p>
			<p>Video :Coming Soon</p>
<p>	<strong> Step by step Instructions : </strong></p><p>How does it work?</p><p> A sketch file is just a regular script file with .ino extension. It contains 2 main procedures: setup() and loop(). Below is the basic structure for doing keyboard emulation:</p>
<pre>
#include <HID.h>
#include <Keyboard.h>
void setup() {
// put your setup code here, to run once:
}
void loop() {
// put your main code here, to run repeatedly:
}
setup() procedure will only be executed once when Arduino is powered on and initialized, while the loop() procedure will be executed repeatedly, over and over again until Arduino is powered off.
When giving instructions to type something, always add delay() command to let the computer process the instructions. You also need to add delay() command when pressing a key combination. For example, here are the commands to press the Windows Key.
Keyboard.press(KEY_LEFT_GUI);
delay(1000);  // the processor need time to register key press
Keyboard.press(‘x’);
Keyboard.releaseAll();
delay(500);  // approximate time needed to process our intruction
</pre>			
	
<hr>

<hr>

		<center><h2 id="#prevention"><strong>Prevention</strong> <a href="#toc">Top</a></h2></center>

			<p>Well, To prevent this kind of attack, you can hold down the Alt key while plugging in a suspicious device.</p>
			
<hr>

<hr>

		<center><h2 id="others"><strong>What else can be done with OTG Hack Drive ?</strong> <a href="#toc">Top</a></h2></center>
				
			<p><b>Reconnaissance:</b>
<pre>
1. Computer Information.
2. Installed Updates.
3. User Document List.
4. Port Scan.
5. Extract SAM File
</pre>

<b>Exploitation:</b>

<pre>
1. Find and Upload File (FTP).
2. Disable Firewall.
3. Open Firewall Port.
4. Start Wi-Fi Access Point.
5. Share C:\ Drive.
6. Enable RDP. 
7. Create a Reverse Shell
</pre>

<b>Reporting:</b>

<pre>
1. FTP Report to External Host.
2. Email Report to your Account.
</pre>
</p>

<hr>
<hr>
<p>Once again, thank you so much for having view on this Paper work. If you have any questions that are beyond the scope of this help file, please feel free to email via my user page contact form. No guarantees, but I'll do my best to assist.</p> 

		

				<p><a href="#toc">Go To Contents</a></p>

				<br><hr>

		<center><p>For Index of /Payloads Visit : <a href="../Payloads/">PayLoads</a></p></center>

		<br><hr>
