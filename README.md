# Quick event planner

A webpage with a calendar on it, for the current month. 
There are boxes for all the days, 
and each contains a button to add events. 
Short (better keep them short, for aesthetic's sake), temporary events 
can be added to each day. 
A day can have multiple events. 
Each day shows the number of events already added to that day. 
All added events are displayed 
in a sorted manner (date-wise first and then alphabetically) 
on the side panel. 

_**Warning:**
Keep in mind that the events are added temporarily, as of now. 
They are stored in JS, so a simple reload will reset the page._

### Why Use It

Handy for a quick planning session. 
You can just sit with your team 
and quickly show them when you are going to do what. 

Since short events are preferred for better readability, 
it is best to use this just to show a group of people 
the sequence of your preplanned events, 
or use it in a quick brainstorming session. 

Kindly do not use it for _storing_ event plans. 
This is meant to be used as a quick-but-handy tool for rough planning. 

### How to Use It

- Click the button on a day to add an event to that day.

- The counter of that day will increase, 
and the event will be displayed in its sorted place on the side panel. 

### How It Works

Any time an event is added, 
it is added to a list 
which is then sorted – 
date-wise first, and then alphabetically. 
So, every time a new event is added, 
the list containing all the events is sorted again 
and the content of the side panel is rewritten.

### Upside

- Good for quick planning.
   There is no database, 
   so you can just open the HTML file in as many tabs as you want 
   to show to as many people you want 
   – without having to worry about 
   connection delay or server overloading or anything like that.

### Downside

- No database – which means everything you do here is temporary. 
   All it takes is an accidental page reload and everything is lost.

- Side panel is cleared and rewritten to every time a new event is added. 
Might affect performance, although  most likely negligibly. 

### Miscellaneous

#### Is there a plan to make it less temporary?

Yes, I understand an accidental F5-press is very likely – and dangerous. 
There is a plan, but not integrating a database. 
I will most likely use JS `localStorage` or something like that. 
This is a quick planning tool, 
and I would like it to stay that way.
