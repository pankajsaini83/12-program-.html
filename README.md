
<html>
<head>
    <title>Student Record</title>
    
</head>
<style>
    body{
         border: 5px solid black;
  div{
    color:black;
    
  }
  
</style>
<body bgcolor="yellow">
<div>
    <marquee><h1> WELCOME COLLEAGE WEBSITE</h1></marquee>
        <h1>Student Attendance</h1>
       <h4> Enter Name:<input type="Name" id="name" placeholder="Enter Name">
        <br>
        <br>
        Enter Roll No:<input type="Number" id="roll" placeholder="Enter Roll No">
        <br>
        <br>
        Please Save:<button onclick="saveStudent()">Save</button>
</h4>
        <h2>Present Students in a Class</h2>
        <ol id="studentList"></ol>
        </div>

</body>
<script>
  function saveStudent() {
    let name = document.getElementById("name").value;
    let roll = document.getElementById("roll").value;
    if (name === "" || roll === "") {
        alert("Please enter all details");
        return;
    }
    let list = document.getElementById("studentList");
    let li = document.createElement("li");
    li.innerText = "Name: " + name + " | Roll No: " + roll;
    list.appendChild(li);
    document.getElementById("name").value = "";
    document.getElementById("roll").value = "";
  }
</script>
</html>
