# ticker
a self-incrementing timer

## What is ticker?
ticker is a self-incrementing timer. ticker will start the timer the color red. It will remain red until the timer has been reached, at which time ticker will turn green. ticker will remain green until clicked/tapped. After being clicked/tapped ticker will turn red once more, increase and reset the countdown, and start counting down once more.

## Why is ticker?
I came up with ticker when I was trying to think of a way to facilitate quitting smoking. Some portion of addiction has to do with habitual routine - generalizing, "once every N hours I do X". I thought it might be interesting to experiment with a tool that allowed N to incrementally increase over time in order to help gradually "wean off" of the addiction. e.g., After the first time you wait 60 minutes, then 61, then 62, ...etc...

## How do I use it?
Grab `ticker.html`, adjust the parameters if needs be (more below), and open it in a browser. Tap-/click-and-hold to see the number of seconds remaining until the next time it will turn green. Tap/click once it turns green to increment and return to red.

## How do I change the parameters?
One of two ways:

* If you want to set the values for a currently-running ticker, simply change the query parameters `startInterval` (the initial countdown, in seconds) and/or `step` (the amount by which to increase the counter, in seconds). For example, if you want to start off at 30 minutes and increment by 3 seconds, try adding `?startInterval=1800&step=3` to the base URL.
* If you want to change the default values for a newly-created `ticker`, edit the values of `DEFAULT_START_INTERVAL_IN_SECONDS` and `DEFAULT_STEP_IN_SECONDS` in `ticker.html`. (Note: The default initial values are 60 minutes and 1 minute, respectively.)

## Q & A
* **Is it well-tested?** Not really, no.
* **Does it work on mobile/Is it Responsive?** Well...at present it works in both my desktop browser and my mobile browser. (See: question on testing above.)
* **Can I share a ticker between devices?** A `ticker` updates the URL on each incremental tap. This is the only mechanism that it uses to maintain state, so at present the only way to share between devices would be to open the full URL of a given `ticker` on another device.
* **Why not maintain state between devices?** Potential future work. I knocked this out in a couple of hours as an experiment, and tried really *really* hard to make it as minimal (and still useful) as I possibly could.
