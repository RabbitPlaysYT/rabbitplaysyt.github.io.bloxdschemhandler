<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Emoji Copy & Paste 😎</title>
  <style>
    body {
      font-family: 'Segoe UI Emoji', sans-serif;
      background: linear-gradient(135deg, #ffafbd, #ffc3a0);
      margin: 0;
      padding: 0;
      text-align: center;
      color: #222;
    }
    header {
      background-color: rgba(255, 255, 255, 0.6);
      padding: 20px 0;
      backdrop-filter: blur(6px);
    }
    h1 {
      font-size: 2em;
      margin: 0;
    }
    .search-container {
      margin: 20px auto;
      width: 80%;
      max-width: 500px;
    }
    #searchInput {
      width: 100%;
      padding: 12px;
      font-size: 16px;
      border: 2px solid rgba(255,255,255,0.5);
      border-radius: 25px;
      background: rgba(255,255,255,0.8);
      backdrop-filter: blur(6px);
      outline: none;
      font-family: inherit;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    #searchInput:focus {
      border-color: #ff6b9d;
      background: white;
    }
    .category {
      background: rgba(255, 255, 255, 0.7);
      margin: 20px auto;
      padding: 15px;
      width: 80%;
      border-radius: 10px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    .category h2 {
      margin-bottom: 10px;
      color: #444;
    }
    .emoji {
      display: inline-block;
      font-size: 2em;
      margin: 10px;
      cursor: pointer;
      transition: transform 0.1s ease;
    }
    .emoji:hover {
      transform: scale(1.2);
    }
    .emoji.hidden {
      display: none;
    }
    #copyNotification {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      background: linear-gradient(135deg, #4facfe, #00f2fe);
      color: white;
      padding: 15px 25px;
      border-radius: 25px;
      font-size: 16px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.3);
      opacity: 0;
      transition: all 0.3s ease;
      z-index: 1000;
      backdrop-filter: blur(10px);
    }
    #copyNotification.show {
      opacity: 1;
      transform: translateX(-50%) translateY(-10px);
    }
    footer {
      margin: 30px 0;
      font-size: 0.9em;
      color: #555;
    }
  </style>
</head>
<body>

  <header>
    <h1>Emoji Copy & Paste 😍</h1>
    <p>Click an emoji to copy it!</p>
  </header>

  <div class="search-container">
    <input type="text" id="searchInput" placeholder="Search emojis...(only about 79% of emojis are here in this..)">
  </div>

  <div class="category">
    <h2>🐾 Animals</h2>
    <div class="emoji" data-keywords="dog puppy pet animal" onclick="copyEmoji('🐶')">🐶</div>
    <div class="emoji" data-keywords="cat kitten pet animal" onclick="copyEmoji('🐱')">🐱</div>
    <div class="emoji" data-keywords="mouse rodent animal" onclick="copyEmoji('🐭')">🐭</div>
    <div class="emoji" data-keywords="hamster pet animal" onclick="copyEmoji('🐹')">🐹</div>
    <div class="emoji" data-keywords="rabbit bunny animal" onclick="copyEmoji('🐰')">🐰</div>
    <div class="emoji" data-keywords="fox animal wild" onclick="copyEmoji('🦊')">🦊</div>
    <div class="emoji" data-keywords="bear animal wild" onclick="copyEmoji('🐻')">🐻</div>
    <div class="emoji" data-keywords="panda bear animal" onclick="copyEmoji('🐼')">🐼</div>
    <div class="emoji" data-keywords="koala animal australia" onclick="copyEmoji('🐨')">🐨</div>
    <div class="emoji" data-keywords="tiger animal wild" onclick="copyEmoji('🐯')">🐯</div>
    <div class="emoji" data-keywords="lion animal wild king" onclick="copyEmoji('🦁')">🦁</div>
    <div class="emoji" data-keywords="cow animal farm" onclick="copyEmoji('🐮')">🐮</div>
    <div class="emoji" data-keywords="pig animal farm" onclick="copyEmoji('🐷')">🐷</div>
    <div class="emoji" data-keywords="pig nose animal" onclick="copyEmoji('🐽')">🐽</div>
    <div class="emoji" data-keywords="frog animal amphibian" onclick="copyEmoji('🐸')">🐸</div>
    <div class="emoji" data-keywords="monkey animal" onclick="copyEmoji('🐵')">🐵</div>
    <div class="emoji" data-keywords="monkey see no evil" onclick="copyEmoji('🙈')">🙈</div>
    <div class="emoji" data-keywords="monkey hear no evil" onclick="copyEmoji('🙉')">🙉</div>
    <div class="emoji" data-keywords="monkey speak no evil" onclick="copyEmoji('🙊')">🙊</div>
    <div class="emoji" data-keywords="monkey animal" onclick="copyEmoji('🐒')">🐒</div>
    <div class="emoji" data-keywords="chicken animal farm" onclick="copyEmoji('🐔')">🐔</div>
    <div class="emoji" data-keywords="penguin animal bird" onclick="copyEmoji('🐧')">🐧</div>
    <div class="emoji" data-keywords="bird animal" onclick="copyEmoji('🐦')">🐦</div>
    <div class="emoji" data-keywords="baby chick bird" onclick="copyEmoji('🐤')">🐤</div>
    <div class="emoji" data-keywords="hatching chick bird" onclick="copyEmoji('🐣')">🐣</div>
    <div class="emoji" data-keywords="baby chick bird" onclick="copyEmoji('🐥')">🐥</div>
    <div class="emoji" data-keywords="duck animal bird" onclick="copyEmoji('🦆')">🦆</div>
    <div class="emoji" data-keywords="eagle bird animal" onclick="copyEmoji('🦅')">🦅</div>
    <div class="emoji" data-keywords="owl bird animal" onclick="copyEmoji('🦉')">🦉</div>
    <div class="emoji" data-keywords="bat animal" onclick="copyEmoji('🦇')">🦇</div>
    <div class="emoji" data-keywords="wolf animal wild" onclick="copyEmoji('🐺')">🐺</div>
    <div class="emoji" data-keywords="boar animal wild" onclick="copyEmoji('🐗')">🐗</div>
    <div class="emoji" data-keywords="horse animal" onclick="copyEmoji('🐴')">🐴</div>
    <div class="emoji" data-keywords="unicorn mythical" onclick="copyEmoji('🦄')">🦄</div>
    <div class="emoji" data-keywords="bee insect" onclick="copyEmoji('🐝')">🐝</div>
    <div class="emoji" data-keywords="worm animal" onclick="copyEmoji('🪱')">🪱</div>
    <div class="emoji" data-keywords="caterpillar insect" onclick="copyEmoji('🐛')">🐛</div>
    <div class="emoji" data-keywords="butterfly insect" onclick="copyEmoji('🦋')">🦋</div>
    <div class="emoji" data-keywords="snail animal" onclick="copyEmoji('🐌')">🐌</div>
    <div class="emoji" data-keywords="ladybug insect" onclick="copyEmoji('🐞')">🐞</div>
    <div class="emoji" data-keywords="ant insect" onclick="copyEmoji('🐜')">🐜</div>
    <div class="emoji" data-keywords="beetle insect" onclick="copyEmoji('🪲')">🪲</div>
    <div class="emoji" data-keywords="cockroach insect" onclick="copyEmoji('🪳')">🪳</div>
    <div class="emoji" data-keywords="spider arachnid" onclick="copyEmoji('🕷️')">🕷️</div>
    <div class="emoji" data-keywords="spider web" onclick="copyEmoji('🕸️')">🕸️</div>
    <div class="emoji" data-keywords="scorpion arachnid" onclick="copyEmoji('🦂')">🦂</div>
    <div class="emoji" data-keywords="turtle animal reptile" onclick="copyEmoji('🐢')">🐢</div>
    <div class="emoji" data-keywords="snake reptile" onclick="copyEmoji('🐍')">🐍</div>
    <div class="emoji" data-keywords="lizard reptile" onclick="copyEmoji('🦎')">🦎</div>
    <div class="emoji" data-keywords="octopus sea animal" onclick="copyEmoji('🐙')">🐙</div>
    <div class="emoji" data-keywords="squid sea animal" onclick="copyEmoji('🦑')">🦑</div>
    <div class="emoji" data-keywords="shrimp sea animal" onclick="copyEmoji('🦐')">🦐</div>
    <div class="emoji" data-keywords="lobster sea animal" onclick="copyEmoji('🦞')">🦞</div>
    <div class="emoji" data-keywords="crab sea animal" onclick="copyEmoji('🦀')">🦀</div>
    <div class="emoji" data-keywords="tropical fish" onclick="copyEmoji('🐠')">🐠</div>
    <div class="emoji" data-keywords="fish" onclick="copyEmoji('🐟')">🐟</div>
    <div class="emoji" data-keywords="pufferfish" onclick="copyEmoji('🐡')">🐡</div>
    <div class="emoji" data-keywords="dolphin sea animal" onclick="copyEmoji('🐬')">🐬</div>
    <div class="emoji" data-keywords="whale sea animal" onclick="copyEmoji('🐳')">🐳</div>
    <div class="emoji" data-keywords="whale sea animal" onclick="copyEmoji('🐋')">🐋</div>
    <div class="emoji" data-keywords="shark sea animal" onclick="copyEmoji('🦈')">🦈</div>
    <div class="emoji" data-keywords="crocodile reptile" onclick="copyEmoji('🐊')">🐊</div>
    <div class="emoji" data-keywords="tiger animal wild" onclick="copyEmoji('🐅')">🐅</div>
    <div class="emoji" data-keywords="leopard animal wild" onclick="copyEmoji('🐆')">🐆</div>
    <div class="emoji" data-keywords="zebra animal" onclick="copyEmoji('🦓')">🦓</div>
    <div class="emoji" data-keywords="gorilla ape animal" onclick="copyEmoji('🦍')">🦍</div>
    <div class="emoji" data-keywords="orangutan ape" onclick="copyEmoji('🦧')">🦧</div>
    <div class="emoji" data-keywords="mammoth extinct animal" onclick="copyEmoji('🦣')">🦣</div>
    <div class="emoji" data-keywords="elephant animal" onclick="copyEmoji('🐘')">🐘</div>
    <div class="emoji" data-keywords="bison animal" onclick="copyEmoji('🦬')">🦬</div>
    <div class="emoji" data-keywords="water buffalo animal" onclick="copyEmoji('🐃')">🐃</div>
    <div class="emoji" data-keywords="ox animal" onclick="copyEmoji('🐂')">🐂</div>
    <div class="emoji" data-keywords="cow animal" onclick="copyEmoji('🐄')">🐄</div>
    <div class="emoji" data-keywords="deer animal" onclick="copyEmoji('🦌')">🦌</div>
    <div class="emoji" data-keywords="dromedary camel" onclick="copyEmoji('🐪')">🐪</div>
    <div class="emoji" data-keywords="bactrian camel" onclick="copyEmoji('🐫')">🐫</div>
    <div class="emoji" data-keywords="llama animal" onclick="copyEmoji('🦙')">🦙</div>
    <div class="emoji" data-keywords="giraffe animal" onclick="copyEmoji('🦒')">🦒</div>
    <div class="emoji" data-keywords="ram animal" onclick="copyEmoji('🐏')">🐏</div>
    <div class="emoji" data-keywords="sheep animal" onclick="copyEmoji('🐑')">🐑</div>
    <div class="emoji" data-keywords="goat animal" onclick="copyEmoji('🐐')">🐐</div>
    <div class="emoji" data-keywords="horse animal" onclick="copyEmoji('🐎')">🐎</div>
    <div class="emoji" data-keywords="pig animal" onclick="copyEmoji('🐖')">🐖</div>
    <div class="emoji" data-keywords="rat rodent" onclick="copyEmoji('🐀')">🐀</div>
    <div class="emoji" data-keywords="mouse rodent" onclick="copyEmoji('🐁')">🐁</div>
    <div class="emoji" data-keywords="rooster chicken" onclick="copyEmoji('🐓')">🐓</div>
    <div class="emoji" data-keywords="turkey bird" onclick="copyEmoji('🦃')">🦃</div>
    <div class="emoji" data-keywords="dove bird peace" onclick="copyEmoji('🕊️')">🕊️</div>
    <div class="emoji" data-keywords="feather bird" onclick="copyEmoji('🪶')">🪶</div>
    <div class="emoji" data-keywords="dog pet" onclick="copyEmoji('🐕')">🐕</div>
    <div class="emoji" data-keywords="poodle dog" onclick="copyEmoji('🐩')">🐩</div>
    <div class="emoji" data-keywords="cat pet" onclick="copyEmoji('🐈')">🐈</div>
    <div class="emoji" data-keywords="black cat" onclick="copyEmoji('🐈‍⬛')">🐈‍⬛</div>
    <div class="emoji" data-keywords="rabbit bunny" onclick="copyEmoji('🐇')">🐇</div>
    <div class="emoji" data-keywords="raccoon animal" onclick="copyEmoji('🦝')">🦝</div>
    <div class="emoji" data-keywords="skunk animal" onclick="copyEmoji('🦨')">🦨</div>
    <div class="emoji" data-keywords="badger animal" onclick="copyEmoji('🦡')">🦡</div>
    <div class="emoji" data-keywords="beaver animal" onclick="copyEmoji('🦫')">🦫</div>
    <div class="emoji" data-keywords="hedgehog animal" onclick="copyEmoji('🦔')">🦔</div>
    <div class="emoji" data-keywords="paw prints animal" onclick="copyEmoji('🐾')">🐾</div>
    <div class="emoji" data-keywords="dragon mythical" onclick="copyEmoji('🐉')">🐉</div>
    <div class="emoji" data-keywords="dragon mythical" onclick="copyEmoji('🐲')">🐲</div>
    <div class="emoji" data-keywords="sauropod dinosaur" onclick="copyEmoji('🦕')">🦕</div>
    <div class="emoji" data-keywords="t-rex dinosaur" onclick="copyEmoji('🦖')">🦖</div>
  </div>

  <div class="category">
    <h2>😎 People</h2>
  <div class="emoji" data-keywords="grinning face happy smile" onclick="copyEmoji('😀')">😀</div>
  <div class="emoji" data-keywords="grinning face big eyes happy" onclick="copyEmoji('😃')">😃</div>
  <div class="emoji" data-keywords="grinning face smiling eyes happy" onclick="copyEmoji('😄')">😄</div>
  <div class="emoji" data-keywords="beaming face smiling eyes happy" onclick="copyEmoji('😁')">😁</div>
  <div class="emoji" data-keywords="grinning squinting face laugh" onclick="copyEmoji('😆')">😆</div>
  <div class="emoji" data-keywords="grinning face sweat nervous" onclick="copyEmoji('😅')">😅</div>
  <div class="emoji" data-keywords="face tears joy lol" onclick="copyEmoji('😂')">😂</div>
  <div class="emoji" data-keywords="rolling floor laughing rofl" onclick="copyEmoji('🤣')">🤣</div>
  <div class="emoji" data-keywords="slightly smiling face" onclick="copyEmoji('🙂')">🙂</div>
  <div class="emoji" data-keywords="upside down face silly" onclick="copyEmoji('🙃')">🙃</div>
  <div class="emoji" data-keywords="winking face wink" onclick="copyEmoji('😉')">😉</div>
  <div class="emoji" data-keywords="smiling face smiling eyes" onclick="copyEmoji('😊')">😊</div>
  <div class="emoji" data-keywords="smiling face halo angel" onclick="copyEmoji('😇')">😇</div>
  <div class="emoji" data-keywords="smiling face hearts in love" onclick="copyEmoji('🥰')">🥰</div>
  <div class="emoji" data-keywords="smiling face heart eyes love" onclick="copyEmoji('😍')">😍</div>
  <div class="emoji" data-keywords="star struck star eyes" onclick="copyEmoji('🤩')">🤩</div>
  <div class="emoji" data-keywords="face blowing kiss" onclick="copyEmoji('😘')">😘</div>
  <div class="emoji" data-keywords="kissing face" onclick="copyEmoji('😗')">😗</div>
  <div class="emoji" data-keywords="kissing face smiling eyes" onclick="copyEmoji('😙')">😙</div>
  <div class="emoji" data-keywords="kissing face closed eyes" onclick="copyEmoji('😚')">😚</div>
  <div class="emoji" data-keywords="smiling face tongue yummy" onclick="copyEmoji('😋')">😋</div>
  <div class="emoji" data-keywords="winking face tongue playful" onclick="copyEmoji('😜')">😜</div>
  <div class="emoji" data-keywords="squinting face tongue crazy" onclick="copyEmoji('😝')">😝</div>
  <div class="emoji" data-keywords="zany face crazy" onclick="copyEmoji('🤪')">🤪</div>
  <div class="emoji" data-keywords="face with tongue silly" onclick="copyEmoji('😛')">😛</div>
  <div class="emoji" data-keywords="smiling face sunglasses cool" onclick="copyEmoji('😎')">😎</div>
  <div class="emoji" data-keywords="smirking face smirk" onclick="copyEmoji('😏')">😏</div>
  <div class="emoji" data-keywords="expressionless face blank" onclick="copyEmoji('😑')">😑</div>
  <div class="emoji" data-keywords="neutral face meh" onclick="copyEmoji('😐')">😐</div>
  <div class="emoji" data-keywords="face without mouth mute" onclick="copyEmoji('😶')">😶</div>
  <div class="emoji" data-keywords="face rolling eyes annoyed" onclick="copyEmoji('🙄')">🙄</div>
  <div class="emoji" data-keywords="thinking face think" onclick="copyEmoji('🤔')">🤔</div>
  <div class="emoji" data-keywords="shushing face quiet" onclick="copyEmoji('🤫')">🤫</div>
  <div class="emoji" data-keywords="zipper mouth secret" onclick="copyEmoji('🤐')">🤐</div>
  <div class="emoji" data-keywords="face with raised eyebrow skeptic" onclick="copyEmoji('🤨')">🤨</div>
  <div class="emoji" data-keywords="neutral face unamused" onclick="copyEmoji('😒')">😒</div>
  <div class="emoji" data-keywords="confused face" onclick="copyEmoji('😕')">😕</div>
  <div class="emoji" data-keywords="slightly frowning face" onclick="copyEmoji('☹️')">☹️</div>
  <div class="emoji" data-keywords="frowning face" onclick="copyEmoji('🙁')">🙁</div>
  <div class="emoji" data-keywords="persevering face" onclick="copyEmoji('😣')">😣</div>
  <div class="emoji" data-keywords="confounded face" onclick="copyEmoji('😖')">😖</div>
  <div class="emoji" data-keywords="worried face" onclick="copyEmoji('😟')">😟</div>
  <div class="emoji" data-keywords="slightly sad disappointed" onclick="copyEmoji('😞')">😞</div>
  <div class="emoji" data-keywords="pensive face sad" onclick="copyEmoji('😔')">😔</div>
  <div class="emoji" data-keywords="sad relieved face" onclick="copyEmoji('😥')">😥</div>
  <div class="emoji" data-keywords="crying face" onclick="copyEmoji('😢')">😢</div>
  <div class="emoji" data-keywords="loudly crying face" onclick="copyEmoji('😭')">😭</div>
  <div class="emoji" data-keywords="weary face tired" onclick="copyEmoji('😩')">😩</div>
  <div class="emoji" data-keywords="tired face exhausted" onclick="copyEmoji('😫')">😫</div>
  <div class="emoji" data-keywords="pleading face puppy eyes" onclick="copyEmoji('🥺')">🥺</div>
  <div class="emoji" data-keywords="angry face mad" onclick="copyEmoji('😠')">😠</div>
  <div class="emoji" data-keywords="pouting face very angry" onclick="copyEmoji('😡')">😡</div>
  <div class="emoji" data-keywords="face symbols mouth swearing" onclick="copyEmoji('🤬')">🤬</div>
  <div class="emoji" data-keywords="face steam nose triumph" onclick="copyEmoji('😤')">😤</div>
  <div class="emoji" data-keywords="face screaming fear scared" onclick="copyEmoji('😱')">😱</div>
  <div class="emoji" data-keywords="fearful face scared" onclick="copyEmoji('😨')">😨</div>
  <div class="emoji" data-keywords="anxious face sweat worried" onclick="copyEmoji('😰')">😰</div>
  <div class="emoji" data-keywords="face open mouth surprised" onclick="copyEmoji('😮')">😮</div>
  <div class="emoji" data-keywords="hushed face surprised" onclick="copyEmoji('😯')">😯</div>
  <div class="emoji" data-keywords="astonished face shocked" onclick="copyEmoji('😲')">😲</div>
  <div class="emoji" data-keywords="flushed face embarrassed" onclick="copyEmoji('😳')">😳</div>
  <div class="emoji" data-keywords="face with diagonal mouth unsure" onclick="copyEmoji('🫤')">🫤</div>
  <div class="emoji" data-keywords="face with peeking eye shy" onclick="copyEmoji('🫣')">🫣</div>
  <div class="emoji" data-keywords="face with monocle inspect" onclick="copyEmoji('🧐')">🧐</div>
  <div class="emoji" data-keywords="woozy face drunk dizzy" onclick="copyEmoji('🥴')">🥴</div>
  <div class="emoji" data-keywords="dizzy face" onclick="copyEmoji('😵')">😵</div>
  <div class="emoji" data-keywords="face with spiral eyes dizzy" onclick="copyEmoji('😵‍💫')">😵‍💫</div>
  <div class="emoji" data-keywords="exploding head mind blown" onclick="copyEmoji('🤯')">🤯</div>
  <div class="emoji" data-keywords="sleeping face" onclick="copyEmoji('😴')">😴</div>
  <div class="emoji" data-keywords="sleepy face" onclick="copyEmoji('😪')">😪</div>
  <div class="emoji" data-keywords="yawning face" onclick="copyEmoji('🥱')">🥱</div>
  <div class="emoji" data-keywords="drooling face" onclick="copyEmoji('🤤')">🤤</div>

  <!-- Sick / medical -->
  <div class="emoji" data-keywords="face medical mask sick" onclick="copyEmoji('😷')">😷</div>
  <div class="emoji" data-keywords="face thermometer sick" onclick="copyEmoji('🤒')">🤒</div>
  <div class="emoji" data-keywords="face head bandage injury" onclick="copyEmoji('🤕')">🤕</div>
  <div class="emoji" data-keywords="nauseated face sick" onclick="copyEmoji('🤢')">🤢</div>
  <div class="emoji" data-keywords="face vomiting" onclick="copyEmoji('🤮')">🤮</div>
  <div class="emoji" data-keywords="sneezing face sick" onclick="copyEmoji('🤧')">🤧</div>
  <div class="emoji" data-keywords="hot face heat" onclick="copyEmoji('🥵')">🥵</div>
  <div class="emoji" data-keywords="cold face freezing" onclick="copyEmoji('🥶')">🥶</div>

  <!-- Money / party -->
  <div class="emoji" data-keywords="money mouth face rich" onclick="copyEmoji('🤑')">🤑</div>
  <div class="emoji" data-keywords="party face celebration" onclick="copyEmoji('🥳')">🥳</div>
  <div class="emoji" data-keywords="cowboy hat face" onclick="copyEmoji('🤠')">🤠</div>
  <div class="emoji" data-keywords="disguised face glasses fake" onclick="copyEmoji('🥸')">🥸</div>

  <!-- Creatures / masks -->
  <div class="emoji" data-keywords="smiling face horns devil" onclick="copyEmoji('😈')">😈</div>
  <div class="emoji" data-keywords="angry face horns devil" onclick="copyEmoji('👿')">👿</div>
  <div class="emoji" data-keywords="ogre monster" onclick="copyEmoji('👹')">👹</div>
  <div class="emoji" data-keywords="goblin monster" onclick="copyEmoji('👺')">👺</div>
  <div class="emoji" data-keywords="clown face" onclick="copyEmoji('🤡')">🤡</div>
  <div class="emoji" data-keywords="ghost spooky" onclick="copyEmoji('👻')">👻</div>
  <div class="emoji" data-keywords="skull death" onclick="copyEmoji('💀')">💀</div>
  <div class="emoji" data-keywords="skull crossbones danger" onclick="copyEmoji('☠️')">☠️</div>
  <div class="emoji" data-keywords="alien ufo" onclick="copyEmoji('👽')">👽</div>
  <div class="emoji" data-keywords="alien monster" onclick="copyEmoji('👾')">👾</div>
  <div class="emoji" data-keywords="robot face" onclick="copyEmoji('🤖')">🤖</div>

  <!-- Hearts / symbols often used as people emotion -->
  <div class="emoji" data-keywords="red heart love" onclick="copyEmoji('❤️')">❤️</div>
  <div class="emoji" data-keywords="orange heart love" onclick="copyEmoji('🧡')">🧡</div>
  <div class="emoji" data-keywords="yellow heart love" onclick="copyEmoji('💛')">💛</div>
  <div class="emoji" data-keywords="green heart love" onclick="copyEmoji('💚')">💚</div>
  <div class="emoji" data-keywords="blue heart love" onclick="copyEmoji('💙')">💙</div>
  <div class="emoji" data-keywords="purple heart love" onclick="copyEmoji('💜')">💜</div>
  <div class="emoji" data-keywords="brown heart love" onclick="copyEmoji('🤎')">🤎</div>
  <div class="emoji" data-keywords="black heart" onclick="copyEmoji('🖤')">🖤</div>
  <div class="emoji" data-keywords="white heart" onclick="copyEmoji('🤍')">🤍</div>
  <div class="emoji" data-keywords="sparkling heart" onclick="copyEmoji('💖')">💖</div>
  <div class="emoji" data-keywords="growing heart" onclick="copyEmoji('💗')">💗</div>
  <div class="emoji" data-keywords="beating heart" onclick="copyEmoji('💓')">💓</div>
  <div class="emoji" data-keywords="two hearts" onclick="copyEmoji('💕')">💕</div>
  <div class="emoji" data-keywords="revolving hearts" onclick="copyEmoji('💞')">💞</div>
  <div class="emoji" data-keywords="heart exclamation" onclick="copyEmoji('❣️')">❣️</div>
  <div class="emoji" data-keywords="broken heart" onclick="copyEmoji('💔')">💔</div>
