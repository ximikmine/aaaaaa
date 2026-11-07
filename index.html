<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Anime Jiggle Lab v7 — Hand + Mesh Fix</title>
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
html, body { height: 100%; overflow: hidden; font-family: system-ui, -apple-system, "Segoe UI", Roboto, sans-serif; font-size: 12px; }
body { background: #06060a; color: #ddd; display: flex; }

#sidebar {
  width: 360px; min-width: 360px; height: 100vh;
  background: #0e0e13; border-right: 1px solid #1c1c24;
  display: flex; flex-direction: column; overflow-y: auto;
  scrollbar-width: thin; scrollbar-color: #2a2a34 #0e0e13;
}
#sidebar::-webkit-scrollbar { width: 5px; }
#sidebar::-webkit-scrollbar-thumb { background: #2a2a34; border-radius: 3px; }

.brand {
  font-size: 12px; font-weight: 700; letter-spacing: 2px; color: #ff7eb6;
  padding: 12px 12px 10px; border-bottom: 1px solid #1c1c24;
  position: sticky; top: 0; background: #0e0e13; z-index: 10;
}
.brand small { display: block; font-size: 8px; color: #444; letter-spacing: 1px; font-weight: 400; margin-top: 2px; }

.upload-zone {
  margin: 8px; padding: 16px 12px; background: #14141a;
  border: 2px dashed #2c2c38; border-radius: 8px; text-align: center;
  cursor: pointer; transition: all 0.15s;
}
.upload-zone:hover { border-color: #ff6fa8; background: #17171f; }
.upload-zone.drag-over { border-color: #ff6fa8; background: #1c1c26; }
.upload-zone .icon { font-size: 26px; margin-bottom: 4px; }
.upload-zone .title { font-size: 12px; color: #ff9ecb; font-weight: 600; margin-bottom: 2px; }
.upload-zone .sub { font-size: 9px; color: #666; line-height: 1.4; }
.upload-zone .sub b { color: #ff6fa8; }

.tabs {
  display: flex; gap: 2px; padding: 6px 8px; flex-wrap: wrap;
  background: #0e0e13; z-index: 4; border-bottom: 1px solid #1c1c24;
}
.tab {
  flex: 1; background: #17171e; border: 1px solid #23232d; color: #888;
  padding: 5px 3px; font-size: 9px; border-radius: 4px; cursor: pointer;
  text-align: center; min-width: 42px; transition: all 0.12s;
  font-family: inherit;
}
.tab:hover { color: #ccc; background: #1d1d26; }
.tab.active { background: #ff6fa8; border-color: #ff6fa8; color: #0e0e13; font-weight: 700; }
.tab .badge { display: inline-block; font-size: 8px; background: rgba(0,0,0,0.3); padding: 0 3px; border-radius: 2px; margin-left: 2px; }

.tab-content { display: none; padding: 8px; flex-direction: column; gap: 6px; }
.tab-content.active { display: flex; }

.group { background: #15151c; border: 1px solid #20202a; border-radius: 6px; padding: 8px; }
.group.collapsed .group-body { display: none; }
.group-title {
  font-size: 10px; text-transform: uppercase; letter-spacing: 1.5px; color: #ff9ecb;
  margin-bottom: 8px; font-weight: 600; cursor: pointer; user-select: none;
  display: flex; justify-content: space-between; align-items: center;
}
.group-title::after { content: '▾'; font-size: 8px; color: #666; }
.group.collapsed .group-title::after { content: '▸'; }
.group-desc { font-size: 9px; color: #666; margin-bottom: 8px; line-height: 1.4; font-style: italic; }

.field { margin-bottom: 8px; }
.field:last-child { margin-bottom: 0; }
.field-head { display: flex; justify-content: space-between; align-items: baseline; margin-bottom: 3px; }
.field-label { font-size: 10px; color: #ccc; font-weight: 500; }
.field-value { color: #ff9ecb; font-variant-numeric: tabular-nums; font-size: 10px; font-weight: 600; }
.field-desc { font-size: 8px; color: #555; margin-top: 2px; line-height: 1.3; }
.field input[type="range"] { width: 100%; accent-color: #ff6fa8; height: 4px; cursor: pointer; }
.field input[type="text"], .field input[type="number"] {
  width: 100%; background: #0a0a0e; color: #ccc; border: 1px solid #23232d;
  border-radius: 4px; padding: 3px 5px; font-size: 10px; font-family: inherit;
}

.row { display: flex; gap: 4px; margin-bottom: 4px; flex-wrap: wrap; }
.row:last-child { margin-bottom: 0; }
.row button { flex: 1; min-width: 0; }

button {
  background: #20202a; color: #bbb; border: 1px solid #2c2c38;
  padding: 5px 6px; border-radius: 4px; cursor: pointer; font-size: 10px;
  transition: all 0.12s; font-family: inherit; white-space: nowrap;
}
button:hover { background: #2a2a36; border-color: #3a3a48; color: #fff; }
button.active { background: #ff6fa8; border-color: #ff6fa8; color: #0e0e13; font-weight: 700; }
button.accent { background: #ff6fa8; border-color: #ff6fa8; color: #0e0e13; font-weight: 700; }
button.danger { background: #a13030; border-color: #a13030; color: #fff; }
button.warn { background: #b07020; border-color: #b07020; color: #fff; }
button.tiny { padding: 3px 5px; font-size: 9px; }
button.wide { width: 100%; flex: none; }
button:disabled { opacity: 0.35; cursor: not-allowed; }

input[type="file"] { display: none; }

.zone-list { display: flex; flex-direction: column; gap: 3px; }
.zone-item {
  display: flex; align-items: center; gap: 5px;
  background: #1a1a22; border: 1px solid #23232d; border-radius: 4px;
  padding: 4px 6px; cursor: pointer;
}
.zone-item:hover { border-color: #3a3a48; }
.zone-item.active { border-color: #ff6fa8; background: #1e1e28; }
.zone-color { width: 12px; height: 12px; border-radius: 2px; flex-shrink: 0; }
.zone-name { flex: 1; font-size: 10px; color: #ccc; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
.zone-vis, .zone-del { font-size: 10px; color: #666; cursor: pointer; padding: 0 2px; }
.zone-vis:hover { color: #ff6fa8; }
.zone-vis.off { color: #333; }
.zone-del { color: #a13030; }
.zone-del:hover { color: #ff5050; }

.stat-grid {
  display: grid; grid-template-columns: 1fr 1fr; gap: 3px;
  font-size: 9px; color: #666; font-variant-numeric: tabular-nums;
}
.stat-grid .v { color: #ff9ecb; }

.help { font-size: 9px; color: #444; line-height: 1.5; padding: 6px; }
.help b { color: #ff6fa8; }
.help kbd { background: #1a1a22; padding: 1px 4px; border-radius: 2px; color: #888; font-size: 8px; border: 1px solid #2a2a34; font-family: monospace; }

.presets-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 3px; }
.presets-grid button { font-size: 9px; padding: 5px 3px; text-align: center; }

#stage {
  flex: 1; height: 100vh; background: #040406;
  display: flex; align-items: center; justify-content: center;
  position: relative; overflow: hidden;
}
#canvas {
  cursor: none; display: block;
  box-shadow: 0 0 120px rgba(255,111,168,0.06);
  max-width: 100%; max-height: 100%;
}

#dropOverlay {
  position: absolute; inset: 0; display: flex; align-items: center; justify-content: center;
  flex-direction: column; gap: 16px; color: #333; background: #040406;
  transition: all 0.2s; pointer-events: none; z-index: 1;
}
#dropOverlay .icon { font-size: 64px; opacity: 0.4; }
#dropOverlay .title { font-size: 16px; color: #555; }
#dropOverlay .sub { font-size: 11px; color: #333; text-align: center; line-height: 1.5; }
#dropOverlay .sub b { color: #ff6fa8; }
#stage.drag-over #dropOverlay { background: #10101a; }
#stage.drag-over #dropOverlay .icon { color: #ff6fa8; opacity: 1; }

#hud {
  position: absolute; top: 10px; left: 10px;
  display: flex; gap: 6px; z-index: 5; pointer-events: none;
}
.hud-pill {
  background: rgba(20,20,28,0.85); border: 1px solid #2a2a34;
  color: #888; padding: 3px 8px; border-radius: 10px;
  font-size: 9px; font-variant-numeric: tabular-nums; backdrop-filter: blur(8px);
}
.hud-pill .v { color: #ff9ecb; }

#toasts {
  position: fixed; bottom: 20px; left: 50%; transform: translateX(-50%);
  display: flex; flex-direction: column; gap: 5px; z-index: 1000; pointer-events: none;
}
.toast {
  background: #1e1e26; color: #ccc; padding: 8px 16px; border-radius: 6px;
  font-size: 11px; border: 1px solid #2c2c38;
  animation: toastIn 0.18s ease-out, toastOut 0.3s ease-in 2s forwards;
  backdrop-filter: blur(8px); max-width: 400px;
}
.toast.error { border-color: #a13030; color: #ff8888; background: #2a1a1a; }
.toast.success { border-color: #38b050; color: #88ff9e; background: #1a2a1e; }
.toast.info { border-color: #3080b0; color: #88ccff; background: #1a2028; }
@keyframes toastIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
@keyframes toastOut { to { opacity: 0; transform: translateY(-10px); } }

#modal {
  position: fixed; inset: 0; background: rgba(0,0,0,0.85);
  display: none; align-items: center; justify-content: center; z-index: 2000;
}
#modal.show { display: flex; }
#modal-box {
  background: #15151c; border: 1px solid #2a2a34; border-radius: 10px;
  padding: 24px; width: 420px; max-width: 90vw;
}
#modal-box h3 { font-size: 14px; color: #ff9ecb; margin-bottom: 12px; }
#modal-box p { font-size: 11px; color: #888; margin-bottom: 16px; line-height: 1.5; }
#modal-box .row { justify-content: flex-end; }

.hand-preview {
  width: 100%; height: 100px; background: #0a0a0e; border-radius: 4px;
  display: flex; align-items: center; justify-content: center;
  margin-bottom: 6px;
}
</style>
</head>
<body>

<aside id="sidebar">
  <div class="brand">ANIME JIGGLE LAB v7<small>hand press · mesh fix · 18+</small></div>

  <div class="upload-zone" id="uploadZone">
    <div class="icon">📁</div>
    <div class="title">Загрузить картинку</div>
    <div class="sub">Клик · drag & drop · <b>Ctrl+V</b><br>Все персонажи 18+</div>
  </div>
  <input type="file" id="fileInput" accept="image/*">

  <div class="tabs">
    <div class="tab active" data-tab="zones">ЗОНЫ <span class="badge" id="zoneCount">0</span></div>
    <div class="tab" data-tab="tool">КИСТЬ</div>
    <div class="tab" data-tab="grab">ЗАХВАТ</div>
    <div class="tab" data-tab="hand">ЛАДОНЬ</div>
    <div class="tab" data-tab="phys">ФИЗИКА</div>
    <div class="tab" data-tab="fx">ЭФФЕКТЫ</div>
    <div class="tab" data-tab="presets">ПРЕСЕТЫ</div>
    <div class="tab" data-tab="model">МОДЕЛЬ</div>
  </div>

  <!-- ZONES -->
  <div class="tab-content active" data-tab="zones">
    <div class="group">
      <div class="group-title">Мягкие зоны</div>
      <div class="group-desc">Каждая зона — независимая область со своими настройками физики.</div>
      <div class="zone-list" id="zoneList"></div>
      <div class="row" style="margin-top:6px">
        <button id="addZoneBtn">+ Зона</button>
        <button id="dupZoneBtn" class="tiny">⧉ Дубль</button>
        <button id="clearZoneBtn" class="warn tiny">Очистить</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Свойства зоны</div>
      <div class="field">
        <div class="field-head"><span class="field-label">Имя</span></div>
        <input type="text" id="zoneName" placeholder="Имя зоны">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Цвет</span></div>
        <div class="row" id="zoneColors"></div>
      </div>
      <div class="row">
        <button id="zoneVisBtn" class="active tiny wide">👁 Видима</button>
        <button id="zonePhysicsBtn" class="active tiny wide">⚙ Физика</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Пины</div>
      <div class="group-desc">Клик по вершине — пришпилить</div>
      <div class="row">
        <button id="pinModeBtn" class="tiny">📌 Режим</button>
        <button id="clearPinsBtn" class="danger tiny">Сброс</button>
      </div>
      <div class="stat-grid" style="margin-top:6px">
        <div>Пинов <span class="v" id="pinCount">0</span></div>
      </div>
    </div>
  </div>

  <!-- TOOL -->
  <div class="tab-content" data-tab="tool">
    <div class="group">
      <div class="group-title">Режим</div>
      <div class="row">
        <button class="mode-btn active" data-mode="grab">✋ Лапать</button>
      </div>
      <div class="row">
        <button class="mode-btn" data-mode="paint">🖌 Красить</button>
        <button class="mode-btn" data-mode="erase">🧽 Стереть</button>
      </div>
      <div class="row">
        <button class="mode-btn" data-mode="smooth">💧 Сгладить</button>
        <button class="mode-btn" data-mode="blur">🌫 Размыть</button>
      </div>
      <div class="row">
        <button class="mode-btn" data-mode="invert">🔄 Инверсия</button>
        <button class="mode-btn" data-mode="pin">📌 Пин</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Кисть</div>
      <div class="field">
        <div class="field-head"><span class="field-label">Размер</span><span class="field-value" id="brushVal">45</span></div>
        <input type="range" id="brushSize" min="4" max="250" step="1" value="45">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Мягкость</span><span class="field-value" id="softVal">0.75</span></div>
        <input type="range" id="softness" min="0.05" max="1" step="0.05" value="0.75">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Сила</span><span class="field-value" id="paintVal">1.00</span></div>
        <input type="range" id="paintStrength" min="0.1" max="1" step="0.05" value="1">
      </div>
    </div>
    <div class="group">
      <div class="group-title">Симметрия</div>
      <div class="row">
        <button id="symNoneBtn" class="active tiny">Свободно</button>
        <button id="symXBtn" class="tiny">По X</button>
        <button id="symYBtn" class="tiny">По Y</button>
        <button id="symXYBtn" class="tiny">X+Y</button>
      </div>
      <div class="row">
        <button id="mirrorBtn" class="tiny wide">🔁 Зеркалить маску</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">История</div>
      <div class="row">
        <button id="undoBtn">↶ Undo</button>
        <button id="redoBtn">↷ Redo</button>
      </div>
      <div class="stat-grid" style="margin-top:4px">
        <div>Undo <span class="v" id="undoCount">0</span></div>
        <div>Redo <span class="v" id="redoCount">0</span></div>
      </div>
    </div>
  </div>

  <!-- GRAB -->
  <div class="tab-content" data-tab="grab">
    <div class="group">
      <div class="group-title">Захват</div>
      <div class="field">
        <div class="field-head"><span class="field-label">Сила прилипания</span><span class="field-value" id="grabVal">0.75</span></div>
        <input type="range" id="grabPow" min="0.05" max="1" step="0.01" value="0.75">
        <div class="field-desc">0.05 = еле тянется · 1.0 = прилипает</div>
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Зона захвата</span><span class="field-value" id="grabRadVal">130</span></div>
        <input type="range" id="grabRadius" min="20" max="500" step="5" value="130">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Мягкость краёв</span><span class="field-value" id="edgeVal">0.15</span></div>
        <input type="range" id="edgeFalloff" min="0" max="1" step="0.05" value="0.15">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Предел растяжения</span><span class="field-value" id="stretchVal">8.0</span></div>
        <input type="range" id="maxStretch" min="1" max="30" step="0.5" value="8">
      </div>
    </div>
    <div class="group">
      <div class="group-title">Режим захвата</div>
      <div class="row">
        <button id="softGrabBtn" class="tiny active">🪶 Плавно</button>
        <button id="deepGrabBtn" class="tiny">📈 Усиление</button>
      </div>
      <div class="row">
        <button id="snapBtn" class="tiny">📌 Snap</button>
        <button id="stickyGrabBtn" class="tiny">🍯 Липкий</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Ограничения</div>
      <div class="row">
        <button id="collidersBtn" class="active tiny">🛡 Коллайдер</button>
        <button id="wallsBtn" class="active tiny">🧱 Стены</button>
      </div>
      <div class="field" style="margin-top:6px">
        <div class="field-head"><span class="field-label">Радиус коллайдера</span><span class="field-value" id="colliderRadVal">2.0</span></div>
        <input type="range" id="colliderRad" min="0.5" max="15" step="0.1" value="2">
      </div>
    </div>
  </div>

  <!-- HAND -->
  <div class="tab-content" data-tab="hand">
    <div class="group">
      <div class="group-title">Ладошка</div>
      <div class="group-desc">Визуальная ладонь следует за курсором. При нажатии — сжимается и «вдавливает» грудь.</div>
      <div class="hand-preview">
        <canvas id="handPreview" width="140" height="100"></canvas>
      </div>
      <div class="row">
        <button id="handShowBtn" class="active tiny wide">👋 Показать</button>
      </div>
      <div class="field" style="margin-top:6px">
        <div class="field-head"><span class="field-label">Размер</span><span class="field-value" id="handSizeVal">80</span></div>
        <input type="range" id="handSize" min="30" max="300" step="5" value="80">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Прозрачность</span><span class="field-value" id="handOpacityVal">0.85</span></div>
        <input type="range" id="handOpacity" min="0.1" max="1" step="0.05" value="0.85">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Поворот</span><span class="field-value" id="handRotVal">-15°</span></div>
        <input type="range" id="handRotation" min="-180" max="180" step="5" value="-15">
      </div>
    </div>
    <div class="group">
      <div class="group-title">Внешний вид</div>
      <div class="row">
        <button id="handSkinLight" class="tiny">Светлая</button>
        <button id="handSkinMedium" class="tiny active">Средняя</button>
        <button id="handSkinDark" class="tiny">Тёмная</button>
      </div>
      <div class="field" style="margin-top:6px">
        <div class="field-head"><span class="field-label">Цвет кожи</span></div>
        <input type="color" id="handColor" value="#ffd4b3" style="width:100%;height:30px;background:#0a0a0e;border:1px solid #23232d;border-radius:4px;cursor:pointer;">
      </div>
      <div class="row" style="margin-top:4px">
        <button id="handShadowBtn" class="active tiny wide">🌑 Тень</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Давление на грудь</div>
      <div class="group-desc">При нажатии ладонь «вдавливает» область вниз — эффект реального нажатия</div>
      <div class="field">
        <div class="field-head"><span class="field-label">Сила давления</span><span class="field-value" id="handPressVal">200</span></div>
        <input type="range" id="handPressForce" min="0" max="800" step="10" value="200">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Радиус давления</span><span class="field-value" id="handRadVal">1.0</span></div>
        <input type="range" id="handRadius" min="0.3" max="2" step="0.05" value="1">
        <div class="field-desc">× размер ладони</div>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Своя картинка</div>
      <div class="group-desc">Загрузите PNG-ладонь (прозрачный фон)</div>
      <div class="row">
        <button id="handCustomBtn" class="tiny">📤 Загрузить</button>
        <button id="handResetBtn" class="danger tiny">Сброс</button>
      </div>
      <input type="file" id="handFile" accept="image/*">
    </div>
  </div>

  <!-- PHYS -->
  <div class="tab-content" data-tab="phys">
    <div class="group">
      <div class="group-title">Пружина</div>
      <div class="field">
        <div class="field-head"><span class="field-label">Скорость возврата</span><span class="field-value" id="stiffVal">6.0</span></div>
        <input type="range" id="stiff" min="0.5" max="40" step="0.5" value="6">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Скорость успокоения</span><span class="field-value" id="dampVal">0.12</span></div>
        <input type="range" id="damp" min="0.01" max="1" step="0.01" value="0.12">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Провисание</span><span class="field-value" id="gravVal">80</span></div>
        <input type="range" id="grav" min="0" max="600" step="5" value="80">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Угол гравитации</span><span class="field-value" id="gravAngleVal">0°</span></div>
        <input type="range" id="gravAngle" min="-180" max="180" step="5" value="0">
      </div>
    </div>
    <div class="group">
      <div class="group-title">Реалистичность</div>
      <div class="field">
        <div class="field-head"><span class="field-label">Анизотропия</span><span class="field-value" id="anisoVal">0.6</span></div>
        <input type="range" id="anisotropy" min="0" max="1" step="0.05" value="0.6">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Нелинейность</span><span class="field-value" id="nonlinVal">0.5</span></div>
        <input type="range" id="nonlinear" min="0" max="3" step="0.1" value="0.5">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Масса снизу</span><span class="field-value" id="massVal">0.4</span></div>
        <input type="range" id="massBottom" min="0" max="1" step="0.05" value="0.4">
      </div>
    </div>
    <div class="group">
      <div class="group-title">Стабильность mesh</div>
      <div class="group-desc">Защита от «поломки» — выворачивания треугольников и артефактов</div>
      <div class="row">
        <button id="meshFixBtn" class="active tiny">🛡 Фикс mesh</button>
        <button id="smoothMeshBtn" class="active tiny">💧 Сглаживание</button>
      </div>
      <div class="field" style="margin-top:6px">
        <div class="field-head"><span class="field-label">Порог инверсии</span><span class="field-value" id="invThreshVal">0.15</span></div>
        <input type="range" id="invThresh" min="0.05" max="0.6" step="0.05" value="0.15">
        <div class="field-desc">Меньше — строже, больше — мягче (может пропускать артефакты)</div>
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Сила сглаживания</span><span class="field-value" id="smoothStrVal">0.15</span></div>
        <input type="range" id="smoothStr" min="0" max="0.5" step="0.05" value="0.15">
      </div>
    </div>
    <div class="group">
      <div class="group-title">Пружинные связи</div>
      <div class="row">
        <button id="springsBtn" class="tiny active">🔗 Включены</button>
      </div>
      <div class="field" style="margin-top:6px">
        <div class="field-head"><span class="field-label">Жёсткость связей</span><span class="field-value" id="springKVal">0.4</span></div>
        <input type="range" id="springK" min="0" max="2" step="0.05" value="0.4">
      </div>
    </div>
    <div class="group">
      <div class="group-title">Сетка</div>
      <div class="field">
        <div class="field-head"><span class="field-label">Разрешение</span><span class="field-value" id="gridResVal">40</span></div>
        <input type="range" id="gridRes" min="15" max="100" step="1" value="40">
      </div>
      <div class="row">
        <button id="rebuildGridBtn" class="wide">Пересоздать</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Точность</div>
      <div class="row">
        <button id="exactSolverBtn" class="active tiny">Стабильно</button>
        <button id="substepBtn" class="tiny">Микро-шаги</button>
      </div>
      <div class="field" style="margin-top:6px">
        <div class="field-head"><span class="field-label">Замедление</span><span class="field-value" id="timeScaleVal">1.0</span></div>
        <input type="range" id="timeScale" min="0.05" max="2" step="0.05" value="1">
      </div>
    </div>
  </div>

  <!-- FX -->
  <div class="tab-content" data-tab="fx">
    <div class="group">
      <div class="group-title">Пассивные эффекты</div>
      <div class="row">
        <button id="breathBtn" class="tiny">🌬 Дыхание</button>
        <button id="windBtn" class="tiny">💨 Ветер</button>
      </div>
      <div class="field" style="margin-top:8px">
        <div class="field-head"><span class="field-label">Амплитуда дыхания</span><span class="field-value" id="breathAmpVal">4.0</span></div>
        <input type="range" id="breathAmp" min="0" max="30" step="0.5" value="4">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Частота дыхания</span><span class="field-value" id="breathFreqVal">1.0</span></div>
        <input type="range" id="breathFreq" min="0.1" max="4" step="0.1" value="1">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Сила ветра</span><span class="field-value" id="windVal">80</span></div>
        <input type="range" id="windForce" min="0" max="500" step="5" value="80">
      </div>
    </div>
    <div class="group">
      <div class="group-title">Мгновенные действия</div>
      <div class="row">
        <button id="shakeBtn">💥 Тряска</button>
        <button id="resetPhysBtn">⟲ Сброс</button>
      </div>
      <div class="row">
        <button id="explodeBtn">💣 Взрыв</button>
        <button id="freezeBtn">❄ Заморозка</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Визуализация</div>
      <div class="row">
        <button id="maskBtn" class="tiny">👁 Маска</button>
        <button id="gridBtn" class="tiny">▦ Сетка</button>
      </div>
      <div class="row">
        <button id="inertiaBtn" class="active tiny">🎞 Инерция</button>
        <button id="pinsBtn" class="tiny">📌 Пины</button>
      </div>
    </div>
  </div>

  <!-- PRESETS -->
  <div class="tab-content" data-tab="presets">
    <div class="group">
      <div class="group-title">Пресеты (20)</div>
      <div class="presets-grid" id="presetsGrid"></div>
    </div>
    <div class="group">
      <div class="group-title">Пользовательские</div>
      <input type="text" id="presetName" placeholder="Имя пресета">
      <div class="row" style="margin-top:4px">
        <button id="savePresetBtn">💾 Сохранить</button>
        <button id="delAllPresetsBtn" class="danger">🗑 Все</button>
      </div>
      <div id="userPresetsList" style="margin-top:6px; display:flex; flex-direction:column; gap:3px;"></div>
    </div>
  </div>

  <!-- MODEL -->
  <div class="tab-content" data-tab="model">
    <div class="group">
      <div class="group-title">Модели</div>
      <div class="row">
        <button id="saveModelBtn">💾 Сохранить</button>
        <button id="loadModelBtn">📂 Загрузить</button>
      </div>
      <div class="row">
        <button id="saveWeightsBtn">📤 Веса</button>
        <button id="loadWeightsBtn">📥 Веса</button>
      </div>
      <div class="row">
        <button id="exportBtn">📸 PNG</button>
        <button id="clearAllBtn" class="danger">🗑 Всё</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Запись</div>
      <div class="field">
        <div class="field-head"><span class="field-label">Длительность (сек)</span></div>
        <input type="number" id="recDuration" value="3" min="1" max="30" step="0.5">
      </div>
      <div class="row">
        <button id="recShakeBtn">🎬 Тряска</button>
        <button id="recGrabBtn">🎬 Авто-лапанье</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Сцена</div>
      <div class="field">
        <div class="field-head"><span class="field-label">Масштаб</span><span class="field-value" id="sceneScaleVal">1.0</span></div>
        <input type="range" id="sceneScale" min="0.3" max="2" step="0.05" value="1">
      </div>
      <div class="field">
        <div class="field-head"><span class="field-label">Фон</span></div>
        <select id="bgSelect" style="width:100%;background:#0a0a0e;color:#ccc;border:1px solid #23232d;border-radius:4px;padding:3px 5px;font-size:10px;">
          <option value="#040406">Чёрный</option>
          <option value="#0e0e13">Тёмный</option>
          <option value="#1a1a22">Серый</option>
          <option value="#ffffff">Белый</option>
          <option value="#ff6fa8">Розовый</option>
          <option value="checker">Шахматка</option>
        </select>
      </div>
      <div class="row">
        <button id="resetCameraBtn" class="wide">⟲ Камера</button>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Статистика</div>
      <div class="stat-grid">
        <div>FPS <span class="v" id="statFps">0</span></div>
        <div>Верш. <span class="v" id="statVerts">0</span></div>
        <div>Инверсий <span class="v" id="statInversions">0</span></div>
        <div>Треуг. <span class="v" id="statTris">0</span></div>
      </div>
    </div>
    <div class="group">
      <div class="group-title">Помощь</div>
      <div class="help">
        <b>Клавиши:</b><br>
        <kbd>1</kbd>–<kbd>4</kbd> режимы · <kbd>R</kbd> сброс · <kbd>Space</kbd> тряска<br>
        <kbd>M</kbd> маска · <kbd>G</kbd> сетка · <kbd>P</kbd> пины<br>
        <kbd>H</kbd> ладонь · <kbd>Ctrl+Z</kbd>/<kbd>Y</kbd> undo/redo<br>
        <kbd>Shift</kbd> быстрая кисть · колесо — размер
      </div>
    </div>
  </div>
</aside>

<main id="stage">
  <canvas id="canvas"></canvas>
  <div id="dropOverlay">
    <div class="icon">🖼</div>
    <div class="title">Перетащите картинку сюда</div>
    <div class="sub">
      или <b>Ctrl+V</b><br>
      или кнопка «Загрузить картинку» слева<br><br>
      Все персонажи — <b>совершеннолетние (18+)</b>
    </div>
  </div>
  <div id="hud">
    <div class="hud-pill">FPS <span class="v" id="hudFps">—</span></div>
    <div class="hud-pill">Зона: <span class="v" id="hudZone">—</span></div>
  </div>
</main>

<div id="toasts"></div>

<div id="modal">
  <div id="modal-box">
    <h3 id="modalTitle">Сообщение</h3>
    <p id="modalText"></p>
    <div class="row">
      <button id="modalCancel">Отмена</button>
      <button id="modalOk" class="accent">OK</button>
    </div>
  </div>
</div>

<script>
'use strict';

/* ============================================================
   0. УТИЛИТЫ
   ============================================================ */
const $ = id => document.getElementById(id);
const $$ = sel => document.querySelectorAll(sel);

function clamp(v, a, b) { return v < a ? a : v > b ? b : v; }
function lerp(a, b, t) { return a + (b - a) * t; }
function smoothstep(t) { return t * t * (3 - 2 * t); }
function uid() { return Math.random().toString(36).slice(2, 10); }
function now() { return performance.now(); }

function toast(msg, kind = '', dur = 2200) {
  const t = document.createElement('div');
  t.className = 'toast ' + kind;
  t.textContent = msg;
  $('toasts').appendChild(t);
  setTimeout(() => t.remove(), dur);
}

function modal(title, text, showCancel = false) {
  return new Promise(res => {
    $('modalTitle').textContent = title;
    $('modalText').textContent = text;
    $('modal').classList.add('show');
    $('modalCancel').style.display = showCancel ? '' : 'none';
    const cleanup = (r) => {
      $('modal').classList.remove('show');
      $('modalOk').onclick = null;
      $('modalCancel').onclick = null;
      res(r);
    };
    $('modalOk').onclick = () => cleanup(true);
    $('modalCancel').onclick = () => cleanup(false);
  });
}

function shadeColor(hex, pct) {
  const num = parseInt(hex.replace('#', ''), 16);
  const r = clamp((num >> 16) + pct, 0, 255) | 0;
  const g = clamp(((num >> 8) & 0xff) + pct, 0, 255) | 0;
  const b = clamp((num & 0xff) + pct, 0, 255) | 0;
  return '#' + ((r << 16) | (g << 8) | b).toString(16).padStart(6, '0');
}

/* ============================================================
   1. СОСТОЯНИЕ
   ============================================================ */
const state = {
  originalImage: null,
  scaledCanvas: null,
  imgW: 0, imgH: 0,

  cols: 0, rows: 0,
  spacingX: 0, spacingY: 0,
  vertices: [],
  triangles: [],
  maskTriangles: [],

  zones: [],
  activeZoneId: null,

  undoStack: [],
  redoStack: [],

  camX: 0, camY: 0, camZoom: 1,

  isDown: false,
  isGrabbing: false,
  pointer: { x: -999, y: -999 },
  lastMove: { x: 0, y: 0 },
  lastPaint: null,
  dragStartCam: null,

  shiftDown: false,
  ctrlDown: false,

  pinMode: false,
  symmetry: 'none',
  brushMode: 'grab',

  breathing: false,
  windOn: false,
  inertia: true,

  autoSave: true,

  fpsAcc: 0, fpsFrames: 0,
  inversions: 0,

  // ЛАДОНЬ
  hand: {
    visible: true,
    size: 80,
    opacity: 0.85,
    rotation: -15 * Math.PI / 180,
    color: '#ffd4b3',
    showShadow: true,
    pressForce: 200,
    radiusScale: 1.0,
    pressAmount: 0,
    image: null,
  },

  cfg: {
    brushSize: 45,
    softness: 0.75,
    paintStrength: 1,

    grabPower: 0.75,
    grabRadius: 130,
    edgeFalloff: 0.15,
    maxStretch: 8,
    colliderRad: 2,
    softGrab: true,
    deepGrab: false,
    stickyGrab: false,

    springK: 0.4,
    springsOn: true,

    stiffness: 6,
    damping: 0.12,
    gravity: 80,
    gravityAngle: 0,
    anisotropy: 0.6,
    nonlinear: 0.5,
    massBottom: 0.4,
    timeScale: 1,

    breathAmp: 4,
    breathFreq: 1,
    windForce: 80,

    showMask: false,
    showGrid: false,
    showPins: false,
    colliders: true,
    walls: true,
    exactSolver: true,
    substep: false,

    meshFix: true,
    smoothMesh: true,
    invThresh: 0.15,
    smoothStr: 0.15,

    sceneScale: 1,
    bg: '#040406',
  },
};

const canvas = $('canvas');
const ctx = canvas.getContext('2d');
const handPreview = $('handPreview');
const hpc = handPreview.getContext('2d');

/* ============================================================
   2. ЗОНЫ
   ============================================================ */
const ZONE_COLORS = ['#ff6fa8','#6fb8ff','#6fff9e','#ffd76f','#c26fff','#ff9e6f','#6ffff0','#ff6fcf','#a0ff6f','#ff6f6f'];

function createZone(name) {
  const id = uid();
  const color = ZONE_COLORS[state.zones.length % ZONE_COLORS.length];
  const zone = {
    id, name: name || ('Зона ' + (state.zones.length + 1)),
    color, visible: true, physicsOn: true,
    weights: new Float32Array(state.vertices.length).fill(0),
    pins: new Uint8Array(state.vertices.length),
  };
  state.zones.push(zone);
  return zone;
}

function getActiveZone() { return state.zones.find(z => z.id === state.activeZoneId); }

function setActiveZone(id) {
  state.activeZoneId = id;
  renderZoneList();
  renderZoneProps();
}

function renderZoneList() {
  const list = $('zoneList');
  list.innerHTML = '';
  for (const z of state.zones) {
    const item = document.createElement('div');
    item.className = 'zone-item' + (z.id === state.activeZoneId ? ' active' : '');
    const color = document.createElement('div');
    color.className = 'zone-color';
    color.style.background = z.color;
    const name = document.createElement('div');
    name.className = 'zone-name';
    name.textContent = z.name;
    const vis = document.createElement('div');
    vis.className = 'zone-vis' + (z.visible ? '' : ' off');
    vis.textContent = z.visible ? '👁' : '🚫';
    vis.addEventListener('click', e => { e.stopPropagation(); z.visible = !z.visible; renderZoneList(); });
    const del = document.createElement('div');
    del.className = 'zone-del';
    del.textContent = '×';
    del.addEventListener('click', e => {
      e.stopPropagation();
      if (state.zones.length <= 1) return toast('Нельзя удалить последнюю', 'error');
      state.zones = state.zones.filter(zz => zz.id !== z.id);
      if (state.activeZoneId === z.id) setActiveZone(state.zones[0].id);
      else renderZoneList();
    });
    item.appendChild(color); item.appendChild(name); item.appendChild(vis); item.appendChild(del);
    item.addEventListener('click', () => setActiveZone(z.id));
    list.appendChild(item);
  }
  $('zoneCount').textContent = state.zones.length;
  $('hudZone').textContent = getActiveZone()?.name || '—';
}

function renderZoneProps() {
  const z = getActiveZone();
  if (!z) return;
  $('zoneName').value = z.name;
  $('zoneVisBtn').classList.toggle('active', z.visible);
  $('zonePhysicsBtn').classList.toggle('active', z.physicsOn);
  $('zoneName').oninput = () => { z.name = $('zoneName').value; renderZoneList(); };
  $('zoneVisBtn').onclick = () => { z.visible = !z.visible; renderZoneProps(); renderZoneList(); };
  $('zonePhysicsBtn').onclick = () => { z.physicsOn = !z.physicsOn; renderZoneProps(); };
  renderZoneColors();
}

function renderZoneColors() {
  const wrap = $('zoneColors');
  wrap.innerHTML = '';
  const z = getActiveZone();
  if (!z) return;
  for (const c of ZONE_COLORS) {
    const btn = document.createElement('button');
    btn.style.cssText = `background:${c};width:20px;height:20px;padding:0;flex:0 0 auto;border:${z.color===c?'2px solid #fff':'1px solid #2c2c38'}`;
    btn.addEventListener('click', () => { z.color = c; renderZoneProps(); renderZoneList(); });
    wrap.appendChild(btn);
  }
}

/* ============================================================
   3. UNDO/REDO
   ============================================================ */
function snapshotZone(zone) {
  return { zoneId: zone.id, weights: new Float32Array(zone.weights), pins: new Uint8Array(zone.pins) };
}
function pushUndo() {
  const z = getActiveZone();
  if (!z) return;
  state.undoStack.push(snapshotZone(z));
  if (state.undoStack.length > 50) state.undoStack.shift();
  state.redoStack = [];
  updateUndoUI();
}
function undo() {
  if (!state.undoStack.length) return toast('Нечего отменять');
  const z = getActiveZone();
  if (!z) return;
  state.redoStack.push(snapshotZone(z));
  const snap = state.undoStack.pop();
  const tz = state.zones.find(zz => zz.id === snap.zoneId);
  if (tz) { tz.weights = snap.weights; tz.pins = snap.pins; }
  updateOmegaAll();
  rebuildMaskTriangles();
  updateUndoUI();
}
function redo() {
  if (!state.redoStack.length) return toast('Нечего повторять');
  const z = getActiveZone();
  if (!z) return;
  state.undoStack.push(snapshotZone(z));
  const snap = state.redoStack.pop();
  const tz = state.zones.find(zz => zz.id === snap.zoneId);
  if (tz) { tz.weights = snap.weights; tz.pins = snap.pins; }
  updateOmegaAll();
  rebuildMaskTriangles();
  updateUndoUI();
}
function updateUndoUI() {
  $('undoCount').textContent = state.undoStack.length;
  $('redoCount').textContent = state.redoStack.length;
}

/* ============================================================
   4. ЗАГРУЗКА КАРТИНКИ
   ============================================================ */
function processFile(file) {
  if (!file) return toast('Файл не выбран', 'error');
  if (!file.type || !file.type.startsWith('image/')) return toast('Не изображение', 'error');
  const reader = new FileReader();
  reader.onerror = () => toast('Ошибка чтения', 'error');
  reader.onload = ev => {
    const img = new Image();
    img.onload = () => {
      if (!img.width || !img.height) return toast('Пустое изображение', 'error');
      loadImageFromElement(img);
    };
    img.onerror = () => toast('Формат не поддерживается', 'error');
    img.src = ev.target.result;
  };
  reader.readAsDataURL(file);
}

$('uploadZone').addEventListener('click', () => $('fileInput').click());
$('fileInput').addEventListener('change', e => { processFile(e.target.files[0]); e.target.value = ''; });

function setupDrop(el) {
  el.addEventListener('dragover', e => {
    e.preventDefault(); e.stopPropagation();
    if (el.id === 'stage') $('stage').classList.add('drag-over');
  });
  el.addEventListener('dragleave', e => {
    e.preventDefault();
    if (el.id === 'stage') $('stage').classList.remove('drag-over');
  });
  el.addEventListener('drop', e => {
    e.preventDefault(); e.stopPropagation();
    $('stage').classList.remove('drag-over');
    if (e.dataTransfer.files[0]) processFile(e.dataTransfer.files[0]);
  });
}
setupDrop($('stage')); setupDrop($('sidebar'));

window.addEventListener('paste', e => {
  const items = e.clipboardData?.items;
  if (!items) return;
  for (const item of items) {
    if (item.type.startsWith('image/')) {
      const f = item.getAsFile();
      if (f) { processFile(f); return; }
    }
  }
});

function loadImageFromElement(img) {
  state.originalImage = img;
  const maxW = Math.min(window.innerWidth - 400, 1400);
  const maxH = window.innerHeight * 0.92;
  const scale = Math.min(maxW / img.width, maxH / img.height, 1);
  state.imgW = Math.max(1, Math.floor(img.width * scale));
  state.imgH = Math.max(1, Math.floor(img.height * scale));

  canvas.width = state.imgW;
  canvas.height = state.imgH;
  canvas.style.width = state.imgW + 'px';
  canvas.style.height = state.imgH + 'px';

  const sc = document.createElement('canvas');
  sc.width = state.imgW; sc.height = state.imgH;
  sc.getContext('2d').drawImage(img, 0, 0, state.imgW, state.imgH);
  state.scaledCanvas = sc;

  state.camX = 0; state.camY = 0; state.camZoom = 1;
  state.zones = []; state.undoStack = []; state.redoStack = [];
  state.activeZoneId = null;

  buildGrid(parseInt($('gridRes').value));
  createZone('Зона 1');
  setActiveZone(state.zones[0].id);

  $('dropOverlay').style.display = 'none';
  updateUndoUI();
  toast('Загружено: ' + state.imgW + '×' + state.imgH, 'success');
}

/* ============================================================
   5. СЕТКА
   ============================================================ */
function buildGrid(res) {
  if (!state.imgW) return;
  const cols = res, rows = res;
  state.cols = cols; state.rows = rows;
  state.spacingX = state.imgW / (cols - 1);
  state.spacingY = state.imgH / (rows - 1);

  state.vertices = [];
  for (let r = 0; r < rows; r++) {
    for (let c = 0; c < cols; c++) {
      const yNorm = r / (rows - 1);
      state.vertices.push({
        ox: c * state.spacingX,
        oy: r * state.spacingY,
        bx: 0, by: 0, bvx: 0, bvy: 0,
        mass: 1 + state.cfg.massBottom * yNorm * 2,
        omegaX: 6, omegaY: 6,
      });
    }
  }

  state.triangles = [];
  for (let r = 0; r < rows - 1; r++) {
    for (let c = 0; c < cols - 1; c++) {
      const i0 = r * cols + c;
      const i1 = r * cols + c + 1;
      const i2 = (r + 1) * cols + c;
      const i3 = (r + 1) * cols + c + 1;
      const l0 = Math.hypot(state.vertices[i1].ox - state.vertices[i0].ox, state.vertices[i1].oy - state.vertices[i0].oy);
      const l1 = Math.hypot(state.vertices[i2].ox - state.vertices[i0].ox, state.vertices[i2].oy - state.vertices[i0].oy);
      // rest area — сохраняем для mesh fix
      const area = (state.vertices[i1].ox - state.vertices[i0].ox) * (state.vertices[i2].oy - state.vertices[i0].oy) -
                   (state.vertices[i2].ox - state.vertices[i0].ox) * (state.vertices[i1].oy - state.vertices[i0].oy);
      state.triangles.push([i0, i1, i2, l0, l1, area]);
      state.triangles.push([i1, i3, i2, l0, l1, area]);
    }
  }
  state.maskTriangles = [];
  updateOmegaAll();
}

function updateOmegaAll() {
  const cfg = state.cfg;
  for (const v of state.vertices) {
    const base = cfg.stiffness;
    v.omegaX = Math.max(0.5, base);
    v.omegaY = Math.max(0.5, base * (1 - cfg.anisotropy * 0.7));
  }
}

function rebuildMaskTriangles() {
  const list = [];
  for (const tri of state.triangles) {
    let maxW = 0;
    for (const z of state.zones) {
      if (!z.visible) continue;
      const w = (z.weights[tri[0]] + z.weights[tri[1]] + z.weights[tri[2]]) / 3;
      if (w > maxW) maxW = w;
    }
    if (maxW > 0.005) list.push(tri);
  }
  state.maskTriangles = list;
}

/* ============================================================
   6. КИСТЬ
   ============================================================ */
function applyBrush(imgX, imgY, radius, mode) {
  const z = getActiveZone();
  if (!z) return;
  const { cols, rows, spacingX, spacingY, vertices } = state;
  const cMin = Math.max(0, Math.floor((imgX - radius) / spacingX));
  const cMax = Math.min(cols - 1, Math.ceil((imgX + radius) / spacingX));
  const rMin = Math.max(0, Math.floor((imgY - radius) / spacingY));
  const rMax = Math.min(rows - 1, Math.ceil((imgY + radius) / spacingY));
  const r2 = radius * radius;
  const soft = state.cfg.softness;
  const innerR = radius * (1 - soft);
  const innerR2 = innerR * innerR;
  const strength = state.cfg.paintStrength;
  const updates = [];

  for (let r = rMin; r <= rMax; r++) {
    for (let c = cMin; c <= cMax; c++) {
      const idx = r * cols + c;
      const v = vertices[idx];
      const dx = v.ox - imgX, dy = v.oy - imgY;
      const d2 = dx * dx + dy * dy;
      if (d2 > r2) continue;
      let t = 1;
      if (d2 > innerR2) {
        const d = Math.sqrt(d2);
        t = 1 - (d - innerR) / (radius - innerR);
        t = smoothstep(t);
      }
      t *= strength;

      if (mode === 'paint') z.weights[idx] = Math.max(z.weights[idx], t);
      else if (mode === 'erase') z.weights[idx] = Math.max(0, z.weights[idx] - t * 0.9);
      else if (mode === 'invert') z.weights[idx] = 1 - z.weights[idx];
      else if (mode === 'smooth' || mode === 'blur') {
        let sum = 0, cnt = 0;
        for (let dr = -1; dr <= 1; dr++) {
          for (let dc = -1; dc <= 1; dc++) {
            const rr = r + dr, cc = c + dc;
            if (rr < 0 || rr >= rows || cc < 0 || cc >= cols) continue;
            sum += z.weights[rr * cols + cc]; cnt++;
          }
        }
        const avg = sum / cnt;
        updates.push({ idx, val: lerp(z.weights[idx], avg, t * (mode === 'blur' ? 1.5 : 1)) });
      } else if (mode === 'pin') {
        z.pins[idx] = 1;
      }
    }
  }
  for (const u of updates) z.weights[u.idx] = u.val;

  // Symmetry
  if (state.symmetry === 'x' || state.symmetry === 'xy') applyBrushMirrored(imgX, imgY, radius, mode, true);
  if (state.symmetry === 'y' || state.symmetry === 'xy') applyBrushMirrored(imgX, imgY, radius, mode, false);

  updateOmegaAll();
  rebuildMaskTriangles();
}

function applyBrushMirrored(imgX, imgY, radius, mode, mirrorX) {
  const z = getActiveZone();
  if (!z) return;
  const { cols, rows, spacingX, spacingY, vertices } = state;
  const mx = mirrorX ? state.imgW - imgX : imgX;
  const my = mirrorX ? imgY : state.imgH - imgY;
  const cMin = Math.max(0, Math.floor((mx - radius) / spacingX));
  const cMax = Math.min(cols - 1, Math.ceil((mx + radius) / spacingX));
  const rMin = Math.max(0, Math.floor((my - radius) / spacingY));
  const rMax = Math.min(rows - 1, Math.ceil((my + radius) / spacingY));
  const r2 = radius * radius;
  const soft = state.cfg.softness;
  const innerR = radius * (1 - soft);
  const innerR2 = innerR * innerR;
  const strength = state.cfg.paintStrength;
  for (let r = rMin; r <= rMax; r++) {
    for (let c = cMin; c <= cMax; c++) {
      const idx = r * cols + c;
      const v = vertices[idx];
      const dx = v.ox - mx, dy = v.oy - my;
      const d2 = dx * dx + dy * dy;
      if (d2 > r2) continue;
      let t = 1;
      if (d2 > innerR2) {
        const d = Math.sqrt(d2);
        t = 1 - (d - innerR) / (radius - innerR);
        t = smoothstep(t);
      }
      t *= strength;
      if (mode === 'paint') z.weights[idx] = Math.max(z.weights[idx], t);
      else if (mode === 'erase') z.weights[idx] = Math.max(0, z.weights[idx] - t * 0.9);
    }
  }
}

function strokeBrush(x0, y0, x1, y1, radius, mode) {
  const dx = x1 - x0, dy = y1 - y0;
  const d = Math.hypot(dx, dy);
  const step = Math.max(1, radius * 0.2);
  const steps = Math.max(1, Math.ceil(d / step));
  for (let i = 0; i <= steps; i++) {
    const t = i / steps;
    applyBrush(x0 + dx * t, y0 + dy * t, radius, mode);
  }
}

function mirrorMaskX() {
  const z = getActiveZone();
  if (!z) return;
  pushUndo();
  const { cols, rows } = state;
  for (let r = 0; r < rows; r++) {
    for (let c = 0; c < Math.floor(cols / 2); c++) {
      const l = r * cols + c, rr = r * cols + (cols - 1 - c);
      const w = Math.max(z.weights[l], z.weights[rr]);
      z.weights[l] = w; z.weights[rr] = w;
    }
  }
  updateOmegaAll();
  rebuildMaskTriangles();
  toast('Маска отзеркалена');
}

/* ============================================================
   7. MESH INTEGRITY (фикс поломки)
   ============================================================ */
function getZoneMaskWeight(i) {
  let m = 0;
  for (const z of state.zones) {
    if (!z.visible || !z.physicsOn) continue;
    if (z.weights[i] > m) m = z.weights[i];
  }
  return m;
}

function hasPinAny(i) {
  for (const z of state.zones) {
    if (!z.visible || !z.physicsOn) continue;
    if (z.pins[i]) return true;
  }
  return false;
}

/**
 * Проверяет каждый треугольник на инверсию (переворот) и чрезмерное сжатие.
 * Плавно возвращает вершины к rest-позициям, если треугольник вывернулся.
 */
function fixMeshIntegrity() {
  if (!state.cfg.meshFix) return;
  const { vertices, triangles } = state;
  const invThresh = state.cfg.invThresh;
  let inversionsFixed = 0;
  let inversionsDetected = 0;

  for (let iter = 0; iter < 2; iter++) {
    let fixed = 0;
    for (const tri of triangles) {
      const [i0, i1, i2, , , restArea] = tri;
      if (Math.abs(restArea) < 1) continue;
      // Пропускаем треугольники вне маски
      if (getZoneMaskWeight(i0) < 0.03 && getZoneMaskWeight(i1) < 0.03 && getZoneMaskWeight(i2) < 0.03) continue;

      const v0 = vertices[i0], v1 = vertices[i1], v2 = vertices[i2];
      // Не трогаем жёстко пришпиленные вершины (только те, что реально пришпилены)
      const pinned0 = hasPinAny(i0), pinned1 = hasPinAny(i1), pinned2 = hasPinAny(i2);

      const x0 = v0.ox + v0.bx, y0 = v0.oy + v0.by;
      const x1 = v1.ox + v1.bx, y1 = v1.oy + v1.by;
      const x2 = v2.ox + v2.bx, y2 = v2.oy + v2.by;
      const curArea = (x1 - x0) * (y2 - y0) - (x2 - x0) * (y1 - y0);

      const ratio = curArea / restArea;

      // Инверсия: знак другой ИЛИ сильное сжатие
      if (ratio < invThresh || ratio > (1 / invThresh)) {
        inversionsDetected++;
        // Возврат к rest (плавный)
        const strength = ratio < 0 ? 0.7 : 0.3;
        if (!pinned0) { v0.bx *= (1 - strength); v0.by *= (1 - strength); }
        if (!pinned1) { v1.bx *= (1 - strength); v1.by *= (1 - strength); }
        if (!pinned2) { v2.bx *= (1 - strength); v2.by *= (1 - strength); }
        // Обнуляем скорости, чтобы не дёргалось
        if (!pinned0) { v0.bvx *= 0.3; v0.bvy *= 0.3; }
        if (!pinned1) { v1.bvx *= 0.3; v1.bvy *= 0.3; }
        if (!pinned2) { v2.bvx *= 0.3; v2.bvy *= 0.3; }
        fixed++;
      }
    }
    inversionsFixed += fixed;
    if (fixed === 0) break;
  }
  state.inversions = inversionsDetected;
}

/**
 * Лапласиан-сглаживание позиций вершин в маске.
 * Устраняет "зазубрины" и "изломы" после физики.
 */
function smoothMesh() {
  if (!state.cfg.smoothMesh) return;
  const blend = state.cfg.smoothStr;
  if (blend <= 0) return;
  const { vertices, cols, rows } = state;

  // Собираем новые позиции только для вершин в маске
  const updates = [];
  for (let r = 1; r < rows - 1; r++) {
    for (let c = 1; c < cols - 1; c++) {
      const i = r * cols + c;
      if (getZoneMaskWeight(i) < 0.05) continue;
      if (hasPinAny(i)) continue;
      const v = vertices[i];
      let sumX = 0, sumY = 0, cnt = 0;
      for (let dr = -1; dr <= 1; dr++) {
        for (let dc = -1; dc <= 1; dc++) {
          if (dr === 0 && dc === 0) continue;
          const j = (r + dr) * cols + (c + dc);
          sumX += vertices[j].bx;
          sumY += vertices[j].by;
          cnt++;
        }
      }
      const avgX = sumX / cnt;
      const avgY = sumY / cnt;
      updates.push({
        v,
        newBx: lerp(v.bx, avgX, blend),
        newBy: lerp(v.by, avgY, blend),
      });
    }
  }
  for (const u of updates) {
    u.v.bx = u.newBx;
    u.v.by = u.newBy;
  }
}

/* ============================================================
   8. ФИЗИКА
   ============================================================ */
function physicsStep(dt) {
  if (!state.vertices.length) return;
  const cfg = state.cfg;
  dt *= cfg.timeScale;
  const substeps = cfg.substep ? 4 : 1;
  for (let s = 0; s < substeps; s++) {
    physicsSubstep(Math.min(dt / substeps, 1 / 60));
  }

  if (cfg.springsOn) springPass(dt);
  if (cfg.meshFix) fixMeshIntegrity();
  if (cfg.smoothMesh) smoothMesh();

  // Анимация ладони
  const targetPress = (state.isDown && state.isGrabbing) ? 1 : 0;
  state.hand.pressAmount = lerp(state.hand.pressAmount, targetPress, dt * 10);

  if (state.inertia) {
    state.camX *= Math.pow(0.98, dt * 60);
    state.camY *= Math.pow(0.98, dt * 60);
  }
}

function physicsSubstep(step) {
  const cfg = state.cfg;
  const t = now() / 1000;
  const breath = state.breathing ? Math.sin(t * cfg.breathFreq * 1.5) * 0.5 + Math.sin(t * cfg.breathFreq * 0.7) * 0.5 : 0;
  const breathForce = breath * cfg.breathAmp;
  const wind = state.windOn ? Math.sin(t * 3) * cfg.windForce : 0;

  const gAngle = cfg.gravityAngle * Math.PI / 180;
  const gravX = cfg.gravity * Math.sin(gAngle);
  const gravY = cfg.gravity * Math.cos(gAngle);

  const doGrab = state.isDown && state.isGrabbing;
  const gx = (state.pointer.x - state.camX) / state.camZoom;
  const gy = (state.pointer.y - state.camY) / state.camZoom;
  const grabR = cfg.grabRadius;
  const grabR2 = grabR * grabR;
  const grabPow = cfg.grabPower * (cfg.softGrab ? 0.5 : 1.0);

  // Давление ладони
  const doHandPress = doGrab && state.hand.visible && state.hand.pressForce > 0;
  const handR = state.hand.size * state.hand.radiusScale * 0.5;
  const handR2 = handR * handR;
  const handForce = state.hand.pressForce * state.hand.pressAmount;

  for (let i = 0; i < state.vertices.length; i++) {
    const v = state.vertices[i];
    const totalW = getZoneMaskWeight(i);

    if (hasPinAny(i)) {
      v.bx = 0; v.by = 0; v.bvx = 0; v.bvy = 0;
      continue;
    }
    if (totalW < 0.005) {
      v.bx *= 0.85; v.by *= 0.85;
      v.bvx *= 0.85; v.bvy *= 0.85;
      continue;
    }

    // Grab
    if (doGrab) {
      const px = v.ox + v.bx, py = v.oy + v.by;
      const dx = gx - px, dy = gy - py;
      const d2 = dx * dx + dy * dy;
      if (d2 < grabR2) {
        const d = Math.sqrt(d2) || 0.001;
        const distFalloff = 1 - d / grabR;
        const edgeFactor = 1 - cfg.edgeFalloff * (1 - totalW);
        const k = grabPow * distFalloff * distFalloff * edgeFactor;
        v.bx += dx * k;
        v.by += dy * k;
        const nx = dx / d, ny = dy / d;
        const vrad = v.bvx * nx + v.bvy * ny;
        if (vrad < 0) { v.bvx -= vrad * nx; v.bvy -= vrad * ny; }
      }
    }

    // Ладонь давит вниз (эффект «вдавливания»)
    if (doHandPress) {
      const px = v.ox + v.bx, py = v.oy + v.by;
      const dx = px - gx, dy = py - gy;
      const d2 = dx * dx + dy * dy;
      if (d2 < handR2) {
        const falloff = 1 - d2 / handR2;
        // Сила вниз + небольшое сжатие к центру
        v.bvy += handForce * falloff * totalW * step;
        const d = Math.sqrt(d2) || 0.001;
        v.bvx -= (dx / d) * handForce * 0.2 * falloff * totalW * step;
        v.bvy -= (dy / d) * handForce * 0.2 * falloff * totalW * step;
      }
    }

    // Spring
    const stretch = Math.hypot(v.bx, v.by) / Math.max(1, state.spacingX);
    const nonlinFactor = 1 + cfg.nonlinear * stretch * stretch;
    const w2x = v.omegaX * v.omegaX * nonlinFactor;
    const w2y = v.omegaY * v.omegaY * nonlinFactor;
    const cx = 2 * cfg.damping * v.omegaX;
    const cy = 2 * cfg.damping * v.omegaY;

    let ax = -w2x * v.bx - cx * v.bvx;
    let ay = -w2y * v.by - cy * v.bvy;

    const mFactor = totalW / v.mass;
    ax += gravX * mFactor;
    ay += gravY * mFactor;
    ay += breathForce * totalW * 0.7;
    ax += wind * totalW * 0.3;

    if (cfg.exactSolver) {
      exactStepAxis(v, ax, step, 'x');
      exactStepAxis(v, ay, step, 'y');
    } else {
      v.bvx += ax * step; v.bvy += ay * step;
      v.bx += v.bvx * step; v.by += v.bvy * step;
    }

    // Collider
    if (cfg.colliders) {
      const maxOff = state.spacingX * cfg.maxStretch;
      const mag = Math.hypot(v.bx, v.by);
      if (mag > maxOff) {
        v.bx = (v.bx / mag) * maxOff;
        v.by = (v.by / mag) * maxOff;
        const nx = v.bx / maxOff, ny = v.by / maxOff;
        const vrad = v.bvx * nx + v.bvy * ny;
        if (vrad > 0) { v.bvx -= vrad * nx; v.bvy -= vrad * ny; }
      }
    }

    // Walls
    if (cfg.walls) {
      const px = v.ox + v.bx, py = v.oy + v.by;
      const wm = 4;
      if (px < wm) { v.bx += wm - px; v.bvx = Math.max(0, v.bvx); }
      if (px > state.imgW - wm) { v.bx -= px - (state.imgW - wm); v.bvx = Math.min(0, v.bvx); }
      if (py < wm) { v.by += wm - py; v.bvy = Math.max(0, v.bvy); }
      if (py > state.imgH - wm) { v.by -= py - (state.imgH - wm); v.bvy = Math.min(0, v.bvy); }
    }
  }
}

function exactStepAxis(v, force, dt, axis) {
  const omega = axis === 'x' ? v.omegaX : v.omegaY;
  const zeta = state.cfg.damping;
  const shift = force / (omega * omega);
  const pos = axis === 'x' ? v.bx : v.by;
  const vel = axis === 'x' ? v.bvx : v.bvy;
  const x0 = pos - shift;
  if (zeta < 1) {
    const wd = omega * Math.sqrt(1 - zeta * zeta);
    const e = Math.exp(-zeta * omega * dt);
    const cos = Math.cos(wd * dt);
    const sin = Math.sin(wd * dt);
    const C = (vel + zeta * omega * x0) / wd;
    const newPos = e * (x0 * cos + C * sin) + shift;
    const newVel = e * (vel * cos - (omega * omega * x0 + zeta * omega * vel) / wd * sin);
    if (axis === 'x') { v.bx = newPos; v.bvx = newVel; }
    else { v.by = newPos; v.bvy = newVel; }
  } else {
    if (axis === 'x') { v.bvx += force * dt; v.bx += v.bvx * dt; }
    else { v.bvy += force * dt; v.by += v.bvy * dt; }
  }
}

function springPass(dt) {
  const k = state.cfg.springK;
  if (k <= 0) return;
  for (const tri of state.triangles) {
    const [i0, i1, i2, restL0, restL1] = tri;
    if (getZoneMaskWeight(i0) < 0.05 && getZoneMaskWeight(i1) < 0.05 && getZoneMaskWeight(i2) < 0.05) continue;
    applySpring(i0, i1, restL0, k, dt);
    applySpring(i0, i2, restL1, k, dt);
  }
}

function applySpring(i, j, restLen, k, dt) {
  const a = state.vertices[i], b = state.vertices[j];
  const ax = a.ox + a.bx, ay = a.oy + a.by;
  const bx = b.ox + b.bx, by = b.oy + b.by;
  const dx = bx - ax, dy = by - ay;
  const curLen = Math.hypot(dx, dy) || 0.001;
  const diff = curLen - restLen;
  const nx = dx / curLen, ny = dy / curLen;
  const force = k * diff;
  if (!hasPinAny(i)) { a.bvx += nx * force * dt; a.bvy += ny * force * dt; }
  if (!hasPinAny(j)) { b.bvx -= nx * force * dt; b.bvy -= ny * force * dt; }
}

/* ============================================================
   9. РЕНДЕР
   ============================================================ */
function render() {
  if (!state.scaledCanvas) {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    return;
  }
  const { imgW, imgH, camX, camY, camZoom, scaledCanvas } = state;

  ctx.setTransform(1, 0, 0, 1, 0, 0);
  ctx.clearRect(0, 0, canvas.width, canvas.height);

  if (state.cfg.bg === 'checker') drawChecker();
  else { ctx.fillStyle = state.cfg.bg; ctx.fillRect(0, 0, canvas.width, canvas.height); }

  ctx.setTransform(camZoom, 0, 0, camZoom, camX, camY);
  ctx.drawImage(scaledCanvas, 0, 0);

  if (state.maskTriangles.length > 0) renderWarp();
  if (state.cfg.showMask) renderMaskOverlay();
  if (state.cfg.showGrid) renderGridOverlay();
  if (state.cfg.showPins) renderPinsOverlay();

  ctx.setTransform(1, 0, 0, 1, 0, 0);
  drawHand();
  renderBrushCursor();
}

function drawChecker() {
  const s = 20;
  ctx.fillStyle = '#14141a';
  ctx.fillRect(0, 0, canvas.width, canvas.height);
  ctx.fillStyle = '#1e1e26';
  for (let y = 0; y < canvas.height; y += s)
    for (let x = 0; x < canvas.width; x += s)
      if (((x / s) + (y / s)) % 2 === 0) ctx.fillRect(x, y, s, s);
}

function renderWarp() {
  const { vertices, maskTriangles } = state;
  const PAD = 0.8;
  for (const tri of maskTriangles) {
    const [i0, i1, i2, , , restArea] = tri;
    const v0 = vertices[i0], v1 = vertices[i1], v2 = vertices[i2];

    const w0 = getZoneMaskWeight(i0);
    const w1 = getZoneMaskWeight(i1);
    const w2 = getZoneMaskWeight(i2);
    const bx0 = v0.bx * w0, by0 = v0.by * w0;
    const bx1 = v1.bx * w1, by1 = v1.by * w1;
    const bx2 = v2.bx * w2, by2 = v2.by * w2;
    const total = Math.abs(bx0) + Math.abs(by0) + Math.abs(bx1) + Math.abs(by1) + Math.abs(bx2) + Math.abs(by2);
    if (total < 0.4) continue;

    const x0 = v0.ox + bx0, y0 = v0.oy + by0;
    const x1 = v1.ox + bx1, y1 = v1.oy + by1;
    const x2 = v2.ox + bx2, y2 = v2.oy + by2;

    const sx0 = v0.ox, sy0 = v0.oy;
    const sx1 = v1.ox, sy1 = v1.oy;
    const sx2 = v2.ox, sy2 = v2.oy;

    const detRest = (sx1 - sx0) * (sy2 - sy0) - (sx2 - sx0) * (sy1 - sy0);
    if (Math.abs(detRest) < 1e-8) continue;

    const detTarget = (x1 - x0) * (y2 - y0) - (x2 - x0) * (y1 - y0);
    // Поломка: треугольник вывернулся — пропускаем (в физике fixMesh должен был это предотвратить)
    if (Math.sign(detTarget) !== Math.sign(detRest)) {
      // Рисуем rest-версию (без искажения) — так лучше, чем артефакт
      continue;
    }
    // Чрезмерное сжатие/растяжение — пропускаем
    const areaRatio = Math.abs(detTarget / detRest);
    if (areaRatio < 0.02 || areaRatio > 50) continue;

    const cx = (x0 + x1 + x2) / 3, cy = (y0 + y1 + y2) / 3;
    const expand = (px, py) => {
      const dx = px - cx, dy = py - cy;
      const d = Math.hypot(dx, dy) || 1;
      return [px + (dx / d) * PAD, py + (dy / d) * PAD];
    };
    const [ex0, ey0] = expand(x0, y0);
    const [ex1, ey1] = expand(x1, y1);
    const [ex2, ey2] = expand(x2, y2);

    const a = ((x1 - x0) * (sy2 - sy0) - (x2 - x0) * (sy1 - sy0)) / detRest;
    const b = ((y1 - y0) * (sy2 - sy0) - (y2 - y0) * (sy1 - sy0)) / detRest;
    const cc = ((x2 - x0) * (sx1 - sx0) - (x1 - x0) * (sx2 - sx0)) / detRest;
    const d = ((y2 - y0) * (sx1 - sx0) - (y1 - y0) * (sx2 - sx0)) / detRest;
    const e = x0 - a * sx0 - cc * sy0;
    const f = y0 - b * sx0 - d * sy0;

    ctx.save();
    ctx.beginPath();
    ctx.moveTo(ex0, ey0); ctx.lineTo(ex1, ey1); ctx.lineTo(ex2, ey2);
    ctx.closePath();
    ctx.clip();
    ctx.transform(a, b, cc, d, e, f);
    ctx.drawImage(state.scaledCanvas, 0, 0);
    ctx.restore();
  }
}

function renderMaskOverlay() {
  const { vertices } = state;
  ctx.save();
  for (const z of state.zones) {
    if (!z.visible) continue;
    ctx.fillStyle = z.color;
    ctx.globalAlpha = 0.35;
    for (let i = 0; i < vertices.length; i++) {
      const w = z.weights[i];
      if (w < 0.02) continue;
      const v = vertices[i];
      const r = 1 + w * 4;
      ctx.beginPath();
      ctx.arc(v.ox + v.bx * w, v.oy + v.by * w, r, 0, Math.PI * 2);
      ctx.fill();
    }
  }
  ctx.globalAlpha = 1;
  ctx.restore();
}

function renderGridOverlay() {
  const { vertices, cols, rows } = state;
  ctx.save();
  ctx.strokeStyle = 'rgba(100,180,255,0.12)';
  ctx.lineWidth = 0.4;
  for (let r = 0; r < rows; r++) {
    ctx.beginPath();
    for (let c = 0; c < cols; c++) {
      const i = r * cols + c;
      const v = vertices[i];
      const w = getZoneMaskWeight(i);
      const px = v.ox + v.bx * w, py = v.oy + v.by * w;
      if (c === 0) ctx.moveTo(px, py); else ctx.lineTo(px, py);
    }
    ctx.stroke();
  }
  for (let c = 0; c < cols; c++) {
    ctx.beginPath();
    for (let r = 0; r < rows; r++) {
      const i = r * cols + c;
      const v = vertices[i];
      const w = getZoneMaskWeight(i);
      const px = v.ox + v.bx * w, py = v.oy + v.by * w;
      if (r === 0) ctx.moveTo(px, py); else ctx.lineTo(px, py);
    }
    ctx.stroke();
  }
  ctx.restore();
}

function renderPinsOverlay() {
  const { vertices } = state;
  ctx.save();
  ctx.fillStyle = '#ff5050';
  for (const z of state.zones) {
    if (!z.visible) continue;
    for (let i = 0; i < vertices.length; i++) {
      if (!z.pins[i]) continue;
      ctx.beginPath();
      ctx.arc(vertices[i].ox, vertices[i].oy, 3, 0, Math.PI * 2);
      ctx.fill();
    }
  }
  ctx.restore();
}

function renderBrushCursor() {
  const { pointer, isDown, cfg, brushMode } = state;
  if (pointer.x < 0) return;
  // Скрываем курсор-кисть если показываем ладонь в режиме grab
  if (state.hand.visible && brushMode === 'grab') return;
  let radius;
  if (brushMode === 'grab') radius = cfg.grabRadius;
  else radius = cfg.brushSize;
  ctx.save();
  ctx.strokeStyle = state.isGrabbing ? 'rgba(255,111,168,0.9)' : 'rgba(255,255,255,0.5)';
  ctx.lineWidth = 1.2;
  ctx.setLineDash(isDown ? [] : [3, 4]);
  ctx.beginPath();
  ctx.arc(pointer.x, pointer.y, radius * state.camZoom, 0, Math.PI * 2);
  ctx.stroke();
  ctx.restore();
}

/* ============================================================
   10. ЛАДОНЬ
   ============================================================ */
function drawHand() {
  if (!state.hand.visible) return;
  if (!state.scaledCanvas) return;
  const { pointer, hand } = state;
  if (pointer.x < 0) return;

  ctx.save();
  ctx.translate(pointer.x, pointer.y);
  ctx.rotate(hand.rotation);
  ctx.globalAlpha = hand.opacity * (0.8 + 0.15 * hand.pressAmount);

  if (hand.image) {
    const s = hand.size * 2;
    ctx.drawImage(hand.image, -s / 2, -s / 2, s, s);
  } else {
    drawProceduralHand(ctx, hand);
  }
  ctx.restore();
}

function drawProceduralHand(c, hand) {
  const s = hand.size / 80; // base scale 80 → 1x
  const press = hand.pressAmount;
  const skin = hand.color;
  const darker = shadeColor(skin, -25);
  const darker2 = shadeColor(skin, -50);
  const lighter = shadeColor(skin, 25);

  if (hand.showShadow) {
    c.shadowColor = 'rgba(0,0,0,0.45)';
    c.shadowBlur = 14 * s;
    c.shadowOffsetY = 6 * s;
  }

  // Контур ладони с 4 пальцами + большой палец
  c.fillStyle = skin;
  c.beginPath();
  // левый край ладони
  c.moveTo(-0.38 * s, 0.30 * s);
  c.quadraticCurveTo(-0.45 * s, 0.05 * s, -0.40 * s, -0.15 * s);
  // указательный
  c.lineTo(-0.32 * s, -0.70 * s + press * 0.10 * s);
  c.quadraticCurveTo(-0.30 * s, -0.85 * s, -0.22 * s, -0.85 * s);
  c.quadraticCurveTo(-0.14 * s, -0.85 * s, -0.13 * s, -0.68 * s);
  // ложбинка
  c.lineTo(-0.11 * s, -0.25 * s);
  // средний (самый длинный)
  c.lineTo(-0.06 * s, -0.78 * s + press * 0.12 * s);
  c.quadraticCurveTo(-0.03 * s, -0.93 * s, 0.05 * s, -0.93 * s);
  c.quadraticCurveTo(0.13 * s, -0.93 * s, 0.14 * s, -0.76 * s);
  c.lineTo(0.14 * s, -0.25 * s);
  // безымянный
  c.lineTo(0.18 * s, -0.72 * s + press * 0.10 * s);
  c.quadraticCurveTo(0.21 * s, -0.86 * s, 0.29 * s, -0.86 * s);
  c.quadraticCurveTo(0.37 * s, -0.86 * s, 0.37 * s, -0.70 * s);
  c.lineTo(0.34 * s, -0.20 * s);
  // мизинец
  c.lineTo(0.39 * s, -0.55 * s + press * 0.08 * s);
  c.quadraticCurveTo(0.42 * s, -0.68 * s, 0.48 * s, -0.68 * s);
  c.quadraticCurveTo(0.55 * s, -0.68 * s, 0.54 * s, -0.52 * s);
  c.lineTo(0.50 * s, -0.05 * s);
  // правый край + большой палец
  c.quadraticCurveTo(0.56 * s, 0.22 * s, 0.42 * s, 0.34 * s);
  c.quadraticCurveTo(0.20 * s, 0.44 * s, 0, 0.44 * s);
  c.quadraticCurveTo(-0.25 * s, 0.44 * s, -0.38 * s, 0.30 * s);
  c.closePath();
  c.fill();

  // Сброс тени для деталей
  c.shadowColor = 'transparent';
  c.shadowBlur = 0;
  c.shadowOffsetY = 0;

  // Ладонные складки
  c.strokeStyle = darker;
  c.lineWidth = 1.4;
  c.lineCap = 'round';
  c.beginPath();
  c.moveTo(-0.11 * s, -0.25 * s);
  c.lineTo(-0.10 * s, 0.10 * s);
  c.moveTo(0.14 * s, -0.25 * s);
  c.lineTo(0.13 * s, 0.10 * s);
  c.moveTo(0.34 * s, -0.20 * s);
  c.lineTo(0.33 * s, 0.08 * s);
  c.stroke();

  // Линии на ладони
  c.strokeStyle = darker2;
  c.lineWidth = 1;
  c.beginPath();
  c.moveTo(-0.28 * s, 0.08 * s);
  c.quadraticCurveTo(-0.10 * s, 0.18 * s, 0.22 * s, 0.12 * s);
  c.stroke();
  c.beginPath();
  c.moveTo(-0.22 * s, 0.22 * s);
  c.quadraticCurveTo(0.0 * s, 0.28 * s, 0.28 * s, 0.22 * s);
  c.stroke();

  // Блики на костяшках
  c.fillStyle = lighter;
  c.globalAlpha = hand.opacity * 0.4;
  for (const kx of [-0.23, 0.05, 0.29]) {
    c.beginPath();
    c.arc(kx * s, -0.35 * s, 0.05 * s, 0, Math.PI * 2);
    c.fill();
  }
  c.globalAlpha = hand.opacity * (0.8 + 0.15 * press);

  // Пальцы «сжимаются» при нажатии — лёгкое затемнение кончиков
  c.fillStyle = darker;
  c.globalAlpha = 0.15 * press * hand.opacity;
  c.beginPath();
  c.arc(-0.22 * s, -0.75 * s, 0.06 * s, 0, Math.PI * 2);
  c.arc(0.05 * s, -0.82 * s, 0.06 * s, 0, Math.PI * 2);
  c.arc(0.29 * s, -0.75 * s, 0.06 * s, 0, Math.PI * 2);
  c.arc(0.48 * s, -0.58 * s, 0.05 * s, 0, Math.PI * 2);
  c.fill();
}

function drawHandPreview() {
  hpc.clearRect(0, 0, handPreview.width, handPreview.height);
  // Превью с базовым размером
  const previewHand = { ...state.hand, size: 80 * (handPreview.height / 180), pressAmount: 0, image: state.hand.image };
  hpc.save();
  hpc.translate(handPreview.width / 2, handPreview.height / 2 + 20);
  if (previewHand.image) {
    const s = previewHand.size * 2;
    hpc.drawImage(previewHand.image, -s / 2, -s / 2, s, s);
  } else {
    drawProceduralHand(hpc, previewHand);
  }
  hpc.restore();
}

/* ============================================================
   11. ВВОД
   ============================================================ */
function getCanvasPos(e) {
  const r = canvas.getBoundingClientRect();
  return {
    x: (e.clientX - r.left) * (canvas.width / r.width),
    y: (e.clientY - r.top) * (canvas.height / r.height),
  };
}
function getImgPos(cp) {
  return { x: (cp.x - state.camX) / state.camZoom, y: (cp.y - state.camY) / state.camZoom };
}

function isInsideAnyMask(imgX, imgY) {
  const { cols, rows, spacingX, spacingY } = state;
  if (imgX < 0 || imgX >= state.imgW || imgY < 0 || imgY >= state.imgH) return false;
  const c = clamp(Math.round(imgX / spacingX), 0, cols - 1);
  const r = clamp(Math.round(imgY / spacingY), 0, rows - 1);
  return getZoneMaskWeight(r * cols + c) > 0.04;
}

canvas.addEventListener('pointerdown', e => {
  if (!state.scaledCanvas) return;
  canvas.setPointerCapture(e.pointerId);
  const cp = getCanvasPos(e);
  const ip = getImgPos(cp);
  state.pointer = cp;
  state.isDown = true;
  state.lastMove = cp;

  if (e.button === 1) {
    state.dragStartCam = { x: cp.x - state.camX, y: cp.y - state.camY };
    return;
  }
  if (state.pinMode) {
    const z = getActiveZone();
    if (z) {
      const { cols, rows, spacingX, spacingY } = state;
      const c = clamp(Math.round(ip.x / spacingX), 0, cols - 1);
      const r = clamp(Math.round(ip.y / spacingY), 0, rows - 1);
      const idx = r * cols + c;
      pushUndo();
      z.pins[idx] = z.pins[idx] ? 0 : 1;
      updatePinCount();
    }
    return;
  }

  const mode = state.shiftDown ? 'paint' : state.brushMode;

  if (mode === 'grab') {
    state.isGrabbing = isInsideAnyMask(ip.x, ip.y);
  } else {
    pushUndo();
    state.lastPaint = ip;
    applyBrush(ip.x, ip.y, state.cfg.brushSize, mode);
  }
});

canvas.addEventListener('pointermove', e => {
  if (!state.scaledCanvas) return;
  const cp = getCanvasPos(e);
  state.pointer = cp;
  const ip = getImgPos(cp);
  if (!state.isDown) return;

  if (state.dragStartCam) {
    state.camX = cp.x - state.dragStartCam.x;
    state.camY = cp.y - state.dragStartCam.y;
    return;
  }
  if (state.brushMode !== 'grab' && !state.pinMode) {
    const mode = state.shiftDown ? 'paint' : state.brushMode;
    if (state.lastPaint) strokeBrush(state.lastPaint.x, state.lastPaint.y, ip.x, ip.y, state.cfg.brushSize, mode);
    state.lastPaint = ip;
    return;
  }
  if (!state.isGrabbing) {
    const dx = cp.x - state.lastMove.x;
    const dy = cp.y - state.lastMove.y;
    state.camX += dx; state.camY += dy;
  }
  state.lastMove = cp;
});

canvas.addEventListener('pointerup', e => {
  if (state.dragStartCam && e.button === 1) state.dragStartCam = null;
  state.isDown = false;
  state.isGrabbing = false;
  state.lastPaint = null;
});

canvas.addEventListener('pointercancel', () => {
  state.isDown = false; state.isGrabbing = false;
  state.lastPaint = null; state.dragStartCam = null;
});

canvas.addEventListener('pointerleave', () => {
  if (!state.isDown) state.pointer = { x: -999, y: -999 };
});

canvas.addEventListener('wheel', e => {
  if (!state.scaledCanvas) return;
  e.preventDefault();
  const delta = Math.sign(e.deltaY);
  if (e.ctrlKey) {
    const old = state.camZoom;
    state.camZoom = clamp(state.camZoom * (delta > 0 ? 0.9 : 1.1), 0.1, 10);
    const cp = getCanvasPos(e);
    state.camX = cp.x - (cp.x - state.camX) * (state.camZoom / old);
    state.camY = cp.y - (cp.y - state.camY) * (state.camZoom / old);
  } else {
    const key = state.brushMode === 'grab' ? 'grabRadius' : 'brushSize';
    const step = state.brushMode === 'grab' ? 5 : 4;
    state.cfg[key] = clamp(state.cfg[key] - delta * step, 4, 500);
    const sid = key === 'grabRadius' ? 'grabRadius' : 'brushSize';
    const vid = key === 'grabRadius' ? 'grabRadVal' : 'brushVal';
    $(sid).value = state.cfg[key];
    $(vid).textContent = state.cfg[key];
  }
}, { passive: false });

canvas.addEventListener('contextmenu', e => e.preventDefault());

window.addEventListener('keydown', e => {
  if (e.target.tagName === 'INPUT' || e.target.tagName === 'TEXTAREA') return;
  if (e.key === 'Shift') state.shiftDown = true;
  if (e.key === 'Control') state.ctrlDown = true;
  if ((e.ctrlKey || state.ctrlDown) && e.key === 'z') { e.preventDefault(); undo(); }
  if ((e.ctrlKey || state.ctrlDown) && e.key === 'y') { e.preventDefault(); redo(); }
  if (e.key === '1') document.querySelector('[data-mode="grab"]')?.click();
  if (e.key === '2') document.querySelector('[data-mode="paint"]')?.click();
  if (e.key === '3') document.querySelector('[data-mode="erase"]')?.click();
  if (e.key === '4') document.querySelector('[data-mode="smooth"]')?.click();
  if (e.key === ' ') { e.preventDefault(); $('shakeBtn')?.click(); }
  if (e.key.toLowerCase() === 'm') $('maskBtn')?.click();
  if (e.key.toLowerCase() === 'g') $('gridBtn')?.click();
  if (e.key.toLowerCase() === 'p') $('pinsBtn')?.click();
  if (e.key.toLowerCase() === 'h') $('handShowBtn')?.click();
  if (e.key === '0') $('resetCameraBtn')?.click();
  if (e.key.toLowerCase() === 'r') $('resetPhysBtn')?.click();
});
window.addEventListener('keyup', e => {
  if (e.key === 'Shift') state.shiftDown = false;
  if (e.key === 'Control') state.ctrlDown = false;
});

function updatePinCount() {
  const z = getActiveZone();
  if (!z) return;
  let cnt = 0;
  for (let i = 0; i < z.pins.length; i++) if (z.pins[i]) cnt++;
  $('pinCount').textContent = cnt;
}

/* ============================================================
   12. ПРЕСЕТЫ
   ============================================================ */
const PRESETS = {
  soft:      { name: '🪶 Мягкая',    cfg: { stiffness: 4, damping: 0.35, gravity: 40, grabPower: 0.55, grabRadius: 140, maxStretch: 6, edgeFalloff: 0.3, anisotropy: 0.4 } },
  medium:    { name: '⚖ Средняя',   cfg: { stiffness: 6, damping: 0.12, gravity: 80, grabPower: 0.75, grabRadius: 130, maxStretch: 8, edgeFalloff: 0.15, anisotropy: 0.6 } },
  bouncy:    { name: '🏀 Прыгучая', cfg: { stiffness: 14, damping: 0.05, gravity: 100, grabPower: 0.9, grabRadius: 110, maxStretch: 10, edgeFalloff: 0.1, anisotropy: 0.5 } },
  heavy:     { name: '🪨 Тяжёлая',  cfg: { stiffness: 3, damping: 0.45, gravity: 250, grabPower: 0.6, grabRadius: 120, maxStretch: 5, edgeFalloff: 0.4, anisotropy: 0.8 } },
  jelly:     { name: '🍮 Желе',     cfg: { stiffness: 10, damping: 0.03, gravity: 70, grabPower: 0.85, grabRadius: 140, maxStretch: 12, edgeFalloff: 0.1, anisotropy: 0.3 } },
  realistic: { name: '🎯 Реализм',  cfg: { stiffness: 8, damping: 0.25, gravity: 120, grabPower: 0.65, grabRadius: 120, maxStretch: 7, edgeFalloff: 0.25, anisotropy: 0.7 } },
  anime:     { name: '✨ Аниме',    cfg: { stiffness: 12, damping: 0.08, gravity: 60, grabPower: 0.9, grabRadius: 130, maxStretch: 11, edgeFalloff: 0.12, anisotropy: 0.5 } },
  extreme:   { name: '💥 Экстрим',  cfg: { stiffness: 20, damping: 0.02, gravity: 150, grabPower: 1, grabRadius: 150, maxStretch: 15, edgeFalloff: 0.05, anisotropy: 0.4 } },
  butter:    { name: '🧈 Масло',    cfg: { stiffness: 2, damping: 0.5, gravity: 30, grabPower: 0.4, grabRadius: 160, maxStretch: 10, edgeFalloff: 0.5, anisotropy: 0.5 } },
  brick:     { name: '🧱 Кирпич',   cfg: { stiffness: 30, damping: 0.8, gravity: 200, grabPower: 0.2, grabRadius: 80, maxStretch: 2, edgeFalloff: 0.8, anisotropy: 0.1 } },
  floaty:    { name: '🎈 Невесомость', cfg: { stiffness: 5, damping: 0.08, gravity: 10, grabPower: 0.5, grabRadius: 150, maxStretch: 12, edgeFalloff: 0.3, anisotropy: 0.2 } },
  springy:   { name: '🌀 Пружина',  cfg: { stiffness: 18, damping: 0.04, gravity: 90, grabPower: 0.95, grabRadius: 120, maxStretch: 9, edgeFalloff: 0.15, anisotropy: 0.4 } },
  wobble:    { name: '🌊 Волна',    cfg: { stiffness: 7, damping: 0.06, gravity: 100, grabPower: 0.8, grabRadius: 140, maxStretch: 10, edgeFalloff: 0.2, anisotropy: 0.6 } },
  saggy:     { name: '⬇ Провисшая', cfg: { stiffness: 4, damping: 0.4, gravity: 300, grabPower: 0.7, grabRadius: 130, maxStretch: 8, edgeFalloff: 0.35, anisotropy: 0.9 } },
  perky:     { name: '⬆ Упругая',   cfg: { stiffness: 15, damping: 0.2, gravity: 30, grabPower: 0.85, grabRadius: 100, maxStretch: 7, edgeFalloff: 0.1, anisotropy: 0.2 } },
  huge:      { name: '🍑 Огромная', cfg: { stiffness: 5, damping: 0.15, gravity: 180, grabPower: 0.7, grabRadius: 180, maxStretch: 14, edgeFalloff: 0.3, anisotropy: 0.7 } },
  tiny:      { name: '🌸 Маленькая', cfg: { stiffness: 20, damping: 0.3, gravity: 40, grabPower: 0.8, grabRadius: 70, maxStretch: 4, edgeFalloff: 0.2, anisotropy: 0.3 } },
  silk:      { name: '🎀 Шёлк',     cfg: { stiffness: 6, damping: 0.05, gravity: 50, grabPower: 0.6, grabRadius: 150, maxStretch: 11, edgeFalloff: 0.15, anisotropy: 0.5 } },
  chaos:     { name: '🌪 Хаос',     cfg: { stiffness: 15, damping: 0.01, gravity: 150, grabPower: 1, grabRadius: 200, maxStretch: 15, edgeFalloff: 0.02, anisotropy: 0.6 } },
  balloon:   { name: '🎈 Воздушный', cfg: { stiffness: 8, damping: 0.05, gravity: 20, grabPower: 0.9, grabRadius: 140, maxStretch: 10, edgeFalloff: 0.1, anisotropy: 0.2 } },
  water:     { name: '💧 Вода',     cfg: { stiffness: 4, damping: 0.08, gravity: 80, grabPower: 0.8, grabRadius: 180, maxStretch: 18, edgeFalloff: 0.2, anisotropy: 0.6 } },
};

function applyPreset(key) {
  const p = PRESETS[key];
  if (!p) return;
  Object.assign(state.cfg, p.cfg);
  syncAllSliders();
  updateOmegaAll();
  toast('Пресет: ' + p.name);
}

function syncAllSliders() {
  const map = {
    brushSize:'brushVal', softness:'softVal', paintStrength:'paintVal',
    grabPower:'grabVal', grabRadius:'grabRadVal', edgeFalloff:'edgeVal',
    maxStretch:'stretchVal', stiffness:'stiffVal', damping:'dampVal',
    gravity:'gravVal', gravityAngle:'gravAngleVal', anisotropy:'anisoVal',
    nonlinear:'nonlinVal', massBottom:'massVal', breathAmp:'breathAmpVal',
    breathFreq:'breathFreqVal', windForce:'windVal', sceneScale:'sceneScaleVal',
    colliderRad:'colliderRadVal', springK:'springKVal', timeScale:'timeScaleVal',
    invThresh:'invThreshVal', smoothStr:'smoothStrVal',
  };
  for (const [k, vid] of Object.entries(map)) {
    const el = $(k); const v = $(vid);
    if (el) el.value = state.cfg[k];
    if (v) v.textContent = typeof state.cfg[k] === 'number' ? state.cfg[k].toFixed(2) : state.cfg[k];
  }
}

function renderPresetsGrid() {
  const grid = $('presetsGrid');
  grid.innerHTML = '';
  for (const [k, p] of Object.entries(PRESETS)) {
    const btn = document.createElement('button');
    btn.textContent = p.name;
    btn.addEventListener('click', () => applyPreset(k));
    grid.appendChild(btn);
  }
}

function loadUserPresets() {
  try { return JSON.parse(localStorage.getItem('anime_jiggle_v7_presets') || '{}'); }
  catch { return {}; }
}
function saveUserPresets(p) { localStorage.setItem('anime_jiggle_v7_presets', JSON.stringify(p)); }
function renderUserPresets() {
  const list = $('userPresetsList');
  const presets = loadUserPresets();
  list.innerHTML = '';
  const keys = Object.keys(presets);
  if (!keys.length) { list.innerHTML = '<div style="font-size:10px;color:#444">Пусто</div>'; return; }
  for (const k of keys) {
    const row = document.createElement('div'); row.className = 'row';
    const b = document.createElement('button');
    b.textContent = k; b.style.flex = '1';
    b.addEventListener('click', () => { Object.assign(state.cfg, presets[k]); syncAllSliders(); updateOmegaAll(); toast('Пресет: ' + k); });
    const del = document.createElement('button');
    del.textContent = '×'; del.className = 'danger tiny';
    del.addEventListener('click', () => { delete presets[k]; saveUserPresets(presets); renderUserPresets(); });
    row.appendChild(b); row.appendChild(del);
    list.appendChild(row);
  }
}

/* ============================================================
   13. UI — ТАБЫ И ГРУППЫ
   ============================================================ */
$$('.tab').forEach(t => {
  t.addEventListener('click', () => {
    $$('.tab').forEach(x => x.classList.remove('active'));
    $$('.tab-content').forEach(x => x.classList.remove('active'));
    t.classList.add('active');
    document.querySelector(`.tab-content[data-tab="${t.dataset.tab}"]`).classList.add('active');
  });
});
$$('.group-title').forEach(title => {
  title.addEventListener('click', () => title.parentElement.classList.toggle('collapsed'));
});

/* ============================================================
   14. UI — СЛАЙДЕРЫ
   ============================================================ */
function bindSlider(id, valId, key, fmt, onChange) {
  const el = $(id), span = $(valId);
  if (!el || !span) return;
  const update = () => {
    const v = parseFloat(el.value);
    state.cfg[key] = v;
    span.textContent = fmt ? fmt(v) : v;
    if (onChange) onChange(v);
  };
  el.addEventListener('input', update);
  update();
}

bindSlider('brushSize','brushVal','brushSize', v => v.toFixed(0));
bindSlider('softness','softVal','softness', v => v.toFixed(2));
bindSlider('paintStrength','paintVal','paintStrength', v => v.toFixed(2));
bindSlider('grabPow','grabVal','grabPower', v => v.toFixed(2));
bindSlider('grabRadius','grabRadVal','grabRadius', v => v.toFixed(0));
bindSlider('edgeFalloff','edgeVal','edgeFalloff', v => v.toFixed(2));
bindSlider('maxStretch','stretchVal','maxStretch', v => v.toFixed(1));
bindSlider('stiff','stiffVal','stiffness', v => v.toFixed(1), updateOmegaAll);
bindSlider('damp','dampVal','damping', v => v.toFixed(2));
bindSlider('grav','gravVal','gravity', v => v.toFixed(0));
bindSlider('gravAngle','gravAngleVal','gravityAngle', v => v.toFixed(0) + '°');
bindSlider('anisotropy','anisoVal','anisotropy', v => v.toFixed(2), updateOmegaAll);
bindSlider('nonlinear','nonlinVal','nonlinear', v => v.toFixed(1));
bindSlider('massBottom','massVal','massBottom', v => v.toFixed(2), () => {
  const rows = state.rows;
  for (let r = 0; r < rows; r++)
    for (let c = 0; c < state.cols; c++) {
      const idx = r * state.cols + c;
      const yNorm = r / (rows - 1);
      state.vertices[idx].mass = 1 + state.cfg.massBottom * yNorm * 2;
    }
});
bindSlider('colliderRad','colliderRadVal','colliderRad', v => v.toFixed(1));
bindSlider('breathAmp','breathAmpVal','breathAmp', v => v.toFixed(1));
bindSlider('breathFreq','breathFreqVal','breathFreq', v => v.toFixed(1));
bindSlider('windForce','windVal','windForce', v => v.toFixed(0));
bindSlider('sceneScale','sceneScaleVal','sceneScale', v => v.toFixed(2), v => {
  canvas.style.transform = `scale(${v})`;
  canvas.style.transformOrigin = 'center';
});
bindSlider('springK','springKVal','springK', v => v.toFixed(2));
bindSlider('timeScale','timeScaleVal','timeScale', v => v.toFixed(2));
bindSlider('invThresh','invThreshVal','invThresh', v => v.toFixed(2));
bindSlider('smoothStr','smoothStrVal','smoothStr', v => v.toFixed(2));

// Слайдеры ладони
bindSlider('handSize','handSizeVal','handSizeProxy', v => v.toFixed(0), v => { state.hand.size = v; drawHandPreview(); });
// Заменим напрямую
$('handSize').addEventListener('input', () => {
  state.hand.size = parseFloat($('handSize').value);
  $('handSizeVal').textContent = state.hand.size.toFixed(0);
  drawHandPreview();
});
$('handOpacity').addEventListener('input', () => {
  state.hand.opacity = parseFloat($('handOpacity').value);
  $('handOpacityVal').textContent = state.hand.opacity.toFixed(2);
});
$('handRotation').addEventListener('input', () => {
  const deg = parseFloat($('handRotation').value);
  state.hand.rotation = deg * Math.PI / 180;
  $('handRotVal').textContent = deg.toFixed(0) + '°';
});
$('handColor').addEventListener('input', () => { state.hand.color = $('handColor').value; drawHandPreview(); });
$('handPressForce').addEventListener('input', () => {
  state.hand.pressForce = parseFloat($('handPressForce').value);
  $('handPressVal').textContent = state.hand.pressForce.toFixed(0);
});
$('handRadius').addEventListener('input', () => {
  state.hand.radiusScale = parseFloat($('handRadius').value);
  $('handRadVal').textContent = state.hand.radiusScale.toFixed(2);
});
$('handShowBtn').addEventListener('click', () => {
  state.hand.visible = !state.hand.visible;
  $('handShowBtn').classList.toggle('active', state.hand.visible);
  $('handShowBtn').textContent = state.hand.visible ? '👋 Показать' : '🚫 Скрыть';
});
$('handShadowBtn').addEventListener('click', () => {
  state.hand.showShadow = !state.hand.showShadow;
  $('handShadowBtn').classList.toggle('active', state.hand.showShadow);
});
$('handSkinLight').addEventListener('click', () => { state.hand.color = '#ffe0c8'; $('handColor').value = '#ffe0c8'; $$('#handSkinLight,#handSkinMedium,#handSkinDark').forEach(b => b.classList.remove('active')); $('handSkinLight').classList.add('active'); drawHandPreview(); });
$('handSkinMedium').addEventListener('click', () => { state.hand.color = '#ffd4b3'; $('handColor').value = '#ffd4b3'; $$('#handSkinLight,#handSkinMedium,#handSkinDark').forEach(b => b.classList.remove('active')); $('handSkinMedium').classList.add('active'); drawHandPreview(); });
$('handSkinDark').addEventListener('click', () => { state.hand.color = '#c08860'; $('handColor').value = '#c08860'; $$('#handSkinLight,#handSkinMedium,#handSkinDark').forEach(b => b.classList.remove('active')); $('handSkinDark').classList.add('active'); drawHandPreview(); });

$('handCustomBtn').addEventListener('click', () => $('handFile').click());
$('handFile').addEventListener('change', e => {
  const f = e.target.files[0];
  if (!f) return;
  const reader = new FileReader();
  reader.onload = ev => {
    const img = new Image();
    img.onload = () => {
      state.hand.image = img;
      drawHandPreview();
      toast('Ладонь загружена', 'success');
    };
    img.src = ev.target.result;
  };
  reader.readAsDataURL(f);
  e.target.value = '';
});
$('handResetBtn').addEventListener('click', () => {
  state.hand.image = null;
  drawHandPreview();
  toast('Своя ладонь удалена');
});

/* ============================================================
   15. UI — КНОПКИ
   ============================================================ */
$$('.mode-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    $$('.mode-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    state.brushMode = btn.dataset.mode;
  });
});

$('symNoneBtn').addEventListener('click', () => { state.symmetry = 'none'; $$('#symNoneBtn,#symXBtn,#symYBtn,#symXYBtn').forEach(b => b.classList.remove('active')); $('symNoneBtn').classList.add('active'); });
$('symXBtn').addEventListener('click', () => { state.symmetry = 'x'; $$('#symNoneBtn,#symXBtn,#symYBtn,#symXYBtn').forEach(b => b.classList.remove('active')); $('symXBtn').classList.add('active'); });
$('symYBtn').addEventListener('click', () => { state.symmetry = 'y'; $$('#symNoneBtn,#symXBtn,#symYBtn,#symXYBtn').forEach(b => b.classList.remove('active')); $('symYBtn').classList.add('active'); });
$('symXYBtn').addEventListener('click', () => { state.symmetry = 'xy'; $$('#symNoneBtn,#symXBtn,#symYBtn,#symXYBtn').forEach(b => b.classList.remove('active')); $('symXYBtn').classList.add('active'); });

$('mirrorBtn').addEventListener('click', mirrorMaskX);
$('undoBtn').addEventListener('click', undo);
$('redoBtn').addEventListener('click', redo);

$('addZoneBtn').addEventListener('click', () => {
  if (!state.scaledCanvas) return toast('Сначала картинку', 'error');
  const z = createZone(); setActiveZone(z.id); toast('Зона создана', 'success');
});
$('dupZoneBtn').addEventListener('click', () => {
  const src = getActiveZone();
  if (!src) return;
  const z = createZone(src.name + ' копия');
  z.weights = new Float32Array(src.weights);
  z.pins = new Uint8Array(src.pins);
  setActiveZone(z.id);
  toast('Зона скопирована');
});
$('clearZoneBtn').addEventListener('click', () => {
  const z = getActiveZone();
  if (!z) return;
  pushUndo();
  z.weights.fill(0);
  rebuildMaskTriangles();
  toast('Зона очищена');
});

$('pinModeBtn').addEventListener('click', () => {
  state.pinMode = !state.pinMode;
  $('pinModeBtn').classList.toggle('active', state.pinMode);
});
$('clearPinsBtn').addEventListener('click', () => {
  const z = getActiveZone();
  if (!z) return;
  pushUndo();
  z.pins.fill(0);
  updatePinCount();
  toast('Пины сброшены');
});

$('softGrabBtn').addEventListener('click', () => { state.cfg.softGrab = !state.cfg.softGrab; $('softGrabBtn').classList.toggle('active', state.cfg.softGrab); });
$('deepGrabBtn').addEventListener('click', () => { state.cfg.deepGrab = !state.cfg.deepGrab; $('deepGrabBtn').classList.toggle('active', state.cfg.deepGrab); });
$('snapBtn').addEventListener('click', () => { state.cfg.softGrab = false; $('softGrabBtn').classList.remove('active'); $('snapBtn').classList.toggle('active'); });
$('stickyGrabBtn').addEventListener('click', () => { state.cfg.stickyGrab = !state.cfg.stickyGrab; $('stickyGrabBtn').classList.toggle('active', state.cfg.stickyGrab); });

$('collidersBtn').addEventListener('click', () => { state.cfg.colliders = !state.cfg.colliders; $('collidersBtn').classList.toggle('active', state.cfg.colliders); });
$('wallsBtn').addEventListener('click', () => { state.cfg.walls = !state.cfg.walls; $('wallsBtn').classList.toggle('active', state.cfg.walls); });
$('exactSolverBtn').addEventListener('click', () => { state.cfg.exactSolver = !state.cfg.exactSolver; $('exactSolverBtn').classList.toggle('active', state.cfg.exactSolver); });
$('substepBtn').addEventListener('click', () => { state.cfg.substep = !state.cfg.substep; $('substepBtn').classList.toggle('active', state.cfg.substep); });
$('springsBtn').addEventListener('click', () => { state.cfg.springsOn = !state.cfg.springsOn; $('springsBtn').classList.toggle('active', state.cfg.springsOn); });
$('meshFixBtn').addEventListener('click', () => { state.cfg.meshFix = !state.cfg.meshFix; $('meshFixBtn').classList.toggle('active', state.cfg.meshFix); });
$('smoothMeshBtn').addEventListener('click', () => { state.cfg.smoothMesh = !state.cfg.smoothMesh; $('smoothMeshBtn').classList.toggle('active', state.cfg.smoothMesh); });

$('breathBtn').addEventListener('click', () => { state.breathing = !state.breathing; $('breathBtn').classList.toggle('active', state.breathing); });
$('windBtn').addEventListener('click', () => { state.windOn = !state.windOn; $('windBtn').classList.toggle('active', state.windOn); });
$('maskBtn').addEventListener('click', () => { state.cfg.showMask = !state.cfg.showMask; $('maskBtn').classList.toggle('active', state.cfg.showMask); });
$('gridBtn').addEventListener('click', () => { state.cfg.showGrid = !state.cfg.showGrid; $('gridBtn').classList.toggle('active', state.cfg.showGrid); });
$('inertiaBtn').addEventListener('click', () => { state.inertia = !state.inertia; $('inertiaBtn').classList.toggle('active', state.inertia); });
$('pinsBtn').addEventListener('click', () => { state.cfg.showPins = !state.cfg.showPins; $('pinsBtn').classList.toggle('active', state.cfg.showPins); });

$('shakeBtn').addEventListener('click', () => {
  for (let i = 0; i < state.vertices.length; i++) {
    if (getZoneMaskWeight(i) > 0.1 && !hasPinAny(i)) {
      state.vertices[i].bvx += (Math.random() - 0.5) * 200;
      state.vertices[i].bvy += (Math.random() - 0.5) * 200 - 60;
    }
  }
});
$('resetPhysBtn').addEventListener('click', () => {
  for (const v of state.vertices) { v.bx = v.by = v.bvx = v.bvy = 0; }
  state.camX = 0; state.camY = 0;
  toast('Сброшено');
});
$('explodeBtn').addEventListener('click', () => {
  const cx = state.imgW / 2, cy = state.imgH / 2;
  for (let i = 0; i < state.vertices.length; i++) {
    if (getZoneMaskWeight(i) < 0.05 || hasPinAny(i)) continue;
    const v = state.vertices[i];
    const dx = v.ox - cx, dy = v.oy - cy;
    const d = Math.hypot(dx, dy) || 1;
    v.bvx += (dx / d) * 300;
    v.bvy += (dy / d) * 300;
  }
});
$('freezeBtn').addEventListener('click', () => {
  for (const v of state.vertices) { v.bvx = 0; v.bvy = 0; }
});

$('rebuildGridBtn').addEventListener('click', async () => {
  if (!state.scaledCanvas) return toast('Сначала картинку', 'error');
  if (!await modal('Пересоздать сетку?', 'Все веса и пины будут потеряны.', true)) return;
  const res = parseInt($('gridRes').value);
  buildGrid(res);
  state.zones = [];
  createZone('Зона 1');
  setActiveZone(state.zones[0].id);
  rebuildMaskTriangles();
  toast('Сетка: ' + res + '×' + res);
});

$('resetCameraBtn').addEventListener('click', () => { state.camX = state.camY = 0; state.camZoom = 1; });
$('gridRes').addEventListener('input', () => { $('gridResVal').textContent = $('gridRes').value; });
$('bgSelect').addEventListener('change', () => { state.cfg.bg = $('bgSelect').value; });

/* Presets */
renderPresetsGrid();
renderUserPresets();
$('savePresetBtn').addEventListener('click', () => {
  const name = $('presetName').value.trim();
  if (!name) return toast('Введите имя', 'error');
  const p = loadUserPresets();
  p[name] = { ...state.cfg };
  saveUserPresets(p);
  $('presetName').value = '';
  renderUserPresets();
  toast('Сохранено: ' + name, 'success');
});
$('delAllPresetsBtn').addEventListener('click', async () => {
  if (!await modal('Удалить все пользовательские пресеты?', '', true)) return;
  saveUserPresets({});
  renderUserPresets();
});

/* Export/Import */
$('exportBtn').addEventListener('click', () => {
  if (!state.scaledCanvas) return toast('Нет картинки', 'error');
  const link = document.createElement('a');
  link.download = 'jiggle_' + Date.now() + '.png';
  link.href = canvas.toDataURL('image/png');
  link.click();
});

$('saveModelBtn').addEventListener('click', () => {
  if (!state.scaledCanvas) return toast('Нет картинки', 'error');
  const data = {
    version: 7,
    imageData: state.scaledCanvas.toDataURL('image/png'),
    imgW: state.imgW, imgH: state.imgH,
    cols: state.cols, rows: state.rows,
    zones: state.zones.map(z => ({
      id: z.id, name: z.name, color: z.color, visible: z.visible, physicsOn: z.physicsOn,
      weights: Array.from(z.weights), pins: Array.from(z.pins),
    })),
    cfg: state.cfg,
    hand: { size: state.hand.size, opacity: state.hand.opacity, rotation: state.hand.rotation, color: state.hand.color, showShadow: state.hand.showShadow, visible: state.hand.visible, pressForce: state.hand.pressForce },
  };
  const blob = new Blob([JSON.stringify(data)], { type: 'application/json' });
  const link = document.createElement('a');
  link.download = 'model_' + Date.now() + '.json';
  link.href = URL.createObjectURL(blob);
  link.click();
  toast('Модель сохранена', 'success');
});

$('loadModelBtn').addEventListener('click', () => {
  const input = document.createElement('input');
  input.type = 'file'; input.accept = '.json';
  input.onchange = e => {
    const f = e.target.files[0]; if (!f) return;
    const reader = new FileReader();
    reader.onload = ev => {
      try { loadModelFromJSON(JSON.parse(ev.target.result)); }
      catch (err) { toast('Ошибка: ' + err.message, 'error'); }
    };
    reader.readAsText(f);
  };
  input.click();
});

function loadModelFromJSON(data) {
  const img = new Image();
  img.onload = () => {
    state.imgW = data.imgW; state.imgH = data.imgH;
    canvas.width = data.imgW; canvas.height = data.imgH;
    canvas.style.width = data.imgW + 'px';
    canvas.style.height = data.imgH + 'px';
    const sc = document.createElement('canvas');
    sc.width = data.imgW; sc.height = data.imgH;
    sc.getContext('2d').drawImage(img, 0, 0);
    state.scaledCanvas = sc;
    state.camX = state.camY = 0; state.camZoom = 1;
    buildGrid(data.cols || 40);
    state.zones = [];
    for (const z of data.zones || []) {
      state.zones.push({
        id: z.id, name: z.name, color: z.color,
        visible: z.visible !== false, physicsOn: z.physicsOn !== false,
        weights: new Float32Array(z.weights),
        pins: new Uint8Array(z.pins || new Array(state.vertices.length).fill(0)),
      });
    }
    if (!state.zones.length) createZone('Зона 1');
    setActiveZone(state.zones[0].id);
    Object.assign(state.cfg, data.cfg || {});
    if (data.hand) Object.assign(state.hand, data.hand);
    syncAllSliders();
    drawHandPreview();
    updateOmegaAll();
    rebuildMaskTriangles();
    $('dropOverlay').style.display = 'none';
    toast('Модель загружена', 'success');
  };
  img.onerror = () => toast('Ошибка картинки', 'error');
  img.src = data.imageData;
}

$('saveWeightsBtn').addEventListener('click', () => {
  const z = getActiveZone();
  if (!z) return toast('Нет зоны', 'error');
  const data = { version: 7, cols: state.cols, rows: state.rows, zoneName: z.name, weights: Array.from(z.weights), pins: Array.from(z.pins) };
  const blob = new Blob([JSON.stringify(data)], { type: 'application/json' });
  const link = document.createElement('a');
  link.download = 'weights_' + Date.now() + '.json';
  link.href = URL.createObjectURL(blob);
  link.click();
  toast('Веса сохранены', 'success');
});

$('loadWeightsBtn').addEventListener('click', () => {
  const z = getActiveZone();
  if (!z) return toast('Сначала картинку', 'error');
  const input = document.createElement('input');
  input.type = 'file'; input.accept = '.json';
  input.onchange = e => {
    const f = e.target.files[0]; if (!f) return;
    const reader = new FileReader();
    reader.onload = ev => {
      try {
        const d = JSON.parse(ev.target.result);
        if (d.cols !== state.cols || d.rows !== state.rows) return toast('Размер сетки не совпадает', 'error');
        pushUndo();
        for (let i = 0; i < state.vertices.length; i++) {
          z.weights[i] = d.weights[i] || 0;
          z.pins[i] = d.pins ? d.pins[i] : 0;
        }
        updateOmegaAll();
        rebuildMaskTriangles();
        updatePinCount();
        toast('Веса загружены', 'success');
      } catch (err) { toast('Ошибка: ' + err.message, 'error'); }
    };
    reader.readAsText(f);
  };
  input.click();
});

$('clearAllBtn').addEventListener('click', async () => {
  if (!await modal('Очистить всё?', '', true)) return;
  state.scaledCanvas = null;
  state.vertices = []; state.triangles = []; state.maskTriangles = [];
  state.zones = []; state.undoStack = []; state.redoStack = [];
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  canvas.width = 0; canvas.height = 0;
  $('dropOverlay').style.display = 'flex';
  renderZoneList();
  updateUndoUI();
  toast('Очищено');
});

/* Recording */
async function recordAnimation(type) {
  if (!state.scaledCanvas) return toast('Нет картинки', 'error');
  if (!canvas.captureStream) return toast('Браузер не поддерживает', 'error');
  const dur = parseFloat($('recDuration').value) * 1000;
  const stream = canvas.captureStream(30);
  const rec = new MediaRecorder(stream, { mimeType: 'video/webm' });
  const chunks = [];
  rec.ondataavailable = e => chunks.push(e.data);
  rec.onstop = () => {
    const blob = new Blob(chunks, { type: 'video/webm' });
    const link = document.createElement('a');
    link.download = 'anim_' + type + '_' + Date.now() + '.webm';
    link.href = URL.createObjectURL(blob);
    link.click();
    toast('Готово', 'success');
  };
  rec.start();
  const start = now();
  let grabAnchor = null;
  if (type === 'grab') {
    let cx = 0, cy = 0, cnt = 0;
    for (let i = 0; i < state.vertices.length; i++) {
      if (getZoneMaskWeight(i) > 0.3) { cx += state.vertices[i].ox; cy += state.vertices[i].oy; cnt++; }
    }
    if (cnt) grabAnchor = { x: cx / cnt, y: cy / cnt };
  }
  const interval = setInterval(() => {
    const t = (now() - start) / 1000;
    if (type === 'shake' && Math.random() < 0.15) {
      for (let i = 0; i < state.vertices.length; i++) {
        if (getZoneMaskWeight(i) > 0.1 && !hasPinAny(i)) {
          state.vertices[i].bvx += (Math.random() - 0.5) * 120;
          state.vertices[i].bvy += (Math.random() - 0.5) * 120 - 30;
        }
      }
    } else if (type === 'grab' && grabAnchor) {
      const a = t * 2;
      state.pointer = {
        x: grabAnchor.x * state.camZoom + state.camX + Math.cos(a) * 50 * state.camZoom,
        y: grabAnchor.y * state.camZoom + state.camY + Math.sin(a) * 50 * state.camZoom,
      };
      state.isDown = true;
      state.isGrabbing = true;
    }
    if (now() - start > dur) { clearInterval(interval); state.isDown = false; state.isGrabbing = false; rec.stop(); }
  }, 1000 / 30);
}
$('recShakeBtn').addEventListener('click', () => recordAnimation('shake'));
$('recGrabBtn').addEventListener('click', () => recordAnimation('grab'));

/* ============================================================
   16. ГЛАВНЫЙ ЦИКЛ
   ============================================================ */
let lastTime = now();

function loop(t) {
  const dt = (t - lastTime) / 1000;
  lastTime = t;

  state.fpsAcc += dt;
  state.fpsFrames++;
  if (state.fpsAcc >= 0.5) {
    const fps = state.fpsFrames / state.fpsAcc;
    $('hudFps').textContent = fps.toFixed(0);
    $('statFps').textContent = fps.toFixed(0);
    $('statVerts').textContent = state.vertices.length;
    $('statTris').textContent = state.maskTriangles.length;
    $('statInversions').textContent = state.inversions || 0;
    state.fpsAcc = 0; state.fpsFrames = 0;
  }

  if (state.scaledCanvas) {
    physicsStep(dt);
    render();
  }
  requestAnimationFrame(loop);
}

/* ============================================================
   17. ИНИЦИАЛИЗАЦИЯ
   ============================================================ */
requestAnimationFrame(loop);
renderZoneList();
syncAllSliders();
updateUndoUI();
updatePinCount();
drawHandPreview();

console.log('[Jiggle Lab v7] Ready — hand + mesh fix');
toast('v7 готова · ладонь + фикс mesh', 'success');
</script>
</body>
</html>
