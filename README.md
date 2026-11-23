# School-Helper📝
Only for the Admin, me!💡🔧

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Private Space</title>

<style>
* { box-sizing: border-box; }

body {
  margin: 0;
  font-family: Georgia, serif;
  background: #f5f1eb;
  color: #35332f;
}

button, input, textarea {
  font: inherit;
}

button {
  cursor: pointer;
  border: none;
}

.hidden { display: none !important; }

.center-screen {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 25px;
}

.login {
  width: min(430px, 100%);
  text-align: center;
}

.login h1 {
  font-size: 35px;
  font-weight: normal;
  margin-bottom: 35px;
}

.login label {
  display: block;
  font-size: 17px;
  margin-bottom: 12px;
}

.login input {
  width: 100%;
  padding: 15px;
  background: transparent;
  border: none;
  border-bottom: 1px solid #aaa;
  text-align: center;
  outline: none;
  font-size: 19px;
}

.main-btn {
  margin-top: 30px;
  background: #393831;
  color: white;
  padding: 13px 35px;
  border-radius: 3px;
  transition: .2s;
}

.main-btn:hover {
  background: #777064;
}

.error {
  color: #a34d45;
  font-size: 13px;
  margin-top: 15px;
}

.verify-box {
  border: 1px solid #c9c3b9;
  padding: 22px;
  margin-top: 25px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
  background: white;
}

.verify-box input {
  width: 20px;
  height: 20px;
}

/* MAIN */

#mainPage {
  min-height: 100vh;
  padding: 55px 25px;
  text-align: center;
}

.logo {
  font-size: 30px;
  font-weight: normal;
  margin-bottom: 12px;
}

.subtitle {
  color: #89847b;
  font-size: 13px;
  letter-spacing: 2px;
  margin-bottom: 65px;
}

.menu {
  display: flex;
  justify-content: center;
  gap: 25px;
  flex-wrap: wrap;
}

.menu-card {
  width: 230px;
  height: 210px;
  background: #fff;
  border: 1px solid #e3ded5;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 17px;
  transition: .25s;
}

.menu-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px #00000010;
}

.menu-card .symbol {
  font-size: 37px;
}

.menu-card h2 {
  font-size: 21px;
  font-weight: normal;
}

/* SUB PAGES */

.sub-page {
  min-height: 100vh;
  padding: 35px 6%;
}

.topbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 35px;
}

.back-btn {
  background: none;
  color: #777;
  font-size: 14px;
  padding: 10px 0;
}

.page-title {
  font-size: 29px;
  font-weight: normal;
}

/* MEMO */

.memo-layout {
  display: grid;
  grid-template-columns: 230px minmax(0, 650px);
  justify-content: center;
  gap: 35px;
}

.gallery {
  background: #fff;
  border: 1px solid #e7e0d5;
  padding: 20px;
  height: fit-content;
}

.gallery h3 {
  font-size: 17px;
  font-weight: normal;
  margin-top: 0;
}

.gallery-item {
  width: 100%;
  background: #f8f5ef;
  padding: 12px;
  margin-top: 9px;
  text-align: left;
  color: #555;
  border: 1px solid transparent;
}

.gallery-item.active {
  border-color: #a9a08e;
  background: #eee9df;
}

.new-memo {
  width: 100%;
  padding: 11px;
  background: #393831;
  color: white;
  margin-bottom: 15px;
}

.paper {
  background: #fffdf5;
  min-height: 590px;
  padding: 40px 45px;
  box-shadow: 0 5px 20px #0000000d;
  border: 1px solid #e8e0d0;
  background-image: repeating-linear-gradient(
    transparent,
    transparent 31px,
    #e9e2d5 32px
  );
  background-position: 0 110px;
}

.paper-title {
  width: 100%;
  border: none;
  border-bottom: 1px solid #cfc5b5;
  background: transparent;
  font-size: 25px;
  outline: none;
  padding: 5px 0 15px;
  margin-bottom: 20px;
  color: #464239;
}

.memo-text {
  width: 100%;
  min-height: 400px;
  resize: vertical;
  border: none;
  outline: none;
  background: transparent;
  font-size: 17px;
  line-height: 32px;
  color: #464239;
  font-family: Georgia, serif;
}

.saved-status {
  color: #888;
  font-size: 12px;
  text-align: right;
  margin-top: 10px;
}

/* PICTURES */

.upload-area {
  max-width: 850px;
  margin: auto;
}

.upload-controls {
  text-align: center;
  padding: 35px;
  border: 1px dashed #c9c1b5;
  background: #fff;
}

.upload-btn {
  padding: 13px 30px;
  background: #393831;
  color: white;
}

.photo-count {
  color: #888;
  margin-top: 15px;
  font-size: 13px;
}

