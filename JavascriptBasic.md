# Javascript Basic [Exercises with Solution]

[Origimal Source](https://www.w3resource.com/javascript-exercises/javascript-basic-exercises.php#EDITOR)

**Q1. Write a JavaScript program to display the current day and time in the following format**

(Sample)
```
Today is : Tuesday.
Current time is : 10 PM : 30 : 38
```

```javascript

// Q1
function rightNow() {
  const today = new Date();

  const daysOfWeek = [
    'Monday',
    'Tuesday',
    'Wednesday',
    'Thursday',
    'Friday',
    'Saturday',
    'Sunday',
  ];
  let day = today.getDay();
  day = daysOfWeek[day];

  let h = today.getHours();
  h = changeHourFormat(h);

  const m = today.getMinutes();

  const s = today.getSeconds();

  console.log(`Today is : ${day}`);
  console.log(`${h}:${m}:${s}`);
}

function changeHourFormat(h) {
  const hours = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12];
  if (h <= 12) {
    return `${h} AM`;
  } else {
    const oneDigitHour = h - 12;
    const currentHour = oneDigitHour + 'PM';
    return currentHour;
  }
}

rightNow();
```