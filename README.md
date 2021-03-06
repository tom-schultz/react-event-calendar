# react-event-calendar
A Calendar component that will display supplied events in a given month. 

## Demo & Examples

Live demo: [dptoot.github.io/react-event-calendar](http://dptoot.github.io/react-event-calendar/)

To build the examples locally, run:

```js
npm install
npm start
```

Then open [`localhost:8080`](http://localhost:8080) in a browser.


## Installation

The easiest way to use react-event-calendar is to install it from NPM



```js
npm install react-event-calendar --save
```
You can also use the standalone build by including `dist/react-event-calendar.js` in your page. If you use this, make sure you have already included React, and it is available as a global variable.


## Usage

Use this component to display a month view of a calendar with supplied event duration indicators.

```js
const EventCalendar = require('react-event-calendar');

const events = [
    {
        start: '2015-07-20',
        end: '2015-07-02',
        title: 'test event',
        description: 'This is a test description of an event',
    },
    {
        start: '2015-07-19',
        end: '2015-07-25',
        title: 'test event',
        description: 'This is a test description of an event',
        data: 'you can add what ever random data you may want to use later',
    },
];

<EventCalendar 
    month={7}
    year={2015}
    events={events} 
    onEventClick={(target, eventData, day) => console.log(eventData) />
```

### Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| events | array | Array of event objects to be represented on the calendar |
| month | int | Selected Month to display |
| year | int | Selected Year to display |
| onEventClick | func(target, eventData, day) | Callback for user click on any event node |
| onEventMouseOver | func(target, eventData, day) | Callback for user mouse over on any event node |
| onEventMouseOut | func(target, eventData, day) | Callback for user mouse out on any event node |

### Note
The component currently allows for up to 10 events to be displayed per day.

## License

The MIT License (MIT)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Copyright (c) 2015 James Lewis.
