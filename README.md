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
  font-family:Arial,Helvetica,sans-serif;
}

html{
  scroll-behavior:smooth;
}

body{
  background:#f4f7fb;
  color:#172033;
  line-height:1.6;
}

header{
  background:#123b70;
  color:white;
  position:sticky;
  top:0;
  z-index:100;
  box-shadow:0 2px 8px rgba(0,0,0,.15);
}

.header{
  width:92%;
  max-width:1150px;
  margin:auto;
  min-height:65px;
  display:flex;
  align-items:center;
  justify-content:space-between;
}

.logo{
  font-size:21px;
  font-weight:bold;
}

nav a{
  color:white;
  text-decoration:none;
  margin-left:15px;
  font-size:14px;
}

.menu-btn{
  display:none;
  background:none;
  border:0;
  color:white;
  font-size:25px;
}

.container{
  width:92%;
  max-width:1150px;
  margin:auto;
}

.hero{
  background:linear-gradient(135deg,#123b70,#1976d2);
  color:white;
  text-align:center;
  padding:75px 20px;
}

.hero h1{
  font-size:43px;
  margin-bottom:12px;
}

.hero p{
  max-width:760px;
  margin:0 auto 25px;
  font-size:17px;
}

.btn{
  display:inline-block;
  border:0;
  border-radius:8px;
  padding:12px 19px;
  background:#ffb703;
  color:#111;
  font-weight:bold;
  cursor:pointer;
  text-decoration:none;
  margin:5px;
}

.btn:hover{
  opacity:.9;
}

.btn.secondary{
  background:white;
  color:#123b70;
}

.btn.dark{
  background:#123b70;
  color:white;
}

section{
  padding:50px 0;
}

.section-title{
  text-align:center;
  margin-bottom:30px;
}

.section-title h2{
  color:#123b70;
  font-size:29px;
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

.form-box{
  background:white;
  padding:25px;
  border-radius:12px;
  box-shadow:0 3px 12px rgba(0,0,0,.07);
  max-width:850px;
  margin:auto;
}

label{
  display:block;
  margin-top:12px;
}

select,
input[type="text"],
textarea{
  width:100%;
  padding:12px;
  border:1px solid #ccd3dc;
  border-radius:7px;
  margin-top:7px;
  margin-bottom:12px;
  font-size:15px;
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

.info{
  background:#e7f0ff;
  border-left:5px solid #1976d2;
  padding:15px;
  margin:15px 0;
  border-radius:6px;
}

.hidden{
  display:none!important;
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

.badge{
  display:inline-block;
  padding:4px 10px;
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
  margin-top:12px;
  border-radius:8px;
  border-left:4px solid #1976d2;
}

.video{
  background:#172033;
  color:white;
  min-height:190px;
  display:flex;
  align-items:center;
  justify-content:center;
  border-radius:10px;
  margin-top:15px;
  text-align:center;
  padding:20px;
}

.price{
  font-size:34px;
  font-weight:bold;
  color:#123b70;
}

.ai-box{
  background:white;
  border-radius:14px;
  padding:25px;
  box-shadow:0 3px 12px rgba(0,0,0,.08);
  max-width:950px;
  margin:auto;
}

.ai-header{
  text-align:center;
  margin-bottom:20px;
}

.ai-header h2{
  color:#123b70;
}

.ai-output{
  margin-top:20px;
}

.ai-output h3{
  color:#123b70;
  margin-bottom:8px;
}

.ai-output ul,
.ai-output ol{
  padding-left:22px;
}

.ai-output p{
  margin-bottom:10px;
}

.chat{
  background:#f5f7fa;
  padding:15px;
  border-radius:10px;
  margin-top:15px;
}

.chat input{
  margin-bottom:5px;
}

footer{
  background:#10243d;
  color:white;
  text-align:center;
  padding:35px 15px;
  margin-top:20px;
}

.small{
  font-size:13px;
  color:#667085;
}

.stat{
  text-align:center;
}

.stat strong{
  display:block;
  font-size:28px;
  color:#123b70;
}

@media(max-width:700px){

  nav{
    display:none;
  }

  .menu-btn{
    display:block;
  }

  .hero h1{
    font-size:31px;
  }

  .hero{
    padding:55px 15px;
  }

}
</style>
</head>

<body>

<header>

<div class="header">

<div class="logo">
🎓 JHI Online School
</div>

<button class="menu-btn" onclick="toggleMenu()">☰</button>

<nav id="mainNav">
<a href="#home">Home</a>
<a href="#programmes">Programmes</a>
<a href="#subjects">Subjects</a>
<a href="#ai">AI Teacher</a>
<a href="#premium">Premium</a>
</nav>

</div>

</header>


<!-- HOME -->

<main id="home">

<section class="hero">

<div class="container">

<h1>JHI Online School</h1>

<p>
Learn from your phone with structured JCE and MSCE lessons,
study notes, assignments, quizzes, examinations and AI-assisted
learning tools.
</p>

<a href="#programmes" class="btn">
Start Learning
</a>

<a href="#ai" class="btn secondary">
🤖 JHI AI Teacher
</a>

</div>

</section>


<!-- STATS -->

<section>

<div class="container">

<div class="grid">

<div class="card stat">
<strong>14+</strong>
Subjects
</div>

<div class="card stat">
<strong>6+</strong>
Months Programme
</div>

<div class="card stat">
<strong>4+</strong>
Subjects Daily
</div>

<div class="card stat">
<strong>K10,000</strong>
Premium / Month
</div>

</div>

</div>

</section>


<!-- PROGRAMMES -->

<section id="programmes">

<div class="container">

<div class="section-title">

<h2>Choose Your Programme</h2>

<p>
Select the programme you want to study.
</p>

</div>


<div class="grid">

<div class="card level-card"
onclick="chooseLevel('JCE')">

<h3>📘 JCE Programme</h3>

<p>
Junior Certificate of Education preparation.
</p>

<button class="btn">
Choose JCE
</button>

</div>


<div class="card level-card"
onclick="chooseLevel('MSCE')">

<h3>📚 MSCE Programme</h3>

<p>
Malawi School Certificate of Education preparation.
</p>

<button class="btn">
Choose MSCE
</button>

</div>

</div>

</div>

</section>


<!-- ENROLMENT -->

<section id="enrolment" class="hidden">

<div class="container">

<div class="section-title">

<h2>Student Enrolment</h2>

<p id="selectedLevelText"></p>

</div>


<div class="form-box">

<label>
<strong>Student Name</strong>
</label>

<input
id="studentName"
type="text"
placeholder="Enter your name"
>


<label>
<strong>Select Form</strong>
</label>

<select id="studentForm">

<option value="">
Choose Form
</option>

<option>
Form 1
</option>

<option>
Form 2
</option>

<option>
Form 3
</option>

<option>
Form 4
</option>

</select>


<h3>
Select Your Subjects
</h3>

<p class="small">
Select at least four subjects.
</p>

<div id="subjectList"></div>


<div class="notice">

<strong>6-Month Programme</strong>

<p>
JHI students should follow a structured programme of at least
six months, including lessons, assignments, revision and
monthly examinations.
</p>

</div>


<button
class="btn"
onclick="enrolStudent()">

Continue to Dashboard

</button>

</div>

</div>

</section>


<!-- DASHBOARD -->

<section id="dashboard" class="dashboard">

<div class="container">

<div class="section-title">

<h2>🎓 Student Dashboard</h2>

<p id="welcome"></p>

</div>


<div class="success">

<strong>Your JHI learning journey has started!</strong>

<br>

Complete your daily lessons and assignments consistently.

</div>


<div class="card">

<h3>Overall Progress</h3>

<div class="progress">

<div
class="progress-bar"
id="progressBar">
</div>

</div>

<p id="progressText">
0% completed
</p>

<button
class="btn"
onclick="increaseProgress()">

Complete Today's Lesson

</button>

</div>


<section>

<h2>
📅 Today's Study Plan
</h2>

<p>
Study at least four subjects per day.
</p>

<br>

<div
id="dailyPlan"
class="grid">
</div>

</section>


<section>

<h2>
📚 My Course Catalogue
</h2>

<br>

<div
id="courseCatalogue"
class="grid">
</div>

</section>


<section>

<h2>
📝 Monthly Examination
</h2>

<br>

<div class="card">

<h3>
Monthly Examination
</h3>

<p>
At the end of each month, students should complete an examination
covering the material studied during that month.
</p>

<br>

<button
class="btn"
onclick="startExam()">

Start Monthly Exam

</button>

</div>

</section>

</div>

</section>


<!-- SUBJECTS -->

<section id="subjects">

<div class="container">

<div class="section-title">

<h2>📚 Subject Catalogue</h2>

<p>
JHI Online School learning areas
</p>

</div>


<div class="grid">

<div class="card">
<h3>Mathematics</h3>
<p>Core mathematics and examination preparation.</p>
</div>

<div class="card">
<h3>Additional Mathematics</h3>
<p>Advanced mathematics preparation.</p>
</div>

<div class="card">
<h3>English</h3>
<p>Language, grammar, comprehension and examination skills.</p>
</div>

<div class="card">
<h3>Chichewa</h3>
<p>Chichewa language and examination preparation.</p>
</div>

<div class="card">
<h3>Physics</h3>
<p>Physics concepts, calculations and practice.</p>
</div>

<div class="card">
<h3>Chemistry</h3>
<p>Chemistry concepts and examination preparation.</p>
</div>

<div class="card">
<h3>Biology</h3>
<p>Biology concepts, diagrams and practice.</p>
</div>

<div class="card">
<h3>Agriculture</h3>
<p>Agricultural science and practical learning.</p>
</div>

<div class="card">
<h3>Life Skills</h3>
<p>Life skills and personal development.</p>
</div>

<div class="card">
<h3>Social Studies</h3>
<p>Society, citizenship and social studies.</p>
</div>

<div class="card">
<h3>Geography</h3>
<p>Physical and human geography.</p>
</div>

<div class="card">
<h3>Bible Knowledge</h3>
<p>Bible knowledge and examination preparation.</p>
</div>

<div class="card">
<h3>French</h3>
<p>French language learning and practice.</p>
</div>

<div class="card">
<h3>Business Studies</h3>
<p>Business concepts and examination preparation.</p>
</div>

</div>

</div>

</section>


<!-- AI TEACHER -->

<section id="ai">

<div class="container">

<div class="ai-box">

<div class="ai-header">

<h2>🤖 JHI AI Teacher</h2>

<p>
Generate structured learning materials for JHI students.
</p>

<div class="info">

The current prototype demonstrates the AI Teacher workflow.
The production version will connect securely to an AI service
and the verified JHI curriculum.

</div>

</div>


<label>
<strong>Subject</strong>
</label>

<select id="aiSubject">

<option>Mathematics</option>
<option>Additional Mathematics</option>
<option>English</option>
<option>Chichewa</option>
<option>Physics</option>
<option>Chemistry</option>
<option>Biology</option>
<option>Agriculture</option>
<option>Life Skills</option>
<option>Social Studies</option>
<option>Geography</option>
<option>Bible Knowledge</option>
<option>French</option>
<option>Business Studies</option>

</select>


<label>
<strong>Programme</strong>
</label>

<select id="aiLevel">

<option>JCE</option>
<option>MSCE</option>

</select>


<label>
<strong>Form</strong>
</label>

<select id="aiForm">

<option>Form 1</option>
<option>Form 2</option>
<option>Form 3</option>
<option>Form 4</option>

</select>


<label>
<strong>Topic</strong>
</label>

<input
id="aiTopic"
type="text"
placeholder="Example: Adding Fractions"
>


<label>
<strong>Difficulty</strong>
</label>

<select id="aiDifficulty">

<option>Beginner</option>
<option>Intermediate</option>
<option>Exam Preparation</option>

</select>


<button
class="btn"
onclick="generateJHILesson()">

🤖 Generate JHI Lesson

</button>


<div
id="aiLoading"
class="notice hidden">

🤖 JHI AI Teacher is preparing your lesson...

</div>


<div
id="aiOutput"
class="ai-output hidden">


<div class="card">

<span class="badge">
JHI AI Teacher
</span>

<h2 id="aiLessonTitle"></h2>


<div class="lesson">

<h3>
📖 Lesson
</h3>

<div id="aiLesson"></div>

</div>


<div class="lesson">

<h3>
📝 Study Notes
</h3>

<div id="aiNotes"></div>

</div>


<div class="lesson">

<h3>
✏️ Assignment
</h3>

<div id="aiAssignment"></div>

</div>


<div class="lesson">

<h3>
🧠 Quiz
</h3>

<div id="aiQuiz"></div>

</div>


<div class="lesson">

<h3>
🎬 Blackboard Video Script
</h3>

<div id="aiVideo"></div>

</div>


<button
class="btn"
onclick="saveJHILesson()">

💾 Save Lesson

</button>


<button
class="btn secondary"
onclick="printJHILesson()">

🖨️ Print / PDF

</button>

</div>

</div>


<!-- AI CHAT -->

<div class="chat">

<h3>
💬 Ask JHI AI Teacher
</h3>

<p class="small">
Prototype mode: ask a question and receive a learning response.
</p>

<input
id="aiQuestion"
type="text"
placeholder="Example: Explain fractions simply"
>

<button
class="btn dark"
onclick="askJHI()">

Ask Teacher

</button>

<div
id="aiAnswer">
</div>

</div>

</div>

</div>

</section>


<!-- PREMIUM -->

<section id="premium">

<div class="container">

<div class="section-title">

<h2>
⭐ JHI Premium
</h2>

<p>
Full monthly learning programme
</p>

</div>


<div
class="card"
style="text-align:center;max-width:650px;margin:auto">

<h3>
Premium Student
</h3>

<div class="price">
K10,000
</div>

<p>
per month
</p>

<br>

<p>✅ All selected subjects</p>
<p>✅ Structured lessons</p>
<p>✅ Study notes</p>
<p>✅ Assignments</p>
<p>✅ Topic quizzes</p>
<p>✅ Examination preparation</p>
<p>✅ Monthly examinations</p>
<p>✅ AI-assisted learning</p>
<p>✅ Six-month study programme</p>

<br>

<button
class="btn"
onclick="subscribe()">

Subscribe for K10,000/month

</button>

<div id="paymentMessage"></div>

</div>

</div>

</section>


<!-- LEARNING SYSTEM -->

<section>

<div class="container">

<div class="section-title">

<h2>
📖 JHI Learning System
</h2>

</div>


<div class="grid">

<div class="card">
<h3>1️⃣ Lesson</h3>
<p>Learn the topic step-by-step.</p>
</div>

<div class="card">
<h3>2️⃣ Video</h3>
<p>Watch the lesson video.</p>
</div>

<div class="card">
<h3>3️⃣ Notes</h3>
<p>Review important concepts.</p>
</div>

<div class="card">
<h3>4️⃣ Assignment</h3>
<p>Practise what you have learned.</p>
</div>

<div class="card">
<h3>5️⃣ Quiz</h3>
<p>Test your understanding.</p>
</div>

<div class="card">
<h3>6️⃣ Monthly Exam</h3>
<p>Measure your progress.</p>
</div>

</div>

</div>

</section>


<!-- CURRICULUM NOTICE -->

<section>

<div class="container">

<div class="notice">

<h3>
📌 Curriculum Standard
</h3>

<p>
JHI Online School content should be aligned with the current
Malawi secondary-school curriculum and appropriate approved
learning materials. Topics should be verified before publication.
</p>

</div>

</div>

</section>

</main>


<footer>

<p>
<strong>🎓 JHI Online School</strong>
</p>

<p>
JCE & MSCE Online Learning Platform
</p>

<p>
© 2026 JHI Online School
</p>

</footer>


<script>

/* ==========================
   JHI ONLINE SCHOOL SYSTEM
========================== */

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


/* MOBILE MENU */

function toggleMenu(){

const nav =
document.getElementById("mainNav");

if(nav.style.display === "block"){

nav.style.display = "none";

}else{

nav.style.display = "block";

}

}


/* SELECT PROGRAMME */

function chooseLevel(level){

selectedLevel = level;

document
.getElementById("enrolment")
.classList.remove("hidden");

document
.getElementById("selectedLevelText")
.innerHTML =
"You selected the <strong>"
+ level +
"</strong> programme.";

const list =
document.getElementById("subjectList");

list.innerHTML = "";

subjects.forEach(function(subject,index){

list.innerHTML += `

<div class="subject">

<input
type="checkbox"
id="subject${index}"
value="${subject}">

<label for="subject${index}">
${subject}
</label>

</div>

`;

});

document
.getElementById("enrolment")
.scrollIntoView();

}


/* ENROL */

function enrolStudent(){

const name =
document.getElementById("studentName")
.value.trim();

const form =
document.getElementById("studentForm")
.value;

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

alert(
"Please select at least 4 subjects."
);

return;

}


localStorage.setItem(
"jhiName",
name
);

localStorage.setItem(
"jhiLevel",
selectedLevel
);

localStorage.setItem(
"jhiForm",
form
);

localStorage.setItem(
"jhiSubjects",
JSON.stringify(selectedSubjects)
);


document
.getElementById("dashboard")
.style.display = "block";


document
.getElementById("welcome")
.innerHTML =
"Welcome, <strong>"
+ name +
"</strong> | "
+ selectedLevel +
" | "
+ form;


buildDailyPlan();

buildCatalogue();

document
.getElementById("dashboard")
.scrollIntoView();

}


/* DAILY PLAN */

function buildDailyPlan(){

const daily =
document.getElementById("dailyPlan");

daily.innerHTML = "";

const today =
selectedSubjects.slice(0,4);


today.forEach(function(subject,index){

daily.innerHTML += `

<div class="card">

<span class="badge">
Subject ${index+1}
</span>

<h3>
${subject}
</h3>

<div class="lesson">

<strong>
Today's Lesson
</strong>

<p>
Complete the assigned JHI lesson
for ${subject}.
</p>

</div>

<div class="video">

🎬<br>
JHI Video Lesson Area

</div>

<div class="lesson">

<strong>
✏️ Assignment
</strong>

<p>
Complete the exercise before moving
to the next lesson.
</p>

</div>

<button
class="btn"
onclick="increaseProgress()">

Mark Complete

</button>

</div>

`;

});

}


/* COURSE CATALOGUE */

function buildCatalogue(){

const catalogue =
document.getElementById("courseCatalogue");

catalogue.innerHTML = "";

selectedSubjects.forEach(function(subject){

catalogue.innerHTML += `

<div class="card">

<span class="badge">
${selectedLevel}
</span>

<h3>
${subject}
</h3>

<p>
Structured learning programme.
</p>

<div class="lesson">
📖 Lesson 1
</div>

<div class="lesson">
📝 Notes
</div>

<div class="lesson">
✏️ Assignment
</div>

<div class="lesson">
🧠 Topic Quiz
</div>

<button
class="btn"
onclick="openCourse('${subject}')">

Open Course

</button>

</div>

`;

});

}


/* COURSE */

function openCourse(subject){

alert(
subject +
" course opened. The full curriculum lesson system will be connected next."
);

}


/* PROGRESS */

function increaseProgress(){

if(progress < 100){

progress += 10;

}

document
.getElementById("progressBar")
.style.width =
progress + "%";

document
.getElementById("progressText")
.innerHTML =
progress + "% completed";

localStorage.setItem(
"jhiProgress",
progress
);

}


/* MONTHLY EXAM */

function startExam(){

alert(
"Monthly examination area opened. The production version will contain subject-specific examination questions and automatic marking."
);

}


/* PREMIUM */

function subscribe(){

document
.getElementById("paymentMessage")
.innerHTML = `

<div class="notice">

<strong>
Premium selected.
</strong>

<br>

Price:
<strong>K10,000 per month</strong>

<br><br>

Payment integration will be connected securely
through the JHI backend.

</div>

`;

}


/* ==========================
   JHI AI TEACHER
========================== */

function generateJHILesson(){

const subject =
document.getElementById("aiSubject")
.value;

const level =
document.getElementById("aiLevel")
.value;

const form =
document.getElementById("aiForm")
.value;

const topic =
document.getElementById("aiTopic")
.value.trim();

const difficulty =
document.getElementById("aiDifficulty")
.value;


if(!topic){

alert(
"Please enter a topic."
);

return;

}


const loading =
document.getElementById("aiLoading");

const output =
document.getElementById("aiOutput");


loading.classList.remove("hidden");

output.classList.add("hidden");


setTimeout(function(){


document
.getElementById("aiLessonTitle")
.innerHTML =
subject +
" — " +
topic;


document
.getElementById("aiLesson")
innerHTML = `

<p>
Welcome to JHI Online School.
</p>

<p>
Today we are learning:
<strong>${topic}</strong>.
</p>

<p>
Programme:
<strong>${level}</strong>
</p>

<p>
Form:
<strong>${form}</strong>
</p>

<h4>
🎯 Learning Objectives
</h4>

<ul>

<li>Understand the meaning of ${topic}.</li>

<li>Identify the important concepts.</li>

<li>Apply the concepts to examples.</li>

<li>Answer examination-style questions.</li>

</ul>

<h4>
📖 Teacher Explanation
</h4>

<p>
The teacher introduces ${topic} using simple
language and step-by-step examples appropriate
for ${form} students.
</p>

<p>
The lesson difficulty is:
<strong>${difficulty}</strong>.
</p>

<h4>
Example
</h4>

<p>
The teacher works through a simple example
on the digital board and explains each step.
</p>

`;


document
.getElementById("aiNotes")
innerHTML = `

<h4>
Key Notes
</h4>

<ul>

<li>
Definition and meaning of ${topic}.
</li>

<li>
Important terms related to the topic.
</li>

<li>
Main principles students should remember.
</li>

<li>
Worked examples should be studied carefully.
</li>

<li>
Practice is required before attempting the topic test.
</li>

</ul>

<h4>
Summary
</h4>

<p>
Review the main concepts of ${topic}
and make sure you can explain them
without looking at your notes.
</p>

`;


document
.getElementById("aiAssignment")
innerHTML = `

<h4>
Assignment
</h4>

<ol>

<li>
Define ${topic} in your own words.
</li>

<li>
Write five important points about ${topic}.
</li>

<li>
Give two examples related to the topic.
</li>

<li>
Explain one practical application.
</li>

<li>
Write one examination-style question.
</li>

</ol>

<p>
<strong>
Instruction:
</strong>
Complete the assignment before moving
to the next lesson.
</p>

`;


document
.getElementById("aiQuiz")
innerHTML = `

<h4>
Quick Quiz
</h4>

<ol>

<li>
What is ${topic}?
</li>

<li>
What is the most important concept?
</li>

<li>
Give one example.
</li>

<li>
Explain why the topic is important.
</li>

<li>
What would you tell another student
about this topic?
</li>

</ol>

<p>
<strong>
Teacher instruction:
</strong>
Review your answers before continuing.
</p>

`;


document
.getElementById("aiVideo")
innerHTML = `

<h4>
🎬 Blackboard Video Script
</h4>

<p>
<strong>
Scene 1 — Introduction
</strong>
</p>

<p>
The JHI teacher appears at the digital
blackboard.
</p>

<p>
"Welcome to JHI Online School.
Today we are learning about ${topic}."
</p>


<p>
<strong>
Scene 2 — Topic
</strong>
</p>

<p>
The teacher writes:
</p>

<div class="info">
${topic}
</div>


<p>
<strong>
Scene 3 — Explanation
</strong>
</p>

<p>
The teacher explains the definition,
key concepts and important terms while
writing them on the board.
</p>


<p>
<strong>
Scene 4 — Worked Example
</strong>
</p>

<p>
The teacher works through an example
step-by-step.
</p>


<p>
<strong>
Scene 5 — Student Exercise
</strong>
</p>

<p>
The teacher writes an exercise on the board
and tells students to pause the video
and solve it.
</p>


<p>
<strong>
Scene 6 — Conclusion
</strong>
</p>

<p>
The teacher summarizes the lesson and
introduces the assignment.
</p>

`;


loading.classList.add("hidden");

output.classList.remove("hidden");

output.scrollIntoView({
behavior:"smooth"
});


},1000);

}


/* SAVE AI LESSON */

function saveJHILesson(){

const data = {

title:
document
.getElementById("aiLessonTitle")
.innerText,

lesson:
document
.getElementById("aiLesson")
.innerText,

notes:
document
.getElementById("aiNotes")
.innerText,

assignment:
document
.getElementById("aiAssignment")
.innerText,

quiz:
document
.getElementById("aiQuiz")
.innerText,

video:
document
.getElementById("aiVideo")
.innerText,

date:
new Date().toISOString()

};


localStorage.setItem(
"jhiLastAILesson",
JSON.stringify(data)
);


alert(
"JHI lesson saved on this device."
);

}


/* PRINT */

function printJHILesson(){

window.print();

}


/* ASK JHI AI */

function askJHI(){

const question =
document
.getElementById("aiQuestion")
.value.trim();


if(!question){

alert(
"Please enter a question."
);

return;

}


document
.getElementById("aiAnswer")
innerHTML = `

<div class="success">

<strong>
JHI Teacher:
</strong>

<p>
That's a good question!
</p>

<p>
Your question was:
<strong>
${escapeHTML(question)}
</strong>
</p>

<p>
The full AI Teacher will answer questions
using the JHI curriculum and provide
step-by-step explanations.
</p>

</div>

`;

}


/* SECURITY HELPER */

function escapeHTML(text){

return text
.replace(/&/g,"&amp;")
.replace(/</g,"&lt;")
.replace(/>/g,"&gt;")
.replace(/"/g,"&quot;")
.replace(/'/g,"&#039;");

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

const savedProgress =
localStorage.getItem("jhiProgress");


if(savedProgress){

progress =
parseInt(savedProgress);

document
.getElementById("progressBar")
.style.width =
progress + "%";

document
.getElementById("progressText")
.innerHTML =
progress + "% completed";

}


if(
savedName &&
savedLevel &&
savedForm &&
savedSubjects
){

selectedLevel =
savedLevel;

selectedSubjects =
JSON.parse(savedSubjects);


document
.getElementById("dashboard")
.style.display =
"block";


document
.getElementById("welcome")
.innerHTML =
"Welcome back, <strong>"
+ savedName +
"</strong> | "
+ savedLevel +
" | "
+ savedForm;


buildDailyPlan();

buildCatalogue();

}

};

</script>

</body>
</html>
