Tabs vs. spaces
===============

I know, you’ve seen this headline a thousand times - and you’ve even seen sitcoms with the topic as part of the storyline. It’s 'tabs vs. spaces', and it’s something that every developer has a take on, and where we just - by sheer stubbornness - refuse to meet on a standard.

So let me propose one!

It basically boils down to this.

- Tabs are for indentation.
- Spaces are for alignment.

See? We meet!

# Indentation

Now I know the first line of that standard makes about half of you explode, and let me assume, that about half of the spaces-people just stopped reading when they saw that line - so at this point we have the tabs-people left (and the bicurious spaces-people) - but please let me explain why tabs are the most practical thing for indentation.

We’re all different - you and I. I might like two-character tab-stops, and you might like four. That’s all fine and dandy - until the day when we find ourselves working on the same code. Now you will freak about all the two-character tab-stops, because the indentation is not what you'd expected (four characters).

This is where tabs steps in - because the practical thing about tabs is, that they come with options. All text editors - since the dawn on ages - has come with the option of setting the width of tab-stops. Now if I’ve just setup my editor two display two-characters for every tab, there would be no problem - because you just defined your editor to use four. Now you don’t have to be double frustrated, when you hit the 100-line pyramid of doom I wrote on line 200 - now you only have to hate me for that. With tabs comes options. All developers hate hardcoded stuff - and using spaces is pretty much you hardcoding your preferred of tab-stop width.

So let’s all agree on **tabs** for **indentation**.

# Spaces

Now why introduce spaces? I thought we just settled on tabs for indentation. Well, I did - but we also just realized that indentation and alignment is not the same thing.

Let’s take an example.

This is indentation - where we use tabs.

	if (mycondition == true) {
		// Do stuff
	}

This is alignment.

	var module1 = require('module1'),
	    module2 = require('module2')

You see the difference? In the above example the two lines are suppose to align - for clarity and ease of reading.

Another example is.

	if (mycondition == true) {
		/*  Here I have a multiline comment
		    which I would like to be aligned,
		    so when I read it, the lines
		    are perfectly aligned.  */
	}

What if the above example was done with tabs, and I had my text editor setup for two-character tab-stops. It would look like the below (which is obviously not the intent).

	if (mycondition == true) {
	  /*  Here I have a multiline comment
	    which I would like to be aligned,
	    so when I read it, the lines
	    are perfectly aligned.  */
	 }

So you see? Using only tabs fucks this up, and - beside the fact that you actually took care to align the lines for me - I cannot read it as easily.

The above looks like this with hidden characters.

	if (mycondition == true) {
	>	/*  Here I have a multiline comment
	>	····which I would like to be aligned,
	>	····so when I read it, the lines
	>	····are perfectly aligned.  */
	}

What?!?!? Tabs and spaces on the same line - are you f&%#€!? kidding me? No, I'm not. This is so practical for every reason. Now me - the two-character-tab-stop-guy comes along, and it looks like this.

	if (mycondition == true) {
	  /*  Here I have a multiline comment
	      which I would like to be aligned,
	      so when I read it, the lines
	      are perfectly aligned.  */
	}

See? Two-character indentation - alignment still works.

So let's also agree on **spaces** for **alignment**.

# The Standard

To recap...

- Tabs are for indentation.
- Spaces are for alignment.

Thanks.

---

Please submit an issue if you'd like to kill me - or have similar or other issues with this document.
