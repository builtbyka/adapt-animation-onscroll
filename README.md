#adapt-component-animate


A basic component animation extension - full credit to Kineo [Kineo's work](https://github.com/cgkineo/adapt-component-animate). This extends their work to add animation when scrolling. Works best when trickle autoscroll is false. 


Uses [velocityjs](http://julian.com/research/velocity/#fade)

```
"_componentAnimate": {
  "_startHeight": 60,   //percentage from top of the window at which to start the animation
  "_start": {       // velocity command for the componentView:preRender
      "position":"relative",
      "left": "-100%"
    },
  "_command": {   // velocity command for the componentView:postRender
      "left": 0
    },
  "_options": {   // velocity options for the componentView:postRender
    "duration": 1500
  }
},

"_componentAnimate": {
  "_startHeight": 60,   //percentage from top of the window at which to start the animation
  "_start": {       // velocity command for the componentView:preRender
      "position":"relative",
      "left": "-100%"
    },
  "_command": "fadeIn", //velocity named commands can also be used
  "_options": {   // velocity options for the componentView:postRender
    "duration": 1500
  }
},

To work with scroll
add 'on scroll true and include a finish height so the animation knows when to complete by'

"_componentAnimate": {
  		"_onScroll": true,
			"_startHeight": 60,
			"_finishHeight": 25,
			"_start": {
				"position":"relative",
				"right": "-100%",
				"opacity": 0
				},
			"_command": {
				"right": 0,
				"opacity": 1
				},
			"_options": {
				"duration": 1
			}
		}
```



