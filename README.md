<!DOCTYPE html>
<style>
.rainbow {
  font-weight: bold;
  font-size: 2em;
  background: linear-gradient(
    to right,
    #ff0000,
    #ff7f00,
    #ffff00,
    #00ff00,
    #0000ff,
    #4b0082,
    #8f00ff
  );
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  animation: rainbow 2s linear infinite;
  background-size: 200% auto;
  margin: 20px 0;
}

@keyframes rainbow {
  0% { background-position: 0% 50%; }
  100% { background-position: 100% 50%; }
}

.input-container {
  margin: 20px;
  padding: 10px;
}
</style>

<div class="input-container">
  <input type="text" id="inputText" placeholder="Enter your text here">
  <button onclick="applyRainbow()">Make Rainbow!</button>
</div>

<script>
function applyRainbow() {
  const text = document.getElementById('inputText').value;
  const element = document.createElement('div');
  element.className = 'rainbow';
  element.textContent = text;
  document.body.appendChild(element);
}
</script>
