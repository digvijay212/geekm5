
#hosted link:https://digvijay212.github.io/geekm5/js/digital%20clock/



#html



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./index.css">
</head>
<body>
    <h2>Digital Clock</h2>
    <div class="clock">
      <div>
        <span id="hour">00</span>
        <span class="text">Hours</span>
      </div>
      <div>
        <span id="minutes">00</span>
        <span class="text">Minutes</span>
      </div>
      <div>
        <span id="seconds">00</span>
        <span class="text">Seconds</span>
      </div>
      <div>
        <span id="ampm"><AM>
        <pm></pm></span>
      </div>
    </div>
    

    <script src="index.js" ></script>
</body>
</html>









#js



const hour = document.getElementById("hour");
const minute = document.getElementById("minutes");
const second = document.getElementById("seconds");
const ampm = document.getElementById("ampm");

function updateClock() {
  let h = new Date().getHours();
  let m = new Date().getMinutes();
  let s = new Date().getSeconds();
  let ampm = "AM";

  if (h > 12) {
    h = h - 12;
    ampm = "PM";
  }

  h = h < 10 ? "0" + h : h;
  m = m < 10 ? "0" + m : m;
  s = s < 10 ? "0" + s : s;

  hour.innerText = h;
  minute.innerText = m;
  second.innerText = s;
  ampm.innerText = ampm;
  setTimeout(() => {
    updateClock();
  }, 1000);
}

updateClock();
