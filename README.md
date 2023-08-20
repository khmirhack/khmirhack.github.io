<!DOCTYPE html>
<html>
<head>
<style>
  #clock {
    font-size: 2em;
    text-align: center;
    margin-top: 50px;
  }
</style>
</head>
<body>

<div id="clock">00:00:00</div>

<script>
function updateClock() {
  const now = new Date();
  const hours = String(now.getHours()).padStart(2, '0');
  const minutes = String(now.getMinutes()).padStart(2, '0');
  const seconds = String(now.getSeconds()).padStart(2, '0');
  const timeString = `${hours}:${minutes}:${seconds}`;
  
  document.getElementById("clock").textContent = timeString;
}

// Update the clock every second
setInterval(updateClock, 1000);

// Initial update
updateClock();
</script>

</body>
</html>
