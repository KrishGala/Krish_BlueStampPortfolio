# Hexapod Robot

<!--Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!-->

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Krish G | Leigh High School | Electrical Engineering | Rising Junior

<img src="KrishG.png" alt="Alt Text" width="50%" height="50%">

<!--  # Final Milestone -->

<!-- **Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.** -->

<!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe> -->

<!--For your final milestone, explain the outcome of your project. Key details to include are:

<!-- # Second Milestone -->

<!-- **Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.** -->

<!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe> -->

<!-- For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone -->

# First Milestone

<!-- **Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.** -->

<iframe width="560" height="315" src="https://www.youtube.com/embed/Xi515reuXZE?si=zpE9ugs6TT8V1UEm" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

This is my first milestone! So far I've set up the Arduino program and the Processing program for the robot. Processing is the built in controller for the robot while Arduino is used for writing my custom code to control each individual servo. The main part of this milestone is to make sure each of the servos are working correctly, which they do. I first used the given controller for the Hexapod to move the servos. I then moved onto the Arduino program where I tested individual servos. I learned that the servos aren't that strong and they started overheating and smoking after running some code that changes the position of the servos from 0 to 180 and back. This led to some of the servos just shutting down for a bit and then restarting because of the load. So, I changed the parameters of the servo to 20 and 40 for easier use on the servo. But using the actual given controller everything looks to be working correctly and in the next step for building. Looks like I didn't actually need to use the extra servo given in the box. In this milestone I've learned alot about how Arduino and the actual board interact. When I tried to run the Arduino code while the actual controller was running it didn't work. So next time I need to keep that in mind anytime I want to run some code. I also learned how to read the control board where each servo's connection is a specific port that I can call for in Arduino. I'm excited for the next step, building and calibrating because I'll finally have the robot made!

 <!-- # Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. -->

```
c++
#include <FNHR.h>
#include <Servo.h>

FNHR robot;

Servo myservo;

int pos = 20;

void setup() {
  robot.Start(true);
  myservo.attach(37); 
}

void loop() {
  for (pos = 20; pos <= 40; pos += 1) { 
    // in steps of 1 degree
    myservo.write(pos);              
    delay(15);                       
  }
  for (pos = 40; pos >= 20; pos -= 1) { 
    myservo.write(pos);              
    delay(15);                       
  }
  robot.Update();
}
```

<!-- c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
-->


<!-- # Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here. -->


# Weevil Starter Project

<iframe width="560" height="315" src="https://www.youtube.com/embed/8W17v3A6jmY?si=norvQOObzwAQvrP6" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


My starter project was the WeevilEye. The purpose of the project was the two LEDs that the weevils 'eyes' would light up if the photo sensor on the backend detected low enough light to send a signal to light the eyes up. It was composed of the mainboard, 2 220 resistors, 1 47k resistor, a battery casing, a disc battery, a photo sensor, and a transistor. This was the first project I soldered on so I was nervous I'd do it wrong. This did somewhat come true because the first time I built the project it didn't work. Not because of my bad solders but I swapped the places of two of my resistors stupidly. The position of the battery holder was extremely intrusive because it was soldered on the opposite of all of the other components that it would be extremely difficult to desolder all of it. So, my instructor and I just decided to restart on a new one and this time it worked. Overall I think this was a good beginner project and I feel more prepared to start my actual one.

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| SparkFun WeevilEye - Beginner Soldering Kit | All parts to create WeevilEye project | $11.25 | <a href="https://www.sparkfun.com/sparkfun-weevileye-beginner-soldering-kit.html"> Link </a> |


# Schematics 
![Weevil Eye Schematic Image](Weevil_Eye-v16-1.png)
[**SOURCE**](https://cdn.sparkfun.com/datasheets/Kits/Weevil_Eye-v16.pdf)
