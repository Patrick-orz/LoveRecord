## Login Manage
[https://staticshield.vercel.app/dashboard](https://staticshield.vercel.app/dashboard)

## Features

### Duration Time

On the head of your website, you can set the starting time when you met each other, became lovers... And then it will show how long that most important thing has happened. 

Starting time can be set in the js script at the end of `index.html`:

```js
// countto
    const date1 = new Date("06/03/2022");
    const date2 = new Date();
    const Difference_In_Time = date2.getTime()-date1.getTime();
    let Difference_In_Days = 0;
    if (Difference_In_Time>0)
        Difference_In_Days=Math.ceil(Difference_In_Time / (1000 * 3600 * 24));

    if (document.getElementById('state1')) {
        document.getElementById("state1").setAttribute("countTo",Difference_In_Days.toString());
        document.getElementById("state1").innerHTML=Difference_In_Days.toString();
        const countUp = new CountUp('state1', document.getElementById("state1").getAttribute("countTo"));
        if (!countUp.error) {
            countUp.start();
        } else {
            console.error(countUp.error);
        }
    }
```

### Events Calendar

Events Calendar uses js plugins and css style to record some important events during your daily life. You can set these events at the end of `index.html`, following the format like:

```js
// calendar
    document.addEventListener('DOMContentLoaded', function () {
        var calendarEl = document.getElementById('calendar');
        var calendar = new FullCalendar.Calendar(calendarEl, {
            plugins: ['interaction', 'dayGrid'],
            defaultDate: '2022-06',
            events: [
                {
                    title: '第1次表白👩‍❤️‍👨',
                    start: '2022-06-03'
                },
                {
                    title: '第1次牵手🤝',
                    start: '2022-06-06'
                }
            ]
        });
        calendar.render();
```

### Love Card

In Love Card, you can write words, especially truth to tell your beloved one how much you love him/her. Or just write down his/her merits.

### Records

Finally, at the end of the homepage, it allows you to put photos and related storied between you and your spouse. 

## Source

This template is designed by [Creative Tim](https://www.creative-tim.com). You can find more information in [Soft UI Design System Pro](https://themes.getbootstrap.com/product/soft-ui-design-system-pro/)