</div>
  </div>

<div class="category">
  <h2>🖐️ Hands & Gestures</h2>

  <!-- Basic hands -->
  <div class="emoji" data-keywords="waving hand hello goodbye hi bye" onclick="copyEmoji('👋')">👋</div>
  <div class="emoji" data-keywords="raised back of hand" onclick="copyEmoji('🤚')">🤚</div>
  <div class="emoji" data-keywords="hand with fingers splayed" onclick="copyEmoji('🖐️')">🖐️</div>
  <div class="emoji" data-keywords="raised hand stop high five" onclick="copyEmoji('✋')">✋</div>
  <div class="emoji" data-keywords="vulcan salute live long prosper" onclick="copyEmoji('🖖')">🖖</div>

  <!-- Pointing -->
  <div class="emoji" data-keywords="backhand index pointing left" onclick="copyEmoji('👈')">👈</div>
  <div class="emoji" data-keywords="backhand index pointing right" onclick="copyEmoji('👉')">👉</div>
  <div class="emoji" data-keywords="backhand index pointing up" onclick="copyEmoji('👆')">👆</div>
  <div class="emoji" data-keywords="backhand index pointing down" onclick="copyEmoji('👇')">👇</div>
  <div class="emoji" data-keywords="index pointing up" onclick="copyEmoji('☝️')">☝️</div>
  <div class="emoji" data-keywords="index pointing at viewer you" onclick="copyEmoji('🫵')">🫵</div>

  <!-- Thumbs / ok -->
  <div class="emoji" data-keywords="thumbs up like approve" onclick="copyEmoji('👍')">👍</div>
  <div class="emoji" data-keywords="thumbs down dislike" onclick="copyEmoji('👎')">👎</div>
  <div class="emoji" data-keywords="ok hand perfect" onclick="copyEmoji('👌')">👌</div>
  <div class="emoji" data-keywords="pinched fingers italian hand" onclick="copyEmoji('🤌')">🤌</div>
  <div class="emoji" data-keywords="pinching hand small tiny" onclick="copyEmoji('🤏')">🤏</div>

  <!-- Fists -->
  <div class="emoji" data-keywords="oncoming fist punch" onclick="copyEmoji('👊')">👊</div>
  <div class="emoji" data-keywords="left facing fist fist bump" onclick="copyEmoji('🤛')">🤛</div>
  <div class="emoji" data-keywords="right facing fist fist bump" onclick="copyEmoji('🤜')">🤜</div>

  <!-- Love / peace / rock -->
  <div class="emoji" data-keywords="victory hand peace sign" onclick="copyEmoji('✌️')">✌️</div>
  <div class="emoji" data-keywords="crossed fingers good luck" onclick="copyEmoji('🤞')">🤞</div>
  <div class="emoji" data-keywords="sign of the horns rock on" onclick="copyEmoji('🤘')">🤘</div>
  <div class="emoji" data-keywords="love you gesture i love you" onclick="copyEmoji('🤟')">🤟</div>
  <div class="emoji" data-keywords="heart hands love" onclick="copyEmoji('🫶')">🫶</div>

  <!-- Praying / clapping / open -->
  <div class="emoji" data-keywords="folded hands pray please thank you" onclick="copyEmoji('🙏')">🙏</div>
  <div class="emoji" data-keywords="clapping hands applause bravo" onclick="copyEmoji('👏')">👏</div>
  <div class="emoji" data-keywords="raising hands celebration yay" onclick="copyEmoji('🙌')">🙌</div>
  <div class="emoji" data-keywords="open hands hug giving" onclick="copyEmoji('👐')">👐</div>
  <div class="emoji" data-keywords="palms up together offering" onclick="copyEmoji('🤲')">🤲</div>
  <div class="emoji" data-keywords="handshake agreement deal" onclick="copyEmoji('🤝')">🤝</div>

  <!-- Directional palms -->
  <div class="emoji" data-keywords="palm facing up" onclick="copyEmoji('🫴')">🫴</div>
  <div class="emoji" data-keywords="palm facing right" onclick="copyEmoji('🫱')">🫱</div>
  <div class="emoji" data-keywords="palm facing left" onclick="copyEmoji('🫲')">🫲</div>

  <!-- Writing / nails / care -->
  <div class="emoji" data-keywords="writing hand" onclick="copyEmoji('✍️')">✍️</div>
  <div class="emoji" data-keywords="nail polish manicure" onclick="copyEmoji('💅')">💅</div>
  <div class="emoji" data-keywords="flexed biceps strong muscle" onclick="copyEmoji('💪')">💪</div>

  <!-- Rude / special -->
  <div class="emoji" data-keywords="middle finger rude" onclick="copyEmoji('🖕')">🖕</div>
</div>

<div class="category">
  <h2>💪 Body Parts</h2>

  <!-- Core body parts -->
  <div class="emoji" data-keywords="flexed biceps arm muscle strong strength gym" onclick="copyEmoji('💪')">💪</div>
  <div class="emoji" data-keywords="mechanical arm prosthetic robot cyber arm" onclick="copyEmoji('🦾')">🦾</div>
  <div class="emoji" data-keywords="mechanical leg prosthetic robot cyber leg" onclick="copyEmoji('🦿')">🦿</div>
  <div class="emoji" data-keywords="leg body part running walking" onclick="copyEmoji('🦵')">🦵</div>
  <div class="emoji" data-keywords="foot body part walking" onclick="copyEmoji('🦶')">🦶</div>

  <!-- Head / senses -->
  <div class="emoji" data-keywords="ear hear listening" onclick="copyEmoji('👂')">👂</div>
  <div class="emoji" data-keywords="ear with hearing aid deaf hearing aid" onclick="copyEmoji('🦻')">🦻</div>
  <div class="emoji" data-keywords="nose smell sniff" onclick="copyEmoji('👃')">👃</div>
  <div class="emoji" data-keywords="eyes look watching see" onclick="copyEmoji('👀')">👀</div>
  <div class="emoji" data-keywords="eye look see" onclick="copyEmoji('👁️')">👁️</div>
  <div class="emoji" data-keywords="tongue taste lick" onclick="copyEmoji('👅')">👅</div>
  <div class="emoji" data-keywords="mouth lips talk speak eat" onclick="copyEmoji('👄')">👄</div>
  <div class="emoji" data-keywords="biting lip lips nervous flirty" onclick="copyEmoji('🫦')">🫦</div>

  <!-- Organs / inside -->
  <div class="emoji" data-keywords="brain mind smart thinking" onclick="copyEmoji('🧠')">🧠</div>
  <div class="emoji" data-keywords="anatomical heart organ" onclick="copyEmoji('🫀')">🫀</div>
  <div class="emoji" data-keywords="lungs breathing organ" onclick="copyEmoji('🫁')">🫁</div>

  <!-- Bones / teeth -->
  <div class="emoji" data-keywords="tooth dental teeth" onclick="copyEmoji('🦷')">🦷</div>
  <div class="emoji" data-keywords="bone skeleton" onclick="copyEmoji('🦴')">🦴</div>
</div>

