<!DOCTYPE html>
<html>
<head>
<title>Simple Grid Game</title>
<style>
body {
font-family: Arial, sans-serif;
text-align: center;
}

table {
border-collapse: collapse;
margin: 20px auto;
}

td, th {
border: 1px solid black;
width: 120px;
height: 80px;
text-align: center;
}

input {
width: 90%;
border: none;
text-align: center;
}

.header {
background-color: #ddd;
font-weight: bold;
}
</style>
</head>

<body>

<h2>Simple Grid Game</h2>
<p>Enter answers that match both the row and column topics.</p>

<table>
<tr>
<th></th>
<th class="header">Alpha,Beta, Unlimited</th>
<th class="header">Green</th>
<th class="header">Sorcery</th>
</tr>

<tr>
<th class="header">Topic A</th>
<td><input></td>
<td><input></td>
<td><input></td>
</tr>

<tr>
<th class="header">Topic B</th>
<td><input></td>
<td><input></td>
<td><input></td>
</tr>

<tr>
<th class="header">Topic C</th>
<td><input></td>
<td><input></td>
<td><input></td>
</tr>
</table>

<button onclick="submitGrid()">Submit</button>

<p id="result"></p>

<script>
function submitGrid() {
let inputs = document.querySelectorAll("input");
let filled = 0;

inputs.forEach(input => {
if (input.value.trim() !== "") {
filled++;
}
});

document.getElementById("result").innerText =
"You filled " + filled + " out of 9 squares!";
}
</script>

</body>
</html>
