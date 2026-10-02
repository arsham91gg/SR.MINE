<!DOCTYPE html>
<html lang="fa" dir="rtl">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>SRMINE</title>

    <link rel="stylesheet" href="style.css">
</head>

<body>

<!-- ================= NAVBAR ================= -->

<header class="navbar">

    <div class="logo">
        <span>SR</span>MINE
    </div>

    <nav>
        <a href="#home">خانه</a>
        <a href="#servers">سرورهای من</a>
        <a href="#features">امکانات</a>
    </nav>

    <button class="login-btn">
        ورود / ثبت‌نام
    </button>

</header>


<!-- ================= HOME ================= -->

<main id="home">

    <section class="hero">

        <div class="hero-content">

            <div class="badge">
                MINECRAFT SERVER PLATFORM
            </div>

            <h1>
                سرور Minecraft خودت رو
                <span>بساز.</span>
            </h1>

            <p>
                ساخت و مدیریت سرور Minecraft
                با چند کلیک ساده.
            </p>

            <div class="hero-buttons">

                <button
                    class="primary-btn"
                    onclick="createServer()">
                    🚀 ساخت سرور
                </button>

                <button
                    class="secondary-btn"
                    onclick="showServers()">
                    🖥️ سرورهای من
                </button>

            </div>

        </div>

    </section>


<!-- ================= FEATURES ================= -->

<section id="features" class="features">

    <div class="section-title">

        <span>SRMINE</span>

        <h2>
            همه‌چیز برای سرور Minecraft
        </h2>

    </div>


    <div class="feature-grid">

        <div class="feature-card">
            <div class="feature-icon">⚡</div>
            <h3>ساخت سریع</h3>
            <p>سرور خودت را در چند مرحله بساز.</p>
        </div>

        <div class="feature-card">
            <div class="feature-icon">🧩</div>
            <h3>Plugins</h3>
            <p>پلاگین‌های سرور را مدیریت کن.</p>
        </div>

        <div class="feature-card">
            <div class="feature-icon">🧱</div>
            <h3>Mods</h3>
            <p>مودهای Minecraft را مدیریت کن.</p>
        </div>

        <div class="feature-card">
            <div class="feature-icon">🌍</div>
            <h3>World</h3>
            <p>مپ‌های سرور را مدیریت کن.</p>
        </div>

        <div class="feature-card">
            <div class="feature-icon">🎨</div>
            <h3>Resource Pack</h3>
            <p>ریسورس پک اختصاصی اضافه کن.</p>
        </div>

        <div class="feature-card">
            <div class="feature-icon">📁</div>
            <h3>Files</h3>
            <p>فایل‌های سرور را مدیریت کن.</p>
        </div>

        <div class="feature-card">
            <div class="feature-icon">⚙️</div>
            <h3>Settings</h3>
            <p>تنظیمات کامل Minecraft.</p>
        </div>

        <div class="feature-card">
            <div class="feature-icon">💾</div>
            <h3>Backup</h3>
            <p>از سرورت نسخه پشتیبان بگیر.</p>
        </div>

    </div>

</section>


<!-- ================= SERVERS ================= -->

<section id="servers" class="servers">

    <div class="section-title">

        <span>CONTROL PANEL</span>

        <h2>
            سرورهای من
        </h2>

    </div>


    <div id="serverContainer">

        <div class="empty-server">

            <div class="empty-icon">
                🖥️
            </div>

            <h3>
                هنوز سروری نداری
            </h3>

            <p>
                اولین سرور Minecraft خودت را بساز.
            </p>

            <button
                class="primary-btn"
                onclick="createServer()">
                + ساخت سرور جدید
            </button>

        </div>

    </div>

</section>

</main>


<!-- ================= CREATE SERVER MODAL ================= -->

<div id="createModal" class="modal">

    <div class="modal-box">

        <button
            class="close-btn"
            onclick="closeModal()">
            ×
        </button>

        <h2>
            🚀 ساخت سرور جدید
        </h2>

        <p class="modal-description">
            مشخصات سرور خودت را انتخاب کن.
        </p>


        <label>
            نام سرور
        </label>

        <input
            id="serverName"
            type="text"
            placeholder="مثلاً Survival SMP"
        >


        <label>
            نسخه Minecraft
        </label>

        <select id="minecraftVersion">

            <option value="1.21">
                Minecraft 1.21
            </option>

            <option value="1.20.6">
                Minecraft 1.20.6
            </option>

            <option value="1.20.4">
                Minecraft 1.20.4
            </option>

        </select>


        <label>
            Software
        </label>

        <select id="serverSoftware">

            <option value="Vanilla">
                Vanilla
            </option>

            <option value="Paper">
                Paper
            </option>

            <option value="Purpur">
                Purpur
            </option>

            <option value="Fabric">
                Fabric
            </option>

            <option value="Forge">
                Forge
            </option>

            <option value="NeoForge">
                NeoForge
            </option>

        </select>


        <label>
            مکان سرور
        </label>

        <select id="serverLocation">

            <option value="🇮🇷 ایران">
                🇮🇷 ایران
            </option>

            <option value="🇩🇪 اروپا">
                🇩🇪 اروپا
            </option>

            <option value="🇺🇸 آمریکا">
                🇺🇸 آمریکا
            </option>

        </select>


        <button
            class="create-final-btn"
            onclick="finishCreateServer()">

            🚀 ساخت سرور

        </button>

    </div>