<div class="category">
  <h2>🔷 Shapes & Squares</h2>

  <!-- Big colored squares -->
  <div class="emoji" data-keywords="blue square shape" onclick="copyEmoji('🟦')">🟦</div>
  <div class="emoji" data-keywords="red square shape" onclick="copyEmoji('🟥')">🟥</div>
  <div class="emoji" data-keywords="yellow square shape" onclick="copyEmoji('🟨')">🟨</div>
  <div class="emoji" data-keywords="green square shape" onclick="copyEmoji('🟩')">🟩</div>
  <div class="emoji" data-keywords="purple square shape" onclick="copyEmoji('🟪')">🟪</div>
  <div class="emoji" data-keywords="brown square shape" onclick="copyEmoji('🟫')">🟫</div>
  <div class="emoji" data-keywords="black large square shape" onclick="copyEmoji('⬛')">⬛</div>
  <div class="emoji" data-keywords="white large square shape" onclick="copyEmoji('⬜')">⬜</div>

  <!-- Small squares / buttons -->
  <div class="emoji" data-keywords="black small square bullet" onclick="copyEmoji('▪️')">▪️</div>
  <div class="emoji" data-keywords="white small square bullet" onclick="copyEmoji('▫️')">▫️</div>
  <div class="emoji" data-keywords="blue square button ui" onclick="copyEmoji('🔵')">🔵</div>
  <div class="emoji" data-keywords="red square button ui" onclick="copyEmoji('🔴')">🔴</div>
  <div class="emoji" data-keywords="white square button ui" onclick="copyEmoji('🔳')">🔳</div>
  <div class="emoji" data-keywords="black square button ui" onclick="copyEmoji('🔲')">🔲</div>

  <!-- Circles -->
  <div class="emoji" data-keywords="blue circle dot" onclick="copyEmoji('🔵')">🔵</div>
  <div class="emoji" data-keywords="red circle dot" onclick="copyEmoji('🔴')">🔴</div>
  <div class="emoji" data-keywords="yellow circle dot" onclick="copyEmoji('🟡')">🟡</div>
  <div class="emoji" data-keywords="green circle dot" onclick="copyEmoji('🟢')">🟢</div>
  <div class="emoji" data-keywords="purple circle dot" onclick="copyEmoji('🟣')">🟣</div>
  <div class="emoji" data-keywords="brown circle dot" onclick="copyEmoji('🟤')">🟤</div>
  <div class="emoji" data-keywords="white circle hollow" onclick="copyEmoji('⚪')">⚪</div>
  <div class="emoji" data-keywords="black circle solid" onclick="copyEmoji('⚫')">⚫</div>

  <!-- Diamonds -->
  <div class="emoji" data-keywords="large blue diamond shape" onclick="copyEmoji('🔷')">🔷</div>
  <div class="emoji" data-keywords="large orange diamond shape" onclick="copyEmoji('🔶')">🔶</div>
  <div class="emoji" data-keywords="small blue diamond shape" onclick="copyEmoji('🔹')">🔹</div>
  <div class="emoji" data-keywords="small orange diamond shape" onclick="copyEmoji('🔸')">🔸</div>
  <div class="emoji" data-keywords="diamond suit card" onclick="copyEmoji('♦️')">♦️</div>

  <!-- Triangles / arrows-like shapes -->
  <div class="emoji" data-keywords="red triangle pointed up" onclick="copyEmoji('🔺')">🔺</div>
  <div class="emoji" data-keywords="red triangle pointed down" onclick="copyEmoji('🔻')">🔻</div>
  <div class="emoji" data-keywords="up pointing small red triangle" onclick="copyEmoji('🔼')">🔼</div>
  <div class="emoji" data-keywords="down pointing small red triangle" onclick="copyEmoji('🔽')">🔽</div>
  <div class="emoji" data-keywords="black small triangle left" onclick="copyEmoji('◀️')">◀️</div>
  <div class="emoji" data-keywords="black small triangle right" onclick="copyEmoji('▶️')">▶️</div>

  <!-- Squares with rounded/other -->
  <div class="emoji" data-keywords="white square rounded corners" onclick="copyEmoji('▢')">▢</div>
  <div class="emoji" data-keywords="white medium square" onclick="copyEmoji('◻️')">◻️</div>
  <div class="emoji" data-keywords="black medium square" onclick="copyEmoji('◼️')">◼️</div>
  <div class="emoji" data-keywords="white medium small square" onclick="copyEmoji('◽')">◽</div>
  <div class="emoji" data-keywords="black medium small square" onclick="copyEmoji('◾')">◾</div>
</div>

<div class="category">
  <h2>♾️ Symbols</h2>

  <!-- Arrows -->
  <div class="emoji" data-keywords="right arrow" onclick="copyEmoji('➡️')">➡️</div>
  <div class="emoji" data-keywords="left arrow" onclick="copyEmoji('⬅️')">⬅️</div>
  <div class="emoji" data-keywords="up arrow" onclick="copyEmoji('⬆️')">⬆️</div>
  <div class="emoji" data-keywords="down arrow" onclick="copyEmoji('⬇️')">⬇️</div>
  <div class="emoji" data-keywords="up right arrow" onclick="copyEmoji('↗️')">↗️</div>
  <div class="emoji" data-keywords="down right arrow" onclick="copyEmoji('↘️')">↘️</div>
  <div class="emoji" data-keywords="down left arrow" onclick="copyEmoji('↙️')">↙️</div>
  <div class="emoji" data-keywords="up left arrow" onclick="copyEmoji('↖️')">↖️</div>
  <div class="emoji" data-keywords="right arrow curving left reply" onclick="copyEmoji('↩️')">↩️</div>
  <div class="emoji" data-keywords="left arrow curving right share" onclick="copyEmoji('↪️')">↪️</div>
  <div class="emoji" data-keywords="right arrow curving up" onclick="copyEmoji('⤴️')">⤴️</div>
  <div class="emoji" data-keywords="right arrow curving down" onclick="copyEmoji('⤵️')">⤵️</div>
  <div class="emoji" data-keywords="shuffle tracks arrows" onclick="copyEmoji('🔀')">🔀</div>
  <div class="emoji" data-keywords="repeat arrows" onclick="copyEmoji('🔁')">🔁</div>
  <div class="emoji" data-keywords="repeat single arrows" onclick="copyEmoji('🔂')">🔂</div>
  <div class="emoji" data-keywords="clockwise arrows circle sync" onclick="copyEmoji('🔄')">🔄</div>
  <div class="emoji" data-keywords="anticlockwise arrows circle" onclick="copyEmoji('🔃')">🔃</div>

  <!-- Stars / sparkles -->
  <div class="emoji" data-keywords="glowing star" onclick="copyEmoji('🌟')">🌟</div>
  <div class="emoji" data-keywords="star" onclick="copyEmoji('⭐')">⭐</div>
  <div class="emoji" data-keywords="sparkles magic shine" onclick="copyEmoji('✨')">✨</div>
  <div class="emoji" data-keywords="dizzy symbol spark" onclick="copyEmoji('💫')">💫</div>
  <div class="emoji" data-keywords="shooting star wish" onclick="copyEmoji('🌠')">🌠</div>

  <!-- Check marks / crosses -->
  <div class="emoji" data-keywords="check mark" onclick="copyEmoji('✔️')">✔️</div>
  <div class="emoji" data-keywords="heavy check mark" onclick="copyEmoji('✅')">✅</div>
  <div class="emoji" data-keywords="white heavy check mark" onclick="copyEmoji('☑️')">☑️</div>
  <div class="emoji" data-keywords="cross mark" onclick="copyEmoji('❌')">❌</div>
  <div class="emoji" data-keywords="cross mark button" onclick="copyEmoji('✖️')">✖️</div>
  <div class="emoji" data-keywords="negative squared cross mark" onclick="copyEmoji('🟥')">🟥</div>
  <div class="emoji" data-keywords="prohibited no symbol" onclick="copyEmoji('🚫')">🚫</div>
  <div class="emoji" data-keywords="no entry" onclick="copyEmoji('⛔')">⛔</div>

  <!-- Info / warning -->
  <div class="emoji" data-keywords="warning sign" onclick="copyEmoji('⚠️')">⚠️</div>
  <div class="emoji" data-keywords="children crossing" onclick="copyEmoji('🚸')">🚸</div>
  <div class="emoji" data-keywords="no pedestrians" onclick="copyEmoji('🚷')">🚷</div>
  <div class="emoji" data-keywords="no bicycles" onclick="copyEmoji('🚳')">🚳</div>
  <div class="emoji" data-keywords="radioactive" onclick="copyEmoji('☢️')">☢️</div>
  <div class="emoji" data-keywords="biohazard" onclick="copyEmoji('☣️')">☣️</div>
  <div class="emoji" data-keywords="information source" onclick="copyEmoji('ℹ️')">ℹ️</div>
  <div class="emoji" data-keywords="exclamation mark" onclick="copyEmoji('❗')">❗</div>
  <div class="emoji" data-keywords="double exclamation" onclick="copyEmoji('‼️')">‼️</div>
  <div class="emoji" data-keywords="question mark" onclick="copyEmoji('❓')">❓</div>
  <div class="emoji" data-keywords="white question mark" onclick="copyEmoji('❔')">❔</div>
  <div class="emoji" data-keywords="white exclamation" onclick="copyEmoji('❕')">❕</div>
  <div class="emoji" data-keywords="exclamation question interrobang" onclick="copyEmoji('⁉️')">⁉️</div>

  <!-- Time / clocks -->
  <div class="emoji" data-keywords="alarm clock" onclick="copyEmoji('⏰')">⏰</div>
  <div class="emoji" data-keywords="stopwatch" onclick="copyEmoji('⏱️')">⏱️</div>
  <div class="emoji" data-keywords="timer clock" onclick="copyEmoji('⏲️')">⏲️</div>
  <div class="emoji" data-keywords="mantelpiece clock" onclick="copyEmoji('🕰️')">🕰️</div>
  <div class="emoji" data-keywords="hourglass done" onclick="copyEmoji('⌛')">⌛</div>
  <div class="emoji" data-keywords="hourglass not done" onclick="copyEmoji('⏳')">⏳</div>
  <div class="emoji" data-keywords="watch wristwatch" onclick="copyEmoji('⌚')">⌚</div>

  <!-- Weather / misc symbols that feel symbolic -->
  <div class="emoji" data-keywords="cyclone swirl" onclick="copyEmoji('🌀')">🌀</div>
  <div class="emoji" data-keywords="black sun rays" onclick="copyEmoji('☀️')">☀️</div>
  <div class="emoji" data-keywords="cloud" onclick="copyEmoji('☁️')">☁️</div>
  <div class="emoji" data-keywords="high voltage lightning" onclick="copyEmoji('⚡')">⚡</div>
  <div class="emoji" data-keywords="snowflake" onclick="copyEmoji('❄️')">❄️</div>
  <div class="emoji" data-keywords="comet" onclick="copyEmoji('☄️')">☄️</div>

  <!-- Music / sound -->
  <div class="emoji" data-keywords="musical note" onclick="copyEmoji('🎵')">🎵</div>
  <div class="emoji" data-keywords="musical notes" onclick="copyEmoji('🎶')">🎶</div>
  <div class="emoji" data-keywords="mute speaker" onclick="copyEmoji('🔇')">🔇</div>
  <div class="emoji" data-keywords="speaker low volume" onclick="copyEmoji('🔈')">🔈</div>
  <div class="emoji" data-keywords="speaker medium volume" onclick="copyEmoji('🔉')">🔉</div>
  <div class="emoji" data-keywords="speaker high volume" onclick="copyEmoji('🔊')">🔊</div>
  <div class="emoji" data-keywords="loudspeaker announcement" onclick="copyEmoji('📢')">📢</div>
  <div class="emoji" data-keywords="megaphone" onclick="copyEmoji('📣')">📣</div>
  <div class="emoji" data-keywords="bell" onclick="copyEmoji('🔔')">🔔</div>
  <div class="emoji" data-keywords="bell with slash silent" onclick="copyEmoji('🔕')">🔕</div>

  <!-- Locks / security -->
  <div class="emoji" data-keywords="locked" onclick="copyEmoji('🔒')">🔒</div>
  <div class="emoji" data-keywords="unlocked" onclick="copyEmoji('🔓')">🔓</div>
  <div class="emoji" data-keywords="locked with pen" onclick="copyEmoji('🔏')">🔏</div>
  <div class="emoji" data-keywords="locked with key" onclick="copyEmoji('🔐')">🔐</div>
  <div class="emoji" data-keywords="key" onclick="copyEmoji('🔑')">🔑</div>
  <div class="emoji" data-keywords="old key" onclick="copyEmoji('🗝️')">🗝️</div>

  <!-- Currency / numbers -->
  <div class="emoji" data-keywords="dollar banknote money" onclick="copyEmoji('💵')">💵</div>
  <div class="emoji" data-keywords="euro banknote" onclick="copyEmoji('💶')">💶</div>
  <div class="emoji" data-keywords="pound banknote" onclick="copyEmoji('💷')">💷</div>
  <div class="emoji" data-keywords="yen banknote" onclick="copyEmoji('💴')">💴</div>
  <div class="emoji" data-keywords="heavy dollar sign" onclick="copyEmoji('💲')">💲</div>
  <div class="emoji" data-keywords="currency exchange" onclick="copyEmoji('💱')">💱</div>
  <div class="emoji" data-keywords="input numbers" onclick="copyEmoji('🔢')">🔢</div>
  <div class="emoji" data-keywords="1234 input" onclick="copyEmoji('🔢')">🔢</div>

  <!-- Misc UI icons -->
  <div class="emoji" data-keywords="gear settings cog" onclick="copyEmoji('⚙️')">⚙️</div>
  <div class="emoji" data-keywords="wrench tool" onclick="copyEmoji('🔧')">🔧</div>
  <div class="emoji" data-keywords="hammer tool" onclick="copyEmoji('🔨')">🔨</div>
  <div class="emoji" data-keywords="link symbol" onclick="copyEmoji('🔗')">🔗</div>
  <div class="emoji" data-keywords="paperclip" onclick="copyEmoji('📎')">📎</div>
  <div class="emoji" data-keywords="linked paperclips" onclick="copyEmoji('🖇️')">🖇️</div>
  <div class="emoji" data-keywords="bookmark tabs" onclick="copyEmoji('📑')">📑</div>
  <div class="emoji" data-keywords="pushpin" onclick="copyEmoji('📌')">📌</div>
  <div class="emoji" data-keywords="round pushpin" onclick="copyEmoji('📍')">📍</div>

  <!-- Religion / peace -->
  <div class="emoji" data-keywords="latin cross christian" onclick="copyEmoji('✝️')">✝️</div>
  <div class="emoji" data-keywords="star and crescent islam" onclick="copyEmoji('☪️')">☪️</div>
  <div class="emoji" data-keywords="star of david jewish" onclick="copyEmoji('✡️')">✡️</div>
  <div class="emoji" data-keywords="om symbol hindu" onclick="copyEmoji('🕉️')">🕉️</div>
  <div class="emoji" data-keywords="peace symbol" onclick="copyEmoji('☮️')">☮️</div>
  <div class="emoji" data-keywords="yin yang" onclick="copyEmoji('☯️')">☯️</div>

  <!-- Zodiac -->
  <div class="emoji" data-keywords="aries zodiac" onclick="copyEmoji('♈')">♈</div>
  <div class="emoji" data-keywords="taurus zodiac" onclick="copyEmoji('♉')">♉</div>
  <div class="emoji" data-keywords="gemini zodiac" onclick="copyEmoji('♊')">♊</div>
  <div class="emoji" data-keywords="cancer zodiac" onclick="copyEmoji('♋')">♋</div>
  <div class="emoji" data-keywords="leo zodiac" onclick="copyEmoji('♌')">♌</div>
  <div class="emoji" data-keywords="virgo zodiac" onclick="copyEmoji('♍')">♍</div>
  <div class="emoji" data-keywords="libra zodiac" onclick="copyEmoji('♎')">♎</div>
  <div class="emoji" data-keywords="scorpius zodiac" onclick="copyEmoji('♏')">♏</div>
  <div class="emoji" data-keywords="sagittarius zodiac" onclick="copyEmoji('♐')">♐</div>
  <div class="emoji" data-keywords="capricorn zodiac" onclick="copyEmoji('♑')">♑</div>
  <div class="emoji" data-keywords="aquarius zodiac" onclick="copyEmoji('♒')">♒</div>
  <div class="emoji" data-keywords="pisces zodiac" onclick="copyEmoji('♓')">♓</div>

  <!-- Infinity / math-ish -->
  <div class="emoji" data-keywords="infinity symbol" onclick="copyEmoji('♾️')">♾️</div>
  <div class="emoji" data-keywords="recycling symbol" onclick="copyEmoji('♻️')">♻️</div>
  <div class="emoji" data-keywords="copyright" onclick="copyEmoji('©️')">©️</div>
  <div class="emoji" data-keywords="registered" onclick="copyEmoji('®️')">®️</div>
  <div class="emoji" data-keywords="trademark" onclick="copyEmoji('™️')">™️</div>
  <div class="emoji" data-keywords="double curly loop" onclick="copyEmoji('➿')">➿</div>
