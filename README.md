<!DOCTYPE html>
<html>
<head>
<title>Notebook</title>
<style>
 input[type="button"] {
  background-color: pink;
 }
</style> 
<script>
  function addItem() {
   var newItem = document.createElement("div");
   newItem.innerHTML = document.getElementById("box").value;
   newItem.onclick = removeItem;
   document.getElementById("list").appendChild(newItem);
   saveList();
 }
 function removeItem() {
  document.getElementById("list").removeChild(this);
  saveList();
 }
function saveList() {
  localStorage.storedList = document.getElementById("list").innerHTML;
 }
function loadList() {
  document.getElementById("list").innerHTML = localStorage.storedList;
  for(var i = 0; i < list.children.lenght; i++) {
   list.children[i].onclick = removeItem;
  }
 }
</script>
</head>
<body>
<div style="background-color: black;">
<div style="color: white;">
<h1>Created by Timur Agaev</h1>
 </div>
</div>
<div style="background-color: blue;">
<div style="color: white;">
<div style="text-align: center;">
 <h1>Task list</h1>
 </div>
</div> 
<div style="background-color: green;">
<div style="text-align: center;">
 <br/>
 <input type="text" id="box" value="Enter the issue here"/>
 <br/>
