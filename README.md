# Baymax_Startup
<br>
Everyone who has seen the movie Big Hero 6 will be familiar with the name Baymax. In the movie Baymax was Personal Healthcare Companion Robot created by Tadashi Hamada to scan everyone and work as a robotic nurse. When I first saw the movie I loved the way Baymax greeted the Hero Hamada when he first turns it on. That made me decide to make software for PC that greets us whenever we turn on our computer. You can make your own Baymax using the following commands, before we go on with the coding you need to have drag and drop one tool called Timer to our main screen like Pic 1.1<br>

<img class=" wp-image-1714 aligncenter" src="http://section9.space/wp-content/uploads/2016/10/1-157x300.png" alt="1" width="195" height="373" />
<p style="text-align: center;">Pic 1.1</p><br>

When you click on Timer you can see one Properties Box on Bottom Right corner. Next you need to change the default Properties of Timer as shown below: <br>
<img class=" wp-image-1719 aligncenter" src="http://section9.space/wp-content/uploads/2016/10/5-300x125.png" alt="5" width="425" height="177" />                  
<br>
Now we can move to the Coding part but first we need add some Reference to our Project. For that go to “Project” and Click on “Add Reference” and search for “System.Speech” and you need to select these Reference.<br>
Next Below using System.Windows.Forms; you need to add these extra namespace like the following<br>

<blockquote>
<br>
using System.Speech.Recognition;<br>
using System.Speech.Synthesis;<br>
using System.IO;<br>
using System.Globalization;<br>
using System.Threading;<br>
using System.Xml.Linq;<br>
using System.Xml;<br>
using System.Web;<br>
<br>
</blockquote>

Next Below 

<blockquote>
“public partial class Form1 : Form<br>
&nbsp &nbsp &nbsp &nbsp {”<br>
</blockquote>

Copy the following codes: 

<blockquote>
<br>
“Random rnd = new Random();<br>
SpeechSynthesizer Baymax = new SpeechSynthesizer();<br>
SpeechRecognitionEngine reg = new SpeechRecognitionEngine();<br>
private DateTime timenow;<br>
String userName = Environment.UserName;”<br>
<br>
</blockquote>

Next Below 
<blockquote>

“public Form1()<br>
{<br>
 &nbsp &nbsp &nbsp &nbsp &nbsp InitializeComponent();”<br>
     
</blockquote>

Copy the following codes:

<blockquote>
“timenow = DateTime.Now;<br>
if (timenow.Hour >= 1 && timenow.Hour < 5)<br>
{ Baymax.Speak("Goodmorning, Its currently " + timenow.GetDateTimeFormats('t')[0] + ". I think you should sleep now, it's too early. Wish you have a good sleep" + userName); }<br>
if (timenow.Hour >= 5 && timenow.Hour < 9)<br>
{ Baymax.Speak("Goodmorning, Its currently " + timenow.GetDateTimeFormats('t')[0] + ". I think you have slept peacefully. have a nice day" +userName ); }<br>
if (timenow.Hour >= 9 && timenow.Hour < 12)<br>
{ Baymax.Speak("Goodmorning, Its currently " + timenow.GetDateTimeFormats('t')[0] + ". how's the day going " + userName); }<br>
if (timenow.Hour >= 12 && timenow.Hour < 18)<br>
{ Baymax.Speak("Good afternoon, Its currently " + timenow.GetDateTimeFormats('t')[0] + ". It is good to see you again " + userName); }<br>
if (timenow.Hour >= 18 && timenow.Hour < 24)<br>
{ Baymax.Speak("Good evening, Its currently " + timenow.GetDateTimeFormats('t')[0] + ". It is good to see you back " + userName); }<br>”

</blockquote>

Now we are going to use the Timer we dragged from the Toolbox for that we are going to create a new string to check the date and time from our PC, as shown below: 

<blockquote>
“public string time()<br>
{<br>
&nbsp &nbsp &nbsp &nbsp &nbsp DateTime timenow = DateTime.Now;<br>
&nbsp &nbsp &nbsp &nbsp &nbsp string o = timenow.GetDateTimeFormats('t')[0];<br>
&nbsp &nbsp &nbsp &nbsp &nbsp return o;<br>
}”<br>
</blockquote>
<br>
Now we are going to our last step, that is to give coding to our “ShutdownTimer” for that double click the Timer we made. When you click on Timer it leads you to the coding page as default the coding will be like this:<br>

<blockquote>
“private void ShutdownTimer_Tick(object sender, EventArgs e)<br>
{<br>
&nbsp &nbsp &nbsp &nbsp &nbsp #Paste your code here<br>
}<br>”
</blockquote>

And paste the following code:<br>

<blockquote>
<br>
“ShutdownTimer.Enabled = true;<br>
Close();”<br>
</blockquote>

Now you are ready to use your Baymax Startup software, you can test your software by pressing “F5”. Before you press “F5” make sure that you have closed every curly braces { }.<br>
If you have any problem with your coding just leave a message 😉 <br>
You can download Baymax Code from the link below :👇<br> https://github.com/stark25795/Baymax_Startup<br>
You can also download "How to make Baymax" PDF from the link below :👇<br> https://drive.google.com/file/d/0BzQ8yfuAE9O1dkVLdFdhLS1JZlk/view?usp=sharing. <br>
✌️👍