</div>


<!-- ================= SERVER PANEL ================= -->

<div id="serverPanel" class="server-panel">


    <!-- SIDEBAR -->

    <aside class="panel-sidebar">

        <div class="panel-logo">
            <span>SR</span>MINE
        </div>


        <button
            class="back-btn"
            onclick="closeServerPanel()">

            ← بازگشت

        </button>


        <div class="sidebar-server">

            <div class="server-dot"></div>

            <div>

                <strong id="panelServerName">
                    Server
                </strong>

                <small id="panelServerStatus">
                    OFFLINE
                </small>

            </div>

        </div>


        <div class="sidebar-menu">

            <button onclick="openPanelPage('overview')">
                🏠 Overview
            </button>

            <button onclick="openPanelPage('console')">
                🖥️ Console
            </button>

            <button onclick="openPanelPage('players')">
                👥 Players
            </button>

            <button onclick="openPanelPage('plugins')">
                🧩 Plugins
            </button>

            <button onclick="openPanelPage('mods')">
                🧱 Mods
            </button>

            <button onclick="openPanelPage('worlds')">
                🌍 Worlds
            </button>

            <button onclick="openPanelPage('resourcepack')">
                🎨 Resource Pack
            </button>

            <button onclick="openPanelPage('files')">
                📁 Files
            </button>

            <button onclick="openPanelPage('backups')">
                💾 Backups
            </button>

            <button onclick="openPanelPage('settings')">
                ⚙️ Settings
            </button>

        </div>

    </aside>


    <!-- PANEL CONTENT -->

    <section class="panel-content">


        <!-- TOP BAR -->

        <div class="panel-topbar">

            <div>

                <h1 id="pageTitle">
                    Overview
                </h1>

                <p id="pageDescription">
                    مدیریت سرور Minecraft
                </p>

            </div>


            <div class="server-actions">

                <button
                    class="start-btn"
                    onclick="serverStart()">

                    ▶ Start

                </button>

                <button
                    class="restart-btn"
                    onclick="serverRestart()">

                    ↻ Restart

                </button>

                <button
                    class="stop-btn"
                    onclick="serverStop()">

                    ■ Stop

                </button>

            </div>

        </div>


        <!-- PAGES -->

        <div id="panelPages">


            <!-- OVERVIEW -->

            <div
                id="page-overview"
                class="panel-page active">

                <div class="status-box">

                    <div>

                        <span class="online-dot"></span>

                        <strong id="overviewStatus">
                            سرور خاموش است
                        </strong>

                    </div>

                    <span>
                        SRMINE
                    </span>

                </div>


                <div class="stats-grid">

                    <div class="stat-card">

                        <span>Players</span>

                        <strong id="playerCount">
                            0 / 20
                        </strong>

                    </div>

                    <div class="stat-card">

                        <span>Version</span>

                        <strong id="overviewVersion">
                            1.21
                        </strong>

                    </div>

                    <div class="stat-card">

                        <span>Software</span>

                        <strong id="overviewSoftware">
                            Paper
                        </strong>

                    </div>

                    <div class="stat-card">

                        <span>Location</span>

                        <strong id="overviewLocation">
                            ایران
                        </strong>

                    </div>

                </div>


                <div class="address-box">

                    <span>
                        آدرس سرور
                    </span>

                    <strong>
                        play.srmine.local
                    </strong>

                    <button
                        onclick="copyServerAddress()">

                        📋 کپی

                    </button>

                </div>

            </div>


            <!-- CONSOLE -->

            <div
                id="page-console"
                class="panel-page">

                <div class="console">

                    <div class="console-header">
                        Console
                    </div>

                    <div
                        id="consoleOutput"
                        class="console-output">

                        <div>
                            [SRMINE] Server console ready...
                        </div>

                        <div>
                            [Server] Waiting for server...
                        </div>

                    </div>


                    <div class="console-input">

                        <input
                            id="commandInput"
                            type="text"
                            placeholder="Command...">

                        <button
                            onclick="sendCommand()">

                            ارسال

                        </button>

                    </div>

                </div>

            </div>


            <!-- PLAYERS -->

            <div
                id="page-players"
                class="panel-page">

                <div class="content-card">

                    <h2>
                        👥 Players
                    </h2>

                    <p>
                        بازیکنان آنلاین سرور اینجا نمایش داده می‌شوند.
                    </p>

                    <div class="player-empty">
                        هیچ بازیکنی آنلاین نیست.
                    </div>

                </div>

            </div>


            <!-- PLUGINS -->

            <div
                id="page-plugins"
                class="panel-page">

                <div class="content-card">

                    <h2>
                        🧩 Plugins
                    </h2>

                    <div class="search-box">

                        <input
                            type="text"
                            placeholder="جستجوی پلاگین...">

                        <button>
                            جستجو
                        </button>

                    </div>


                    <div class="plugin-list">

                        <div class="plugin-item">

                            <div>
                                <strong>
                                    EssentialsX
                                </strong>

                                <small>
                                    مدیریت امکانات سرور
                                </small>
                            </div>

                            <button>
                                نصب
                            </button>

                        </div>


                        <div class="plugin-item">

                            <div>
                                <strong>
                                    WorldEdit
                                </strong>

                                <small>
                                    ابزار ساخت و ویرایش مپ
                                </small>
                            </div>

                            <button>
                                نصب
                            </button>

                        </div>


                        <div class="plugin-item">

                            <div>
                                <strong>
                                    ViaVersion
                                </strong>

                                <small>
                                    پشتیبانی از نسخه‌های مختلف
                                </small>
                            </div>

                            <button>
                                نصب
                            </button>

                        </div>

                    </div>

                </div>

            </div>


            <!-- MODS -->

            <div
                id="page-mods"
                class="panel-page">

                <div class="content-card">

                    <h2>
                        🧱 Mods
                    </h2>

                    <p>
                        مودهای سازگار با نسخه سرور را مدیریت کن.
                    </p>

                    <div class="upload-box">

                        <span>
                            📤
                        </span>

                        <strong>
                            آپلود Mod
                        </strong>

                        <small>
                            فایل JAR را انتخاب کن.
                        </small>

                        <input
                            type="file"
                            accept=".jar">

                    </div>

                </div>

            </div>


            <!-- WORLDS -->

            <div
                id="page-worlds"
                class="panel-page">

                <div class="content-card">

                    <h2>
                        🌍 Worlds
                    </h2>

                    <div class="world-list">

                        <div class="world-item">

                            <strong>
                                🌎 world
                            </strong>

                            <button>
                                مدیریت
                            </button>

                        </div>

                        <div class="world-item">

                            <strong>
                                🔥 world_nether
                            </strong>

                            <button>
                                مدیریت
                            </button>

                        </div>

                        <div class="world-item">

                            <strong>
                                🌌 world_the_end
                            </strong>

                            <button>
                                مدیریت
                            </button>

                        </div>

                    </div>

                    <button class="primary-btn">
                        + آپلود Map
                    </button>

                </div>

            </div>


            <!-- RESOURCE PACK -->

            <div
                id="page-resourcepack"
                class="panel-page">

                <div class="content-card">

                    <h2>
                        🎨 Resource Pack
                    </h2>

                    <p>
                        ریسورس پک سرور را تنظیم کن.
                    </p>

                    <input
                        type="file"
                        accept=".zip">

                    <label class="checkbox">

                        <input type="checkbox">

                        اجباری کردن Resource Pack

                    </label>

                </div>

            </div>


            <!-- FILES -->

            <div
                id="page-files"
                class="panel-page">

                <div class="content-card">

                    <h2>
                        📁 Files
                    </h2>

                    <div class="file-list">

                        <div>📄 server.properties</div>
                        <div>📄 eula.txt</div>
                        <div>📁 plugins/</div>
                        <div>📁 world/</div>
                        <div>📁 mods/</div>

                    </div>

                </div>

            </div>


            <!-- BACKUPS -->

            <div
                id="page-backups"
                class="panel-page">

                <div class="content-card">

                    <h2>
                        💾 Backups
                    </h2>

                    <p>
                        از اطلاعات سرور نسخه پشتیبان تهیه کن.
                    </p>

                    <button class="primary-btn">
                        + ساخت Backup
                    </button>

                </div>

            </div>


            <!-- SETTINGS -->

            <div
                id="page-settings"
                class="panel-page">

                <div class="content-card">

                    <h2>
                        ⚙️ Settings
                    </h2>


                    <div class="setting-row">

                        <div>
                            <strong>
                                Server Name
                            </strong>

                            <small>
                                نام سرور
                            </small>
                        </div>

                        <input
                            type="text"
                            value="My Server">

                    </div>


                    <div class="setting-row">

                        <div>
                            <strong>
                                Max Players
                            </strong>

                            <small>
                                حداکثر بازیکن
                            </small>
                        </div>

                        <input
                            type="number"
                            value="20">

                    </div>


                    <div class="setting-row">

                        <div>
                            <strong>
                                Difficulty
                            </strong>

                            <small>
                                سختی بازی
                            </small>
                        </div>

                        <select>

                            <option>Easy</option>
                            <option selected>Normal</option>
                            <option>Hard</option>

                        </select>

                    </div>


                    <div class="setting-row">

                        <div>
                            <strong>
                                PvP
                            </strong>

                            <small>
                                فعال بودن PvP
                            </small>

                        </div>

                        <input
                            type="checkbox"
                            checked>

                    </div>


                    <button class="primary-btn">
                        ذخیره تنظیمات
                    </button>

                </div>

            </div>


        </div>

    </section>

</div>


<!-- FOOTER -->

<footer>

    <div class="logo">
        <span>SR</span>MINE
    </div>

    <p>
        Minecraft Server Platform
    </p>

    <small>
        © 2026 SRMINE
    </small>

</footer>


<script src="script.js"></script>

</body>
</html>
