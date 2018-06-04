---
layout: post
published: true
mathjax: true
featured: true
comments: false
title: Anonymous Functions
categories:
  - software
tags: '"Anonymous Functions" "Lamba Expressions" "Android" "Java" "Javascript"'
---
## What's in a name?

Lately I've been working my way through the free version of Udacity's [Android Basics](https://www.udacity.com/course/android-basics-nanodegree-by-google--nd803) course. It's a great and extremely newbie friendly path to learning android dev, and I've had a lot of fun with it, although if you have coding experience you may find yourself skipping a lot of sections. In the past couple weeks I've encountered something I haven't really used before: ****Anonymous functions**** They are heavily used when writing/overriding many builtin Android methods, including OnClickListeners, which are used to respond to when a user taps on an element of your app (something you are going to do a lot). Here's an example from my code:

		//defines and grabs a view from the xml layout
		TextView numbersView = (TextView) findViewById(R.id.numbers);
		
        //calls the setOnClickListener method on that view
        //passing in a NEW FUNCTION AS A PARAMETER?
        numbersView.setOnClickListener(new View.OnClickListener(){
			
            @Override
            public void onClick(View view){
                Intent intent = new Intent(MainActivity.this, NumbersActivity.class);
                startActivity(intent);
            }
        }
        );
        
This left me blinking the first time I encountered it. The program said that this was more concise that defining a function elsewhere to only use it once, and yes, sure, but it also seemed a lot less readable. Ultimately I just accepted it as a convention and have used it a few dozen times since. But it keeps eating at me. Exactly what are these for? It can't just be concision. 

Sounds like its time to plumb the depths of Anonymous Functions.

