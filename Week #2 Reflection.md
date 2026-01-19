# Week #2 Reflection:

I spent a lot of time in the p5js editor this week. First off, I think I understand the positioning mechanics now! Well, somewhat... When working in 2D, (0, 0) corresponds to the top left corner. So an increase in X moves things to the right, and an increase in Y moves them down. I must say, I'm curious as to why this is the case? It doesn't seem very intuitive, at least to me. But I am glad I understand it now, as it was really confusing me last week. I also learned in class that when working in WEBGL, which is 3D graphics, (0, 0) is NOT the top left corner, but instead the dead center of the canvas.

I have yet to figure out what that means for non-centered things, though, as what I was designing didn't require me to get that far yet. I am really proud of what I've gotten done with torus', though. I designed three interloping torus' (I'm not sure if interloping is the right term, so imagine the way that smaller and smaller measuring cups stack into each other) that spin independently of each other. For a split second, they have all the same orientations, then they continue to pivot off from each other. I think the effect is quite cool.
[View the rotating torus' here](https://editor.p5js.org/tanwat27/full/4-f8q_YiG)
And here's the code:
let angle;

function setup() {
  createCanvas(400, 400, WEBGL);
  angle = 0;
}

function draw() {
  background(220);
  
  rotateX (angle);
    rotateY (angle);
  
  angle = angle + .03;
  fill ("blue");
  stroke ("red");
  torus(60,15);
  
  rotateX (angle);
  
  fill ("pink");
  stroke ("purple");
  rotate(HALF_PI);
  torus(25,15);
  
  rotateX (angle);
  
  fill ("green");
  stroke ("yellow");
  rotate (HALF_PI);
  torus (95,15);
  
}

END OF CODE :)

I also made my second github upload (is that what I should be calling it?) ! I made a png out of a burger I saw someone post on social media, saved it to my computer, and added it to my github respository so that it was accessible within p5js. I am curious if there is other ways to access images, but this is definetly solid! I used the upload link with the loadImage command in p5 to make infinite burgers follow the cursor in the canvas. It's simple, but I think being able to load images is going to be super helpful.
[View the Infinite Burger Here](https://editor.p5js.org/tanwat27/full/n7-ZVwfld)

Videos:

After watching the "while & for" Loops video, I gained an insight into my idea for the clock project. When I made my rotating torus code, I was thinking about how I could turn it into a clock. I thought about how the outermost ring could represent seconds, the middle minutes, and the innermost hours. Then the outermost would rotate on the y-axis 180 degrees every second, the middle 180 degrees on the x-axis every minute, and the innermost 180 degrees on the y-axis every hour (in the opposite direction of the seconds ring). But then I wanted to figure out some way to differentiate between odd and even (like when the clock turns from 5 to 6), and the only thing I could come up with would be the rings being different colors split down the middle (like a bagel). But I have NO idea how I would ever do that. But now I'm thinking that I could use an if statement, like if the hour is odd, this ring is this color, if it's even, the ring is this color. Now I just need to get to coding it, and I might have a working clock by the end of the week!
