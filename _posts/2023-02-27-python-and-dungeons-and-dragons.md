---
title: Python & Dungeons and Dragons
date: 2023-02-27 22:47
comments: true
categories: [Engineering Projects, Programming]
---
<!-- wp:image {"align":"left","id":78,"width":342,"height":191,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image alignleft size-large is-resized"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2023/02/dndsymbol.png?w=1024" alt="" class="wp-image-78" width="342" height="191" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>In my high school senior year, I was lucky enough to be taught a bit of Python by my Engineering teacher Mr. Groller as part of the Project Lead The Way program. We went through a little tutorial, and it took us through all the basics, which I’m really thankful for. I then learned more coding skills in depth when I took a C++ class where I made a full card game with ASCII art in the command window and everything. I was SUPER proud of that project and probably worked on it more than I should have lol. That takes us to today, where the closest thing I am doing to coding is working with MATLAB to analyze data and work with matrices and Ordinary Differential Equations. Coding and knowing how a programming language works is still super helpful, as there is still while and for loops in MATLAB, as well as strings and other basic genres of coding stuff. I do miss creating a program that purely works with user input and a command line though, as I just found it so satisfying when something would work perfectly and you could check it by just playing around with the program. Everything was external! Any flaws that existed were found pretty quickly! Anyway, all this is to say I brushed off the cobwebs and attempted to write a simple program in Python again, modeling the Death Saving throw in Dungeons and Dragons (A game that I just tried out with SJSU’s DND club and had a bunch of fun with!). I’m planning on transforming the default Adobe Portfolio website I am using to a cooler, self made and unique website coded all by myself. Here’s to keeping old skills fresh and continuing to build upon them! :D</p>
<!-- /wp:paragraph -->

<!-- wp:code {"fontSize":"small"} -->
<pre class="wp-block-code has-small-font-size"><code>import random

	# I figured that python would be the best program to do this in, but perhaps javascript would be better. To summarize
	# what actually comprises websites - html puts text and objects in classes and elements and then CSS allows us to
	# change the properties of those classes and make them dynamic and cool. For a simple computation like the one below,
	# I would need a programming language. Python is server side, meaning it happens on a server and then gets sent to a
	# phone screen, while javascript is client side. This stuff is super simple, so it should happen client side, in java
	print("Careful Adventurer! Your health points have been diminished to zero after taking a lethal friendly fire h"
		  "it! \nYour mortality is now no longer in your control, but rather in Fate's hands. \n"
		  )

	Success = 0
	Failure = 0
	terminate = 0
	while terminate == 0:
		input("Roll a Death Saving throw to see if you will survive.")
		throw = random.randrange(0, 21)
		print(throw)
		# the addition of success and fail throws
		if throw == 20:
			print("You have rolled a natural 20! Your soul fights vigorously against dissipating and you strive to "
				  "continue living! Two Success throws have been added to your total!")
			Success = Success + 2
		elif throw &gt;= 10:
			print("You have rolled above a 10, and thus get a success marker. Your soul stirs and you are closer to"
				  " regaining life ")
			Success = Success + 1
		elif throw == 1:
			print("you have rolled a gnarly one. You feel the grimy hands of your slain enemies reach around your body"
				  "and forcefully drag you down, farther into the darkness")
			Failure = Failure + 2
		else:
			print("You have rolled below a 10, and you sink farther into the next plane")
			Failure = Failure + 1
		# terminating if any of the end conditions are met
		if Failure &gt;= 3:
			print("I'm sorry dear adventurer, but you feel your life force quietly lift from your body as you enter the "
				  "next plane. \nGood luck in your next life ...\n"
				  "Thanks for playing and sorry about dying :o")
			terminate = 1
		elif Success == 2 and Failure == 2:
			print("Which way will the strings of fate bend?! For you are on the edge. Whichever way will this go?\n")
			print("You now have", Failure, "Failure Throws and", Success, "Success Throws\n")
		elif Failure == 2:
			print("You are near death! Careful! One more failure throw and you WILL DIE!\n")
		elif Success &gt;= 3:
			print("You are still battered and bruised, but your soul has successfully held on to your body!\n"
				  "You remain at zero health points, and are stable! :)\n"
				  "Thanks for playing and congratulations on living!")
			terminate = 1
		else:
			print("You now have", Failure, "Failure Throws and", Success, "Success Throws\n")</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Now, I obviously did not want to show off my code through screenshots, but rather through a small demo that you could see on the website, but I wrote this in python. As you can see from the comment at the top of the image, I thought that any old language would work and I would be able to simply plug it into anything and it would just … work. Wrong! I’m sure any software engineers reading are rolling their eyes. Apparently JavaScript is the best language to work client side, so I will attempt to write this again in that language. Additionally, I am learning HTML and CSS to create my own, unique website eventually, that will be able to have snippets of fun code or projects I want to show off. Thanks for reading!</p>
<!-- /wp:paragraph -->