.photo-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
  gap: 20px;
  margin-top: 30px;
}

.photo-card {
  background: white;
  border: 1px solid #e8e1d8;
  padding: 10px;
}

.photo-card img {
  width: 100%;
  height: 170px;
  object-fit: cover;
}

.photo-card button {
  width: 100%;
  margin-top: 9px;
  padding: 10px;
  background: #393831;
  color: white;
}

.photo-card .remove-btn {
  background: #eeeae3;
  color: #555;
}

/* MODAL */

.modal-bg {
  position: fixed;
  inset: 0;
  background: #00000055;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  z-index: 10;
}

.modal {
  background: #fff;
  width: min(360px, 100%);
  padding: 30px;
  text-align: center;
}

.modal h3 {
  font-weight: normal;
  font-size: 21px;
}

.modal-actions {
  display: flex;
  justify-content: center;
  gap: 12px;
  margin-top: 25px;
}

.modal-actions button {
  padding: 11px 25px;
  background: #393831;
  color: white;
}

.modal-actions .cancel {
  background: #eae7e1;
  color: #444;
}

@media(max-width:650px) {
  .memo-layout {
    grid-template-columns: 1fr;
  }

  .gallery {
    order: 2;
  }

  .paper {
    padding: 25px 20px;
  }

  .sub-page {
    padding: 20px;
  }
}
</style>
</head>

<body>

<!-- LOGIN 1 -->
<section id="step1" class="center-screen">
  <div class="login">
    <h1>Who are you?</h1>
    <label><b>[USERNAME]</b></label>
    <input id="username" placeholder="Type your answer..." autocomplete="off">
    <button class="main-btn" onclick="checkStep(1)">Enter</button>
    <p id="error1" class="error"></p>
  </div>
</section>

<!-- LOGIN 2 -->
<section id="step2" class="center-screen hidden">
  <div class="login">
    <h1>pasword</h1>
    <input id="password" type="password" placeholder="Type your answer..." autocomplete="off">
    <button class="main-btn" onclick="checkStep(2)">Enter</button>
    <p id="error2" class="error"></p>
  </div>
</section>

<!-- LOGIN 3 -->
<section id="step3" class="center-screen hidden">
  <div class="login">
    <h1>What is 🥜?</h1>
    <input id="peanut" placeholder="Type your answer..." autocomplete="off">
    <button class="main-btn" onclick="checkStep(3)">Enter</button>
    <p id="error3" class="error"></p>
  </div>
</section>

<!-- HUMAN VERIFICATION -->
<section id="step4" class="center-screen hidden">
  <div class="login">
    <h1>One last thing.</h1>
    <div class="verify-box">
      <span>Verify you're a human</span>
      <input type="checkbox" id="human">
    </div>
    <button class="main-btn" onclick="verifyHuman()">Continue</button>
    <p id="error4" class="error"></p>
  </div>
</section>

<!-- MAIN -->
<section id="mainPage" class="hidden">
  <h1 class="logo">Your Private Space</h1>
  <p class="subtitle">A LITTLE PLACE JUST FOR YOU</p>

  <div class="menu">
    <button class="menu-card" onclick="openPage('memoPage')">
      <span class="symbol">✎</span>
      <h2>Memo</h2>
    </button>

    <button class="menu-card" onclick="openPage('picturePage')">
      <span class="symbol">▧</span>
      <h2>Uploaded Pictures</h2>
    </button>
  </div>
</section>

<!-- MEMO PAGE -->
<section id="memoPage" class="sub-page hidden">
  <div class="topbar">
    <button class="back-btn" onclick="openPage('mainPage')">← Back</button>
    <h1 class="page-title">Memo</h1>
    <span></span>
  </div>

  <div class="memo-layout">
    <aside class="gallery">
      <h3>Memo Gallery</h3>
      <button class="new-memo" onclick="newMemo()">+ New Memo</button>
      <div id="memoGallery"></div>
    </aside>

    <div>
      <div class="paper">
        <input id="memoTitle" class="paper-title"
          placeholder="Untitled memo...">
        <textarea id="memoText" class="memo-text"
          placeholder="Write something..."></textarea>
      </div>
      <div id="savedStatus" class="saved-status">
        Automatically saved
      </div>
    </div>
  </div>
</section>

<!-- PICTURE PAGE -->
<section id="picturePage" class="sub-page hidden">
  <div class="topbar">
    <button class="back-btn" onclick="openPage('mainPage')">← Back</button>
    <h1 class="page-title">Uploaded Pictures</h1>
    <span></span>
  </div>

  <div class="upload-area">
    <div class="upload-controls">
      <input type="file" id="fileInput" accept="image/*" multiple hidden>
      <button class="upload-btn"
        onclick="document.getElementById('fileInput').click()">
        My PC
      </button>
      <p>Select pictures from your computer.</p>
      <div id="photoCount" class="photo-count">0 / 20 pictures</div>
    </div>

    <div id="photoGrid" class="photo-grid"></div>
  </div>
