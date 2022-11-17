# vanilla-calendar
It's a simple calendar in JS Vanilla
# Description:
A simple, lightweight, vanilla JavaScript inline calendar that allows you to filter dates, set available dates/weekdays, enable/disable past dates and much more.

# How to use it:
Import the vanilla-calendar’s JavaScript and CSS files:
<link rel="stylesheet" href="src/css/vanilla-calendar-min.css">
<script src="src/js/vanilla-calendar-min.js"></script>

# Create a placeholder element for the inline calendar.

<div id="myCalendar" class="vanilla-calendar"></div>

# Create a new instance and render a basic calendar inside the container you just created.

let myCalendar = new VanillaCalendar({
    selector: "#myCalendar"
})
Determine whether to enable past dates. Default: true.
let myCalendar = new VanillaCalendar({
    selector: "#myCalendar",
    pastDates: false
})

# Set the available dates & weekdays. Default: empty array.

let myCalendar = new VanillaCalendar({
    selector: "#myCalendar",
    availableWeekDays: [
      {day: 'monday', others: values},
      {day: 'tuesday', others: values}
    ],
    availableDates: [
      {date: '2019-09-15', others: values},
      {date: '2019-09-16', others: values},
      {date: '2019-09-17', others: values},
      {date: '2019-09-25', others: values},
      {date: '2019-09-26', others: values}
    ]
})

# Enable/disable date filtering. Default: false.

let myCalendar = new VanillaCalendar({
    selector: "#myCalendar",
    datesFilter: true
})

# Localize the month & week names.
let myCalendar = new VanillaCalendar({
    selector: "#myCalendar",
    months: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
    shortWeekday: ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat']
})
Do some cool stuff as the user select a date.

# let myCalendar = new VanillaCalendar({
    selector: "#myCalendar",
    onSelect: (data, elem) => {}
})

# Customize the init date & today’s date.

let myCalendar = new VanillaCalendar({
    selector: "#myCalendar",
    date: new Date(),
    todaysDate: new Date()
})

# API methods.

// re-init the calendar
myCalendar.init();
// destroy the calendar
myCalendar.destroy();
// reset the calendar
myCalendar.reset();
// update options
myCalendar.set(options);
