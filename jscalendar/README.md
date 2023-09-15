#link
https://digvijay212.github.io/geekm5/jscalendar/
Mini-Calender

This is a simple mini calendar that displays the current month, day, and year. It is built using HTML, CSS, and JavaScript.
Getting Started

To get started, clone the repository and open the index.html file in a web browser. You should see a simple calendar that displays the current month, day, and year.

#html
 <div class="calendar-container">
        <p class="month-name" id="month-name">october</p>
        <p class="day-name" id="day-name">Friday</p>
        <p class="day-number" id="day-number">12</p>
        <p class="year" id="year">2020</p>
      </div>




#js

const monthNameEl = document.getElementById("month-name");
const dayNameEl = document.getElementById("day-name");
const dayNumEl = document.getElementById("day-number");
const yearEl = document.getElementById("year");

const date = new Date();
const month = date.getMonth();
monthNameEl.innerText = date.toLocaleString("en", {
  month: "long",
});

dayNameEl.innerText = date.toLocaleString("en", {
  weekday: "long",
});

dayNumEl.innerText = date.getDate();

yearEl.innerText = date.getFullYear();
 
