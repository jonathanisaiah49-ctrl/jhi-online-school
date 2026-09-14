<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>JHI Online School | JCE & MSCE</title>

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
  font-family:Arial,sans-serif;
}

body{
  background:#f4f7fb;
  color:#172033;
  line-height:1.6;
}

header{
  background:#123b70;
  color:white;
  padding:18px;
  position:sticky;
  top:0;
  z-index:10;
}

.header{
  max-width:1100px;
  margin:auto;
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:15px;
}

.logo{
  font-size:22px;
  font-weight:bold;
}

nav a{
  color:white;
  text-decoration:none;
  margin-left:15px;
  font-size:14px;
}

.container{
  width:92%;
  max-width:1100px;
  margin:auto;
}

.hero{
  background:linear-gradient(135deg,#123b70,#1976d2);
  color:white;
  padding:70px 20px;
  text-align:center;
}

.hero h1{
  font-size:42px;
  margin-bottom:15px;
}

.hero p{
  max-width:700px;
  margin:0 auto 25px;
}

.btn{
  display:inline-block;
  padding:12px 20px;
  border:0;
  border-radius:8px;
  background:#ffb703;
  color:#111;
  font-weight:bold;
  cursor:pointer;
  text-decoration:none;
  margin:5px;
}

.btn.secondary{
  background:white;
  color:#123b70;
}

section{
  padding:45px 0;
}

.section-title{
  text-align:center;
  margin-bottom:30px;
}

.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:18px;
}

.card{
  background:white;
  padding:22px;
  border-radius:12px;
  box-shadow:0 3px 12px rgba(0,0,0,.08);
}

.card h3{
  color:#123b70;
  margin-bottom:8px;
}

.level-card{
  cursor:pointer;
  border:2px solid transparent;
  transition:.2s;
}

.level-card:hover{
  border-color:#1976d2;
  transform:translateY(-2px);
}

.subject{
  display:flex;
  align-items:center;
  gap:10px;
  padding:9px;
  border-bottom:1px solid #eee;
}

.subject input{
  width:18px;
  height:18px;
}

.form-box{
  background:white;
  padding:25px;
  border-radius:12px;
  margin-bottom:20px;
  box-shadow:0 3px 12px rgba(0,0,0,.07);
}

select,input[type="text"]{
  width:100%;
  padding:12px;
  border:1px solid #ccc;
  border-radius:7px;
  margin-top:8px;
  margin-bottom:15px;
}

.notice{
  background:#fff3cd;
  border-left:5px solid #ffb703;
  padding:15px;
  margin:15px 0;
  border-radius:6px;
}

.success{
  background:#d1e7dd;
  border-left:5px solid #198754;
  padding:15px;
  margin:15px 0;
  border-radius:6px;
}

.dashboard{
  display:none;
}

.progress{
  background:#ddd;
  border-radius:20px;
  height:18px;
  overflow:hidden;
  margin:10px 0;
}

.progress-bar{
  width:0%;
  height:100%;
  background:#1976d2;
  transition:.3s;
}

.subject-card{
  position:relative;
}

.badge{
  display:inline-block;
  padding:4px 9px;
  border-radius:20px;
  background:#e7f0ff;
  color:#123b70;
  font-size:12px;
  font-weight:bold;
  margin-bottom:8px;
}

.lesson{
  background:#f8f9fa;
  padding:15px;
  margin-top:10px;
  border-radius:8px;
  border-left:4px solid #1976d2;
}

.video{
  background:#172033;
  color:white;
  height:180px;
  display:flex;
  align-items:center;
  justify-content:center;
  border-radius:10px;
  margin-top:15px;
  text-align:center;
  padding:20px;
}

.price{
  font-size:32px;
  font-weight:bold;
  color:#123b70;
}

footer{
  background:#10243d;
  color:white;
  text-align:center;
  padding:30px 15px;
  margin-top:30px;
}

.hidden{
  display:none!important;
}

@media(max-width:650px){
  .hero h1{
    font-size:30px;
  }

  nav{
    display:none;
  }

  .header{
    justify-content:center;
  }
}
</style>
</head>

<body>

<header>
<div class="header">
<div class="logo">🎓 JHI Online School</div>

<nav>
<a href="#home">Home</a>
<a href="#programmes">Programmes</a>
<a href="#subjects">Subjects</a>
<a href="#premium">Premium</a>
</nav>
</div>
</header>


