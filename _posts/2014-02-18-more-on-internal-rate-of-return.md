---
title: More on Internal Rate of Return
author: Jared
layout: post
permalink: /investing/more-on-internal-rate-of-return/
tags:
  - Investing
---
After my brief explanation of Internal Rate of Return (IRR), I thought I would go in to a little more detail to give a better explanation. While IRR is not necessarily the best predictive tool for an investment, it is useful and the methodology and application is foundational for other analytical tools &#8211; so it’s important to have a grasp of this. But to start, let’s recap the time value of money.

### Time Value of Money

We have discussed previously that the value of a dollar changes over time &#8211; notably each dollar has less purchasing power the further into the future you go. It can be said then that if you want to discover the future value of a given present dollar amount, you *discount* it. This discounting converts the future value in to today’s equivalent to allow you to compare like-for-like amounts. The rate at which the vale of money depreciates over time is referred to as the *discount rate.*

*![image][1]*

<span>The diagram above is a timeline showing a series of cash flows starting today (T</span><sub></sub><span>) and in to the future. Here we see than an initial investment of $772 is invested today and then each year, for the next 10 years, $100 is received from the investment. In this case, by year 10 we will have received $1,000 from our initial investment of $772. The difference is our interest received and, because of the time value of money, we expect that this amount is higher since $100 in 10 years time will not be worth the same as $100 today.</span>

### Net Present Value

Net Present Value (NPV) can be used to decide whether an investment is worthwhile or not. In short, you calculate the NPV as the sum of all the discounted cash flows based on your required interest rate. If the result is positive then you should make the investment; if the result is negative then you should not.

The formula follows.

![image][2]

To make things easier (and save you having to remember formulas etc.) you can put use Excel to calculate the NPV for you. Simply enter =NPV(8%,-772,100,100,100,100,100,100,100,100,100,100) into a cell and it will give you the answer -$93.51. Since the result is negative then you would reject the investment at an 8% discount rate.

But you might ask, what discount rate would give us a zero NPV (break even)? This could be useful to know since that rate may actually be acceptable to us and requiring an 8% return in the current market might not be achievable. Here comes the Internal Rate of Return.

### <span>Internal Rate of Return</span>

<span>Here, we make the assumption that NPV = 0 and then solve for <em>r</em> in the above equation. The maths on this one is even more complicated but thankfully Excel also has IRR as a built in formula. In order for this to work, it actually uses an iterative process of trial and error (thankfully your computer will do it in the blink of an eye) but to work properly you have to give the formula a guess at what you think the rate is. In this case, we will stick with 8% since it can’t be too far off the mark.</span>

<span>If you enter =IRR({-772,100,100,100,100,100,100,100,100,100,100},8%) in excel then you should return a result of 5%. If 5% was an acceptable rate of return for our investment then we would accept the opportunity, otherwise we would reject it.</span>

<span>This example was rather simple since we had even cash flows for the entire series. But NPV and IRR have the ability to handle variable values for the series, including additional reinvestment in later years (you just adjust the value as being positive or negative). I guess what I’m trying to convey is that you shouldn’t let the simplicity of this example convince you that NPV and IRR are not powerful tools &#8211; they most certainly are.</span>

<span>If you are game, try your hand at calculating the NPV and IRR for the below example which is a little bit trickier. Still assume an 8% discount rate as above and feel free to comment with your results. Would you accept this investment?</span>

<span><img alt="image" src="https://31.media.tumblr.com/d66fba441a1371b0a6a9f96501037c85/tumblr_inline_n12xu5eDz91sw89p8.gif" /></span>

 [1]: https://31.media.tumblr.com/b000e126f9e66792931ca04540f2b11c/tumblr_inline_n12w9wBvj01sw89p8.gif
 [2]: https://31.media.tumblr.com/5fd9f60e3e08277ee853f37d44cbd82f/tumblr_inline_n12xgezFKV1sw89p8.gif
