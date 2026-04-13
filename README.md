
<html>
<head>
    <title> Welcome first page</title>
    
</head>
<style>
    h1{
        color:red;
        }
    body{
         border: 8px solid black;
        }
  div{
    color:black;
    
  }
  
</style>
<body bgcolor="aqua">
<div>
    <marquee><h1> WELCOME COLLEAGE WEBSITE</h1></marquee>
        <h1>Student Attendance</h1>
       <h4> Enter Name:<input type="Name" id="name" placeholder="Enter Name">
        <br>
        <br>
        Enter Roll No:<input type="Number" id="roll" placeholder="Enter Roll No">
        <br>
        <br>
            Enter Your course :<input type="text" id="course" placeholder="Enter Your course">
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
      let coursee = document.getElementById("course").value;
    if (name === "" || roll === "") {
        alert("Please enter complete information");
        return;
    }
    let list = document.getElementById("studentList");
    let li = document.createElement("li");
    li.innerText = "Name: " + name + " | Roll No: " + roll+"| Course:"+coursee;
    list.appendChild(li);
    document.getElementById("name").value = "";
       document.write("<br>");
    document.getElementById("roll").value = "";
      document.write("<br>");
    document.getElementById("coursee").value = " ";
  }
</script>
</html>