<div class="emoji" data-keywords="curl loop" onclick="copyEmoji('➰')">➰</div>
<div class="emoji" data-keywords="wavy dash" onclick="copyEmoji('〰️')">〰️</div>
<div class="emoji" data-keywords="hollow red circle record" onclick="copyEmoji('⭕')">⭕</div>
<div class="emoji" data-keywords="black small square" onclick="copyEmoji('▪️')">▪️</div>
<div class="emoji" data-keywords="white small square" onclick="copyEmoji('▫️')">▫️</div>
<div class="emoji" data-keywords="black medium square" onclick="copyEmoji('◼️')">◼️</div>
<div class="emoji" data-keywords="white medium square" onclick="copyEmoji('◻️')">◻️</div>
<div class="emoji" data-keywords="black medium small square" onclick="copyEmoji('◾')">◾</div>
<div class="emoji" data-keywords="white medium small square" onclick="copyEmoji('◽')">◽</div>
<div class="emoji" data-keywords="white large square" onclick="copyEmoji('⬜')">⬜</div>
<div class="emoji" data-keywords="black large square" onclick="copyEmoji('⬛')">⬛</div>
<div class="emoji" data-keywords="red circle" onclick="copyEmoji('🔴')">🔴</div>
<div class="emoji" data-keywords="yellow circle" onclick="copyEmoji('🟡')">🟡</div>
<div class="emoji" data-keywords="green circle" onclick="copyEmoji('🟢')">🟢</div>
<div class="emoji" data-keywords="purple circle" onclick="copyEmoji('🟣')">🟣</div>
<div class="emoji" data-keywords="brown circle" onclick="copyEmoji('🟤')">🟤</div>
<div class="emoji" data-keywords="white circle" onclick="copyEmoji('⚪')">⚪</div>
<div class="emoji" data-keywords="black circle" onclick="copyEmoji('⚫')">⚫</div>
<div class="emoji" data-keywords="hollow red diamond" onclick="copyEmoji('♦️')">♦️</div>
<div class="emoji" data-keywords="black club suit" onclick="copyEmoji('♣️')">♣️</div>
<div class="emoji" data-keywords="black spade suit" onclick="copyEmoji('♠️')">♠️</div>
<div class="emoji" data-keywords="black heart suit" onclick="copyEmoji('♥️')">♥️</div>
<div class="emoji" data-keywords="joker playing card" onclick="copyEmoji('🃏')">🃏</div>
<div class="emoji" data-keywords="mahjong red dragon" onclick="copyEmoji('🀄')">🀄</div>

<div class="emoji" data-keywords="left right arrow" onclick="copyEmoji('↔️')">↔️</div>
<div class="emoji" data-keywords="up down arrow" onclick="copyEmoji('↕️')">↕️</div>
<div class="emoji" data-keywords="top arrow" onclick="copyEmoji('🔝')">🔝</div>
<div class="emoji" data-keywords="end arrow" onclick="copyEmoji('🔚')">🔚</div>
<div class="emoji" data-keywords="on arrow" onclick="copyEmoji('🔛')">🔛</div>
<div class="emoji" data-keywords="soon arrow" onclick="copyEmoji('🔜')">🔜</div>
<div class="emoji" data-keywords="back arrow" onclick="copyEmoji('🔙')">🔙</div>

<div class="emoji" data-keywords="sparkle asterisk symbol" onclick="copyEmoji('✳️')">✳️</div>
<div class="emoji" data-keywords="eight spoked asterisk" onclick="copyEmoji('✳️')">✳️</div>
<div class="emoji" data-keywords="eight pointed star" onclick="copyEmoji('✴️')">✴️</div>
<div class="emoji" data-keywords="star of david" onclick="copyEmoji('✡️')">✡️</div>
<div class="emoji" data-keywords="white star" onclick="copyEmoji('☆')">☆</div>

<div class="emoji" data-keywords="black small diamond" onclick="copyEmoji('◆')">◆</div>
<div class="emoji" data-keywords="white small diamond" onclick="copyEmoji('◇')">◇</div>

<div class="emoji" data-keywords="double vertical bar pause" onclick="copyEmoji('⏸️')">⏸️</div>
<div class="emoji" data-keywords="black square for stop" onclick="copyEmoji('⏹️')">⏹️</div>
<div class="emoji" data-keywords="black circle for record" onclick="copyEmoji('⏺️')">⏺️</div>

<div class="emoji" data-keywords="input latin letters" onclick="copyEmoji('🔤')">🔤</div>
<div class="emoji" data-keywords="input uppercase letters" onclick="copyEmoji('🔠')">🔠</div>
<div class="emoji" data-keywords="input lowercase letters" onclick="copyEmoji('🔡')">🔡</div>
<div class="emoji" data-keywords="input symbols" onclick="copyEmoji('🔣')">🔣</div>

<div class="emoji" data-keywords="ab button" onclick="copyEmoji('🆎')">🆎</div>
<div class="emoji" data-keywords="cl button" onclick="copyEmoji('🆑')">🆑</div>
<div class="emoji" data-keywords="sos button" onclick="copyEmoji('🆘')">🆘</div>
<div class="emoji" data-keywords="new button" onclick="copyEmoji('🆕')">🆕</div>
<div class="emoji" data-keywords="up button" onclick="copyEmoji('🆙')">🆙</div>
<div class="emoji" data-keywords="cool button" onclick="copyEmoji('🆒')">🆒</div>
<div class="emoji" data-keywords="free button" onclick="copyEmoji('🆓')">🆓</div>
<div class="emoji" data-keywords="id button" onclick="copyEmoji('🆔')">🆔</div>
<div class="emoji" data-keywords="ok button" onclick="copyEmoji('🆗')">🆗</div>
<div class="emoji" data-keywords="ng button" onclick="copyEmoji('🆖')">🆖</div>

<div class="emoji" data-keywords="circled m metro" onclick="copyEmoji('Ⓜ️')">Ⓜ️</div>
<div class="emoji" data-keywords="circled letter p parking" onclick="copyEmoji('🅿️')">🅿️</div>
<div class="emoji" data-keywords="no one under eighteen 18" onclick="copyEmoji('🔞')">🔞</div>
<div class="emoji" data-keywords="no mobile phones" onclick="copyEmoji('📵')">📵</div>
<div class="emoji" data-keywords="non potable water" onclick="copyEmoji('🚱')">🚱</div>
<div class="emoji" data-keywords="potable water" onclick="copyEmoji('🚰')">🚰</div>
<div class="emoji" data-keywords="wheelchair symbol accessibility" onclick="copyEmoji('♿')">♿</div>
<div class="emoji" data-keywords="restroom wc" onclick="copyEmoji('🚻')">🚻</div>
<div class="emoji" data-keywords="men’s room" onclick="copyEmoji('🚹')">🚹</div>
<div class="emoji" data-keywords="women’s room" onclick="copyEmoji('🚺')">🚺</div>
<div class="emoji" data-keywords="baby symbol changing" onclick="copyEmoji('🚼')">🚼</div>
<div class="emoji" data-keywords="passport control" onclick="copyEmoji('🛂')">🛂</div>
<div class="emoji" data-keywords="customs" onclick="copyEmoji('🛃')">🛃</div>
<div class="emoji" data-keywords="baggage claim" onclick="copyEmoji('🛄')">🛄</div>
<div class="emoji" data-keywords="left luggage" onclick="copyEmoji('🛅')">🛅</div>

</div>

<div class="category">
  <h2>⚽ Sports & Activities</h2>

  <!-- Balls & games -->
  <div class="emoji" data-keywords="soccer football ball sport" onclick="copyEmoji('⚽')">⚽</div>
  <div class="emoji" data-keywords="basketball ball sport" onclick="copyEmoji('🏀')">🏀</div>
  <div class="emoji" data-keywords="american football ball sport" onclick="copyEmoji('🏈')">🏈</div>
  <div class="emoji" data-keywords="baseball ball sport" onclick="copyEmoji('⚾')">⚾</div>
  <div class="emoji" data-keywords="softball ball sport" onclick="copyEmoji('🥎')">🥎</div>
  <div class="emoji" data-keywords="tennis ball sport" onclick="copyEmoji('🎾')">🎾</div>
  <div class="emoji" data-keywords="volleyball ball sport" onclick="copyEmoji('🏐')">🏐</div>
  <div class="emoji" data-keywords="rugby football ball sport" onclick="copyEmoji('🏉')">🏉</div>
  <div class="emoji" data-keywords="flying disc frisbee sport" onclick="copyEmoji('🥏')">🥏</div>
  <div class="emoji" data-keywords="ping pong table tennis" onclick="copyEmoji('🏓')">🏓</div>
  <div class="emoji" data-keywords="badminton racquet shuttlecock" onclick="copyEmoji('🏸')">🏸</div>
  <div class="emoji" data-keywords="field hockey stick ball" onclick="copyEmoji('🏑')">🏑</div>
  <div class="emoji" data-keywords="ice hockey stick puck" onclick="copyEmoji('🏒')">🏒</div>
  <div class="emoji" data-keywords="lacrosse stick ball" onclick="copyEmoji('🥍')">🥍</div>
  <div class="emoji" data-keywords="cricket game bat ball" onclick="copyEmoji('🏏')">🏏</div>
  <div class="emoji" data-keywords="bowling ball pins" onclick="copyEmoji('🎳')">🎳</div>
  <div class="emoji" data-keywords="billiards 8 ball pool" onclick="copyEmoji('🎱')">🎱</div>

  <!-- People doing sports -->
  <div class="emoji" data-keywords="person running runner" onclick="copyEmoji('🏃')">🏃</div>
  <div class="emoji" data-keywords="person walking" onclick="copyEmoji('🚶')">🚶</div>
  <div class="emoji" data-keywords="person surfing" onclick="copyEmoji('🏄')">🏄</div>
  <div class="emoji" data-keywords="person swimming" onclick="copyEmoji('🏊')">🏊</div>
  <div class="emoji" data-keywords="person golfing" onclick="copyEmoji('🏌️')">🏌️</div>
  <div class="emoji" data-keywords="person biking bicycle" onclick="copyEmoji('🚴')">🚴</div>
  <div class="emoji" data-keywords="person mountain biking" onclick="copyEmoji('🚵')">🚵</div>
  <div class="emoji" data-keywords="horse racing jockey" onclick="copyEmoji('🏇')">🏇</div>
  <div class="emoji" data-keywords="skier skiing" onclick="copyEmoji('⛷️')">⛷️</div>
  <div class="emoji" data-keywords="snowboarder snowboarding" onclick="copyEmoji('🏂')">🏂</div>
  <div class="emoji" data-keywords="person fencing" onclick="copyEmoji('🤺')">🤺</div>
  <div class="emoji" data-keywords="person lifting weights gym" onclick="copyEmoji('🏋️')">🏋️</div>
  <div class="emoji" data-keywords="person doing cartwheel gymnastics" onclick="copyEmoji('🤸')">🤸</div>
  <div class="emoji" data-keywords="person playing handball" onclick="copyEmoji('🤾')">🤾</div>
  <div class="emoji" data-keywords="person playing water polo" onclick="copyEmoji('🤽')">🤽</div>
  <div class="emoji" data-keywords="person bouncing ball basketball" onclick="copyEmoji('⛹️')">⛹️</div>
  <div class="emoji" data-keywords="person in lotus position yoga" onclick="copyEmoji('🧘')">🧘</div>

  <!-- Equipment -->
  <div class="emoji" data-keywords="fishing pole fish" onclick="copyEmoji('🎣')">🎣</div>
  <div class="emoji" data-keywords="boxing glove" onclick="copyEmoji('🥊')">🥊</div>
  <div class="emoji" data-keywords="martial arts uniform karate judo" onclick="copyEmoji('🥋')">🥋</div>
  <div class="emoji" data-keywords="goal net" onclick="copyEmoji('🥅')">🥅</div>
  <div class="emoji" data-keywords="ice skate" onclick="copyEmoji('⛸️')">⛸️</div>
  <div class="emoji" data-keywords="skateboard" onclick="copyEmoji('🛹')">🛹</div>
  <div class="emoji" data-keywords="sled" onclick="copyEmoji('🛷')">🛷</div>
  <div class="emoji" data-keywords="canoe boat" onclick="copyEmoji('🛶')">🛶</div>

  <!-- Hobbies / games -->
  <div class="emoji" data-keywords="video game controller" onclick="copyEmoji('🎮')">🎮</div>
  <div class="emoji" data-keywords="joystick retro game" onclick="copyEmoji('🕹️')">🕹️</div>
  <div class="emoji" data-keywords="trophy award" onclick="copyEmoji('🏆')">🏆</div>
  <div class="emoji" data-keywords="sports medal" onclick="copyEmoji('🏅')">🏅</div>
  <div class="emoji" data-keywords="first place medal gold" onclick="copyEmoji('🥇')">🥇</div>
  <div class="emoji" data-keywords="second place medal silver" onclick="copyEmoji('🥈')">🥈</div>
  <div class="emoji" data-keywords="third place medal bronze" onclick="copyEmoji('🥉')">🥉</div>
  <div class="emoji" data-keywords="direct hit dart bullseye" onclick="copyEmoji('🎯')">🎯</div>
  <div class="emoji" data-keywords="game die dice" onclick="copyEmoji('🎲')">🎲</div>
  <div class="emoji" data-keywords="puzzle piece" onclick="copyEmoji('🧩')">🧩</div>
  <div class="emoji" data-keywords="slot machine" onclick="copyEmoji('🎰')">🎰</div>
  <div class="emoji" data-keywords="jo-jo yoyo toy" onclick="copyEmoji('🪀')">🪀</div>
  <div class="emoji" data-keywords="kite" onclick="copyEmoji('🪁')">🪁</div>
  <div class="emoji" data-keywords="pool 8 ball billiards" onclick="copyEmoji('🎱')">🎱</div>

  <!-- Party / events -->
  <div class="emoji" data-keywords="party popper celebration" onclick="copyEmoji('🎉')">🎉</div>
  <div class="emoji" data-keywords="confetti ball party" onclick="copyEmoji('🎊')">🎊</div>
  <div class="emoji" data-keywords="balloon birthday" onclick="copyEmoji('🎈')">🎈</div>
  <div class="emoji" data-keywords="ribbon decoration" onclick="copyEmoji('🎀')">🎀</div>
  <div class="emoji" data-keywords="wrapped gift present" onclick="copyEmoji('🎁')">🎁</div>
  <div class="emoji" data-keywords="ticket event" onclick="copyEmoji('🎟️')">🎟️</div>
  <div class="emoji" data-keywords="admission tickets" onclick="copyEmoji('🎫')">🎫</div>