<main id="home">

<section class="hero">
<div class="container">

<h1>JHI Online School</h1>

<p>
Online learning for Malawi's JCE and MSCE students.
Study lessons, notes, exercises, quizzes and examination preparation
from your phone.
</p>

<a href="#programmes" class="btn">Start Learning</a>
<a href="#premium" class="btn secondary">Premium K10,000/month</a>

</div>
</section>


<section id="programmes">

<div class="container">

<div class="section-title">
<h2>Choose Your Programme</h2>
<p>Select the examination programme you are preparing for.</p>
</div>

<div class="grid">

<div class="card level-card" onclick="chooseLevel('JCE')">
<h3>📘 JCE Programme</h3>
<p>Junior Certificate of Education preparation.</p>
<button class="btn">Choose JCE</button>
</div>

<div class="card level-card" onclick="chooseLevel('MSCE')">
<h3>📚 MSCE Programme</h3>
<p>Malawi School Certificate of Education preparation.</p>
<button class="btn">Choose MSCE</button>
</div>

</div>
</div>
</section>


<section id="enrolment" class="hidden">

<div class="container">

<div class="section-title">
<h2>Student Enrolment</h2>
<p id="selectedLevelText"></p>
</div>

<div class="form-box">

<label><strong>Student Name</strong></label>
<input id="studentName" type="text" placeholder="Enter your name">

<label><strong>Select Form</strong></label>

<select id="studentForm">
<option value="">Choose Form</option>
<option>Form 1</option>
<option>Form 2</option>
<option>Form 3</option>
<option>Form 4</option>
</select>

<h3>Select Your Subjects</h3>

<p>
Choose the subjects you want to study.
Your daily programme will organize at least 4 subjects per study day.
</p>

<div id="subjectList"></div>

<div class="notice">
<strong>Important:</strong> Your full programme is designed to run for
at least <strong>6 months</strong>. Students should follow the weekly
lessons, exercises, topic tests and monthly examinations.
</div>

<button class="btn" onclick="enrolStudent()">Continue to Dashboard</button>

</div>
</div>
</section>


<section id="dashboard" class="dashboard">

<div class="container">

<div class="section-title">
<h2>🎓 Student Dashboard</h2>
<p id="welcome"></p>
</div>

<div class="success">
<strong>6-Month Study Programme</strong><br>
Stay consistent. Complete your daily lessons, assignments,
topic tests and monthly examinations.
</div>

<div class="card">
<h3>Overall Progress</h3>

<div class="progress">
<div class="progress-bar" id="progressBar"></div>
</div>

<p id="progressText">0% completed</p>

<button class="btn" onclick="increaseProgress()">
Complete Today's Lesson
</button>
</div>


<section>

<h2>📅 Today's Study Plan</h2>

<p>
You should study at least <strong>4 subjects per day</strong>.
Complete the lesson and assignment for each subject.
</p>

<div id="dailyPlan" class="grid"></div>

</section>


<section>

<h2>📚 My Course Catalogue</h2>

<div id="courseCatalogue" class="grid"></div>

</section>


<section>

<h2>📝 Monthly Examination</h2>

<div class="card">

<h3>Monthly Examination</h3>

<p>
At the end of every month, students should complete a monthly
examination covering the material studied during that month.
</p>

<div class="notice">
Month <strong id="examMonth">1</strong> examination:
complete your lessons and assignments before attempting the exam.
</div>

<button class="btn" onclick="startExam()">
Start Monthly Exam
</button>

</div>

</section>

</div>
</section>


<section id="subjects">

<div class="container">

<div class="section-title">
<h2>📚 JHI Subject Catalogue</h2>
<p>Available learning areas</p>
</div>

<div class="grid">

<div class="card"><h3>Mathematics</h3><p>Core mathematics lessons and examination practice.</p></div>

<div class="card"><h3>Additional Mathematics</h3><p>Advanced mathematics preparation.</p></div>

<div class="card"><h3>English</h3><p>Language, comprehension, grammar and examination skills.</p></div>

<div class="card"><h3>Chichewa</h3><p>Chichewa language and examination preparation.</p></div>

<div class="card"><h3>Physics</h3><p>Physics concepts, calculations and practice.</p></div>

<div class="card"><h3>Chemistry</h3><p>Chemistry concepts, experiments and examination practice.</p></div>

