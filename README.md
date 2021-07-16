<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>East dark mode</title>
	<style>
		body{
		  margin: 0;
		  padding: 0;
		  font-family: sans-serif;
		}
		main{
		  margin: 5vh 15%;
		}
		h1{
		  font-size: 40px;
		  font-weight: 400;
		  text-align: center;
		}
		img{
		  width:50%;
		  height:auto;
		}
		p{
		  text-align: justify;
		  font-size: 18px;
		}
		label{
			position: absolute;
			width: 45px;
			height: 22px;
			right: 20px;
			top: 20px;
			border: 2px solid;
			border-radius: 20px;
		}
		label:before{
			position: absolute;
			content: '';
			width:20px;
			height: 20px;
			left: 1px;
			top: 1px;
			border-radius: 50%;
			background: #000;
			cursor: pointer;
			transition: 0.4s;
		}
		label.active:before{
			left: 24px;
			background: #fff;
		}
		body.night{
			background: #2C2B2B;
			color: #fff;
		}
		@media screen and (min-width:900px) {
		  .respon{
			display: flex;
		  }
		  img{
			height:50%;
			width:auto;
			padding-top: 3vh;
			padding-right: 5%;
		  }
		  p{
			max-width: 80%;
			line-height: 30px;
		  }
		}
	</style>
</head>
<body>
  <header>
	<label  id="dark-change"></label>
  </header>
  <main>
	  <h1></h1>
	  <div class="respon">
		<img src="">
		<p></p>
	  </div>
  </main>
	<script>
		var content = document.getElementsByTagName('body')[0];
		var darkMode = document.getElementById('dark-change');
		darkMode.addEventListener('click', function(){
			darkMode.classList.toggle('active');
			content.classList.toggle('night');
		})
	</script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<!-- <link rel="stylesheet" href="style.css"> -->
	<script src="translation.js"></script>

	<style>
		body{
	font-size: 18px;
}
.header {
	width: 90%;
	margin: 40px auto 20px;
	color: rgb(255, 10, 10);
	background-color: rgb(156, 233, 40);
	text-align: center;
	border: 1px solid rgb(255, 169, 169);
	border-radius: 10px 10px 10px 10px;
}

.wrapper {
	width: 80%;
	margin: 15px auto;
	border: 0px solid rgb(104, 102, 102)
}
.wrapper:after {
content: "";
display: block;
clear: both;
}
.words{
	width: 80%;
	float: left;
}
.word{
	width: 50%;
	float: left;
	padding-left: 50px;
}
#word_list{
	max-height: 400px;
	overflow: scroll;
}
li{
	list-style-type: none;
	line-height: 1.9em;
}
li:hover{
	cursor: pointer;
	color: rgb(0, 55, 311);
}
ul {
	margin-left: -15px;
}
#search{
	margin-top: 15px;
	margin-right: center;
	margin-bottom: 15px;
	margin-left: center;
}
/* button{
	height: 28px;
	color: rgb(17, 0, 252);
	background-color: lawngreen;
	border: none;
	border-radius: 4px;
} */

	</style>



	<title>Eng-Kur</title>
</head>
<body>
	<div class="header">
		<h1>English-Kurdish dictonary</h1>
	</div>

	<div class="wrapper">
		<div class="words">
			<input type="text" id="search" placeholder="search..">
			<button onclick="search()">Search</button>
			<ul id="word_list"></ul>
		</div>

		<div class="word">
			<h3 id="word_text"></h3>
			<p id="definition"></p>
			<hr>
			<h3>Related word</h3>
			<li id="related"></li>
		</div>
	</div>

</body>
</html>