</div>

 <div class="category">
  <h2>🌍 Travel & Places</h2>

  <!-- Maps & earth -->
  <div class="emoji" data-keywords="globe showing europe africa world earth" onclick="copyEmoji('🌍')">🌍</div>
  <div class="emoji" data-keywords="globe showing americas world earth" onclick="copyEmoji('🌎')">🌎</div>
  <div class="emoji" data-keywords="globe showing asia australia world earth" onclick="copyEmoji('🌏')">🌏</div>
  <div class="emoji" data-keywords="globe with meridians world" onclick="copyEmoji('🌐')">🌐</div>
  <div class="emoji" data-keywords="world map" onclick="copyEmoji('🗺️')">🗺️</div>
  <div class="emoji" data-keywords="map of japan" onclick="copyEmoji('🗾')">🗾</div>
  <div class="emoji" data-keywords="compass navigation" onclick="copyEmoji('🧭')">🧭</div>

  <!-- Nature / landscapes -->
  <div class="emoji" data-keywords="snow capped mountain" onclick="copyEmoji('🏔️')">🏔️</div>
  <div class="emoji" data-keywords="mountain" onclick="copyEmoji('⛰️')">⛰️</div>
  <div class="emoji" data-keywords="volcano" onclick="copyEmoji('🌋')">🌋</div>
  <div class="emoji" data-keywords="mount fuji japan" onclick="copyEmoji('🗻')">🗻</div>
  <div class="emoji" data-keywords="desert" onclick="copyEmoji('🏜️')">🏜️</div>
  <div class="emoji" data-keywords="desert island tropical" onclick="copyEmoji('🏝️')">🏝️</div>
  <div class="emoji" data-keywords="national park landscape" onclick="copyEmoji('🏞️')">🏞️</div>
  <div class="emoji" data-keywords="beach with umbrella sea" onclick="copyEmoji('🏖️')">🏖️</div>
  <div class="emoji" data-keywords="camping tent night" onclick="copyEmoji('🏕️')">🏕️</div>
  <div class="emoji" data-keywords="stadium sports arena" onclick="copyEmoji('🏟️')">🏟️</div>

  <!-- City & sky scenes -->
  <div class="emoji" data-keywords="foggy city bridge" onclick="copyEmoji('🌁')">🌁</div>
  <div class="emoji" data-keywords="night with stars" onclick="copyEmoji('🌃')">🌃</div>
  <div class="emoji" data-keywords="sunrise over mountains" onclick="copyEmoji('🌄')">🌄</div>
  <div class="emoji" data-keywords="sunrise" onclick="copyEmoji('🌅')">🌅</div>
  <div class="emoji" data-keywords="cityscape" onclick="copyEmoji('🏙️')">🏙️</div>
  <div class="emoji" data-keywords="cityscape at dusk" onclick="copyEmoji('🌆')">🌆</div>
  <div class="emoji" data-keywords="sunset" onclick="copyEmoji('🌇')">🌇</div>
  <div class="emoji" data-keywords="bridge at night" onclick="copyEmoji('🌉')">🌉</div>

  <!-- Buildings -->
  <div class="emoji" data-keywords="house" onclick="copyEmoji('🏠')">🏠</div>
  <div class="emoji" data-keywords="house with garden" onclick="copyEmoji('🏡')">🏡</div>
  <div class="emoji" data-keywords="office building" onclick="copyEmoji('🏢')">🏢</div>
  <div class="emoji" data-keywords="japanese post office" onclick="copyEmoji('🏣')">🏣</div>
  <div class="emoji" data-keywords="post office" onclick="copyEmoji('🏤')">🏤</div>
  <div class="emoji" data-keywords="hospital" onclick="copyEmoji('🏥')">🏥</div>
  <div class="emoji" data-keywords="bank" onclick="copyEmoji('🏦')">🏦</div>
  <div class="emoji" data-keywords="hotel" onclick="copyEmoji('🏨')">🏨</div>
  <div class="emoji" data-keywords="love hotel" onclick="copyEmoji('🏩')">🏩</div>
  <div class="emoji" data-keywords="convenience store" onclick="copyEmoji('🏪')">🏪</div>
  <div class="emoji" data-keywords="school" onclick="copyEmoji('🏫')">🏫</div>
  <div class="emoji" data-keywords="department store" onclick="copyEmoji('🏬')">🏬</div>
  <div class="emoji" data-keywords="factory" onclick="copyEmoji('🏭')">🏭</div>
  <div class="emoji" data-keywords="japanese castle" onclick="copyEmoji('🏯')">🏯</div>
  <div class="emoji" data-keywords="castle" onclick="copyEmoji('🏰')">🏰</div>
  <div class="emoji" data-keywords="derelict house abandoned" onclick="copyEmoji('🏚️')">🏚️</div>

  <!-- Landmarks & religious buildings -->
  <div class="emoji" data-keywords="classical building museum" onclick="copyEmoji('🏛️')">🏛️</div>
  <div class="emoji" data-keywords="wedding church chapel" onclick="copyEmoji('💒')">💒</div>
  <div class="emoji" data-keywords="tokyo tower" onclick="copyEmoji('🗼')">🗼</div>
  <div class="emoji" data-keywords="statue of liberty" onclick="copyEmoji('🗽')">🗽</div>
  <div class="emoji" data-keywords="church" onclick="copyEmoji('⛪')">⛪</div>
  <div class="emoji" data-keywords="mosque" onclick="copyEmoji('🕌')">🕌</div>
  <div class="emoji" data-keywords="synagogue" onclick="copyEmoji('🕍')">🕍</div>
  <div class="emoji" data-keywords="hindu temple" onclick="copyEmoji('🛕')">🛕</div>
  <div class="emoji" data-keywords="shinto shrine" onclick="copyEmoji('⛩️')">⛩️</div>
  <div class="emoji" data-keywords="kaaba" onclick="copyEmoji('🕋')">🕋</div>
  <div class="emoji" data-keywords="fountain" onclick="copyEmoji('⛲')">⛲</div>

  <!-- Transport & places-lite icons -->
  <div class="emoji" data-keywords="bus stop sign" onclick="copyEmoji('🚏')">🚏</div>
  <div class="emoji" data-keywords="fuel pump petrol gas station" onclick="copyEmoji('⛽')">⛽</div>
  <div class="emoji" data-keywords="anchor port harbor" onclick="copyEmoji('⚓')">⚓</div>
  <div class="emoji" data-keywords="construction barrier roadwork" onclick="copyEmoji('🚧')">🚧</div>
  <div class="emoji" data-keywords="vertical traffic light" onclick="copyEmoji('🚦')">🚦</div>
  <div class="emoji" data-keywords="horizontal traffic light" onclick="copyEmoji('🚥')">🚥</div>
</div>

 <div class="category">
  <h2>💡 Tools & Tech</h2>

  <!-- Phones & communication -->
  <div class="emoji" data-keywords="mobile phone smartphone" onclick="copyEmoji('📱')">📱</div>
  <div class="emoji" data-keywords="mobile phone with arrow send" onclick="copyEmoji('📲')">📲</div>
  <div class="emoji" data-keywords="telephone receiver call" onclick="copyEmoji('📞')">📞</div>
  <div class="emoji" data-keywords="telephone" onclick="copyEmoji('☎️')">☎️</div>
  <div class="emoji" data-keywords="fax machine" onclick="copyEmoji('📠')">📠</div>
  <div class="emoji" data-keywords="pager" onclick="copyEmoji('📟')">📟</div>
  <div class="emoji" data-keywords="satellite antenna dish" onclick="copyEmoji('📡')">📡</div>

  <!-- Computers & screens -->
  <div class="emoji" data-keywords="laptop computer pc" onclick="copyEmoji('💻')">💻</div>
  <div class="emoji" data-keywords="desktop computer pc" onclick="copyEmoji('🖥️')">🖥️</div>
  <div class="emoji" data-keywords="printer" onclick="copyEmoji('🖨️')">🖨️</div>
  <div class="emoji" data-keywords="keyboard" onclick="copyEmoji('⌨️')">⌨️</div>
  <div class="emoji" data-keywords="computer mouse" onclick="copyEmoji('🖱️')">🖱️</div>
  <div class="emoji" data-keywords="trackball" onclick="copyEmoji('🖲️')">🖲️</div>
  <div class="emoji" data-keywords="minidisc disc" onclick="copyEmoji('💽')">💽</div>
  <div class="emoji" data-keywords="floppy disk" onclick="copyEmoji('💾')">💾</div>
  <div class="emoji" data-keywords="optical disc cd" onclick="copyEmoji('📀')">📀</div>
  <div class="emoji" data-keywords="dvd disc" onclick="copyEmoji('💿')">💿</div>

  <!-- Power & light -->
  <div class="emoji" data-keywords="battery" onclick="copyEmoji('🔋')">🔋</div>
  <div class="emoji" data-keywords="electric plug power" onclick="copyEmoji('🔌')">🔌</div>
  <div class="emoji" data-keywords="light bulb idea" onclick="copyEmoji('💡')">💡</div>
  <div class="emoji" data-keywords="flashlight torch" onclick="copyEmoji('🔦')">🔦</div>
  <div class="emoji" data-keywords="candle" onclick="copyEmoji('🕯️')">🕯️</div>
  <div class="emoji" data-keywords="diya lamp" onclick="copyEmoji('🪔')">🪔</div>
  <div class="emoji" data-keywords="magnifying glass tilted left search" onclick="copyEmoji('🔍')">🔍</div>
  <div class="emoji" data-keywords="magnifying glass tilted right search" onclick="copyEmoji('🔎')">🔎</div>

  <!-- Coding / dev-friendly -->
  <div class="emoji" data-keywords="gear cog settings" onclick="copyEmoji('⚙️')">⚙️</div>
  <div class="emoji" data-keywords="hammer and wrench tools" onclick="copyEmoji('🛠️')">🛠️</div>
  <div class="emoji" data-keywords="wrench tool" onclick="copyEmoji('🔧')">🔧</div>
  <div class="emoji" data-keywords="screwdriver tool" onclick="copyEmoji('🪛')">🪛</div>
  <div class="emoji" data-keywords="hammer tool" onclick="copyEmoji('🔨')">🔨</div>
  <div class="emoji" data-keywords="axe tool" onclick="copyEmoji('🪓')">🪓</div>
  <div class="emoji" data-keywords="pick pickaxe mining" onclick="copyEmoji('⛏️')">⛏️</div>
  <div class="emoji" data-keywords="hammer and pick tools" onclick="copyEmoji('⚒️')">⚒️</div>
  <div class="emoji" data-keywords="nut and bolt hardware" onclick="copyEmoji('🔩')">🔩</div>
  <div class="emoji" data-keywords="clamp vice" onclick="copyEmoji('🗜️')">🗜️</div>
  <div class="emoji" data-keywords="carpentry saw" onclick="copyEmoji('🪚')">🪚</div>
  <div class="emoji" data-keywords="toolbox tools" onclick="copyEmoji('🧰')">🧰</div>
  <div class="emoji" data-keywords="brick wall" onclick="copyEmoji('🧱')">🧱</div>

  <!-- Science & lab -->
  <div class="emoji" data-keywords="microscope lab science" onclick="copyEmoji('🔬')">🔬</div>
  <div class="emoji" data-keywords="telescope space" onclick="copyEmoji('🔭')">🔭</div>
  <div class="emoji" data-keywords="satellite antenna" onclick="copyEmoji('📡')">📡</div>
  <div class="emoji" data-keywords="test tube lab" onclick="copyEmoji('🧪')">🧪</div>
  <div class="emoji" data-keywords="petri dish lab" onclick="copyEmoji('🧫')">🧫</div>
  <div class="emoji" data-keywords="dna double helix" onclick="copyEmoji('🧬')">🧬</div>
  <div class="emoji" data-keywords="syringe injection" onclick="copyEmoji('💉')">💉</div>
  <div class="emoji" data-keywords="pill capsule medicine" onclick="copyEmoji('💊')">💊</div>
  <div class="emoji" data-keywords="stethoscope medical" onclick="copyEmoji('🩺')">🩺</div>

  <!-- Security / keys (tech-adjacent) -->
  <div class="emoji" data-keywords="locked" onclick="copyEmoji('🔒')">🔒</div>
  <div class="emoji" data-keywords="unlocked" onclick="copyEmoji('🔓')">🔓</div>
  <div class="emoji" data-keywords="lock with ink pen" onclick="copyEmoji('🔏')">🔏</div>
  <div class="emoji" data-keywords="lock with key" onclick="copyEmoji('🔐')">🔐</div>
  <div class="emoji" data-keywords="key" onclick="copyEmoji('🔑')">🔑</div>
  <div class="emoji" data-keywords="old key" onclick="copyEmoji('🗝️')">🗝️</div>
  <div class="emoji" data-keywords="joystick game controller retro" onclick="copyEmoji('🕹️')">🕹️</div>
<div class="emoji" data-keywords="video game controller console" onclick="copyEmoji('🎮')">🎮</div>
<div class="emoji" data-keywords="headphone audio music" onclick="copyEmoji('🎧')">🎧</div>
<div class="emoji" data-keywords="studio microphone recording" onclick="copyEmoji('🎙️')">🎙️</div>
<div class="emoji" data-keywords="level slider audio mixer" onclick="copyEmoji('🎚️')">🎚️</div>
<div class="emoji" data-keywords="control knobs mixer" onclick="copyEmoji('🎛️')">🎛️</div>

<div class="emoji" data-keywords="radio" onclick="copyEmoji('📻')">📻</div>
<div class="emoji" data-keywords="television tv screen" onclick="copyEmoji('📺')">📺</div>
<div class="emoji" data-keywords="mobile phone off mute" onclick="copyEmoji('📴')">📴</div>
<div class="emoji" data-keywords="antenna bars signal" onclick="copyEmoji('📶')">📶</div>
<div class="emoji" data-keywords="satellite orbit space" onclick="copyEmoji('🛰️')">🛰️</div>
<div class="emoji" data-keywords="radar" onclick="copyEmoji('📡')">📡</div>

<div class="emoji" data-keywords="calculator" onclick="copyEmoji('🧮')">🧮</div>
<div class="emoji" data-keywords="printer office" onclick="copyEmoji('🖨️')">🖨️</div>
<div class="emoji" data-keywords="fax technology" onclick="copyEmoji('📠')">📠</div>
<div class="emoji" data-keywords="scanner photocopier" onclick="copyEmoji('🖨️')">🖨️</div>

<div class="emoji" data-keywords="watch wristwatch" onclick="copyEmoji('⌚')">⌚</div>
<div class="emoji" data-keywords="alarm clock" onclick="copyEmoji('⏰')">⏰</div>
<div class="emoji" data-keywords="stopwatch timer" onclick="copyEmoji('⏱️')">⏱️</div>
<div class="emoji" data-keywords="timer clock" onclick="copyEmoji('⏲️')">⏲️</div>
<div class="emoji" data-keywords="mantelpiece clock" onclick="copyEmoji('🕰️')">🕰️</div>
<div class="emoji" data-keywords="hourglass done" onclick="copyEmoji('⌛')">⌛</div>
<div class="emoji" data-keywords="hourglass not done loading" onclick="copyEmoji('⏳')">⏳</div>

<div class="emoji" data-keywords="link chain" onclick="copyEmoji('🔗')">🔗</div>
<div class="emoji" data-keywords="chains metal" onclick="copyEmoji('⛓️')">⛓️</div>
<div class="emoji" data-keywords="hook metal" onclick="copyEmoji('🪝')">🪝</div>
<div class="emoji" data-keywords="magnet horseshoe" onclick="copyEmoji('🧲')">🧲</div>

<div class="emoji" data-keywords="safety pin" onclick="copyEmoji('🧷')">🧷</div>
<div class="emoji" data-keywords="sewing needle" onclick="copyEmoji('🪡')">🪡</div>
<div class="emoji" data-keywords="thread spool" onclick="copyEmoji('🧵')">🧵</div>
<div class="emoji" data-keywords="yarn ball" onclick="copyEmoji('🧶')">🧶</div>

<div class="emoji" data-keywords="straight ruler measure" onclick="copyEmoji('📏')">📏</div>
<div class="emoji" data-keywords="triangular ruler set square" onclick="copyEmoji('📐')">📐</div>
<div class="emoji" data-keywords="abacus math" onclick="copyEmoji('🧮')">🧮</div>
<div class="emoji" data-keywords="clipboard" onclick="copyEmoji('📋')">📋</div>
<div class="emoji" data-keywords="file folder" onclick="copyEmoji('📁')">📁</div>
<div class="emoji" data-keywords="open file folder" onclick="copyEmoji('📂')">📂</div>
<div class="emoji" data-keywords="card index dividers" onclick="copyEmoji('🗂️')">🗂️</div>
<div class="emoji" data-keywords="calendar" onclick="copyEmoji('📅')">📅</div>
<div class="emoji" data-keywords="tear off calendar" onclick="copyEmoji('📆')">📆</div>

<div class="emoji" data-keywords="wastebasket bin trash" onclick="copyEmoji('🗑️')">🗑️</div>
<div class="emoji" data-keywords="file cabinet" onclick="copyEmoji('🗄️')">🗄️</div>
<div class="emoji" data-keywords="envelope email" onclick="copyEmoji('✉️')">✉️</div>
<div class="emoji" data-keywords="incoming envelope" onclick="copyEmoji('📨')">📨</div>
<div class="emoji" data-keywords="envelope with arrow outbox" onclick="copyEmoji('📩')">📩</div>
<div class="emoji" data-keywords="e-mail symbol" onclick="copyEmoji('📧')">📧</div>
<div class="emoji" data-keywords="inbox tray" onclick="copyEmoji('📥')">📥</div>
<div class="emoji" data-keywords="outbox tray" onclick="copyEmoji('📤')">📤</div>

<div class="emoji" data-keywords="package parcel" onclick="copyEmoji('📦')">📦</div>
<div class="emoji" data-keywords="money bag" onclick="copyEmoji('💰')">💰</div>
<div class="emoji" data-keywords="coin money" onclick="copyEmoji('🪙')">🪙</div>
<div class="emoji" data-keywords="credit card" onclick="copyEmoji('💳')">💳</div>
<div class="emoji" data-keywords="receipt bill" onclick="copyEmoji('🧾')">🧾</div>
<div class="emoji" data-keywords="bar chart graph" onclick="copyEmoji('📊')">📊</div>
<div class="emoji" data-keywords="chart increasing" onclick="copyEmoji('📈')">📈</div>
<div class="emoji" data-keywords="chart decreasing" onclick="copyEmoji('📉')">📉</div>

</div>

