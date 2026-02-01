<!DOCTYPE html>


#yesBtn {
background: #e63946;
color: white;
margin-right: 10px;
}


#noBtn {
background: #adb5bd;
color: white;
position: absolute;
}


.celebration {
display: none;
animation: pop 0.6s ease forwards;
}


@keyframes pop {
from { transform: scale(0.8); opacity: 0; }
to { transform: scale(1); opacity: 1; }
}


.reward-btn {
margin-top: 20px;
background: #ffbe0b;
color: #000;
font-weight: bold;
}
</style>
</head>
<body>
<div class="card" id="mainCard">
<h1>Will you be my Valentine? 💖</h1>
<div class="buttons">
<button id="yesBtn">Yes 💕</button>
<button id="noBtn">No 😅</button>
</div>
</div>


<div class="card celebration" id="celebrationCard">
<h1>YAYYYYY!!! 🎉🥰</h1>
<p>You just made my day 💘</p>
<button class="reward-btn" onclick="showReward()">🎁 Reward</button>
<p id="rewardText" style="display:none; margin-top:15px; font-weight:bold;">
Congratulations 🎊 I have ordered your Winston 🐶❤️
</p>
</div>


<script>
const noBtn = document.getElementById('noBtn');
const yesBtn = document.getElementById('yesBtn');
const mainCard = document.getElementById('mainCard');
const celebrationCard = document.getElementById('celebrationCard');


noBtn.addEventListener('mouseenter', moveNo);
noBtn.addEventListener('touchstart', moveNo);


function moveNo() {
const x = Math.random() * 200 - 100;
const y = Math.random() * 100 - 50;
noBtn.style.transform = `translate(${x}px, ${y}px)`;
}


yesBtn.addEventListener('click', () => {
mainCard.style.display = 'none';
celebrationCard.style.display = 'block';
});


function showReward() {
document.getElementById('rewardText').style.display = 'block';
}
</script>
</body>
</html>
