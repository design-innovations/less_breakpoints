#LESS breakpoints
================

An expanded variety of breakpoints created for more accurate styling across a wide range of media sizes.

These were originally created in SASS using IF statements and I finally found a way to port them into LESS by using the method developed at [http://blog.scur.pl/2012/06/variable-media-queries-less-css/](http://).

The breakpoints were developed after doing a lot of research and testing while building [www.expertgriller.com](http://) which needed much more accuracy with breakpoints than what comes standard with Bootstrap 3.x. (disclaimer: parts of the site may not break correctly now since the client has taken over the updates)

All "up to" options include all sizes up to that size but does not include that media. For example, if you choose @up-to-desktop then it will affect all sizes until it reaches (and includes) 1 pixel smaller than desktop. The individual names (ie. tablet portrait) only pertain to that one range of sizes. The options with "and bigger" range from the size chosen up through large desktop sizes.

## Options include:

###Phone

- Phone
- Super small phone
- Small phone
- Phone only

### Small tablets

- Tablet-portrait
- Up to tablet portrait
- Tablet portrait and bigger

###Tablet landscape

- Tablet landscape
- Up to tablet landscape
- Tablet landscape and bigger

###Desktop

- Up to desktop
- Desktop
- Desktop and bigger

###Large desktop

- Large desktop
- Up to large desktop

### Pixel density

- Non-retina
- Retina (Targetting only Apple products with retina.)
- High Density (for all high density media including retina.)

##Usage

First of all, you must be using LESS version 1.3.0 or greater. Usage couldn't be easier. Simply wrap your code in @media followed by the breakpoing you would like to use.

		#sidebar {
			width: 30%;
			@media @up-to-tablet-portrait {
				width: 100%;
			}
		}

For high-density usage you can do the following:

		#logo {
			background-image: url('../images/logo.png');
			@media @highdensity {
				background-image: url('../images/logo@2x.png');
			}
		}

I hope you enjoy this mixin. It has saved me many hours of work and it makes code much easier to read. If you have any ideas on how to improve it please let me know.

##Try the new breakpoint debugging box!

I have added a handy breakpoint debugging box for HTML and PHP! Just copy the following code below the body tag and add the LESS or CSS into your page.

	<div id="debug-box"></div>
	
It will now tell you which breakpoint you are currently viewing. Resize the browser and it will dynamically change according to the screen size.

I have also included a handy piece of PHP you can add to your page so only people at the IP listed sees the debugging area so it can be used on a live site to debug.