<div class="category">
  <h2>🚗 Cars & Vehicles</h2>

  <!-- Cars -->
  <div class="emoji" data-keywords="automobile car vehicle" onclick="copyEmoji('🚗')">🚗</div>
  <div class="emoji" data-keywords="oncoming automobile car" onclick="copyEmoji('🚘')">🚘</div>
  <div class="emoji" data-keywords="sport utility vehicle suv" onclick="copyEmoji('🚙')">🚙</div>
  <div class="emoji" data-keywords="racing car race" onclick="copyEmoji('🏎️')">🏎️</div>
  <div class="emoji" data-keywords="taxi cab" onclick="copyEmoji('🚕')">🚕</div>
  <div class="emoji" data-keywords="oncoming taxi cab" onclick="copyEmoji('🚖')">🚖</div>
  <div class="emoji" data-keywords="police car" onclick="copyEmoji('🚓')">🚓</div>
  <div class="emoji" data-keywords="oncoming police car" onclick="copyEmoji('🚔')">🚔</div>
  <div class="emoji" data-keywords="ambulance emergency" onclick="copyEmoji('🚑')">🚑</div>
  <div class="emoji" data-keywords="fire engine truck" onclick="copyEmoji('🚒')">🚒</div>
  <div class="emoji" data-keywords="pickup truck" onclick="copyEmoji('🛻')">🛻</div>
  <div class="emoji" data-keywords="delivery truck lorry" onclick="copyEmoji('🚚')">🚚</div>
  <div class="emoji" data-keywords="articulated lorry semi truck" onclick="copyEmoji('🚛')">🚛</div>
  <div class="emoji" data-keywords="tractor farm vehicle" onclick="copyEmoji('🚜')">🚜</div>

  <!-- Buses & public transport -->
  <div class="emoji" data-keywords="bus public transport" onclick="copyEmoji('🚌')">🚌</div>
  <div class="emoji" data-keywords="oncoming bus" onclick="copyEmoji('🚍')">🚍</div>
  <div class="emoji" data-keywords="trolleybus electric bus" onclick="copyEmoji('🚎')">🚎</div>
  <div class="emoji" data-keywords="minibus van" onclick="copyEmoji('🚐')">🚐</div>

  <!-- Bikes & small vehicles -->
  <div class="emoji" data-keywords="bicycle bike" onclick="copyEmoji('🚲')">🚲</div>
  <div class="emoji" data-keywords="kick scooter" onclick="copyEmoji('🛴')">🛴</div>
  <div class="emoji" data-keywords="motor scooter moped" onclick="copyEmoji('🛵')">🛵</div>
  <div class="emoji" data-keywords="auto rickshaw tuk tuk" onclick="copyEmoji('🛺')">🛺</div>
  <div class="emoji" data-keywords="motorcycle motorbike" onclick="copyEmoji('🏍️')">🏍️</div>

  <!-- Road / traffic signs -->
  <div class="emoji" data-keywords="motorway highway road" onclick="copyEmoji('🛣️')">🛣️</div>
  <div class="emoji" data-keywords="railway track rails" onclick="copyEmoji('🛤️')">🛤️</div>
  <div class="emoji" data-keywords="fuel pump petrol gas station" onclick="copyEmoji('⛽')">⛽</div>
  <div class="emoji" data-keywords="wheel tyre tire" onclick="copyEmoji('🛞')">🛞</div>
  <div class="emoji" data-keywords="police car light siren" onclick="copyEmoji('🚨')">🚨</div>
  <div class="emoji" data-keywords="horizontal traffic light" onclick="copyEmoji('🚥')">🚥</div>
  <div class="emoji" data-keywords="vertical traffic light" onclick="copyEmoji('🚦')">🚦</div>
  <div class="emoji" data-keywords="stop sign octagonal" onclick="copyEmoji('🛑')">🛑</div>
  <div class="emoji" data-keywords="construction barrier roadwork" onclick="copyEmoji('🚧')">🚧</div>
</div>

 <div class="category">
  <h2>🚀 Trains, Planes & Boats</h2>

  <!-- Trains -->
  <div class="emoji" data-keywords="locomotive train" onclick="copyEmoji('🚂')">🚂</div>
  <div class="emoji" data-keywords="railway car carriage" onclick="copyEmoji('🚃')">🚃</div>
  <div class="emoji" data-keywords="high speed train" onclick="copyEmoji('🚄')">🚄</div>
  <div class="emoji" data-keywords="bullet train" onclick="copyEmoji('🚅')">🚅</div>
  <div class="emoji" data-keywords="train railway" onclick="copyEmoji('🚆')">🚆</div>
  <div class="emoji" data-keywords="metro subway train" onclick="copyEmoji('🚇')">🚇</div>
  <div class="emoji" data-keywords="light rail tram" onclick="copyEmoji('🚈')">🚈</div>
  <div class="emoji" data-keywords="station platform" onclick="copyEmoji('🚉')">🚉</div>
  <div class="emoji" data-keywords="tram streetcar" onclick="copyEmoji('🚊')">🚊</div>
  <div class="emoji" data-keywords="monorail" onclick="copyEmoji('🚝')">🚝</div>
  <div class="emoji" data-keywords="mountain railway" onclick="copyEmoji('🚞')">🚞</div>
  <div class="emoji" data-keywords="suspension railway" onclick="copyEmoji('🚟')">🚟</div>
  <div class="emoji" data-keywords="railway track rails" onclick="copyEmoji('🛤️')">🛤️</div>

  <!-- Air -->
  <div class="emoji" data-keywords="airplane plane flight" onclick="copyEmoji('✈️')">✈️</div>
  <div class="emoji" data-keywords="small airplane plane" onclick="copyEmoji('🛩️')">🛩️</div>
  <div class="emoji" data-keywords="airplane departure takeoff" onclick="copyEmoji('🛫')">🛫</div>
  <div class="emoji" data-keywords="airplane arrival landing" onclick="copyEmoji('🛬')">🛬</div>
  <div class="emoji" data-keywords="seat airplane train" onclick="copyEmoji('💺')">💺</div>
  <div class="emoji" data-keywords="helicopter" onclick="copyEmoji('🚁')">🚁</div>
  <div class="emoji" data-keywords="parachute" onclick="copyEmoji('🪂')">🪂</div>
  <div class="emoji" data-keywords="satellite orbit space" onclick="copyEmoji('🛰️')">🛰️</div>
  <div class="emoji" data-keywords="rocket space" onclick="copyEmoji('🚀')">🚀</div>
  <div class="emoji" data-keywords="flying saucer ufo" onclick="copyEmoji('🛸')">🛸</div>

  <!-- Water -->
  <div class="emoji" data-keywords="sailboat boat" onclick="copyEmoji('⛵')">⛵</div>
  <div class="emoji" data-keywords="speedboat motorboat" onclick="copyEmoji('🚤')">🚤</div>
  <div class="emoji" data-keywords="passenger ship cruise" onclick="copyEmoji('🛳️')">🛳️</div>
  <div class="emoji" data-keywords="ferry boat" onclick="copyEmoji('⛴️')">⛴️</div>
  <div class="emoji" data-keywords="ship boat" onclick="copyEmoji('🚢')">🚢</div>
  <div class="emoji" data-keywords="canoe kayak" onclick="copyEmoji('🛶')">🛶</div>
  <div class="emoji" data-keywords="anchor harbor port" onclick="copyEmoji('⚓')">⚓</div>

  <!-- Cable / mountain transport -->
  <div class="emoji" data-keywords="aerial tramway cable car" onclick="copyEmoji('🚡')">🚡</div>
  <div class="emoji" data-keywords="mountain cableway" onclick="copyEmoji('🚠')">🚠</div>
  <div class="emoji" data-keywords="ropeway gondola" onclick="copyEmoji('🚡')">🚡</div>
</div>

 <div class="category">
  <h2>📚 School & Office</h2>

  <!-- Writing & drawing -->
  <div class="emoji" data-keywords="pencil writing" onclick="copyEmoji('✏️')">✏️</div>
  <div class="emoji" data-keywords="fountain pen" onclick="copyEmoji('🖋️')">🖋️</div>
  <div class="emoji" data-keywords="pen ballpoint" onclick="copyEmoji('🖊️')">🖊️</div>
  <div class="emoji" data-keywords="paintbrush art" onclick="copyEmoji('🖌️')">🖌️</div>
  <div class="emoji" data-keywords="crayon" onclick="copyEmoji('🖍️')">🖍️</div>
  <div class="emoji" data-keywords="memo pencil note" onclick="copyEmoji('📝')">📝</div>

  <!-- Books & study -->
  <div class="emoji" data-keywords="open book reading" onclick="copyEmoji('📖')">📖</div>
  <div class="emoji" data-keywords="books stack" onclick="copyEmoji('📚')">📚</div>
  <div class="emoji" data-keywords="blue book" onclick="copyEmoji('📘')">📘</div>
  <div class="emoji" data-keywords="orange book" onclick="copyEmoji('📙')">📙</div>
  <div class="emoji" data-keywords="green book" onclick="copyEmoji('📗')">📗</div>
  <div class="emoji" data-keywords="notebook" onclick="copyEmoji('📓')">📓</div>
  <div class="emoji" data-keywords="notebook with decorative cover" onclick="copyEmoji('📔')">📔</div>
  <div class="emoji" data-keywords="ledger book accounting" onclick="copyEmoji('📒')">📒</div>
  <div class="emoji" data-keywords="scroll document" onclick="copyEmoji('📜')">📜</div>
  <div class="emoji" data-keywords="page facing up document" onclick="copyEmoji('📄')">📄</div>
  <div class="emoji" data-keywords="page with curl" onclick="copyEmoji('📃')">📃</div>

  <!-- Paper & files -->
  <div class="emoji" data-keywords="bookmark" onclick="copyEmoji('🔖')">🔖</div>
  <div class="emoji" data-keywords="bookmark tabs" onclick="copyEmoji('📑')">📑</div>
  <div class="emoji" data-keywords="card index" onclick="copyEmoji('📇')">📇</div>
  <div class="emoji" data-keywords="clipboard" onclick="copyEmoji('📋')">📋</div>
  <div class="emoji" data-keywords="file folder" onclick="copyEmoji('📁')">📁</div>
  <div class="emoji" data-keywords="open file folder" onclick="copyEmoji('📂')">📂</div>
  <div class="emoji" data-keywords="card file box" onclick="copyEmoji('🗃️')">🗃️</div>
  <div class="emoji" data-keywords="file cabinet" onclick="copyEmoji('🗄️')">🗄️</div>
  <div class="emoji" data-keywords="wastebasket trash bin" onclick="copyEmoji('🗑️')">🗑️</div>

  <!-- Stationery -->
  <div class="emoji" data-keywords="pushpin pin" onclick="copyEmoji('📌')">📌</div>
  <div class="emoji" data-keywords="round pushpin location pin" onclick="copyEmoji('📍')">📍</div>
  <div class="emoji" data-keywords="paperclip" onclick="copyEmoji('📎')">📎</div>
  <div class="emoji" data-keywords="linked paperclips" onclick="copyEmoji('🖇️')">🖇️</div>
  <div class="emoji" data-keywords="straight ruler measure" onclick="copyEmoji('📏')">📏</div>
  <div class="emoji" data-keywords="triangular ruler set square" onclick="copyEmoji('📐')">📐</div>
  <div class="emoji" data-keywords="round push button radio" onclick="copyEmoji('🔘')">🔘</div>

  <!-- Calendars & planning -->
  <div class="emoji" data-keywords="calendar" onclick="copyEmoji('📅')">📅</div>
  <div class="emoji" data-keywords="tear off calendar" onclick="copyEmoji('📆')">📆</div>
  <div class="emoji" data-keywords="spiral calendar" onclick="copyEmoji('🗓️')">🗓️</div>
  <div class="emoji" data-keywords="spiral notepad" onclick="copyEmoji('🗒️')">🗒️</div>

  <!-- Mail & inbox -->
  <div class="emoji" data-keywords="envelope mail letter" onclick="copyEmoji('✉️')">✉️</div>
  <div class="emoji" data-keywords="incoming envelope" onclick="copyEmoji('📨')">📨</div>
  <div class="emoji" data-keywords="envelope with arrow sent" onclick="copyEmoji('📩')">📩</div>
  <div class="emoji" data-keywords="e-mail symbol" onclick="copyEmoji('📧')">📧</div>
  <div class="emoji" data-keywords="inbox tray" onclick="copyEmoji('📥')">📥</div>
  <div class="emoji" data-keywords="outbox tray" onclick="copyEmoji('📤')">📤</div>
  <div class="emoji" data-keywords="package parcel" onclick="copyEmoji('📦')">📦</div>

  <!-- Charts & money (office-ish) -->
  <div class="emoji" data-keywords="chart increasing up graph" onclick="copyEmoji('📈')">📈</div>
  <div class="emoji" data-keywords="chart decreasing down graph" onclick="copyEmoji('📉')">📉</div>
  <div class="emoji" data-keywords="bar chart stats" onclick="copyEmoji('📊')">📊</div>
  <div class="emoji" data-keywords="money bag" onclick="copyEmoji('💰')">💰</div>
  <div class="emoji" data-keywords="coin money" onclick="copyEmoji('🪙')">🪙</div>
  <div class="emoji" data-keywords="credit card" onclick="copyEmoji('💳')">💳</div>
  <div class="emoji" data-keywords="receipt bill" onclick="copyEmoji('🧾')">🧾</div>
</div>

 <div class="category">
  <h2>🧥 Clothes & Style</h2>

  <!-- Head & face wear -->
  <div class="emoji" data-keywords="top hat" onclick="copyEmoji('🎩')">🎩</div>
  <div class="emoji" data-keywords="graduation cap" onclick="copyEmoji('🎓')">🎓</div>
  <div class="emoji" data-keywords="billed cap baseball hat" onclick="copyEmoji('🧢')">🧢</div>
  <div class="emoji" data-keywords="crown royal king queen" onclick="copyEmoji('👑')">👑</div>
  <div class="emoji" data-keywords="rescue worker helmet" onclick="copyEmoji('⛑️')">⛑️</div>
  <div class="emoji" data-keywords="womans hat" onclick="copyEmoji('👒')">👒</div>
  <div class="emoji" data-keywords="scarf" onclick="copyEmoji('🧣')">🧣</div>
  <div class="emoji" data-keywords="glasses eyeglasses" onclick="copyEmoji('👓')">👓</div>
  <div class="emoji" data-keywords="sunglasses shades" onclick="copyEmoji('🕶️')">🕶️</div>
  <div class="emoji" data-keywords="goggles safety" onclick="copyEmoji('🥽')">🥽</div>
  <div class="emoji" data-keywords="face mask medical" onclick="copyEmoji('😷')">😷</div>

  <!-- Upper body clothes -->
  <div class="emoji" data-keywords="t shirt tshirt" onclick="copyEmoji('👕')">👕</div>
  <div class="emoji" data-keywords="jeans trousers pants" onclick="copyEmoji('👖')">👖</div>
  <div class="emoji" data-keywords="coat jacket" onclick="copyEmoji('🧥')">🧥</div>
  <div class="emoji" data-keywords="dress" onclick="copyEmoji('👗')">👗</div>
  <div class="emoji" data-keywords="kimono robe" onclick="copyEmoji('👘')">👘</div>
  <div class="emoji" data-keywords="sari dress" onclick="copyEmoji('🥻')">🥻</div>
  <div class="emoji" data-keywords="one piece swimsuit" onclick="copyEmoji('🩱')">🩱</div>
  <div class="emoji" data-keywords="briefs underwear" onclick="copyEmoji('🩲')">🩲</div>
  <div class="emoji" data-keywords="shorts" onclick="copyEmoji('🩳')">🩳</div>
  <div class="emoji" data-keywords="lab coat doctor" onclick="copyEmoji('🥼')">🥼</div>
  <div class="emoji" data-keywords="safety vest" onclick="copyEmoji('🦺')">🦺</div>

  <!-- Footwear -->
  <div class="emoji" data-keywords="socks" onclick="copyEmoji('🧦')">🧦</div>
  <div class="emoji" data-keywords="running shoe sneaker" onclick="copyEmoji('👟')">👟</div>
  <div class="emoji" data-keywords="high heel shoe" onclick="copyEmoji('👠')">👠</div>
  <div class="emoji" data-keywords="womans sandal" onclick="copyEmoji('👡')">👡</div>
  <div class="emoji" data-keywords="boot" onclick="copyEmoji('👢')">👢</div>
  <div class="emoji" data-keywords="ballet shoes" onclick="copyEmoji('🩰')">🩰</div>
  <div class="emoji" data-keywords="flip flop sandal" onclick="copyEmoji('🩴')">🩴</div>

  <!-- Accessories & jewelry -->
  <div class="emoji" data-keywords="handbag purse" onclick="copyEmoji('👜')">👜</div>
  <div class="emoji" data-keywords="clutch bag" onclick="copyEmoji('👝')">👝</div>
  <div class="emoji" data-keywords="shopping bags" onclick="copyEmoji('🛍️')">🛍️</div>
  <div class="emoji" data-keywords="briefcase" onclick="copyEmoji('💼')">💼</div>
  <div class="emoji" data-keywords="school backpack bag" onclick="copyEmoji('🎒')">🎒</div>
  <div class="emoji" data-keywords="luggage suitcase" onclick="copyEmoji('🧳')">🧳</div>
  <div class="emoji" data-keywords="ring diamond" onclick="copyEmoji('💍')">💍</div>
  <div class="emoji" data-keywords="gem stone diamond" onclick="copyEmoji('💎')">💎</div>
  <div class="emoji" data-keywords="lipstick makeup" onclick="copyEmoji('💄')">💄</div>
  <div class="emoji" data-keywords="necklace jewelry" onclick="copyEmoji('📿')">📿</div>

  <!-- Badges & uniforms -->
  <div class="emoji" data-keywords="military medal" onclick="copyEmoji('🎖️')">🎖️</div>
  <div class="emoji" data-keywords="police badge shield" onclick="copyEmoji('🛡️')">🛡️</div>