<div class="card"><h3>Biology</h3><p>Biology concepts, diagrams and examination preparation.</p></div>

<div class="card"><h3>Agriculture</h3><p>Agricultural science and practical knowledge.</p></div>

<div class="card"><h3>Life Skills</h3><p>Life skills and personal development.</p></div>

<div class="card"><h3>Social Studies</h3><p>Society, citizenship and social studies preparation.</p></div>

<div class="card"><h3>Geography</h3><p>Physical and human geography.</p></div>

<div class="card"><h3>Bible Knowledge</h3><p>Bible knowledge and examination preparation.</p></div>

<div class="card"><h3>French</h3><p>French language learning and practice.</p></div>

<div class="card"><h3>Business Studies</h3><p>Business concepts and examination preparation.</p></div>

</div>
</div>
</section>


<section id="premium">

<div class="container">

<div class="section-title">
<h2>⭐ JHI Premium</h2>
<p>One monthly subscription for the full learning programme.</p>
</div>

<div class="card" style="text-align:center;max-width:600px;margin:auto">

<h3>Premium Student</h3>

<div class="price">K10,000</div>

<p>per month</p>

<br>

<p>✅ All selected subjects</p>
<p>✅ Full lessons</p>
<p>✅ Video lessons</p>
<p>✅ Study notes</p>
<p>✅ Topic exercises</p>
<p>✅ Topic quizzes</p>
<p>✅ Examination preparation</p>
<p>✅ Monthly examinations</p>
<p>✅ 6-month structured programme</p>

<br>

<button class="btn" onclick="subscribe()">
Subscribe for K10,000/month
</button>

<p id="paymentMessage"></p>

</div>
</div>
</section>


<section>

<div class="container">

<div class="section-title">
<h2>📖 Learning Structure</h2>
</div>

<div class="grid">

<div class="card">
<h3>1. Lesson</h3>
<p>Learn the topic using a structured JHI lesson.</p>
</div>

<div class="card">
<h3>2. Video</h3>
<p>Watch the lesson video where available.</p>
</div>

<div class="card">
<h3>3. Notes</h3>
<p>Review the important points from the lesson.</p>
</div>

<div class="card">
<h3>4. Assignment</h3>
<p>Every lesson ends with an exercise or assignment.</p>
</div>

<div class="card">
<h3>5. Topic Test</h3>
<p>Test your understanding before moving forward.</p>
</div>

<div class="card">
<h3>6. Monthly Exam</h3>
<p>Review your progress with a monthly examination.</p>
</div>

</div>
</div>
</section>


<section>

<div class="container">

<div class="notice">

<h3>📌 Curriculum Standard</h3>

<p>
JHI Online School should align its courses with the current Malawi
secondary-school curriculum and approved learning materials.
Course topics should be verified against the current official
curriculum before being published as syllabus topics.
</p>

<br>

<p>
Reference sources include the Malawi Institute of Education (MIE)
and the Malawi National Examinations Board (MANEB).
</p>

</div>

</div>
</section>

</main>


<footer>

<p><strong>JHI Online School</strong></p>

<p>JCE & MSCE Online Learning Platform</p>

<p>© 2026 JHI Online School. All rights reserved.</p>

</footer>


<script>

const subjects = [
"Mathematics",
"Additional Mathematics",
"English",
"Chichewa",
"Physics",
"Chemistry",
"Biology",
"Agriculture",
"Life Skills",
"Social Studies",
"Geography",
"Bible Knowledge",
"French",
"Business Studies"
];

let selectedLevel = "";
let selectedSubjects = [];
let progress = 0;


/* SELECT LEVEL */

function chooseLevel(level){

selectedLevel = level;

document.getElementById("enrolment").classList.remove("hidden");

document.getElementById("selectedLevelText").innerHTML =
"You selected the <strong>"+level+"</strong> programme.";

const list = document.getElementById("subjectList");

list.innerHTML = "";

subjects.forEach(function(subject,index){

list.innerHTML += `
<div class="subject">
<input type="checkbox" id="subject${index}" value="${subject}">
<label for="subject${index}">${subject}</label>
</div>
`;

});

document.getElementById("enrolment").scrollIntoView({
behavior:"smooth"
});

}


/* ENROL STUDENT */

