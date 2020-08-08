# Quip

Quip (QUIck Planner) is basically a calendar of the current month where
you can add notes to a day and see them in a sorted fashion.
This makes planning the sequence of events a little easier (and nicer)
than typing in a text editor or on a sticky note (physical or digital).

The interface is very minimal, though.
Only a 100-character event title (the note name) can be added, but nothing more.
No detail.

_**Note:**
The interface is not very mobile-friendly,
but it behaves sufficiently well for screen widths above 600px._

### Warning

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

- Click on the 'Add' button for a date.

  A prompt will appear, requiring you to write an event title.

- Write an event title, and press the enter key or click on 'Okay'.

  The event title will show up on the sidebar (on the right),
preceded by the date.
Every time a new entry is added,
all entries on the sidebar are automatically sorted:
based on date first, and then alphabetically,

- To remove all added events, click on the cross icon on the sidebar.

  A pop-up will appear, warning about the removal.
If you click on the 'Yes' button,
all data will be removed and the page will be reloaded.

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

- Multiple instances simultaneously usable in different browser tabs.

  Since all event data is saved in the session storage,
the same page opened in different browser tabs will not share data.
You can open the HTML file in as many tabs as you want
to use multiple instances simultaneously.

### Downside

- There is no database, everything is stored in the session storage.
If a browser tab is closed, all data from that tab is lost.

- The limit on event titles is 100 characters.
A longer title may be entered in the prompt's input field,
but everything after the limit will be truncated.

- The sidebar is cleared and rewritten to every time a new event is added.
This might affect performance, although most likely negligibly.

- Sidebar entries do not provide hyphenation.
Long words are automatically broken, but _without_ any hyphen/dash character.

### License

[GNU General Public License v3.0](https://www.gnu.org/licenses/quick-guide-gplv3.html)

### Future Plan

- Provide data export feature
- Show only the events of a specific date upon user interaction

### Miscellaneous

#### Is there a plan to add a database?

Most likely, no.
This is a quick planning tool, and the developer would like it to stay that way.