</div>

 <div class="category">
  <h2>🌿 Nature & Weather</h2>

  <!-- Plants & trees -->
  <div class="emoji" data-keywords="seedling sprout plant" onclick="copyEmoji('🌱')">🌱</div>
  <div class="emoji" data-keywords="potted plant" onclick="copyEmoji('🪴')">🪴</div>
  <div class="emoji" data-keywords="herb plant" onclick="copyEmoji('🌿')">🌿</div>
  <div class="emoji" data-keywords="four leaf clover lucky" onclick="copyEmoji('🍀')">🍀</div>
  <div class="emoji" data-keywords="shamrock clover" onclick="copyEmoji('☘️')">☘️</div>
  <div class="emoji" data-keywords="fallen leaf autumn" onclick="copyEmoji('🍂')">🍂</div>
  <div class="emoji" data-keywords="maple leaf" onclick="copyEmoji('🍁')">🍁</div>
  <div class="emoji" data-keywords="leaf fluttering wind" onclick="copyEmoji('🍃')">🍃</div>
  <div class="emoji" data-keywords="sheaf of rice crop" onclick="copyEmoji('🌾')">🌾</div>
  <div class="emoji" data-keywords="ear of corn maize" onclick="copyEmoji('🌽')">🌽</div>
  <div class="emoji" data-keywords="grapes vine" onclick="copyEmoji('🍇')">🍇</div>
  <div class="emoji" data-keywords="mushroom" onclick="copyEmoji('🍄')">🍄</div>
  <div class="emoji" data-keywords="cactus desert" onclick="copyEmoji('🌵')">🌵</div>
  <div class="emoji" data-keywords="palm tree tropical" onclick="copyEmoji('🌴')">🌴</div>
  <div class="emoji" data-keywords="evergreen tree" onclick="copyEmoji('🌲')">🌲</div>
  <div class="emoji" data-keywords="deciduous tree" onclick="copyEmoji('🌳')">🌳</div>
  <div class="emoji" data-keywords="tanabata tree" onclick="copyEmoji('🎋')">🎋</div>

  <!-- Flowers -->
  <div class="emoji" data-keywords="cherry blossom flower sakura" onclick="copyEmoji('🌸')">🌸</div>
  <div class="emoji" data-keywords="white flower" onclick="copyEmoji('💮')">💮</div>
  <div class="emoji" data-keywords="rosette flower badge" onclick="copyEmoji('🏵️')">🏵️</div>
  <div class="emoji" data-keywords="bouquet flowers" onclick="copyEmoji('💐')">💐</div>
  <div class="emoji" data-keywords="rose flower" onclick="copyEmoji('🌹')">🌹</div>
  <div class="emoji" data-keywords="wilted flower dead" onclick="copyEmoji('🥀')">🥀</div>
  <div class="emoji" data-keywords="sunflower" onclick="copyEmoji('🌻')">🌻</div>
  <div class="emoji" data-keywords="hibiscus flower" onclick="copyEmoji('🌺')">🌺</div>

  <!-- Sky & celestial -->
  <div class="emoji" data-keywords="sun" onclick="copyEmoji('☀️')">☀️</div>
  <div class="emoji" data-keywords="sun behind small cloud" onclick="copyEmoji('🌤️')">🌤️</div>
  <div class="emoji" data-keywords="sun behind cloud" onclick="copyEmoji('⛅')">⛅</div>
  <div class="emoji" data-keywords="sun behind large cloud" onclick="copyEmoji('🌥️')">🌥️</div>
  <div class="emoji" data-keywords="sun behind rain cloud" onclick="copyEmoji('🌦️')">🌦️</div>
  <div class="emoji" data-keywords="rainbow" onclick="copyEmoji('🌈')">🌈</div>
  <div class="emoji" data-keywords="moon crescent" onclick="copyEmoji('🌙')">🌙</div>
  <div class="emoji" data-keywords="new moon" onclick="copyEmoji('🌑')">🌑</div>
  <div class="emoji" data-keywords="first quarter moon" onclick="copyEmoji('🌓')">🌓</div>
  <div class="emoji" data-keywords="full moon" onclick="copyEmoji('🌕')">🌕</div>
  <div class="emoji" data-keywords="glowing star" onclick="copyEmoji('🌟')">🌟</div>
  <div class="emoji" data-keywords="shooting star" onclick="copyEmoji('🌠')">🌠</div>
  <div class="emoji" data-keywords="milky way galaxy" onclick="copyEmoji('🌌')">🌌</div>

  <!-- Weather -->
  <div class="emoji" data-keywords="cloud" onclick="copyEmoji('☁️')">☁️</div>
  <div class="emoji" data-keywords="cloud with rain" onclick="copyEmoji('🌧️')">🌧️</div>
  <div class="emoji" data-keywords="cloud with lightning" onclick="copyEmoji('🌩️')">🌩️</div>
  <div class="emoji" data-keywords="cloud with lightning rain storm" onclick="copyEmoji('⛈️')">⛈️</div>
  <div class="emoji" data-keywords="cloud with snow" onclick="copyEmoji('🌨️')">🌨️</div>
  <div class="emoji" data-keywords="cyclone swirl" onclick="copyEmoji('🌀')">🌀</div>
  <div class="emoji" data-keywords="tornado cyclone" onclick="copyEmoji('🌪️')">🌪️</div>
  <div class="emoji" data-keywords="fog" onclick="copyEmoji('🌫️')">🌫️</div>
  <div class="emoji" data-keywords="snowflake" onclick="copyEmoji('❄️')">❄️</div>
  <div class="emoji" data-keywords="snowman" onclick="copyEmoji('☃️')">☃️</div>
  <div class="emoji" data-keywords="snowman without snow" onclick="copyEmoji('⛄')">⛄</div>
  <div class="emoji" data-keywords="droplet water" onclick="copyEmoji('💧')">💧</div>
  <div class="emoji" data-keywords="sweat droplets splash" onclick="copyEmoji('💦')">💦</div>
  <div class="emoji" data-keywords="water wave sea" onclick="copyEmoji('🌊')">🌊</div>

  <!-- Fire & disasters -->
  <div class="emoji" data-keywords="fire flame" onclick="copyEmoji('🔥')">🔥</div>
  <div class="emoji" data-keywords="comet" onclick="copyEmoji('☄️')">☄️</div>
</div>

 <div class="category">
  <h2>🏁 Flags & Signals</h2>

  <!-- Racing / markers -->
  <div class="emoji" data-keywords="chequered flag race finish" onclick="copyEmoji('🏁')">🏁</div>
  <div class="emoji" data-keywords="triangular flag post" onclick="copyEmoji('🚩')">🚩</div>
  <div class="emoji" data-keywords="crossed flags japan festival" onclick="copyEmoji('🎌')">🎌</div>
  <div class="emoji" data-keywords="black flag" onclick="copyEmoji('🏴')">🏴</div>
  <div class="emoji" data-keywords="white flag surrender" onclick="copyEmoji('🏳️')">🏳️</div>
  <div class="emoji" data-keywords="rainbow flag pride lgbt" onclick="copyEmoji('🏳️‍🌈')">🏳️‍🌈</div>
  <div class="emoji" data-keywords="transgender flag" onclick="copyEmoji('🏳️‍⚧️')">🏳️‍⚧️</div>

  <!-- Signal flags -->
  <div class="emoji" data-keywords="pirate flag skull crossbones" onclick="copyEmoji('🏴‍☠️')">🏴‍☠️</div>
  <div class="emoji" data-keywords="warning flag on pole" onclick="copyEmoji('🚩')">🚩</div>

  <!-- Example country flags (you can add more) -->
  <div class="emoji" data-keywords="flag united kingdom uk britain" onclick="copyEmoji('🇬🇧')">🇬🇧</div>
  <div class="emoji" data-keywords="flag united states usa america" onclick="copyEmoji('🇺🇸')">🇺🇸</div>
  <div class="emoji" data-keywords="flag ireland irish" onclick="copyEmoji('🇮🇪')">🇮🇪</div>
  <div class="emoji" data-keywords="flag european union eu" onclick="copyEmoji('🇪🇺')">🇪🇺</div>
  <div class="emoji" data-keywords="flag canada" onclick="copyEmoji('🇨🇦')">🇨🇦</div>
  <div class="emoji" data-keywords="flag australia" onclick="copyEmoji('🇦🇺')">🇦🇺</div>
  <div class="emoji" data-keywords="flag japan" onclick="copyEmoji('🇯🇵')">🇯🇵</div>
  <div class="emoji" data-keywords="flag germany" onclick="copyEmoji('🇩🇪')">🇩🇪</div>
  <div class="emoji" data-keywords="flag france" onclick="copyEmoji('🇫🇷')">🇫🇷</div>
  <div class="emoji" data-keywords="flag italy" onclick="copyEmoji('🇮🇹')">🇮🇹</div>
  <div class="emoji" data-keywords="flag spain" onclick="copyEmoji('🇪🇸')">🇪🇸</div>
  <div class="emoji" data-keywords="flag brazil" onclick="copyEmoji('🇧🇷')">🇧🇷</div>
  <div class="emoji" data-keywords="flag india" onclick="copyEmoji('🇮🇳')">🇮🇳</div>
  <div class="emoji" data-keywords="flag china" onclick="copyEmoji('🇨🇳')">🇨🇳</div>
  <div class="emoji" data-keywords="flag south korea" onclick="copyEmoji('🇰🇷')">🇰🇷</div>
</div>

 <div class="category">
  <h2>💞 Extra Hearts & Emotions</h2>

  <!-- Extra hearts / love -->
  <div class="emoji" data-keywords="heart with arrow love" onclick="copyEmoji('💘')">💘</div>
  <div class="emoji" data-keywords="heart with ribbon gift" onclick="copyEmoji('💝')">💝</div>
  <div class="emoji" data-keywords="sparkling heart love" onclick="copyEmoji('💖')">💖</div>
  <div class="emoji" data-keywords="growing heart" onclick="copyEmoji('💗')">💗</div>
  <div class="emoji" data-keywords="beating heart" onclick="copyEmoji('💓')">💓</div>
  <div class="emoji" data-keywords="revolving hearts" onclick="copyEmoji('💞')">💞</div>
  <div class="emoji" data-keywords="two hearts" onclick="copyEmoji('💕')">💕</div>
  <div class="emoji" data-keywords="heart decoration" onclick="copyEmoji('💟')">💟</div>
  <div class="emoji" data-keywords="heart exclamation" onclick="copyEmoji('❣️')">❣️</div>
  <div class="emoji" data-keywords="broken heart sad" onclick="copyEmoji('💔')">💔</div>

  <!-- Extra emotion symbols -->
  <div class="emoji" data-keywords="anger symbol comic" onclick="copyEmoji('💢')">💢</div>
  <div class="emoji" data-keywords="dizzy symbol" onclick="copyEmoji('💫')">💫</div>
  <div class="emoji" data-keywords="sweat droplets" onclick="copyEmoji('💦')">💦</div>
  <div class="emoji" data-keywords="dash symbol fast running" onclick="copyEmoji('💨')">💨</div>
  <div class="emoji" data-keywords="zzz sleeping" onclick="copyEmoji('💤')">💤</div>
  <div class="emoji" data-keywords="collision boom" onclick="copyEmoji('💥')">💥</div>
  <div class="emoji" data-keywords="bomb explosion" onclick="copyEmoji('💣')">💣</div>
  <div class="emoji" data-keywords="thought balloon thinking" onclick="copyEmoji('💭')">💭</div>
  <div class="emoji" data-keywords="speech balloon chat" onclick="copyEmoji('💬')">💬</div>
  <div class="emoji" data-keywords="left speech bubble" onclick="copyEmoji('🗨️')">🗨️</div>
  <div class="emoji" data-keywords="right anger bubble swear" onclick="copyEmoji('🗯️')">🗯️</div>
</div>

 
 <div class="category">
  <h2>🎭 Activity & Entertainment</h2>

  <!-- Shows & arts -->
  <div class="emoji" data-keywords="circus tent show festival" onclick="copyEmoji('🎪')">🎪</div>
  <div class="emoji" data-keywords="performing arts theater masks" onclick="copyEmoji('🎭')">🎭</div>
  <div class="emoji" data-keywords="artist palette painting art" onclick="copyEmoji('🎨')">🎨</div>
  <div class="emoji" data-keywords="clapper board movie film" onclick="copyEmoji('🎬')">🎬</div>
  <div class="emoji" data-keywords="ticket event" onclick="copyEmoji('🎟️')">🎟️</div>
  <div class="emoji" data-keywords="admission tickets concert cinema" onclick="copyEmoji('🎫')">🎫</div>
  <div class="emoji" data-keywords="microphone singing karaoke" onclick="copyEmoji('🎤')">🎤</div>
  <div class="emoji" data-keywords="headphone music listen" onclick="copyEmoji('🎧')">🎧</div>
  <div class="emoji" data-keywords="musical score sheet music" onclick="copyEmoji('🎼')">🎼</div>
  <div class="emoji" data-keywords="musical keyboard piano" onclick="copyEmoji('🎹')">🎹</div>
  <div class="emoji" data-keywords="violin music" onclick="copyEmoji('🎻')">🎻</div>
  <div class="emoji" data-keywords="trumpet music" onclick="copyEmoji('🎺')">🎺</div>
  <div class="emoji" data-keywords="saxophone music" onclick="copyEmoji('🎷')">🎷</div>
  <div class="emoji" data-keywords="guitar music" onclick="copyEmoji('🎸')">🎸</div>
  <div class="emoji" data-keywords="banjo music" onclick="copyEmoji('🪕')">🪕</div>
  <div class="emoji" data-keywords="drum with drumsticks" onclick="copyEmoji('🥁')">🥁</div>
  <div class="emoji" data-keywords="long drum instrument" onclick="copyEmoji('🪘')">🪘</div>

  <!-- Fairground & fun -->
  <div class="emoji" data-keywords="ferris wheel fair" onclick="copyEmoji('🎡')">🎡</div>
  <div class="emoji" data-keywords="roller coaster theme park" onclick="copyEmoji('🎢')">🎢</div>
  <div class="emoji" data-keywords="carousel horse ride" onclick="copyEmoji('🎠')">🎠</div>

  <!-- Celebrations (extra) -->
  <div class="emoji" data-keywords="sparkler celebration" onclick="copyEmoji('🎇')">🎇</div>
  <div class="emoji" data-keywords="fireworks" onclick="copyEmoji('🎆')">🎆</div>
  <div class="emoji" data-keywords="wind chime festival" onclick="copyEmoji('🎐')">🎐</div>
  <div class="emoji" data-keywords="japanese dolls festival" onclick="copyEmoji('🎎')">🎎</div>
  <div class="emoji" data-keywords="carp streamer festival" onclick="copyEmoji('🎏')">🎏</div>
  <div class="emoji" data-keywords="pine decoration new year" onclick="copyEmoji('🎍')">🎍</div>
  <div class="emoji" data-keywords="moon viewing ceremony" onclick="copyEmoji('🎑')">🎑</div>
  <div class="emoji" data-keywords="studio microphone broadcast podcast" onclick="copyEmoji('🎙️')">🎙️</div>
<div class="emoji" data-keywords="level slider mixer audio" onclick="copyEmoji('🎚️')">🎚️</div>
<div class="emoji" data-keywords="control knobs mixer" onclick="copyEmoji('🎛️')">🎛️</div>
<div class="emoji" data-keywords="radio" onclick="copyEmoji('📻')">📻</div>
<div class="emoji" data-keywords="television tv" onclick="copyEmoji('📺')">📺</div>
<div class="emoji" data-keywords="movie camera film" onclick="copyEmoji('🎥')">🎥</div>
<div class="emoji" data-keywords="film projector" onclick="copyEmoji('📽️')">📽️</div>
<div class="emoji" data-keywords="cinema film frames" onclick="copyEmoji('🎦')">🎦</div>
<div class="emoji" data-keywords="dvd disc" onclick="copyEmoji('📀')">📀</div>
<div class="emoji" data-keywords="cd disc" onclick="copyEmoji('💿')">💿</div>
<div class="emoji" data-keywords="videocassette vhs tape" onclick="copyEmoji('📼')">📼</div>
<div class="emoji" data-keywords="camera" onclick="copyEmoji('📷')">📷</div>
<div class="emoji" data-keywords="camera with flash" onclick="copyEmoji('📸')">📸</div>
<div class="emoji" data-keywords="video camera" onclick="copyEmoji('📹')">📹</div>

<div class="emoji" data-keywords="sparkler handheld firework" onclick="copyEmoji('🎇')">🎇</div>
<div class="emoji" data-keywords="fireworks celebration" onclick="copyEmoji('🎆')">🎆</div>
<div class="emoji" data-keywords="tanabata tree festival" onclick="copyEmoji('🎋')">🎋</div>
<div class="emoji" data-keywords="rice cracker festival food" onclick="copyEmoji('🍘')">🍘</div>
<div class="emoji" data-keywords="rice ball onigiri" onclick="copyEmoji('🍙')">🍙</div>