function enrolStudent(){

const name =
document.getElementById("studentName").value.trim();

const form =
document.getElementById("studentForm").value;

if(!name){

alert("Please enter your name.");

return;
}

if(!form){

alert("Please select your form.");

return;
}

selectedSubjects = [];

subjects.forEach(function(subject,index){

const checkbox =
document.getElementById("subject"+index);

if(checkbox.checked){

selectedSubjects.push(subject);

}

});

if(selectedSubjects.length < 4){

alert("Please select at least 4 subjects.");

return;
}

localStorage.setItem("jhiName",name);
localStorage.setItem("jhiLevel",selectedLevel);
localStorage.setItem("jhiForm",form);
localStorage.setItem(
"jhiSubjects",
JSON.stringify(selectedSubjects)
);

document.getElementById("dashboard").style.display="block";

document.getElementById("welcome").innerHTML =
"Welcome, <strong>"+name+
"</strong> | "+selectedLevel+
" | "+form;

buildDailyPlan();

buildCatalogue();

document.getElementById("dashboard").scrollIntoView({
behavior:"smooth"
});

}


/* DAILY PLAN */

function buildDailyPlan(){

const daily =
document.getElementById("dailyPlan");

daily.innerHTML="";

let todaySubjects =
selectedSubjects.slice(0,4);

todaySubjects.forEach(function(subject,index){

daily.innerHTML += `

<div class="card subject-card">

<span class="badge">Day Study ${index+1}</span>

<h3>${subject}</h3>

<p><strong>Today's lesson:</strong></p>

<div class="lesson">
Topic 1 — Official syllabus topic
</div>

<p style="margin-top:10px">
📺 Watch lesson video
</p>

<div class="video">
▶ Video Lesson Area
<br>
External video can be embedded here.
</div>

<p style="margin-top:10px">
📝 Read JHI study notes
</p>

<div class="lesson">
Study notes for this lesson will appear here.
</div>

<p style="margin-top:10px">
✏️ Assignment
</p>

<div class="lesson">
Complete the exercise for today's lesson
before moving to the next lesson.
</div>

</div>

`;

});

}


/* COURSE CATALOGUE */

function buildCatalogue(){

const catalogue =
document.getElementById("courseCatalogue");

catalogue.innerHTML="";

selectedSubjects.forEach(function(subject){

catalogue.innerHTML += `

<div class="card">

<span class="badge">${selectedLevel}</span>

<h3>${subject}</h3>

<p>
Structured lessons covering the current approved
curriculum for your programme.
</p>

<div class="lesson">
<strong>Topic 1</strong><br>
Official syllabus topic
</div>

<div class="lesson">
<strong>Topic 2</strong><br>
Official syllabus topic
</div>

<div class="lesson">
<strong>Topic 3</strong><br>
Official syllabus topic
</div>

<button class="btn" onclick="openCourse('${subject}')">
Open Course
</button>

</div>

`;

});

}


/* COURSE */

function openCourse(subject){

alert(
subject+
" course opened. Lessons, videos, notes, assignments and topic tests will be added here."
);

}


/* PROGRESS */

function increaseProgress(){

if(progress < 100){

progress += 10;

}

document.getElementById("progressBar").style.width =
progress+"%";

document.getElementById("progressText").innerHTML =
progress+"% completed";

}


/* MONTHLY EXAM */

function startExam(){

alert(
"Monthly examination area opened. Your exam should cover the lessons studied during the current month."
);

}


/* PREMIUM */

function subscribe(){

document.getElementById("paymentMessage").innerHTML =
`
<div class="notice">
<strong>Premium subscription selected.</strong><br>
Payment integration will be connected here.
<br><br>
Price: <strong>K10,000 per month</strong>
</div>
`;

}


/* LOAD SAVED STUDENT */

window.onload=function(){

const savedName =
localStorage.getItem("jhiName");

const savedLevel =
localStorage.getItem("jhiLevel");

const savedForm =
localStorage.getItem("jhiForm");

const savedSubjects =
localStorage.getItem("jhiSubjects");

if(savedName && savedLevel && savedForm && savedSubjects){

selectedLevel=savedLevel;

selectedSubjects=JSON.parse(savedSubjects);

document.getElementById("dashboard").style.display="block";

document.getElementById("welcome").innerHTML =
"Welcome back, <strong>"+savedName+
"</strong> | "+savedLevel+
" | "+savedForm;

buildDailyPlan();

buildCatalogue();

}

};

</script>

</body>
</html>
