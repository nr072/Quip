# Quip

Quip (QUIck Planner) is basically a calendar of the current month where
you can temporarily add noted to a day and see them in a sorted fashion.
This makes planning the sequence of events a little easier (and nicer)
than typing in a text editor or on a sticky note (physical or digital).

The interface is very minimal, though.
Only a 100-character event title (the note name) can be added, but nothing more.
No detail.

And the event titles are saved in a JavaScript variable.
So, they are highly temporary.
A simple tab reload will reset the page to its default, blank state.
Future plans include
using either session storage and/or providing a feature to export data.

_**Note:**
The interface is not very mobile-friendly,
but if behaves sufficiently well for screen widths above 600px._

### Warning

- The event data are highly temporary.
A simple tab reload will
remove everything and reset the page to its default, blank state.

- This was created and tested using
Mozilla Firefox version 79.0.
There may be discrepancies in case of other browsers
or other versions of the same browser.

### Why Use It

Handy for a quick planning session,
both in terms of individual and group planning.
Quip makes it very easy to
add events to different days and check out which comes after which.

Since short events are preferred for better readability,
it is best to use this just to
show a group of people the _sequence_ of your preplanned events,
or use it in a quick brainstorming session.

Kindly do not use Quip for _storing_ anything.
It is meant to be used as a quick-but-handy tool for rough planning.

### Features

- Add short event titles to various dates of the current month.

- See all titles in a sorted fashion.

### How to Use It

Since it is only a webpage, you need to open it in your browser
(simply by dragging the HTML file onto a browser tab,
or by serving the page and then opening it in the browser)
to use Quip.

#### Serving the page

Using Python 2,
you can run the following command in the Command Prompt or a terminal
and then access the page at `http://127.0.0.1:8000` in your browser:

```
python2 -m SimpleHTTPServer
```

Using Python 3:

```
python3 -m http.server
```

#### Using Quip

1. Click on the 'Add' button for a date.  
A prompt will appear, requiring you to write an event title.

2. Write an event title, and press the enter key or click on 'Okay'.  
The event title will show up in the sidebar (on the right),
preceded by the date.

All titles in the sidebar are automatically sorted,
based on date first and then alphabetically,
every time a new entry is added.

### How It Works

Each time an event is created, it is added to a list.
The list is then sorted: date-wise first, and then alphabetically.
And then all the entries of the side panel are rewritten,
replaced by the newly sorted ones.

### Upside

- Good for quick planning.

  There is no database.
So, you can just open the HTML file in as many tabs as you want
to use multiple instances simultaneously,
without having to worry about connection delay or anything like that.

### Downside

- There is no no database, which means everything you do here is temporary.
All it takes is an accidental page reload and everything is lost.
(Though warnings do pop up when you press 'F5' or 'CTRL+R'.)

- The limit on event titles is 100 characters.
A longer title may be entered in the prompt's input field,
but everything after the limit will be truncated.

- The sidebar is cleared and rewritten to every time a new event is added.
This might affect performance, although  most likely negligibly.

- Sidebar entries do not provide hyphenation.
Long words are automatically broken, but _without_ any hyphen/dash character.

### License

[GNU General Public License v3.0](https://www.gnu.org/licenses/quick-guide-gplv3.html)

### Future Plan

- Make data more persistent
  - Use session storage
  - Provide data export feature
- Show only the events of a specific date upon user interaction

### Miscellaneous

#### Is there a plan to make it less temporary?

Yes.
The risk of an accidental reload is dangerously obvious.
Session storage will most likely be used to solve this.
Plus, a feature to export data to file is planned.

A database will probably never be integrated.
This is a quick planning tool, and the developer would like it to stay that way.