<script type="text/javascript">
var dictionary = [
{
		word: "Apple",
		def: "سێڤ",
		rel:["سێڤا سور","سێڤا زه‌ر"]
	},
	{
		word: "Always",
		def: "هەمی دەما",
		rel:["هەمی گاڤا"," ‌"]
	},
	{
		word: "Absolutely‏",
		def: "چ پێنەڤێت‏",
		rel:["",""]
	},
	{
		word: "As long as",
		def: "ما دەم",
		rel:["",""]
	},
	{
		word: "‏‏Agreed‏",
		def: "ئەس رازیمە‏",
		rel:["","ئەم پێک هاتین"]
	},
	{
		word: "Although",
		def: "هەر چەندە",
		rel:["",""]
	},
	{
		word: "Be patience‏",
		def: "بێهن فرەهـ بە‏",
		rel:["",""]
	},
	{
		word: "Bring it to me",
		def: "بۆمن بینە",
		rel:["بوومن بینە","بۆمن بینە ‌"]
	},
	{
		word: "‏‏‏‏Book",
		def: "پەڕتووک",
		rel:["",""]
	},
	{
		word: "Breakfast‏",
		def: "تێشت‏",
		rel:["",""]
	},
	{
		word: "‏‏Banana",
		def: "موز",
		rel:["","مۆز"]
	},
	{
		word: "Bosom Friend‏",
		def: "هەڤالێ رح ب رح‏",
		rel:["",""]
	},
	{
		word: "‏‏By all means‏",
		def: "چ پێنەڤێت‏",
		rel:["",""]
	},
	{
		word: "Best woman in the world is My Mom.‏",
		def: "باشترین ژن دجیهانێ دا دەیکامنە‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏Before",
		def: "ژبەری",
		rel:["",""]
	},
	{
		word: "Come again?‏",
		def: "دووبارە ئاخڤتنا خۆ بێژە ڤە‏",
		rel:["",""]
	},
	{
		word: "Cool",
		def: "سار",
		rel:["تەزی"," ‌"]
	},
	{
		word: "Change",
		def: "بگوهرە",
		rel:["گوهرین"," بگۆهڕە‌"]
	},
	{
	   word: "Conscience‏",
		def: "وژدان‏",
		rel:["",""]
	},
	{
		word: "Camera‏",
		def: "کامیرە‏",
		rel:["",""]
	},
	{
		word: "Congratulbations",
		def: "پیرۆزبیت",
		rel:["",""]
	},
	{
		word: "Bye for now‏",
		def: "جارێ بخاترا تە‏",
		rel:["",""]
	},
	{
		word: "‏‏Cleaner‏",
		def: "‏‏‏‏‏باقژی ",
		rel:["باقژکرن","دەرمانێ باقژی یێ"]
	},
	{
		word: "‏‏‏‏‏City",
		def: "باژێر",
		rel:["","باژێڕ"]
	},
	{
		word: "‏‏Clock",
		def: "دەمژمێر",
		rel:["",""]
	},
	{
		word: "Car",
		def: "ترومبێل",
		rel:["توموبیل","تومبێل"]
	},
	{
		word: "Can you repeat that please?‏",
		def: "‏‏دێ شێی دووبارە کەی؟‏‏",
		rel:["",""]
	},
	{
		word: "‏Cant comprehend what you say ‏",
		def: "تێناگەهم تۆ جت بێژی‏",
		rel:["",""]
	},
	{
		word: "‏Can you say that again?‏",
		def: "‏دێ شێی بێژی یە ڤە‏",
		rel:["",""]
	},
	{
		word: "Come what may‏",
		def: "چ جێبیت بلا جێبیت‏",
		rel:["",""]
	},
	{
		word: "‏Color‏",
		def: "رەنگ‏",
		rel:["",""]
	},
	{
		word: "Do you want?‏",
		def: "تە دڤێت؟‏",
		rel:["",""]
	},
	{
		word: "Don't speak ill of anyone‏",
		def: "ب خرابی بەحسێ کەسێ نەکە‏",
		rel:["",""]
	},
	{
		word: "Don't apologize‏",
		def: "داخازا لێبورینێ نەخازە‏",
		rel:["",""]
	},
	{
		word: "Don't flatter yourself‏",
		def: "خۆ شرین نەکە‏",
		rel:["",""]
	},
	{
		word: "Don't interrupt me‏",
		def: "من نە راوستینە‏",
		rel:["",""]
	},
	{
		word: "‏‏Diet‏",
		def: "‏‏‏‏‏ڕێجیم ",
		rel:[""," "]
	},
	{
		word: "‏‏Days",
		def: "روژ",
		rel:["","ڕۆژ"]
	},
	{
		word: "‏‏‏‏‏Door",
		def: "دەرگەهـ",
		rel:["",""]
	},
	{
		word: "Don't worry about it‏",
		def: "‏‏‏ بخو نەکە خەم‏‏",
		rel:["",""]
	},
	{
		word: "Download‏",
		def: "‏دا گرتن‏",
		rel:["","تژی کرن"]
	},
	{
		word: "Don’t lie",
		def: "درەوا نەکە",
		rel:["دڕەوا نەکە","  ‌"]
	},
	{
		word: "Don't break my spirit‏",
		def: "من بێ بوها نەکە‏",
		rel:["",""]
	},
	{
		word: "‏‏Don't tell anyone‏",
		def: "نە بێژە چ کەسا‏",
		rel:["",""]
	},
	{
		word: "‏‏Don't mention it‏",
		def: "پێتڤی سۆپاسی ناکەت‏",
		rel:["",""]
	},
	{
		word: "Don't care‏",
		def: "توو ژهەژی‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏Don't care",
		def: "گرنگی یێ پێنە دە",
		rel:["",""]
	},
	{
		word: "Damn",
		def: "نەفرەت بیت",
		rel:["",""]
	},
	{
		word: "Do it later",
		def: "وێ باشی یێ بکە",
		rel:["",""]
	},
	{
		word: "Does he know you?",
		def: "ئەو تە دنیاسیت؟",
		rel:["",""]
	},
	{
		word: "‏‏‏‏Date",
		def: "تاریخ",
		rel:["","بەروار"]
	},
	{
		word: "Excuse me ?‏",
		def: "ببورە ئاخڤتنا خۆ دووبارە بکە‏",
		rel:["",""]
	},
	{
		word: "Everyone is happy‏",
		def: "هەمی کەیف خۆشن‏",
		rel:["",""]
	},
	{
		word: "‏Eye",
		def: "چاڤ",
		rel:["",""]
	},
	{
		word: "Eat something",
		def: "تشتەکی بخۆ",
		rel:["تشتەکی بخو","  ‌"]
	},
	{
		word: "Forever",
		def: "حەتا حەتایێ ",
		rel:["",""]
	},
	{
		word: "Forget about it‏",
		def: "ژبیرکە چنینە‏",
		rel:["",""]
	},
	{
		word: "Farewell‏",
		def: "بخێربمینی‏",
		rel:["",""]
	},
	{
		word: "Flawless‏",
		def: "بێ کێماسی‏",
		rel:["",""]
	},
	{
		word: "For my sake‏",
		def: "سەر خاترا من‏",
		rel:["",""]
	},
	{
		word: "‏‏‏Foot",
		def: "پێ",
		rel:["",""]
	},
	{
		word: "Fish‏",
		def: "ماسی‏",
		rel:["",""]
	},
	{
		word: "For my sake‏",
		def: "سەر خاترامن‏",
		rel:["",""]
	},
	{
		word: "Fair- Weather Friend‏",
		def: "هەڤالێ مەسلەحچی‏",
		rel:["",""]
	},
	{
		word: "False Friend‏",
		def: "هەڤالێ خراب‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏For you",
		def: "ژبەر تە",
		rel:["","بوتە"]
	},
	{
		word: "Good Luck‏",
		def: "بەختەکێ باش‏",
		rel:["",""]
	},
	{
		word: "General‏",
		def: "گشتی‏",
		rel:["",""]
	},
	{
		word: "Good morning‏",
		def: "سپێدە باش‏",
		rel:["",""]
	},
	{
		word: "‏‏Googbye",
		def: "بخاتراتە",
		rel:["","بخاتڕاتە"]
	},
	{
		word: "God Forbid‏",
		def: "خۆدێ نەکەت  ‏",
		rel:["","خۆدێ نەکری "]
	},
	{
		word: "Glasses‏",
		def: " بەر چاڤك‏",
		rel:["",""]
	},
	{
		word: "Got it‏",
		def: "تێ گەهشتم‏",
		rel:["",""]
	},
	{
		word: "God rest his soul‏",
		def: "خۆدێ عەفو بکەت‏",
		rel:["",""]
	},
	{
		word: "God rest her soul‏",
		def: "خۆدێ وێ عەفو بکەت‏",
		rel:["",""]
	},
	{
		word: "God willing‏",
		def: " خۆدێ حەسکەت‏",
		rel:["","إن شاءالله"]
	},
	{
		word: "God damn you‏",
		def: "نەفرەتێت خۆدێ لتەبن‏",
		rel:["",""]
	},
	{
		word: "‏‏Give me",
		def: "بدە من",
		rel:["",""]
	},
	{
		word: "Hello‏",
		def: "سلاف‏",
		rel:["",""]
	},
	{
		word: "How are you feeling today?‏",
		def: "توو ئەڤرۆکە چاوانی؟‏",
		rel:["",""]
	},
	{
		word: "He was my father",
		def: "ئەو بابێ منە ",
		rel:["",""]
	},
	{
		word: "He is my brother‏",
		def: "ئەو برایێ منە‏",
		rel:["",""]
	},
	{
		word: "‏‏Half",
		def: "نیڤەك",
		rel:["","نیڤەک"]
	},
	{
		word: "Have it your way‏",
		def: "بکەیڤا خوی‏",
		rel:["",""]
	},
	{
		word: "‏‏Hand",
		def: "دەست",
		rel:["",""]
	},
	{
		word: "‏Heart",
		def: "دل",
		rel:["","دڵ"]
	},
	{
		word: "‏‏‏‏Hair",
		def: "پرج",
		rel:["",""]
	},
	{
		word: "I will do my best",
		def: "ئەس چ سەر خۆ ناهێلم",
		rel:["",""]
	},
	{
		word: "I don't understand",
		def: "ئەس تێناگەهم",
		rel:["",""]
	},
	{
		word: "I,m hungry‏",
		def: "ئەس برسیمە‏",
		rel:["",""]
	},
	{
		word: "I believe you‏",
		def: "ئەس ژتە باوەرکەم‏",
		rel:["",""]
	},
	{
		word: "I trust you‏",
		def: "باوەریامن بتە دهێت‏",
		rel:["",""]
	},
	{
		word: "‏‏It was nothing‏",
		def: "پێتڤی ناکەت‏",
		rel:["","من چنە کریە بۆتە"]
	},
	{
		word: "‏Importance‏",
		def: "گرنگی‏",
		rel:["",""]
	},
	{
		word: "I couldn't be bettero‏",
		def: "ئەس باشتر نابم‏",
		rel:["","گەلەك باشم"]
	},
	{
		word: "I can not say‏",
		def: "ئەس نەشێم بێژم‏",
		rel:["",""]
	},
	{
		word: "I still love you‏",
		def: "ئەس هێشتا حەشتەکەم‏",
		rel:["",""]
	},
	{
		word: "I'm Ok‏",
		def: "ئەس باشم‏",
		rel:["",""]
	},
	{
		word: "I'm on cloud nine‏",
		def: "ئەس گەلەك گەلەك کەیف خوشم‏",
		rel:["",""]
	},
	{
		word: "I'm over the moon‏",
		def: "ئەس زێدە زێدە کەیف خوشم‏",
		rel:["",""]
	},
	{
		word: "I'm alright‏",
		def: "ب سلامەتم‏",
		rel:["","ئەس باشم"]
	},
	{
		word: "I'm well‏",
		def: "ئەس باشم‏",
		rel:["","تەندروستیامن یا باشە"]
	},
	{
		word: "I'm great, thanks‏",
		def: "ئەس باشم سۆپاس‏",
		rel:["",""]
	},
	{
		word: "I'm alright‏",
		def: "ب سلامەتم‏",
		rel:["","ئەس باشم"]
	},
	{
		word: "I will Go‏",
		def: "ئەس دێ چم‏",
		rel:["",""]
	},
	{
		word: "I'm surprised to see you here‏",
		def: "مەندە هوش بوم بدیتناتە لڤێرە‏",
		rel:["",""]
	},
	{
		word: "It's nice to see you again‏",
		def: "دووبارە بێخوش بوم بدیتناتە‏",
		rel:["",""]
	},
	{
		word: "It's nice to meet you‏",
		def: "بێخوش بوم بنیاسیناتە‏",
		rel:["",""]
	},
	{
		word: "I can't thank you enough‏",
		def: "ئەس نزانم چاوا سۆپاسیاتە بکەم‏",
		rel:["",""]
	},
	{
		word: "It's Not important‏",
		def: "نەیا گرنگە‏",
		rel:["",""]
	},
	{
		word: "I beg Your Pardon‏",
		def: "هیڤی دکەم لمن ببورە‏",
		rel:["",""]
	},
	{
		word: "I apologize‏",
		def: "داخازا لێبورینێ دخازم‏",
		rel:["",""]
	},
	{
		word: "I'm Torn‏",
		def: "ئەس دوو دلم‏",
		rel:["",""]
	},
	{
		word: "I'm unsure‏",
		def: "ئەس نە بشت ڕاستم‏",
		rel:["",""]
	},
	{
		word: "I agree‏",
		def: "دگەل بوچونا تەمە‏",
		rel:["",""]
	},
	{
		word: "I'm agree‏",
		def: "ئەس رازیمە‏",
		rel:["",""]
	},
	{
		word: "I know him Well‏",
		def: "ئەز وی باش دنیاسم‏",
		rel:["",""]
	},
	{
		word: "I know what do you mean‏",
		def: "دزانم مەرەماتە جیە تێ گەهشتم‏",
		rel:["",""]
	},
	{
		word: "I Get it Now‏",
		def: "نوکە تێ گەهشتم‏",
		rel:["",""]
	},
	{
		word: "I feel you‏",
		def: "ئەس تە دگەهم‏",
		rel:["",""]
	},
	{
		word: "I see‏",
		def: "ئەس تێدگەهم‏",
		rel:["",""]
	},
	{
		word: "It's up to me‏",
		def: "ئەس بکەیڤا خومە‏",
		rel:["",""]
	},
	{
		word: "I'm happy to help‏",
		def: "بێخۆشم کو هاریکاربم‏",
		rel:["",""]
	},
	{
		word: "I'm feeling down‏",
		def: "ئەس گەلەك هەست بخەمگینی یێ کەم‏",
		rel:["",""]
	},
	{
		word: "If I'm not mistaken‏",
		def: "ئەگەر ئەس خەلەت نەبم‏",
		rel:["",""]
	},
	{
		word: "I pity you‏",
		def: "دلێ من دمینیتە بتەڤە ‏",
		rel:["",""]
	},
	{
		word: "I'm so relieved‏",
		def: "ئەس گەلەك مرتاحم ‏",
		rel:["",""]
	},
	{
		word: "I feel depressed‏",
		def: "ئەس گەلەك بێزارم‏",
		rel:["ئەس گەلەك بێ تاقەتم","ئەس گەلەك خەمگینم"]
	},
	{
		word: "I'm mad",
		def: "ئەس تۆڕە مە",
		rel:["ئەس توورە مە","ئەس توڕە مە ‌"]
	},
	{
		word: "I'm very busy‏",
		def: "‏‏‏‏‏گەلەك بشولم",
		rel:[""," "]
	},
	{
		word: "‏I can't thank you enough‏",
		def: "چەند سۆپاسی یا تە بکەم کێمە‏",
		rel:["",""]
	},
	{
		word: "‏‏I'm thankful",
		def: "ئەس سۆپاس دارم",
		rel:["",""]
	},
	{
		word: "I'm thirsty",
		def: "ئەس تێهنی مە",
		rel:["ئەس تێ هنی مە"," ‌"]
	},
	{
		word: "It's ok‏",
		def: "‏‏‏‏‏چنینە ",
		rel:[""," "]
	},
	{
		word: "‏I'm well‏",
		def: "‏‏‏‏‏ئەس باشم ",
		rel:[""," "]
	},
	{
		word: "I can't take it anymore‏",
		def: "نەشێم ئێدی تەحەملێ بکەم‏",
		rel:["",""]
	},
	{
		word: "‏‏I'm very well‏",
		def: "‏‏‏‏‏ئەس گەلەك باشم ",
		rel:[""," "]
	},
	{
		word: "I'm tired‏",
		def: "‏‏‏‏‏ماندی مە ",
		rel:[""," "]
	},
	{
		word: "I Dunno maybe‏",
		def: "‏‏‏  نزانم بەلکی‏‏",
		rel:["",""]
	},
	{
		word: "I'm not very well‏",
		def: "‏‏‏‏‏نە گەلەك باشم",
		rel:[""," "]
	},
	{
		word: "I'm terrible‏",
		def: "‏‏‏‏‏گەلەك خرابم",
		rel:[""," "]
	},
	{
		word: "I don't speak English‏",
		def: "‏‏‏‏‏ئینگلیزی نزانم ",
		rel:[""," "]
	},
	{
		word: "‏I only speakvery little English‏",
		def: "‏‏‏بیجەك ئینگلیزی دزانم‏‏",
		rel:["",""]
	},
	{
		word: "‏‏I don't speak very little English‏",
		def: "‏‏‏گەلەك ئینگلیزی نزانم‏‏",
		rel:["",""]
	},
	{
		word: "‏‏I'm sorry",
		def: "من ببورە",
		rel:["","لمن ببۆڕە"]
	},
	{
		word: "I'm thankful",
		def: "ئەس مەمنونم",
		rel:["ئەس مەمنوونم"," ئەس مەمنۆنم‌"]
	},
	{
		word: "I'm full",
		def: "ئەس تێرم",
		rel:["ئەس تێڕم"," ‌"]
	},
	{
		word: "I don’t care",
		def: "بۆ من نە گرنگە",
		rel:["بوو من نە گڕنگە"," بومن نە یا گرنگە‌"]
	},
	{
		word: "I fell it",
		def: "هەست پێدکەم",
		rel:["هەست پێ کرن"," هەست پێت کەم‌"]
	},
	{
		word: "It was useful",
		def: "یاب مڤا بۆ",
		rel:["یا بڤا بوو"," یاب مڤا بوو‌"]
	},
	{
		word: "I'm at your service‏",
		def: "ئەس دخزمەت دامە‏",
		rel:["",""]
	},
	{
		word: "I don’t get it",
		def: "ئەس تێ نا گەهم",
		rel:["ئەس تێناگەهم"," ‌"]
	},
	{
		word: "It’s your turn",
		def: "دۆرا تەیە",
		rel:["دوڕا تەیە"," دووڕا تەیە‌"]
	},
	{
		word: "‏‏I'm on my last legs‏",
		def: "ئەس گەلەك ماندی مە‏",
		rel:["",""]
	},
	{
		word: "‏‏I'm tied up‏",
		def: "ئەس گەلەك بشولم‏",
		rel:["","ئەس گەلەك مژیلم"]
	},
	{
		word: "I love you‏",
		def: "ئەس حەشتەکەم‏",
		rel:["",""]
	},
	{
		word: "| detest you‏",
		def: "کەربێت من ژتە ڤەبن‏",
		rel:["",""]
	},
	{
		word: "I have no use for you‏",
		def: "توو بێ بوهای لدەڤ من‏",
		rel:["",""]
	},
	{
		word: "I loathe you‏",
		def: "زێدە من کەرب ژتە ڤەبن‏",
		rel:["",""]
	},
	{
		word: "I can't anymore‏",
		def: "ئەس زێدەتر نەشێم‏",
		rel:["",""]
	},
	{
		word: "‏I want to go",
		def: "من دڤێت بچم",
		rel:["",""]
	},
	{
		word: "‏‏I have to go",
		def: "پێتڤیە ئەس بچم",
		rel:["",""]
	},
	{
		word: "‏‏‏I Want to stay",
		def: "من دڤێت بمینم",
		rel:["",""]
	},
	{
		word: "I believe you‏‏",
		def: "ئەس ژتە باوەرکەم‏",
		rel:["",""]
	},
	{
		word: "I'm successful",
		def: "ئەس سەرکەفتی مە",
		rel:["",""]
	},
	{
		word: "‏‏It was useful",
		def: "ئەو یاب مڤا بۆ",
		rel:["",""]
	},
	{
		word: "It's not mine",
		def: "ئەو نەیا منە",
		rel:["",""]
	},
	{
		word: "It's yours",
		def: "ئەو یا تەیە",
		rel:["",""]
	},
	{
		word: "It's theirs",
		def: "ئەو یا وانایە",
		rel:["",""]
	},
	{
		word: "It's ours",
		def: "ئەو یا مەیە",
		rel:["",""]
	},
	{
		word: "It's his",
		def: "ئەو یا ویە",
		rel:["",""]
	},
	{
		word: "It's hers",
		def: "ئەو یا وێ یە",
		rel:["",""]
	},
	{
		word: "I promise",
		def: "ئەس سۆزێ دەم",
		rel:["",""]
	},
	{
		word: "It's late",
		def: "درەنگە",
		rel:["",""]
	},
	{
		word: "It's early",
		def: "هێشتا زیە",
		rel:["",""]
	},
	{
		word: "Ifound you",
		def: "من توو دیتی",
		rel:["",""]
	},
	{
		word: "I feel ill",
		def: "هەست ب نساخیێ دکەم",
		rel:["",""]
	},
	{
		word: "Just Kidding‏",
		def: "بتنێ بۆ خوشی‏",
		rel:["","من یاری کرن"]
	},
	{
		word: "In my childhood",
		def: "دزارۆکینی یامن دا ",
		rel:["",""]
	},
	{
		word: "Just say No‏",
		def: "بتنێ بێژە نەخێر‏",
		rel:["",""]
	},
	{
		word: "Jeans‏",
		def: " کابوو‏",
		rel:["",""]
	},
	{
		word: "‏‏Keep it dark‏",
		def: "بلا نهینی بیت‏",
		rel:["","نهینی بپارێزە"]
	},
	{
		word: "Love u all‏",
		def: "حەش وە خرا کەم‏",
		rel:["",""]
	},
	{
		word: "Likewise‏",
		def: "ئەس ژیک ب هەمان شێوە‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏Loding",
		def: "چاڤەرێ",
		rel:["چاڤەرێ بە","چاڤەرێ بون"]
	},
	{
		word: "Let's try‏",
		def: "‏دا خوب جەربینن‏",
		rel:["","دا سەحکەینێ"]
	},
	{
		word: "‏Letter‏",
		def: "پیت‏",
		rel:["","حەرف "]
	},
	{
		word: "Long time no see‏",
		def: "من ژمێژە توو نەدیتیە‏",
		rel:["",""]
	},
	{
		word: "Life‏",
		def: "ژیان‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏Late",
		def: "درەنگ",
		rel:["","گیروبون"]
	},
	{
		word: "Much better‏",
		def: "گەلەك باشترم‏",
		rel:["",""]
	},
	{
		word: "May Allah be with You‏",
		def: "خۆدێ دگەل تەبیت‏",
		rel:["","تە رۆژامن خۆش کر"]
	},
	{
		word: "May Allah Reward You‏",
		def: "خۆدێ خێراتە بنڤێسیت‏",
		rel:["","تە رۆژامن خۆش کر"]
	},
	{
		word: "‏‏Moon",
		def: "هەیڤ ",
		rel:["",""]
	},
	{
		word: "‏‏Market‏",
		def: "‏‏‏‏‏فروشگەهـ",
		rel:["",""]
	},
	{
		word: "‏‏Minute",
		def: "خوڵەك",
		rel:["","خولەک"]
	},
	{
		word: "‏Money‏",
		def: "‏‏‏‏‏پارە",
		rel:["",""]
	},
	{
		word: "‏Message‏",
		def: "نامە‏",
		rel:["","ڕیسالە"]
	},
	{
		word: "Me too‏",
		def: "ئەس ژیک هەر وەسا‏",
		rel:["",""]
	},
	{
		word: "Man‏",
		def: "زەلام‏",
		rel:["",""]
	},
	{
		word: "Miles away‏",
		def: "هزرێت من نە ڤێرە بوون‏",
		rel:["",""]
	},
	{
		word: "‏‏My hands are full‏",
		def: "ئەس گەلەك بکارم مژیلم‏",
		rel:["","نەشێم چ کارێت دی بکەم"]
	},
	{
		word: "‏‏Meat‏",
		def: "گوشت‏",
		rel:["",""]
	},
	{
		word: "Not too bad‏",
		def: "باشە نەگەلەك خرابە‏",
		rel:["",""]
	},
	{
		word: "Nope‏",
		def: "نەخێر‏",
		rel:["",""]
	},
	{
		word: "No thanks‏",
		def: "نەخێر سۆپاس‏",
		rel:["",""]
	},
	{
		word: "No need to apologize‏",
		def: "پێتڤی ناکەت داخازا لێبورینێ بخازی‏",
		rel:["",""]
	},
	{
		word: "No problem",
		def: "نە ئاریشەیە",
		rel:["ئاریشە نینە"," نە ئاڕیشەیە‌"]
	},
	{
		word: "Never mind‏",
		def: "‏‏‏ نە گرنگە‏‏",
		rel:["",""]
	},
	{
		word: "Not at all",
		def: "خۆ تشتەك نینە",
		rel:["خوو تشتەك نینە"," خو تشتەك نینە‌"]
	},
	{
		word: "Nobody understand me‏",
		def: "کەس دمن ناگەهیت‏",
		rel:["",""]
	},
	{
		word: "Not too bad‏",
		def: "باشە نە خرابە‏",
		rel:["",""]
	},
	{
		word: "Not at all",
		def: "تشتەك نینە",
		rel:["","پێنەڤێت"]
	},
	{
		word: "Out of the question‏",
		def: "نەخێر چێنابیت‏",
		rel:["","هەما بسیار نەکە"]
	},
		{
		word: "Out of my mouth‏",
		def: "تەب دلێ من گوت‏",
		rel:["","You took the words right"]
	},
	{
		word: "Out of my hand‏",
		def: "نە بدەستێ منە‏",
		rel:["",""]
	},
	{
		word: "Open up to me‏",
		def: "دلێ خو بۆمن فەکە‏",
		rel:["","یا دلێ خۆ بومن بێژە"]
	},
	{
		word: "Old Friend‏",
		def: "هەڤالێ کەڤن‏",
		rel:["",""]
	},
	{
		word: "On the contrary",
		def: "بەڕۆڤاژی",
		rel:["بەروڤاژی"," بەرووڤاژی‌"]
	},
	{
		word: "Put Your Trust in Allah‏",
		def: "ب هیڤیا خۆدێ ڤە‏",
		rel:["","بێ هێلە هیڤیا خۆدێ ڤە"]
	},
	{
		word: "Please accept my apologies‏",
		def: "هیڤی دکەم داخازامن یا لێبورینێ قەبیل بکە‏",
		rel:["",""]
	},
	{
		word: "Please forgive me‏",
		def: "هیڤی دکەم لمن ببورە‏",
		rel:["",""]
	},
	{
		word: "Pull the other one, i don't think so‏",
		def: "ئەز وەسا هزر ناکەم‏",
		rel:["","هەرە بۆ ئیکێ خشیم بێژە"]
	},
	{
		word: "Please speak more slowly‏",
		def: "‏هیڤی دکەم هێدی تر باخفە‏",
		rel:["",""]
	},
	{
		word: "‏Photo‏",
		def: "وێنە‏",
		rel:["","ڕسم"]
	},
	{
		word: "Please‏",
		def: "هیڤی دکەم‏",
		rel:["",""]
	},
	{
		word: "Radio‏",
		def: "راديو‏",
		rel:["",""]
	},
	{
		word: "Say it again‏",
		def: "بێژە ڤە‏",
		rel:["",""]
	},
	{
		word: "Same Old‏",
		def: "وەکی خویە‏",
		rel:["","وەکی بەرێ یە"]
	},
	{
		word: "Shoes‏",
		def: " بێلاڤ‏",
		rel:["",""]
	},
	{
		word: "She has the right to Go‏",
		def: "وێ ماف یێ هەی کو بجیت‏",
		rel:["",""]
	},
	{
		word: "Shorts‏",
		def: " شۆرت‏",
		rel:["",""]
	},
	{
		word: "Same here‏",
		def: "ئەس ژیک‏",
		rel:["",""]
	},
	{
		word: "See you‏",
		def: "دێ تەبینم ڤە‏",
		rel:["",""]
	},
	{
		word: "See you soon‏",
		def: "ل نێزیک دێ تەبینم‏",
		rel:["",""]
	},
	{
		word: "See you later‏",
		def: "باشی دێ تەبینم‏",
		rel:["",""]
	},
	{
		word: "Socks‏",
		def: " گورە‏",
		rel:["",""]
	},
	{
		word: "Scissors‏",
		def: " مەقەس‏",
		rel:["",""]
	},
	{
		word: "Speed",
		def: "بلەز",
		rel:["ب لەز"," ‌"]
	},
	{
		word: "‏‏Sorry",
		def: "ببورە",
		rel:["","ببۆڕە"]
	},
	{
		word: "‏‏Seconds",
		def: "سانی",
		rel:["",""]
	},
	{
		word: "Say something",
		def: "تشەکی بێژە",
		rel:["تشتەکی بێژە"," ‌"]
	},
	{
		word: "Sleep",
		def: "نفستن",
		rel:["نفستن"," ‌"]
	},
	{
		word: "‏‏So what?‏",
		def: "ڤێچا جیە ؟‏",
		rel:["","بومن نە خەمە"]
	},
	{
		word: "Today",
		def: "ئەڤرۆکە ",
		rel:["",""]
	},
	{
		word: "Tonight",
		def: "ئەڤ شەڤە ",
		rel:["",""]
	},
	{
		word: "‏‏‏Tell me something",
		def: "گرنگی یێ پێنە دە",
		rel:["",""]
	},
	{
		word: "This is my new car‏",
		def: "ئەڤە ترومبێلامن یا نییە‏",
		rel:["",""]
	},
	{
		word: "That's clear, Thank you‏",
		def: "یا ڕونە سۆپاس بوتە‏",
		rel:["",""]
	},
	{
		word: "Take care‏",
		def: "چاڤێ تە لتەبیت‏",
		rel:["","تە هاش خۆ هەبیت"]
	},
	{
		word: "True Friend‏",
		def: "هەڤالێ وەڤادار‏",
		rel:["","هەڤالێ راستەقینە"]
	},
	{
		word: "Turn off the lights‏",
		def: "گلوپا بفەمرینە ‏",
		rel:["",""]
	},
	{
		word: "Time‏",
		def: "دەم",
		rel:["",""]
	},
	{
		word: "‏‏Talk‏",
		def: "ئاخڤتن‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏‏Tree",
		def: "دار",
		rel:["",""]
	},
		{
		word: "‏‏Tea‏",
		def: "چا‏",
		rel:["",""]
	},
	{
		word: "That's all i need‏",
		def: "ئەو ژمن کێم بوو‏",
		rel:["",""]
	},
	{
		word: "‏‏The electricity went out‏",
		def: "کەهرەب چوو‏",
		rel:["",""]
	},
	{
		word: "‏‏The power is back‏",
		def: "کەهرەب هات‏",
		rel:["",""]
	},
	{
		word: "Take it",
		def: "بگرە",
		rel:["",""]
	},
	{
		word: "Try again",
		def: "پێکولا بکەڤە",
		rel:["",""]
	},
	{
		word: "‏‏‏‏‏University",
		def: "زانكو",
		rel:["","زانكۆ"]
	},
	{
		word: "‏‏Update‏",
		def: "‏‏‏‏‏نویکرن ",
		rel:["","نیکرن"]
	},
	{
		word: "What's up?‏",
		def: "چ حالێ تەیە؟‏",
		rel:["",""]
	},
	{
		word: "What do you Need?‏",
		def: "توو پێتڤی بچی؟‏",
		rel:["",""]
	},
	{
		word: "What do you Know?‏",
		def: "توو چ دزانی؟‏",
		rel:["",""]
	},
	{
		word: "What do you think?‏",
		def: "توو چ هزر دکەی؟‏",
		rel:["",""]
	},
	{
		word: "What do you Make?‏",
		def: "توو چدکەی؟‏",
		rel:["",""]
	},
	{
		word: "What do you See?‏",
		def: "توو چ دبینی؟‏",
		rel:["",""]
	},
	{
		word: "What do you Mean?‏",
		def: "مەرەماتە چیە؟‏",
		rel:["",""]
	},
	{
		word: "What do you Work?‏",
		def: "تۆ چ کاردکەی؟‏",
		rel:["",""]
	},
	{
		word: "What do you Say?‏",
		def: "تۆ چدبێژی؟‏",
		rel:["",""]
	},
	{
		word: "What do you have ?‏",
		def: "تە چ هەیە؟‏",
		rel:["",""]
	},
	{
		word: "Who is that?‏",
		def: "ئەو کیە ؟‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏‏Water",
		def: "ئاڤ",
		rel:["",""]
	},
	{
		word: "‏‏Wound‏",
		def: "‏‏‏‏‏برین",
		rel:["",""]
	},
	{
		word: "‏Word‏",
		def: "پەیڤ‏",
		rel:["","وێشە "]
	},
	{
		word: "Woman‏",
		def: "ژن‏",
		rel:["","ئافرەت"]
	},
	{
		word: "We have the right to learn English‏",
		def: "مە ماف یێ هەی کو فێری ئینگلیزی بین‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏Wait",
		def: "خوو بگرە",
		rel:["","چاڤەرێ بە"]
	},
	{
		word: "Surely‏",
		def: " بەلێ بێگومان‏",
		rel:["",""]
	},
	{
		word: "You look good today‏",
		def: "توو ئەفرۆ باش دیار دکەی‏",
		rel:["",""]
	},
	{
		word: "Yup‏",
		def: "بەلێ‏",
		rel:["",""]
	},
	{
		word: "You deserve it‏",
		def: "توو ژهەژی‏",
		rel:["",""]
	},
	{
		word: "You made my day‏",
		def: "تە ئەس کەیڤ خۆش کرم‏",
		rel:["","تە رۆژامن خۆش کر"]
	},
	{
		word: "You don't say!‏",
		def: "توو بخۆدێ؟‏",
		rel:["","نەبابو نە ژدل؟"]
	},
	{
		word: "‏‏Years",
		def: "سال ",
		rel:["","ساڵ"]
	},
	{
		word: "You bent my ear‏",
		def: "تە گوهێت من برن‏",
		rel:["","تە مێشکێ من بر"]
	},
	{
		word: "‏‏You jinxed me‏",
		def: "تە ئەز چاڤین کرم‏",
		rel:[""," تە چاڤەك لمن دا "]
	},
	{
		word: "You have the right to know‏",
		def: "تە ماف یێ هەی کو بزانی‏",
		rel:["",""]
	},
	{
		word: "‏‏You haven't aged a day‏",
		def: "توو نەهاتیە گوهورین‏",
		rel:["","هێشتا وەکی خوی"]
	},
	{
		word: "ئاخڤتن‏",
		def: "‏talk‏",
		rel:["",""]
	},
	{
		word: "سێڤ",
		def: "Apple",
		rel:["Red Apple","Yellow Apple"]
	},
	{
		word: "سەر خاترا من ‏",
		def: "For my sake‏",
		rel:["",""]
	},
	{
		word: "بومن بینە",
		def: "Bring it to me",
		rel:[""," ‌"]
	},
	{
		word: "بخو نەکە خەم ‏",
		def: "Don't worry about it‏",
		rel:["",""]
	},
	{
		word: "خۆدێ دگەل تەبیت‏",
		def: "May Allah be with You‏",
		rel:["",""]
	},
	{
		word: "خۆدێ خێراتە بنڤێسیت‏",
		def: "May Allah Reward You‏",
		rel:["",""]
	},
	{
		word: "خۆدێ نەکەت‏",
		def: "God Forbid‏",
		rel:["",""]
	},
	{
		word: " خۆدێ حەسکەت‏",
		def: "God willing‏",
		rel:["",""]
	},
	{
		word: "خۆدێ عەفو بکەت‏",
		def: "God rest his soul‏",
		rel:["",""]
	},
	{
		word: "خۆدێ وێ عەفو بکەت‏",
		def: "God rest her soull‏",
		rel:["",""]
	},
	{
		word: "خۆ شرین نەکە‏",
		def: "Don't flatter yourself‏",
		rel:["",""]
	},
	{
		word: "سلاف‏",
		def: "Hello‏",
		rel:["",""]
	},
	{
		word: "سار",
		def: "Cool",
		rel:[""," ‌"]
	},
	{
		word: "سال‏",
		def: "Years ",
		rel:["","ساڵ"]
	},
	{
		word: "سەر خاترامن‏",
		def: "For my sake‏",
		rel:["",""]
	},
	{
		word: "بگوهرە",
		def: "Change",
		rel:[""," ‌"]
	},
	{
		word: "تێشت‏",
		def: "Breakfast‏",
		rel:["",""]
	},
	{
		word: "تە گوهێت من برن‏",
		def: "You bent my ear‏",
		rel:["",""]
	},
	{
		word: "تە ماف یێ هەی کو بزانی‏",
		def: "You have the right to know‏",
		rel:["",""]
	},
	{
		word: "ترومبێل",
		def: "Car",
		rel:["",""]
	},
	{
		word: "‏‏‏‏تشتەك نینە",
		def: "Not at all",
		rel:["",""]
	},
	{
		word: "‏‏‏‏تاریخ",
		def: "Date",
		rel:["",""]
	},
	{
		word: "‏‏‏‏درەنگ",
		def: "Late",
		rel:["",""]
	},
	{
		word: "داخازا لێبورینێ نەخازە‏",
		def: "Don't apologize‏",
		rel:["",""]
	},
	{
		word: "داخازا لێبورینێ دخازم‏",
		def: "I apologize‏",
		rel:["",""]
	},
	{
		word: "دگەل بوچونا تەمە‏",
		def: "I agree‏",
		rel:["",""]
	},
	{
		word: "دووبارە ئاخڤتنا خۆ بێژە ڤە‏",
		def: "Come again?‏",
		rel:["",""]
	},
	{
		word: "دووبارە بێخوش بوم بدیتناتە‏",
		def: "It's nice to see you again‏",
		rel:["",""]
	},
	{
		word: "دڵ‏",
		def: "‏Heart",
		rel:["",""]
	},
	{
		word: "دلێ من دمینیتە بتەڤە‏",
		def: "I pity you‏",
		rel:["",""]
	},
	{
		word: "دەرگەهـ‏",
		def: "‏‏‏‏‏Door",
		rel:["",""]
	},
	{
		word: "درەوا نەکە",
		def: "Don’t lie",
		rel:["","  ‌"]
	},
	{
		word: "‏دا گرتن ‏",
		def: "Download‏",
		rel:["",""]
	},
	{
		word: "دەمژمێر‏",
		def: "Clock",
		rel:["",""]
	},
	{
		word: "‏دێ شێی دووبارە کەی؟‏",
		def: "Can you repeat that please?‏",
		rel:["",""]
	},
	{
		word: "دزانم مەرەماتە جیە تێ گەهشتم‏",
		def: "I know what do you mean‏",
		rel:["",""]
	},
	{
		word: "نفستن",
		def: "Sleep",
		rel:["Sleep"," ‌"]
	},
	{
		word: "‏‏‏‏نەفرەت بیت",
		def: "‏Damn",
		rel:["",""]
	},
	{
		word: "نەیا گرنگە‏",
		def: "It's Not important‏",
		rel:["",""]
	},
	{
		word: "نە گرنگە‏",
		def: "Never mind‏",
		rel:["",""]
	},
	{
		word: "نوکە تێ گەهشتم ‏",
		def: "I Get it Now‏",
		rel:["",""]
	},
	{
		word: "نەخێر‏",
		def: "Nope‏",
		rel:["",""]
	},
	{
		word: "نەخێر سۆپاس‏",
		def: "No thanks‏",
		rel:["",""]
	},
	{
		word: "نەخێر چێنابیت‏",
		def: "Out of the question‏",
		rel:["",""]
	},
	{
		word: "نە بدەستێ منە‏",
		def: "Out of my hand‏",
		rel:["",""]
	},
	{
		word: "نەشێم ئێدی تەحەملێ بکەم‏",
		def: "I can't take it anymore‏",
		rel:["",""]
	},
	{
		word: "نە گەلەك باشم‏",
		def: "‏‏‏‏‏‏‏‏I'm not very well",
		rel:["",""]
	},
	{
		word: "نامە‏",
		def: "Message‏",
		rel:["",""]
	},
	{
		word: "نە ئاریشەیە",
		def: "No problem",
		rel:[""," ‌"]
	},
	{
		word: "نویکرن‏",
		def: "‏‏‏‏‏‏‏Update",
		rel:["",""]
	},
	{
		word: "نیڤەك‏",
		def: "Half",
		rel:["",""]
	},
	{
		word: "نزانم بەلکی‏",
		def: "‏I Dunno maybe‏",
		rel:["",""]
	},
	{
		word: "نەفرەتێت خۆدێ لتەبن‏",
		def: "God damn you‏",
		rel:["",""]
	},
	{
		word: "نە بێژە ج کەسا‏",
		def: "‏‏Don't tell anyone‏",
		rel:["",""]
	},
	{
		word: "توو ئەفرۆ باش دیار دکەی‏",
		def: "You look good today‏",
		rel:["",""]
	},
	{
		word: "توو ژهەژی‏",
		def: "You deserve it‏",
		rel:["",""]
	},
	{
		word: "توو بێ بوهای لدەڤ من‏",
		def: "I have no use for you‏‏‏",
		rel:["",""]
	},
	{
		word: "توو ئەڤرۆکە چاوانی؟‏",
		def: "How are you feeling today?‏",
		rel:["",""]
	},
	{
		word: "توو پێتڤی بچی؟‏",
		def: "What do you Need?‏",
		rel:["",""]
	},
	{
		word: "توو چ دزانی؟‏",
		def: "What do you Know?‏",
		rel:["",""]
	},
	{
		word: "توو چ هزر دکەی؟‏",
		def: "What do you think?‏",
		rel:["",""]
	},
	{
		word: "توو چدکەی؟‏",
		def: "What do you Make?‏",
		rel:["",""]
	},
	{
		word: "توو چ دبینی؟‏",
		def: "What do you See?‏",
		rel:["",""]
	},
	{
		word: "تۆ چ کاردکەی؟‏",
		def: "What do you Work?‏",
		rel:["",""]
	},
	{
		word: "تۆ چدبێژی؟‏",
		def: "What do you Say?‏",
		rel:["",""]
	},
	{
		word: "توو بخۆدێ‏",
		def: "You don't say!‏",
		rel:["",""]
	},
	{
		word: "توو نەهاتیە گوهورین‏",
		def: "‏‏You haven't aged a day‏",
		rel:["",""]
	},
	{
		word: "توو ژهەژی‏",
		def: "Don't care‏",
		rel:["",""]
	},
	{
		word: "تە ئەس کەیڤ خۆش کرم‏",
		def: "You made my day‏",
		rel:["",""]
	},
	{
		word: "تەب دلێ من گوت‏",
		def: "Out of my mouth‏",
		rel:["",""]
	},
	{
		word: "تە چ هەیە؟‏",
		def: "What do you have ?‏",
		rel:["",""]
	},
	{
		word: "تە دڤێت؟‏",
		def: "Do you want?‏",
		rel:["",""]
	},
	{
		word: "‏تێناگەهم تۆ جت بێژی‏",
		def: "Cant comprehend what you say‏",
		rel:["",""]
	},
	{
		word: "تێ گەهشتم‏",
		def: "Got it‏",
		rel:["",""]
	},
	{
		word: "تشتەکی بخو",
		def: "Eat something",
		rel:["","  ‌"]
	},
	{
		word: "‏‏‏‏ئەس چ سەر خۆ ناهێلم",
		def: "‏‏I will do my best",
		rel:["",""]
	},
	{
		word: "ئەس برسیمە‏",
		def: "I,m hungry‏",
		rel:["",""]
	},
	{
		word: "ئەس زێدەتر نەشێم‏",
		def: "I can't anymore‏",
		rel:["",""]
	},
	{
		word: "ئەس باشم‏",
		def: "I'm Ok‏",
		rel:["",""]
	},
	{
		word: "ئەس باشم‏",
		def: "I'm well ‏",
		rel:["",""]
	},
	{
		word: "ئەس رازیمە‏",
		def: "‏‏Agreed‏",
		rel:["",""]
	},
	{
		word: "ئەس گەلەك باشم سۆپاس‏",
		def: "I'm great, thanks‏",
		rel:["",""]
	},
	{
		word: "ئەس نزانم چاوا سۆپاسیاتە بکەم‏",
		def: "I can't thank you enough‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەس سۆپاس دارم",
		def: "‏‏I'm thankful",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەس تێناگەهم",
		def: "‏‏I don't understand",
		rel:["",""]
	},
	{
		word: "ئەس تێناگەهم",
		def: "I don’t get it",
		rel:[""," ‌"]
	},
	{
		word: "ئەس بکەیڤا خومە‏",
		def: "It's up to me‏",
		rel:["",""]
	},
	{
		word: "ئەس نەشێم بێژم‏",
		def: "I can not say‏",
		rel:["",""]
	},
	{
		word: "ئەس گەلەك بێزارم‏",
		def: "I feel depressed‏",
		rel:["",""]
	},
	{
		word: "ئەس دوو دلم‏",
		def: "I'm Torn‏",
		rel:["",""]
	},
	{
		word: "ئەس حەشتەکەم‏",
		def: "I love you‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەس حەش وی دکەم ",
		def: "I like him",
		rel:["",""]
	},
	{
		word: "ئەس تە دگەهم‏",
		def: "I feel you‏",
		rel:["","I understand you"]
	},
	{
		word: "ئەس تێدگەهم‏",
		def: "i see‏",
		rel:["","I understand"]
	},
	{
		word: "ئەس وی باش دنیاسم‏",
		def: "I know him Well‏",
		rel:["",""]
	  },
	  {
		word: " ئەس دخزمەت دامە‏",
		def: "I'm at your service‏",
		rel:["",""]
	},
	{
		word: "ئەس تورە مە",
		def: "I'm mad",
		rel:[""," ‌"]
	},
	{
		word: "ئەس رازیمە‏",
		def: "I'm agree‏",
		rel:["",""]
	},
	{
		word: "ئەس گەلەک هەست بخەمگینی یێ کەم ‏",
		def: "I'm feeling down‏",
		rel:["",""]
	},
	{
		word: "ئەس هێشتا حەشتەکەم‏",
		def: "I still love you‏",
		rel:["",""]
	},
	{
		word: "ئەگەر ئەس خەلەت نەبم‏",
		def: "If I'm not mistaken‏",
		rel:["",""]
	},
	{
		word: "ئەس گەلەك مرتاحم‏",
		def: "I'm so relieved‏",
		rel:["",""]
	},
	{
		word: "ئەس گەلەك باشم‏",
		def: "‏‏‏‏‏‏‏I'm very well",
		rel:["",""]
	},
	{
		word: "ئەس تێهنی مە",
		def: "Im thirsty",
		rel:[""," ‌"]
	},
	{
		word: "ئەس باشم‏",
		def: "‏‏‏‏‏‏‏‏I'm well",
		rel:["",""]
	},
	{
		word: "ئەس باشتر بابم‏",
		def: "I couldn't be better‏",
		rel:["",""]
	},
	{
		word: "ئەس مەمنونم",
		def: "I'm thankful",
		rel:[""," ‌"]
	},
	{
		word: "ئەس تێرم",
		def: "I'm full",
		rel:[""," ‌"]
	},
	{
		word: "ئەس ژیک‏",
		def: "Same here‏",
		rel:["",""]
	},
	{
		word: "ئەس ژیک هەر وەسا‏",
		def: "Me too‏",
		rel:["","So am i"]
	},
	{
		word: "ئەس ژیک ب هەمان شێوە‏",
		def: "Likewise‏",
		rel:["",""]
	},
	{
		word: "ئەس وەسا هزر ناکەم‏",
		def: "Pull the other one, i don't think so‏",
		rel:["",""]
	},
	{
		word: "ئەس نە بشت ڕاستم‏",
		def: "I'm unsure‏",
		rel:["",""]
	},
	{
		word: "ئەس دێ چم‏",
		def: "I will Go‏",
		rel:["",""]
	},
	{
		word: "ئەس گەلەك گەلەك کەیف خوشم‏",
		def: "I'm on cloud nine‏",
		rel:["",""]
	},
	{
		word: "ئەس زێدە زێدە کەیف خوشم‏",
		def: "I'm over the moon‏",
		rel:["",""]
	},
	{
		word: "ئەس گەلەك ماندی مە‏",
		def: "‏‏I'm on my last legs‏",
		rel:["",""]
	},
	{
		word: "ئەس گەلەك بشولم‏",
		def: "‏‏I'm tied up‏",
		rel:["",""]
	},
	{
		word: "ئەس ژتە باوەرکەم‏",
		def: "I believe you‏",
		rel:["",""]
	},
	{
		word: "ئەس گەلەك بکارم مژیلم‏",
		def: "‏‏My hands are full‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەس سەرکەفتی مە",
		def: "‏‏I'm successful",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەس سۆزێ دەم",
		def: "‏‏I promise",
		rel:["",""]
	},
	{
		word: "ئەڤە ترومبیلامن یا نیە‏",
		def: "This is my new car‏",
		rel:["",""]
	},
	{
		word: "ماندی مە ‏",
		def: "‏‏‏‏‏‏I'm tired",
		rel:["",""]
	},
	{
		word: "گەلەك خرابم‏",
		def: "‏‏‏‏‏‏I'm terrible",
		rel:["",""]
	},
	{
		word: "بتنێ بێژە نەخێر‏",
		def: "Just say No‏",
		rel:["",""]
	},
	{
		word: "بومن نە گرنگە",
		def: "I don’t care",
		rel:[""," ‌"]
	},
	{
		word: "باشترین ژن دجیهانێ دا دەیکامنە‏",
		def: "Best woman in the world is My Mom.‏",
		rel:["",""]
	},
	{
		word: "بەلێ بێگومان‏",
		def: "Surely‏",
		rel:["",""]
	},
	{
		word: "ب هیڤیا خۆدێ ڤە‏",
		def: "May Allah be with You‏",
		rel:["",""]
	},
	{
		word: "بێهن فرەهـ بە‏",
		def: "Be patience‏",
		rel:["",""]
	},
	 {
		word: "باشە نە گەلەك خرابە‏",
		def: "Not too bad‏",
		rel:["",""]
	},
	{
		word: "پێتڤی ناکەت داخازا لێبورینێ بخازی‏",
		def: "No need to apologize‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏پێتڤیە ئەس بچم",
		def: "‏‏I have to go",
		rel:["",""]
	},
	{
		word: "‏‏‏‏پیرۆزبیت",
		def: "Congratulbations",
		rel:["",""]
	},
	{
		word: "‏‏‏‏پێکولا بکەڤە",
		def: "‏‏Try again",
		rel:["",""]
	},
	{
		word: "🦶🏻پێ‏",
		def: "‏‏‏Foot",
		rel:["",""]
	},
	{
		word: "ب سلامەتم‏",
		def: "I'm alright‏",
		rel:["",""]
	},
	{
		word: "ب خرابى بەحسێ کەسێ نەکە‏",
		def: "Don't speak ill of anyone‏",
		rel:["",""]
	},
	{
		word: "بێ کێماسی‏",
		def: "Flawless‏",
		rel:["",""]
	},
	{
		word: "بێژە ڤە‏",
		def: "Say it again‏",
		rel:["",""]
	},
	{
		word: "باشە نە خرابە‏",
		def: "Not too bad‏",
		rel:["",""]
	},
	{
		word: "باوەریامن بتە دهێت‏",
		def: "I trust you‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏بدە من",
		def: "‏‏Give me",
		rel:["",""]
	},
	{
		word: "‏‏‏‏بگرە",
		def: "‏‏Take it",
		rel:["",""]
	},
	{
		word: "پەیڤ‏",
		def: "Word‏",
		rel:["",""]
	},
	{
		word: "پێتڤی ناکەت‏",
		def: "‏‏It was nothing‏",
		rel:["",""]
	},
	{
		word: "پێتڤی سۆپاسی ناکەت‏",
		def: "‏‏Don't mention it‏",
		rel:["",""]
	},
	{
		word: "سپێدە باش‏",
		def: "Good morning‏",
		rel:["",""]
	},
	{
		word: "ببورە ئاخڤتنا خۆ دووبارە بکە‏",
		def: "Excuse me ?‏",
		rel:["",""]
	},
	{
		word: "بەلێ‏",
		def: "Yup‏",
		rel:["",""]
	},
	{
		word: "باقژی‏",
		def: "‏‏‏‏‏‏‏Cleaner",
		rel:["",""]
	},
	{
		word: "بیجەك ئینگلیزی دزانم‏",
		def: "‏I only speakvery little English‏‏",
		rel:["",""]
	},
	{
		word: "پەڕتووک‏",
		def: "‏‏‏‏Book",
		rel:["",""]
	},
	{
		word: "برچ‏",
		def: "‏‏‏‏Hair",
		rel:["",""]
	},
	{
		word: "بلا نهینی بیت‏",
		def: "‏‏Keep it dark‏",
		rel:["",""]
	},
	{
		word: "باشە نە گەلەك خرابە‏",
		def: "Not too bad‏",
		rel:["",""]
	},
	{
		word: "کامیرە‏",
		def: "Camera ‏",
		rel:["",""]
	},
	{
		word: "کابوو‏",
		def: "Jeans‏",
		rel:["",""]
	},
	{
		word: "کەهرەب چوو‏",
		def: "‏‏The electricity went out‏",
		rel:["",""]
	},
	{
		word: "کەهرەب هات‏",
		def: "‏‏The power is back‏",
		rel:["",""]
	},
	{
		word: "کەس دمن ناگەهیت‏",
		def: "Nobody understand me‏",
		rel:["",""]
	},
	{
		word: "کەربێت من ژتە ڤەبن‏",
		def: "‏‏| detest you‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏گرنگی یێ پێنە دە",
		def: "Tell me something",
		rel:["",""]
	},
	{
		word: "گەلەك باشترم‏",
		def: "Much better‏",
		rel:["",""]
	},
	{
		word: "گشتی‏",
		def: "General‏",
		rel:["",""]
	},
		{
		word: "گرنگی‏",
		def: "‏Importance‏",
		rel:["",""]
	},
	{
		word: "گەلەك بشولم‏",
		def: "‏‏‏‏‏‏I'm very busy",
		rel:["",""]
	},
	{
		word: "گلوپا بفەمرینە‏",
		def: "Turn off the lights‏",
		rel:["",""]
	},
	{
		word: "گەلەك ئینگلیزی نزانم‏",
		def: "‏‏‏I don't speak very little English‏‏",
		rel:["",""]
	},
	{
		word: "گورە‏",
		def: "Socks‏",
		rel:["",""]
	},
	{
		word: "گوشت‏",
		def: "‏‏Meat‏",
		rel:["",""]
	},
	{
		word: "بێلاڤ‏",
		def: "Shoes‏",
		rel:["",""]
	},
	{
		word: "برین‏",
		def: "‏‏‏‏‏‏‏Wound",
		rel:["",""]
	},
	{
		word: "باشی دێ تەبینم‏",
		def: "See you later‏",
		rel:["",""]
	},
	{
		word: "پیت‏",
		def: "Letter‏",
		rel:["",""]
	},
	{
		word: "بێخۆشم کو هاریکاربم ‏",
		def: "I'm happy to help ‏",
		rel:["",""]
	},
	{
		word: "باژێر‏",
		def: "‏‏‏‏‏City",
		rel:["",""]
	},
	{
		word: "بکەیڤا خوی‏",
		def: "Have it your way‏",
		rel:["",""]
	},
	{	word: "پارە‏",
		def: "‏‏‏‏‏‏Money",
		rel:["",""]
	},
	{
		word: "هیڤی دکەم داخازامن یا لێبورینێ قەبیل بکە‏",
		def: "Please accept my apologies‏",
		rel:["",""]
	},
	{
		word: "هزرێت من نە ڤێرە بوون‏",
		def: "Miles away‏",
		rel:["",""]
	},
	{
		word: "هیڤی دکەم لمن ببورە‏",
		def: "Please forgive me‏",
		rel:["",""]
	},
	{
		word: "هەمی کەیف خۆشن‏",
		def: "Everyone is happy‏",
		rel:["",""]
	},
	{
		word: "هەمی دەما",
		def: "Always",
		rel:[""," ‌"]
	},
	{
		word: "هەیڤ‏",
		def: "Moon ",
		rel:["",""]
	},
	{
		word: "هەست پێدکەم",
		def: "I fell it",
		rel:[""," ‌"]
	},
	{
		word: "هەڤالێ وەڤادار‏",
		def: "True Friend‏",
		rel:["",""]
	},
	{
		word: "هەڤالێ رح ب رح‏",
		def: "Bosom Friend‏",
		rel:["",""]
	},
	{
		word: "هەڤالێ خراب‏",
		def: "False Friend‏",
		rel:["",""]
	},
	{
		word: "هەڤالێ مەسلەحچی‏",
		def: "Fair- Weather Friend‏",
		rel:["",""]
	},
	{
		word: "هیڤی دکەم‏",
		def: "Please‏",
		rel:["",""]
	},
	{
		word: "‏هیڤی دکەم هێدی تر باخفە ‏",
		def: "Please speak more slowly‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏هەر چەندە",
		def: "‏Although",
		rel:["",""]
	},
	{
		word: "‏‏‏‏هێشتا زیە",
		def: "‏It's early",
		rel:["",""]
	},
	{
		word: "‏‏‏‏هەست ب نساخیێ دکەم",
		def: "‏I feel ill",
		rel:["",""]
	},
	{
		word: "یاب مڤا بو",
		def: "It was useful",
		rel:[""," ‌"]
	},
	{
		word: "یا ڕونە سۆپاس بوتە‏",
		def: "That's clear, Thank you‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەڤرۆکە ",
		def: "Today",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەڤ شەڤە ",
		def: "Tonight",
		rel:["",""]
	},
	{
		word: "ئەو کیە ؟‏",
		def: "Who is that?‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەو تە دنیاسیت",
		def: "Does he know you?",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەو بابێ منە ",
		def: "He was my father",
		rel:["",""]
	},
	{
		word: "ئەو برایێ منە‏",
		def: "He is my brother‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەو یاب مڤا بۆ",
		def: "‏‏It was useful",
		rel:["",""]
	},
	{
		word: "ئەو ژمن کێم بوو‏",
		def: "That's all i need‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەو یا تەیە",
		def: "‏‏It's yours",
		rel:["",""]
	},
	{
		word: "ئەو نەیا منە",
		def: "Its not mine",
		rel:[""," ‌"]
	},
	{
		word: "‏‏‏‏ئەو یا وانایە",
		def: "‏‏It's theirs",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەو یا مەیە",
		def: "‏‏It's ours",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەو یا ویە",
		def: "‏‏It's his",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ئەو یا وێ یە",
		def: "‏‏It's hers",
		rel:["",""]
	},
	{
		word: "‏‏‏‏دزارۆکینی یامن دا ",
		def: "In my childhood",
		rel:["",""]
	},
	{
		word: "دێ تەبینم ڤە‏",
		def: "See you‏",
		rel:["",""]
	},
	{
		word: "دلێ خۆ بومن فەکە‏",
		def: "Open up to me‏",
		rel:["",""]
	},
	{
		word: "دەست‏",
		def: "‏‏Hand",
		rel:["",""]
	},
	{
		word: "‏‏دەم",
		def: "Time",
		rel:["",""]
	},
	{
		word: "دێ شێی بێژی یە ڤە‏",
		def: "Can you say that again?‏",
		rel:["",""]
	},
	{
		word: "دار‏",
		def: "‏‏‏‏‏Tree",
		rel:["",""]
	},
	{
		word: "‏دا خوب جەربینن ‏",
		def: "Let's try‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏درەنگە",
		def: "‏It's late",
		rel:["",""]
	},
	{
		word: "ڕێجیم‏",
		def: "‏‏‏‏‏‏‏Diet",
		rel:["",""]
	},
	{
		word: "زەلام‏",
		def: "Man‏",
		rel:["",""]
	},
	{
		word: "ژن‏",
		def: "Woman‏",
		rel:["",""]
	},
	{
		word: "ژیان‏",
		def: "Life‏",
		rel:["",""]
	},
	{
		word: "ژبیرکە چنینە‏",
		def: "Forget about it‏",
		rel:["",""]
	},
	{
		word: "دورا تەیە",
		def: "It’s your turn",
		rel:[""," ‌"]
	},
	{
		word: "بەروڤاژی",
		def: "On the contrary",
		rel:[""," ‌"]
	},
	{
		word: "چنینە ‏",
		def: "‏‏‏‏‏‏It's ok",
		rel:["",""]
	},
	{
		word: "ئینگلیزی نزانم ‏",
		def: "‏‏‏‏‏‏I don't speak English",
		rel:["",""]
	},
	{
		word: "لمن ببورە‏",
		def: "I'm sorry",
		rel:["",""]
	},
	{
		word: "بخاتراتە‏",
		def: "Googbye",
		rel:["",""]
	},
	{
		word: "بخێربمینی‏",
		def: "Farewell‏",
		rel:["",""]
	},
	{
		word: "ببورە‏",
		def: "Sorry",
		rel:["",""]
	},
	{
		word: "بێخوش بوم  بنیاسیناتە ‏",
		def: "It's nice to meet you‏",
		rel:["",""]
	},
	{
		word: "فروشگەهـ‏",
		def: "‏‏‏‏‏‏‏Market",
		rel:["",""]
	},
	{
		word: "مەندە هوش بوم بدیتناتە لڤێرە‏",
		def: "I'm surprised to see you here‏",
		rel:["",""]
	},
	{
		word: "مەرەماتە چیە؟‏",
		def: "What do you Mean?‏",
		rel:["",""]
	},
	{
		word: "من ژمێژە توو نەدیتیە‏",
		def: "Long time no see‏",
		rel:["",""]
	},
	{
		word: "من بێ بوها نەکە‏",
		def: "Don't break my spirit‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏من دڤێت بچم",
		def: "‏‏I want to go",
		rel:["",""]
	},
	{
		word: "‏‏‏‏من دڤێت بمینم",
		def: "‏‏I Want to stay",
		rel:["",""]
	},
	{
		word: "مەقەس ‏",
		def: "Scissors‏",
		rel:["",""]
	},
	{
		word: "من نە راوستینە‏",
		def: "Don't interrupt me‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏من توو دیتی",
		def: "‏Ifound you",
		rel:["",""]
	},
	{
		word: "مە ماف یێ هەی کو فێری ئینگلیزی بین‏",
		def: "We have the right to learn English‏",
		rel:["",""]
	},
	{
		word: "موز‏",
		def: "Banana",
		rel:["",""]
	},
	{
		word: "ماسی‏",
		def: "Fish‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ما دەم",
		def: "‏As long as",
		rel:["",""]
	},
	{
		word: "‏‏‏‏حەتا حەتایێ",
		def: "Forever",
		rel:["",""]
	},
	{
		word: "حەش وە خرا کەم‏",
		def: "Love u all‏",
		rel:["",""]
	},
	{
		word: "خولەك‏",
		def: "Minute",
		rel:["",""]
	},
	{
		word: "‏‏‏‏خوو بگرە",
		def: "Wait",
		rel:["",""]
	},
	{
		word: "چا‏",
		def: "‏‏Tea‏",
		rel:["",""]
	},
	{
		word: "چ پێنەڤێت‏",
		def: "‏‏By all means‏",
		rel:["",""]
	},
	{
		word: "ڤێجا جیە‏",
		def: "‏So what‏",
		rel:["",""]
	},
	{
		word: "جارێ بخاترا تە‏",
		def: "Bye for now‏",
		rel:["",""]
	},
	{
		word: "چاڤێ تە لتەبیت‏",
		def: "Take care‏",
		rel:["",""]
	},
	{
		word: "چاڤ‏",
		def: "‏Eye",
		rel:["",""]
	},
	{
		word: "چاڤەرێ‏",
		def: "‏‏‏‏Loding",
		rel:["",""]
	},
	{
		word: "چەند سۆپاسی یا ته بکەم هەر کێمه‏",
		def: "I can't thank you enough‏",
		rel:["",""]
	},
	{
		word: "سانی‏",
		def: "Seconds",
		rel:["",""]
	},
	{
		word: "چ حالێ تەیە؟‏",
		def: "What's up?‏",
		rel:["",""]
	},
	{
		word: "چ پێنەفێت‏",
		def: "Absolutely‏",
		rel:["",""]
	},
	{
		word: "چ جێبیت بلا جێبیت‏",
		def: "Come what may‏",
		rel:["",""]
	},
	{
		word: "تە ئەز چاڤین کرم‏",
		def: "‏You jinxed me‏",
		rel:["",""]
	},
	{
		word: "خو تشتەك نینە",
		def: "Not at all",
		rel:[""," ‌"]
	},
	{
		word: "راديو‏",
		def: "Radio‏",
		rel:["",""]
	},
	{
		word: "رەنگ‏",
		def: "‏Color‏",
		rel:["",""]
	},
	{
		word: "روژ‏",
		def: "Days",
		rel:["","ڕۆژ"]
	},
	{
		word: "زانکو‏",
		def: "‏‏‏‏‏University ",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ژبەر تە",
		def: "For you",
		rel:["",""]
	},
	{
		word: "‏‏‏‏ژبەری",
		def: "Before",
		rel:["",""]
	},
	{
		word: "بتنێ بۆ خوشی‏",
		def: "Just Kidding‏",
		rel:["",""]
	},
	{
		word: "بلەز",
		def: "Speed",
		rel:[""," ‌"]
	},
	{
		word: "بەر چاڤك ‏",
		def: "Glasses‏",
		rel:["",""]
	},
	{
		word: "تشتەکی بێژە",
		def: "Say something",
		rel:[""," ‌"]
	},
	{
		word: "وێنە‏",
		def: "Photo‏",
		rel:["",""]
	},
	{
		word: "ل نێزیک دێ تەبینم‏",
		def: "See you soon‏",
		rel:["",""]
	},
	{
		word: "وەکی خویە‏",
		def: "Same Old‏",
		rel:["",""]
	},
	{
		word: "وژدان‏",
		def: "Conscience‏",
		rel:["",""]
	},
	{
		word: "زێدە من کەرب ژتە ڤەبن‏",
		def: "I loathe you‏",
		rel:["",""]
	},
	{
		word: "‏‏‏‏وێ باشی یێ بکە",
		def: "‏Do it later",
		rel:["",""]
	},
	{
		word: "وێ ماف یێ هەی کو بجیت‏",
		def: "She has the right to Go‏",
		rel:["",""]
	},
];



init = function () {
	for (let i = 0; i < dictionary.length; i++) {
		const element = dictionary[i];
		document.getElementById('word_list').innerHTML += "<li onclick='show(" + i + ")'>" + dictionary[i].word + "</li>"		
	}	
}

init();

show = function (i) {
	document.getElementById('word_text').innerHTML = dictionary[i].word;
	document.getElementById('definition').innerHTML = dictionary[i].def;

	var list = "";
	for (let j = 0; j < dictionary[i].rel.length; j++) {
		list += "<li>" + dictionary[i].rel[j] + "</li>";
		document.getElementById('related').innerHTML = list
		
	}
}
show(0);

search = function () {
	query = document.getElementById('search').value;
	if(query == "search"){
		return;
	}		

found = -1;
for (let i = 0; i < dictionary.length; i++) {
	if(query == dictionary[i].word){
		found = i;
		console.log(found = i);
		break;
	}else{
		document.getElementById('word_text').innerHTML = "Word not found";
		document.getElementById('definition').innerHTML = "Definition not found";
		document.getElementById('related').innerHTML = "Related not found";
	}
}
	if(found >= 0){
		show(found);
	}
}


</script>
