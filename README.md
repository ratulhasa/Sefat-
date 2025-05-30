<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <title>বাটন মেনু</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }
    .hidden {
      display: none;
    }
    .button {
      margin: 5px;
      padding: 10px 20px;
      background-color: #007bff;
      color: white;
      border: none;
      cursor: pointer;
      border-radius: 4px;
    }
    .button:hover {
      background-color: #0056b3;
    }
    #uidDisplay {
      margin-top: 15px;
      font-weight: bold;
      color: green;
    }
  </style>
</head>
<body>

  <!-- মূল বাটন -->
  <button class="button" onclick="showMenu()">এখানে প্রবেশ করুন</button>

  <!-- তিনটি নতুন বাটন -->
  <div id="linkButtons" class="hidden">
    <a href="https://www.tiktok.com/@sefat91111" target="_blank">
      <button class="button">আমার TikTok প্রোফাইলে জান</button>
    </a>
    <a href="https://www.facebook.com/share/1AdRagHx4q/" target="_blank">
      <button class="button">আমার Facebook প্রোফাইলে জান </button>
    </a>
    <button class="button" onclick="showUID()">আমার free fire UID নিন</button>
  </div>

  <!-- UID প্রদর্শন -->
  <div id="uidDisplay" class="hidden"> 
  
  UID: 6157998477</div>
  <script>
    function showMenu() {
      const btnGroup = document.getElementById('linkButtons');
      btnGroup.classList.remove('hidden');

      // 20 সেকেন্ড পর বাটনগুলো লুকানো হবে
      setTimeout(() => {
        btnGroup.classList.add('hidden');
      }, 20000); // 20,০০০ মিলিসেকেন্ড = 20 সেকেন্ড
    }

    function showUID() {
      const uidDiv = document.getElementById('uidDisplay');
      uidDiv.classList.remove('hidden');

      // ১০ সেকেন্ড পর UID লুকানো হবে
      setTimeout(() => {
        uidDiv.classList.add('hidden');
      }, 10000); // ১০,০০০ মিলিসেকেন্ড = ১০ সেকেন্ড
    }
  </script>

</body>
</html> 

















<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>স্বাগতম</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #000;
      height: 100vh;
    }

    .welcome {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 3em;
      font-family: sans-serif;
      background: linear-gradient(45deg, #ff0000, #00ff00, #0000ff, #ff0000);
      background-size: 400% 400%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: gradientAnimation 5s infinite;
    }

    @keyframes gradientAnimation {
      0% {
        background-position: 0% 50%;
      }
      50% {
        background-position: 100% 50%;
      }
      100% {
        background-position: 0% 50%;
      }
    }
  </style>
</head>
<body>
  <h1 class="welcome">স্বাগতম</h1>
</body>
</html>












<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Developer Sefat</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background-color: #000;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding-top: 100px; /* উপরের থেকে দুই আঙুল পরিমাণ নিচে আনা হয়েছে */
    }

    .typewriter {
      font-size: 1.2em; /* লেখার আকার আরও ছোট করা হয়েছে */
      font-family: monospace;
      overflow: hidden;
      white-space: nowrap;
      border-right: 0.15em solid orange;
      background: linear-gradient(90deg, #ff0000, #00ff00, #0000ff);
      background-size: 200% auto;
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      -webkit-text-fill-color: transparent;
      animation:
        typing 4s steps(15, end),
        blink-caret 0.75s step-end infinite,
        textShine 5s ease-in-out infinite alternate,
        fadeOut 1s ease-in 9s forwards;
    }

    @keyframes typing {
      from { width: 0 }
      to { width: 15ch }
    }

    @keyframes blink-caret {
      from, to { border-color: transparent }
      50% { border-color: orange }
    }

    @keyframes textShine {
      0% {
        background-position: 0% 50%;
      }
      100% {
        background-position: 100% 50%;
      }
    }

    @keyframes fadeOut {
      to {
        opacity: 0;
        visibility: hidden;
      }
    }
  </style>
</head>
<body>
  <div class="typewriter">Developer Sefat</div>
</body>
</html>


<link rel="manifest" href="manifest.json">
</html>
<script>
  if ('serviceWorker' in navigator) {
    window.addEventListener('load', function() {
      navigator.serviceWorker.register('/serviceworker.js')
        .then(function(registration) {
          console.log('ServiceWorker registration successful with scope: ', registration.scope);
        }, function(error) {
          console.log('ServiceWorker registration failed: ', error);
        });
    });
  }
</script>