<div class="emoji" data-keywords="wrapped gift present" onclick="copyEmoji('🎁')">🎁</div>
<div class="emoji" data-keywords="love letter envelope heart" onclick="copyEmoji('💌')">💌</div>
<div class="emoji" data-keywords="reminder ribbon awareness" onclick="copyEmoji('🎗️')">🎗️</div>
<div class="emoji" data-keywords="label tag" onclick="copyEmoji('🏷️')">🏷️</div>

<div class="emoji" data-keywords="joystick retro gaming" onclick="copyEmoji('🕹️')">🕹️</div>
<div class="emoji" data-keywords="video game controller" onclick="copyEmoji('🎮')">🎮</div>
<div class="emoji" data-keywords="chess pawn board game" onclick="copyEmoji('♟️')">♟️</div>
<div class="emoji" data-keywords="mahjong tile red dragon" onclick="copyEmoji('🀄')">🀄</div>
<div class="emoji" data-keywords="joker card playing" onclick="copyEmoji('🃏')">🃏</div>
<div class="emoji" data-keywords="karaoke bar music" onclick="copyEmoji('🎤')">🎤</div>
<div class="emoji" data-keywords="slot machine casino" onclick="copyEmoji('🎰')">🎰</div>
<div class="emoji" data-keywords="game die dice" onclick="copyEmoji('🎲')">🎲</div>
<div class="emoji" data-keywords="puzzle piece game" onclick="copyEmoji('🧩')">🧩</div>
<div class="emoji" data-keywords="yo-yo toy" onclick="copyEmoji('🪀')">🪀</div>
<div class="emoji" data-keywords="kite outdoor toy" onclick="copyEmoji('🪁')">🪁</div>
<div class="emoji" data-keywords="crystal ball fortune telling" onclick="copyEmoji('🔮')">🔮</div>

</div>

 
  <div class="category">
    <h2>🍕 Food</h2>
  <!-- Fruit -->
  <div class="emoji" data-keywords="grapes fruit" onclick="copyEmoji('🍇')">🍇</div>
  <div class="emoji" data-keywords="melon fruit" onclick="copyEmoji('🍈')">🍈</div>
  <div class="emoji" data-keywords="watermelon fruit" onclick="copyEmoji('🍉')">🍉</div>
  <div class="emoji" data-keywords="tangerine orange fruit" onclick="copyEmoji('🍊')">🍊</div>
  <div class="emoji" data-keywords="lemon fruit" onclick="copyEmoji('🍋')">🍋</div>
  <div class="emoji" data-keywords="banana fruit" onclick="copyEmoji('🍌')">🍌</div>
  <div class="emoji" data-keywords="pineapple fruit" onclick="copyEmoji('🍍')">🍍</div>
  <div class="emoji" data-keywords="mango fruit" onclick="copyEmoji('🥭')">🥭</div>
  <div class="emoji" data-keywords="red apple fruit" onclick="copyEmoji('🍎')">🍎</div>
  <div class="emoji" data-keywords="green apple fruit" onclick="copyEmoji('🍏')">🍏</div>
  <div class="emoji" data-keywords="pear fruit" onclick="copyEmoji('🍐')">🍐</div>
  <div class="emoji" data-keywords="peach fruit" onclick="copyEmoji('🍑')">🍑</div>
  <div class="emoji" data-keywords="cherries fruit" onclick="copyEmoji('🍒')">🍒</div>
  <div class="emoji" data-keywords="strawberry fruit" onclick="copyEmoji('🍓')">🍓</div>
  <div class="emoji" data-keywords="kiwi fruit" onclick="copyEmoji('🥝')">🥝</div>
  <div class="emoji" data-keywords="tomato fruit" onclick="copyEmoji('🍅')">🍅</div>
  <div class="emoji" data-keywords="coconut fruit" onclick="copyEmoji('🥥')">🥥</div>

  <!-- Vegetables -->
  <div class="emoji" data-keywords="avocado vegetable" onclick="copyEmoji('🥑')">🥑</div>
  <div class="emoji" data-keywords="eggplant aubergine vegetable" onclick="copyEmoji('🍆')">🍆</div>
  <div class="emoji" data-keywords="potato vegetable" onclick="copyEmoji('🥔')">🥔</div>
  <div class="emoji" data-keywords="carrot vegetable" onclick="copyEmoji('🥕')">🥕</div>
  <div class="emoji" data-keywords="ear of corn maize vegetable" onclick="copyEmoji('🌽')">🌽</div>
  <div class="emoji" data-keywords="hot pepper chili" onclick="copyEmoji('🌶️')">🌶️</div>
  <div class="emoji" data-keywords="cucumber vegetable" onclick="copyEmoji('🥒')">🥒</div>
  <div class="emoji" data-keywords="leafy green lettuce" onclick="copyEmoji('🥬')">🥬</div>
  <div class="emoji" data-keywords="broccoli vegetable" onclick="copyEmoji('🥦')">🥦</div>
  <div class="emoji" data-keywords="garlic vegetable" onclick="copyEmoji('🧄')">🧄</div>
  <div class="emoji" data-keywords="onion vegetable" onclick="copyEmoji('🧅')">🧅</div>
  <div class="emoji" data-keywords="peanuts nuts" onclick="copyEmoji('🥜')">🥜</div>
  <div class="emoji" data-keywords="beans kidney" onclick="copyEmoji('🫘')">🫘</div>
  <div class="emoji" data-keywords="chestnut" onclick="copyEmoji('🌰')">🌰</div>

  <!-- Bread & breakfast -->
  <div class="emoji" data-keywords="bread loaf" onclick="copyEmoji('🍞')">🍞</div>
  <div class="emoji" data-keywords="croissant pastry" onclick="copyEmoji('🥐')">🥐</div>
  <div class="emoji" data-keywords="baguette bread" onclick="copyEmoji('🥖')">🥖</div>
  <div class="emoji" data-keywords="flatbread pita" onclick="copyEmoji('🫓')">🫓</div>
  <div class="emoji" data-keywords="pretzel" onclick="copyEmoji('🥨')">🥨</div>
  <div class="emoji" data-keywords="bagel" onclick="copyEmoji('🥯')">🥯</div>
  <div class="emoji" data-keywords="pancakes breakfast" onclick="copyEmoji('🥞')">🥞</div>
  <div class="emoji" data-keywords="waffle breakfast" onclick="copyEmoji('🧇')">🧇</div>
  <div class="emoji" data-keywords="cheese wedge" onclick="copyEmoji('🧀')">🧀</div>
  <div class="emoji" data-keywords="egg breakfast" onclick="copyEmoji('🍳')">🍳</div>
  <div class="emoji" data-keywords="bacon" onclick="copyEmoji('🥓')">🥓</div>
  <div class="emoji" data-keywords="butter" onclick="copyEmoji('🧈')">🧈</div>

  <!-- Meals / fast food -->
  <div class="emoji" data-keywords="green salad" onclick="copyEmoji('🥗')">🥗</div>
  <div class="emoji" data-keywords="popcorn snack" onclick="copyEmoji('🍿')">🍿</div>
  <div class="emoji" data-keywords="pizza slice" onclick="copyEmoji('🍕')">🍕</div>
  <div class="emoji" data-keywords="hamburger burger" onclick="copyEmoji('🍔')">🍔</div>
  <div class="emoji" data-keywords="french fries chips" onclick="copyEmoji('🍟')">🍟</div>
  <div class="emoji" data-keywords="hot dog" onclick="copyEmoji('🌭')">🌭</div>
  <div class="emoji" data-keywords="sandwich" onclick="copyEmoji('🥪')">🥪</div>
  <div class="emoji" data-keywords="taco" onclick="copyEmoji('🌮')">🌮</div>
  <div class="emoji" data-keywords="burrito" onclick="copyEmoji('🌯')">🌯</div>
  <div class="emoji" data-keywords="stuffed flatbread pita" onclick="copyEmoji('🥙')">🥙</div>
  <div class="emoji" data-keywords="falafel" onclick="copyEmoji('🧆')">🧆</div>
  <div class="emoji" data-keywords="cooked rice bowl" onclick="copyEmoji('🍚')">🍚</div>
  <div class="emoji" data-keywords="rice ball" onclick="copyEmoji('🍙')">🍙</div>
  <div class="emoji" data-keywords="rice cracker" onclick="copyEmoji('🍘')">🍘</div>
  <div class="emoji" data-keywords="bento box" onclick="copyEmoji('🍱')">🍱</div>
  <div class="emoji" data-keywords="spaghetti pasta" onclick="copyEmoji('🍝')">🍝</div>
  <div class="emoji" data-keywords="steaming bowl ramen" onclick="copyEmoji('🍜')">🍜</div>
  <div class="emoji" data-keywords="pot of food stew" onclick="copyEmoji('🍲')">🍲</div>
  <div class="emoji" data-keywords="fondue" onclick="copyEmoji('🫕')">🫕</div>
  <div class="emoji" data-keywords="curry rice" onclick="copyEmoji('🍛')">🍛</div>
  <div class="emoji" data-keywords="shallow pan food paella" onclick="copyEmoji('🥘')">🥘</div>
  <div class="emoji" data-keywords="tamale" onclick="copyEmoji('🫔')">🫔</div>

  <!-- Asian food / seafood -->
  <div class="emoji" data-keywords="sushi" onclick="copyEmoji('🍣')">🍣</div>
  <div class="emoji" data-keywords="fried shrimp tempura" onclick="copyEmoji('🍤')">🍤</div>
  <div class="emoji" data-keywords="oden stew" onclick="copyEmoji('🍢')">🍢</div>
  <div class="emoji" data-keywords="dango sweets" onclick="copyEmoji('🍡')">🍡</div>
  <div class="emoji" data-keywords="fish cake swirl" onclick="copyEmoji('🍥')">🍥</div>
  <div class="emoji" data-keywords="takeout box" onclick="copyEmoji('🥡')">🥡</div>
  <div class="emoji" data-keywords="lobster seafood" onclick="copyEmoji('🦞')">🦞</div>
  <div class="emoji" data-keywords="crab seafood" onclick="copyEmoji('🦀')">🦀</div>
  <div class="emoji" data-keywords="shrimp prawn seafood" onclick="copyEmoji('🦐')">🦐</div>
  <div class="emoji" data-keywords="oyster seafood" onclick="copyEmoji('🦪')">🦪</div>

  <!-- Sweets & desserts -->
  <div class="emoji" data-keywords="soft ice cream" onclick="copyEmoji('🍦')">🍦</div>
  <div class="emoji" data-keywords="shaved ice" onclick="copyEmoji('🍧')">🍧</div>
  <div class="emoji" data-keywords="ice cream dessert" onclick="copyEmoji('🍨')">🍨</div>
  <div class="emoji" data-keywords="doughnut donut" onclick="copyEmoji('🍩')">🍩</div>
  <div class="emoji" data-keywords="cookie biscuit" onclick="copyEmoji('🍪')">🍪</div>
  <div class="emoji" data-keywords="birthday cake" onclick="copyEmoji('🎂')">🎂</div>
  <div class="emoji" data-keywords="shortcake slice of cake" onclick="copyEmoji('🍰')">🍰</div>
  <div class="emoji" data-keywords="cupcake" onclick="copyEmoji('🧁')">🧁</div>
  <div class="emoji" data-keywords="pie dessert" onclick="copyEmoji('🥧')">🥧</div>
  <div class="emoji" data-keywords="chocolate bar" onclick="copyEmoji('🍫')">🍫</div>
  <div class="emoji" data-keywords="candy sweet" onclick="copyEmoji('🍬')">🍬</div>
  <div class="emoji" data-keywords="lollipop sweet" onclick="copyEmoji('🍭')">🍭</div>
  <div class="emoji" data-keywords="custard pudding" onclick="copyEmoji('🍮')">🍮</div>
  <div class="emoji" data-keywords="honey pot" onclick="copyEmoji('🍯')">🍯</div>
  <div class="emoji" data-keywords="fortune cookie" onclick="copyEmoji('🥠')">🥠</div>
  <div class="emoji" data-keywords="mooncake" onclick="copyEmoji('🥮')">🥮</div>

  <!-- Drinks -->
  <div class="emoji" data-keywords="baby bottle milk" onclick="copyEmoji('🍼')">🍼</div>
  <div class="emoji" data-keywords="glass of milk" onclick="copyEmoji('🥛')">🥛</div>
  <div class="emoji" data-keywords="hot beverage coffee tea" onclick="copyEmoji('☕')">☕</div>
  <div class="emoji" data-keywords="teapot" onclick="copyEmoji('🫖')">🫖</div>
  <div class="emoji" data-keywords="teacup without handle green tea" onclick="copyEmoji('🍵')">🍵</div>
  <div class="emoji" data-keywords="sake bottle cup" onclick="copyEmoji('🍶')">🍶</div>
  <div class="emoji" data-keywords="bottle with popping cork champagne" onclick="copyEmoji('🍾')">🍾</div>
  <div class="emoji" data-keywords="wine glass" onclick="copyEmoji('🍷')">🍷</div>
  <div class="emoji" data-keywords="cocktail glass martini" onclick="copyEmoji('🍸')">🍸</div>
  <div class="emoji" data-keywords="tropical drink cocktail" onclick="copyEmoji('🍹')">🍹</div>
  <div class="emoji" data-keywords="beer mug" onclick="copyEmoji('🍺')">🍺</div>
  <div class="emoji" data-keywords="clinking beer mugs" onclick="copyEmoji('🍻')">🍻</div>
  <div class="emoji" data-keywords="clinking glasses cheers" onclick="copyEmoji('🥂')">🥂</div>
  <div class="emoji" data-keywords="tumbler glass whisky" onclick="copyEmoji('🥃')">🥃</div>
  <div class="emoji" data-keywords="cup with straw soda" onclick="copyEmoji('🥤')">🥤</div>
  <div class="emoji" data-keywords="bubble tea boba" onclick="copyEmoji('🧋')">🧋</div>
  <div class="emoji" data-keywords="mate drink" onclick="copyEmoji('🧉')">🧉</div>

  <!-- Dishware / utensils -->
  <div class="emoji" data-keywords="fork and knife" onclick="copyEmoji('🍴')">🍴</div>
  <div class="emoji" data-keywords="fork and knife with plate" onclick="copyEmoji('🍽️')">🍽️</div>
  <div class="emoji" data-keywords="bowl with spoon" onclick="copyEmoji('🥣')">🥣</div>
  <div class="emoji" data-keywords="spoon utensil" onclick="copyEmoji('🥄')">🥄</div>
  <div class="emoji" data-keywords="kitchen knife" onclick="copyEmoji('🔪')">🔪</div>
  <div class="emoji" data-keywords="chopsticks" onclick="copyEmoji('🥢')">🥢</div>
</div>
  </div>

  <footer>
    Made with ❤️ — Add more sections below!
  </footer>

  <div id="copyNotification"></div>

  <script>
    // fallback for non-secure contexts
    function fallbackCopyText(text) {
      const textarea = document.createElement('textarea');
      textarea.value = text;
      textarea.style.position = 'fixed';
      textarea.style.opacity = '0';
      document.body.appendChild(textarea);
      textarea.focus();
      textarea.select();
      try {
        document.execCommand('copy');
      } catch (err) {
        console.error('Copy failed', err);
      }
      document.body.removeChild(textarea);
    }

    function copyEmoji(emoji) {
      if (navigator.clipboard && window.isSecureContext) {
        navigator.clipboard.writeText(emoji).then(showCopied.bind(null, emoji));
      } else {
        fallbackCopyText(emoji);
        showCopied(emoji);
      }
    }

    function showCopied(emoji) {
      const notification = document.getElementById('copyNotification');
      notification.textContent = `${emoji} ✅ Copied to clipboard!`;
      notification.classList.add('show');
      setTimeout(() => {
        notification.classList.remove('show');
      }, 2000);
    }

    const searchInput = document.getElementById('searchInput');
    const categories = document.querySelectorAll('.category');

    searchInput.addEventListener('input', function(e) {
      const searchTerm = e.target.value.toLowerCase().trim();
      const emojis = document.querySelectorAll('.emoji');

      // Show/hide emojis
      emojis.forEach(emoji => {
        const keywords = (emoji.getAttribute('data-keywords') || '').toLowerCase();
        if (searchTerm === '' || keywords.includes(searchTerm)) {
          emoji.classList.remove('hidden');
        } else {
          emoji.classList.add('hidden');
        }
      });

      // Show/hide entire categories
      categories.forEach(category => {
        const emojiChildren = category.querySelectorAll('.emoji');
        let hasVisible = false;
        emojiChildren.forEach(emoji => {
          if (!emoji.classList.contains('hidden')) {
            hasVisible = true;
          }
        });
        if (!hasVisible && searchTerm !== '') {
          category.style.display = 'none';
        } else {
          category.style.display = '';
        }
      });
    });
  </script>

</body>
</html>

