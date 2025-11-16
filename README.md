<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Terminal Glitch Birthday</title>

<style>
body {
  background: black;
  color: #00ff55;
  font-family: "Courier New", monospace;
  padding: 25px;
  white-space: pre-wrap;
}
.glitch {
  animation: glitch 0.3s infinite;
}
@keyframes glitch {
  0% { text-shadow: 2px 0 red; }
  20% { text-shadow: -2px 0 blue; }
  40% { text-shadow: 2px 0 green; }
  60% { text-shadow: -2px 0 yellow; }
  80% { text-shadow: 3px 0 purple; }
  100% { text-shadow: -3px 0 cyan; }
}
</style>

</head>
<body>

<div id="output"></div>

<script>
const text = 
`> System Booting...
> Accessing SYED_AZZIM files...
> WARNING: too handsome. Adjust brightness.

> Loading birthday message...
████░░░ 40%
██████░ 72%
████████ 100%

---------------------------------------------
🎉 HAPPY BIRTHDAY SYED! 🎉

Semoga Allah murahkan rezeki,
tenangkan hati,
dan bagi kekuatan melalui apa saja.

You deserve peace & happiness.

---------------------------------------------
> End of transmission.`;

let i = 0;
function type() {
  if (i < text.length) {
    document.getElementById("output").innerHTML += 
      <span class="glitch">${text.charAt(i)}</span>;
    i++;
    setTimeout(type, 35);
  }
}
type();
</script>

</body>
</html>