</section>

<!-- MODAL -->
<div id="modalBg" class="modal-bg hidden">
  <div class="modal">
    <h3 id="modalTitle">Notice</h3>
    <p id="modalMessage"></p>
    <div class="modal-actions">
      <button id="modalYes">Yes</button>
      <button id="modalCancel" class="cancel">Cancel</button>
    </div>
  </div>
</div>

<script>

/* LOGIN */

function checkStep(step) {
  const answers = {
    1: "26s.park",
    2: "150809",
    3: "pnbt"
  };

  const ids = {
    1: "username",
    2: "password",
    3: "peanut"
  };

  const input = document.getElementById(ids[step]);
  const error = document.getElementById("error" + step);

  if (input.value.trim() === answers[step]) {
    document.getElementById("step" + step).classList.add("hidden");
    document.getElementById("step" + (step + 1)).classList.remove("hidden");
    error.textContent = "";
  } else {
    error.textContent = "Incorrect answer. Try again.";
    input.value = "";
  }
}

function verifyHuman() {
  if (!document.getElementById("human").checked) {
    document.getElementById("error4").textContent =
      "Please verify you're a human.";
    return;
  }

  document.getElementById("step4").classList.add("hidden");
  document.getElementById("mainPage").classList.remove("hidden");
}

/* ENTER KEY */

document.querySelectorAll(".login input").forEach(input => {
  input.addEventListener("keydown", e => {
    if (e.key === "Enter") {
      const step = Number(input.closest("section").id.replace("step", ""));
      if (step <= 3) checkStep(step);
    }
  });
});

/* PAGE NAVIGATION */

function openPage(page) {
  ["mainPage", "memoPage", "picturePage"].forEach(id => {
    document.getElementById(id).classList.add("hidden");
  });

  document.getElementById(page).classList.remove("hidden");

  if (page === "memoPage") {
    renderMemos();
  }

  if (page === "picturePage") {
    renderPhotos();
  }
}

/* MODAL */

function showModal(title, message, yesFunction, cancelFunction) {
  const bg = document.getElementById("modalBg");
  bg.classList.remove("hidden");

  document.getElementById("modalTitle").textContent = title;
  document.getElementById("modalMessage").textContent = message;

  document.getElementById("modalYes").onclick = () => {
    bg.classList.add("hidden");
    if (yesFunction) yesFunction();
  };

  document.getElementById("modalCancel").onclick = () => {
    bg.classList.add("hidden");
    if (cancelFunction) cancelFunction();
  };
}

/* MEMO SYSTEM */

let memos = JSON.parse(localStorage.getItem("privateMemos") || "[]");
let currentMemo = null;
let askingForSheet = false;

function saveMemos() {
  localStorage.setItem("privateMemos", JSON.stringify(memos));
}

function newMemo() {
  const memo = {
    id: Date.now(),
    title: "",
    text: ""
  };

  memos.unshift(memo);
  currentMemo = memo.id;

  saveMemos();
  renderMemos();
}

function renderMemos() {
  const gallery = document.getElementById("memoGallery");
  gallery.innerHTML = "";

  memos.forEach(memo => {
    const button = document.createElement("button");
    button.className = "gallery-item" +
      (memo.id === currentMemo ? " active" : "");

    button.textContent = memo.title || "Untitled memo";

    button.onclick = () => {
      currentMemo = memo.id;
      loadMemo();
    };

    gallery.appendChild(button);
  });

  if (!currentMemo && memos.length) {
    currentMemo = memos[0].id;
  }

  if (!currentMemo) {
    newMemo();
    return;
  }

  loadMemo();
}

function loadMemo() {
  const memo = memos.find(m => m.id === currentMemo);
  if (!memo) return;

  document.getElementById("memoTitle").value = memo.title;
  document.getElementById("memoText").value = memo.text;

  document.getElementById("memoGallery").querySelectorAll("button")
    .forEach((button, index) => {
      button.classList.toggle(
        "active",
        memos[index].id === currentMemo
      );
    });
}

function updateMemo() {
  const memo = memos.find(m => m.id === currentMemo);
  if (!memo) return;

  memo.title = document.getElementById("memoTitle").value;
  memo.text = document.getElementById("memoText").value;

  saveMemos();

  document.getElementById("savedStatus").textContent =
    "✓ Automatically saved";

  renderGalleryOnly();
}

