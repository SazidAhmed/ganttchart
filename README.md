<div align="center">
    <img src="https://github.com/frappe/design/blob/master/logos/logo-2019/frappe-gantt-logo.png" height="128">
    <h2>Frappe Gantt</h2>
    <p align="center">
        <p>A simple, interactive, modern gantt chart library for the web</p>
        <a href="https://frappe.github.io/gantt">
            <b>View the demo »</b>
        </a>
    </p>
</div>

<p align="center">
    <a href="https://frappe.github.io/gantt">
        <img src="https://cloud.githubusercontent.com/assets/9355208/21537921/4a38b194-cdbd-11e6-8110-e0da19678a6d.png">
    </a>
</p>

### Install
```
npm install frappe-gantt
```

### Usage
Include it in your HTML:
```
<script src="frappe-gantt.min.js"></script>
<link rel="stylesheet" href="frappe-gantt.css">
```

And start hacking:
```js
var tasks = [
    {
        start: '2018-10-01 00',
        end: '2018-10-01 05',
        name: 'Redesign website',
        id: "Task 0",
        progress: 20
    },
    {
        start: '2018-10-01 01',
        end: '2018-10-01 08',
        name: 'Write new content',
        id: "Task 1",
        progress: 5,
        dependencies: 'Task 0'
    },
    {
        start: '2018-10-01 07',
        end: '2018-10-01 18',
        name: 'Apply new styles',
        id: "Task 2",
        progress: 10,
        dependencies: 'Task 1'
    }
  ...
]
var gantt = new Gantt("#gantt", tasks);
```

You can also pass various options to the Gantt constructor:
```js
var gantt = new Gantt("#gantt", tasks, {
    header_height: 50,
    column_width: 30,
    step: 24,
    view_modes: ['Hour','Quarter Day', 'Half Day', 'Day', 'Week', 'Month'],
    bar_height: 20,
    bar_corner_radius: 3,
    arrow_curve: 5,
    padding: 18,
    view_mode: 'Hour',   
    date_format: 'YYYY-MM-DD',
    custom_popup_html: null
});
```

If you want to contribute:

1. Clone this repo.
2. `cd` into project directory
3. `yarn`
4. `yarn run dev`

License: MIT

------------------
Project maintained by [frappe](https://github.com/frappe)
