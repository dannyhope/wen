# tshow

**Specify times for page elements to be revealed**

<!--**Reveal parts of a page at specific times**-->

## Background

I run a [conference](http://uxbrighton.org.uk/2014 "one of my conferences") and would like to provide a better experience by updating the website throughout the day – showing a list of resteraunts at lunch time, for example. Since it’s a static site, the only way of acheiving this would be to hand and upload changes in real time, which is too disctracting, when you’re trying to focus on introducing speakers. So, for me, this is a perannial problem.

tShow lets you quickly add attributes to specify when elements should be visible, so that you don’t have to constantly tend to your website in order for something important to appear in a timely manner.

**Please will you make this for me?**

## Example

Here’s a paragraph which I want to control…

    <p>Hello world!</p>

…I add the magic stuff…

    <p tshow"2014-11-10T1100Z--2015, 2016--2017" tscroll="2014-11-10">Hello world!</p>

…and now it behaves thusly…

The paragraph will be visible between 11:00 (UTC) on November the 10th, 2014 and the 1st of January 2015, and then for all of 2016 and then never be shown again.

The paragraph would smoothly scroll into view, provided the following conditions are met:

- the element is visible at 11:10 on November the 10th 2014 (which it would be in this example)
- the user loads the page during the 10th of November

## Markup

Specify date/time ranges in custom attributes:

| attribute   |      value      |  explaination |
|----------|-------------|------|
| tshow |  `[datetime]--[datetime]` | when to show it |
| tscroll |  `[date/time]--[datetime]`, `autoscroll`  | when to scroll to it, whether automatically scroll when the user has the page open |

Both can contain as little as 1 date, whcih is taken as the start date.

If no timezone is specified, then it just uses the users local time.