function renderGalleryOnly() {
  const gallery = document.getElementById("memoGallery");
  gallery.innerHTML = "";

  memos.forEach(memo => {
    const button = document.createElement("button");
    button.className = "gallery-item" +
      (memo.id === currentMemo ? " active" : "");
    button.textContent = memo.title || "Untitled memo";

    button.onclick = () => {
      currentMemo = memo.id;
      loadMemo();
    };

    gallery.appendChild(button);
  });
}

document.getElementById("memoTitle").addEventListener("input", updateMemo);

document.getElementById("memoText").addEventListener("input", function() {
  updateMemo();

  const memo = memos.find(m => m.id === currentMemo);
  if (!memo || askingForSheet || memo.text.length <= 37) return;

  askingForSheet = true;

  showModal(
    "Use another sheet?",
    "Your memo has more than 37 characters. Would you like another sheet?",
    () => {
      const current = memos.find(m => m.id === currentMemo);
      if (!current) {
        askingForSheet = false;
        return;
      }

      const overflow = current.text.slice(37);
      current.text = current.text.slice(0, 37);

      const next = {
        id: Date.now(),
        title: "",
        text: overflow
      };

      memos.unshift(next);
      currentMemo = next.id;

      saveMemos();
      renderMemos();
      askingForSheet = false;
    },
    () => {
      askingForSheet = false;
    }
  );
});

/* PICTURE STORAGE - INDEXED DB */

let db;

const request = indexedDB.open("PrivatePictureStorage", 1);

request.onupgradeneeded = e => {
  db = e.target.result;
  db.createObjectStore("pictures", { keyPath: "id" });
};

request.onsuccess = e => {
  db = e.target.result;
  renderPhotos();
};

function getPhotos(callback) {
  if (!db) {
    callback([]);
    return;
  }

  const transaction = db.transaction("pictures", "readonly");
  const store = transaction.objectStore("pictures");
  const request = store.getAll();

  request.onsuccess = () => {
    callback(request.result.sort((a,b) => a.id - b.id));
  };
}

function savePhoto(photo) {
  return new Promise(resolve => {
    const transaction = db.transaction("pictures", "readwrite");
    transaction.objectStore("pictures").put(photo);
    transaction.oncomplete = resolve;
  });
}

function deletePhoto(id) {
  return new Promise(resolve => {
    const transaction = db.transaction("pictures", "readwrite");
    transaction.objectStore("pictures").delete(id);
    transaction.oncomplete = resolve;
  });
}

function fileToDataURL(file) {
  return new Promise((resolve, reject) => {
    const reader = new FileReader();
    reader.onload = () => resolve(reader.result);
    reader.onerror = reject;
    reader.readAsDataURL(file);
  });
}

/* UPLOAD */

document.getElementById("fileInput").addEventListener("change", async function(e) {
  const files = Array.from(e.target.files || [])
    .filter(file => file.type.startsWith("image/"));

  for (const file of files) {
    const data = await fileToDataURL(file);

    const photos = await new Promise(resolve => getPhotos(resolve));

    if (photos.length >= 20) {
      const oldest = photos[0];

      const confirmed = await new Promise(resolve => {
        showModal(
          "Warning",
          "Should we delete first image?",
          () => resolve(true),
          () => resolve(false)
        );
      });

      if (!confirmed) continue;

      await deletePhoto(oldest.id);
    }

    await savePhoto({
      id: Date.now() + Math.random(),
      name: file.name,
      data: data
    });

    renderPhotos();
  }

  this.value = "";
});

/* PHOTO GALLERY */

function renderPhotos() {
  getPhotos(photos => {
    const grid = document.getElementById("photoGrid");
    grid.innerHTML = "";

    document.getElementById("photoCount").textContent =
      photos.length + " / 20 pictures";

    photos.forEach(photo => {
      const card = document.createElement("div");
      card.className = "photo-card";

      const img = document.createElement("img");
      img.src = photo.data;
      img.alt = photo.name;

      const copy = document.createElement("button");
      copy.textContent = "Copy";
      copy.onclick = () => copyPhoto(photo);

      const remove = document.createElement("button");
      remove.className = "remove-btn";
      remove.textContent = "Delete";
      remove.onclick = async () => {
        await deletePhoto(photo.id);
        renderPhotos();
      };

      card.append(img, copy, remove);
      grid.appendChild(card);
    });
  });
}

/* COPY IMAGE */

async function copyPhoto(photo) {
  try {
    if (!navigator.clipboard || !window.ClipboardItem) {
      throw new Error("Clipboard image copying is not supported.");
    }

    const response = await fetch(photo.data);
    const blob = await response.blob();

    await navigator.clipboard.write([
      new ClipboardItem({
        [blob.type]: blob
      })
    ]);

    alert("Image copied! You can now press Ctrl + V.");
  } catch (error) {
    alert("Could not copy the image. Please use HTTPS and allow clipboard permission.");
  }
}

</script>
</body>
</html>
