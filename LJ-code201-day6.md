## day 6
The good: Still really enjoying JS. Had a tough hour + where, despite asking a TA for help, we just couldn't find a bug in a very, very simple for loop. Was trying to iterate through an array and simply sum the totals (to get the daily total for 'cookies sold' at a given location), but it kept coming back zero. The initial code was:

cookiesDayTotal: 0,
cookiesPerDayCalculation: function(){
  for (var i = 0; i < hours.length; i++) {
    this.cookiesPerHour[i] += this.cookiesDayTotal;
  }
},

and we were both code-blind to the two obvious mistakes here. First, the syntax for the += was swapped. I was reading it as "add this index value of the cookiesPerHour array to the total value of the cookiesDayTotal variable", e.g., *left-to-right* like "normal" math. Instead, these values needed to be switched, so that it reads "to the property cookiesDayTotal, add the index value of this iteration of the cookiesPerHour array". That was a bit of a brain buster, because it was, in a way, 'unlearning' a lifetime of addition. As well, to be sure it was working out as needed, a fellow student pointed out I should actually return the value outside the for loop. After an hour of not getting it to work with one assistant, two of my classmates picked out the problem in moments, gave me a great help, and the final bit of code in that object looked like:

cookiesDayTotal: 0,
cookiesPerDayCalculation: function(){
  for (var i = 0; i < hours.length; i++) {
    this.cookiesDayTotal += this.cookiesPerHour[i];
  }
  return this.cookiesDayTotal;
},

Which worked fine and plugged into my sales.html without issue.

I'm also noticing I'm understanding the flow of classes much better and finding resources I need more quickly, both from online places like stackoverflow, and within our LMS and class youtube sites, readings, etc. Hopefully this helps with not constantly feeling like I'm just a little bit behind!
