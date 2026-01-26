# Week #3 Reflection:

## In p5js:

This week I started trying to recreate Wall Drawing 56 (from Mass MoCA) in p5js. I got about 70% of it done, but I am really stumped at a certain part. Let me illustrate:

[This](https://massmoca.org/event/walldrawing56/) is the image I am trying to recreate (simply, without the wobble effect on the lines)

And [this](https://raw.githubusercontent.com/tanwat27/tw-CT20/refs/heads/main/wall%20drawing%2056%20attempt.png) is an image of what I have so far. Here is the [link](https://editor.p5js.org/tanwat27/sketches/KqlaRqAbN) to my editor.

I completed a lot of it by following along in class.

My issue is that I don't quite understand how to add the diagonal lines on the bottom half. There are two sets of diagonal lines:

- Ones that fall right to left across the entire bottom half of the image (all parallel to each other)
- Ones that fall left to right across the bottom left quadrant (parallel to eachother, but perpendicular to the other lines)

I am going to look further into the mechanics of diagonal lines and see if I can figure it out. The most complicated part will probably be using a while loop to do so, and getting the proportions right.

## Readings:

I took a look at the Iteration page from *Coding as Creative Medium*. From my understanding, what I was looking at was a bunch of exercises with outcomes that you would need to use "for" or "while" loops to achieve. I took a stab at the first one, "Seven Circles".

It said that you need to use a margin because the circles can't be on the edge. If I'm using a while loop, setting a "margin" is as simple as setting the starting position of the original circle away from the edge (greater than 0), and using a spacing and circle diameter that would ensure the seventh circle is that same distance from the edge.

I decided 40 pixels should be a good margin. So I multiplied 40*9 (seven segments, plus one on each side) and got 360. 360 now becomes my canvas width. Height doesnt matter as much, so I just used 360 again. Then I decided 30px should be a good size for the circles. But since I'm starting at 40px, that's where the center of the first circle is. So there's really a 25px margin on each side. So I subtracted 50 from 360, and I'm left with 310. Divide 310 by 7 and you get 44. So I used 44px as my spacing.

Then I used the "let" feature:

let x = 0
let m = 40 (this is the margin)
let y = height / 2 (this is the y-coord of the circles)
let d = 30 (diameter of circles)

Then I used a while loop in the draw area:

while (x < 7) {
	circle (m, y, d);
	m = m + 44;
	x++;
	}
}

x++ adds one circle until we reach seven circles

At first I used while (x <= 7), but then I ended up with an eighth circle. I realized this was because it was counting 0, 1, 2, 3, 4, 5, 6, 7, which is eight instances. So then I got rid of the = and got seven circles.

Something in my math was kind of funky because it looks like there's a wider margin on the right side than the left, but this is a good start. I was able to do this by loosely following [this Coding Train video.](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/4-loops/1-while-for)

[Here's the sketch link](https://editor.p5js.org/tanwat27/sketches/cEJcDY-TN)




