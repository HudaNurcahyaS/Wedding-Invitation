# Wedding-Invitation
Undangan Pernikahan Huda &amp; Desy
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Undangan Pernikahan - Huda & Desy</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #fdfcfb 0%, #e2d1c3 100%);
            overflow: hidden;
            color: #5a4a3a;
        }
        
        .loading-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            text-align: center;
            padding: 20px;
            transition: opacity 0.8s ease;
        }
        
        .couple-names {
            font-size: 32px;
            color: #8b7355;
            margin-bottom: 10px;
            font-weight: bold;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }
        
        .wedding-title {
            font-size: 18px;
            color: #666;
            margin-bottom: 30px;
            letter-spacing: 2px;
        }
        
        .loading-text {
            font-size: 16px;
            color: #555;
            margin-bottom: 25px;
            max-width: 300px;
            line-height: 1.5;
        }
        
        .open-btn {
            padding: 15px 40px;
            font-size: 16px;
            background: #d4af37;
            color: white;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            box-shadow: 0 4px 15px rgba(212, 175, 55, 0.3);
        }
        
        .open-btn:hover {
            background: #b8941f;
            transform: scale(1.05);
        }
        
        .music-note {
            font-size: 24px;
            margin-bottom: 15px;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .hidden {
            display: none;
        }
        
        #mainContent {
            width: 100%;
            height: 100vh;
            border: none;
        }
        
        .music-controls {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 10000;
            display: flex;
            gap: 10px;
            background: rgba(255, 255, 255, 0.9);
            padding: 10px 15px;
            border-radius: 50px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(5px);
        }
        
        .music-btn {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            border: none;
            background: #d4af37;
            color: white;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 16px;
            transition: all 0.2s ease;
        }
        
        .music-btn:hover {
            background: #b8941f;
            transform: scale(1.1);
        }
        
        .audio-permission {
            background: rgba(255, 255, 255, 0.95);
            padding: 15px;
            border-radius: 10px;
            margin-top: 20px;
            max-width: 300px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }
        
        .permission-btn {
            padding: 8px 20px;
            font-size: 14px;
            background: #8b7355;
            color: white;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            margin-top: 10px;
            transition: all 0.3s ease;
        }
        
        .permission-btn:hover {
            background: #6d5a45;
        }
    </style>
</head>
<body>
    <!-- Loading Screen -->
    <div id="loadingScreen" class="loading-screen">
        <div class="music-note">🎵</div>
        <div class="couple-names">Huda Nurcahyo Saputro<br>&<br>Desy Irmaya</div>
        <div class="wedding-title">The Wedding Celebration</div>
        <div class="loading-text">
            Untuk pengalaman terbaik, musik akan diputar otomatis setelah Anda membuka undangan
        </div>
        <button class="open-btn" onclick="openInvitation()">
            Buka Undangan
        </button>
        
        <div class="audio-permission">
            <p style="font-size: 14px; margin-bottom: 10px;">Jika musik tidak otomatis terputar, klik tombol di bawah:</p>
            <button class="permission-btn" onclick="enableAudio()">Aktifkan Musik</button>
        </div>
    </div>

    <!-- Konten Undangan Google Sites -->
    <div id="mainContent" class="hidden">
        <iframe 
            src="https://sites.google.com/view/w-invitation/beranda" 
            width="100%" 
            height="100%" 
            frameborder="0"
            id="invitationFrame">
        </iframe>
    </div>

    <!-- Kontrol Musik -->
    <div id="musicControls" class="music-controls hidden">
        <button id="playPauseBtn" class="music-btn">⏸️</button>
        <button id="stopBtn" class="music-btn">⏹️</button>
        <button id="volumeBtn" class="music-btn">🔊</button>
    </div>

    <script>
        let musicPlayer = null;
        let isMusicPlaying = false;
        let userInteracted = false;
        
        function openInvitation() {
            // 1. Sembunyikan loading screen dengan efek fade
            const loadingScreen = document.getElementById('loadingScreen');
            loadingScreen.style.opacity = '0';
            
            setTimeout(() => {
                loadingScreen.style.display = 'none';
                
                // 2. Tampilkan konten utama
                document.getElementById('mainContent').classList.remove('hidden');
                
                // 3. Tampilkan kontrol musik
                document.getElementById('musicControls').classList.remove('hidden');
                
                // 4. Coba play musik (hanya jika user sudah berinteraksi)
                if (userInteracted) {
                    playWeddingMusic();
                }
                
            }, 800);
        }
        
        function enableAudio() {
            userInteracted = true;
            document.querySelector('.audio-permission').style.display = 'none';
            playWeddingMusic();
        }
        
        function playWeddingMusic() {
            // Hanya buat satu instance musik
            if (!musicPlayer && userInteracted) {
                musicPlayer = document.createElement('iframe');
                musicPlayer.src = 'https://www.youtube.com/embed/Ph94XLpDKm0?autoplay=1&loop=1&playlist=Ph94XLpDKm0&mute=0';
                musicPlayer.width = '0';
                musicPlayer.height = '0';
                musicPlayer.style.display = 'none';
                musicPlayer.allow = 'autoplay; encrypted-media';
                document.body.appendChild(musicPlayer);
                
                isMusicPlaying = true;
                updateMusicControls();
                console.log('Musik mulai diputar...');
            }
        }
        
        function stopWeddingMusic() {
            if (musicPlayer) {
                // Hapus iframe untuk menghentikan musik
                musicPlayer.remove();
                musicPlayer = null;
                isMusicPlaying = false;
                
                // Perbarui tombol
                updateMusicControls();
                console.log('Musik dihentikan...');
            }
        }
        
        function toggleMusic() {
            if (isMusicPlaying) {
                // Jika musik sedang diputar, pause dengan membuat ulang iframe
                stopWeddingMusic();
            } else {
                // Jika musik dihentikan, putar ulang
                playWeddingMusic();
            }
        }
        
        function toggleVolume() {
            // Untuk YouTube iframe, kita tidak bisa mengontrol volume secara langsung
            // Solusinya adalah membuat iframe baru dengan volume yang berbeda
            if (musicPlayer && isMusicPlaying) {
                stopWeddingMusic();
                // Beri jeda sebelum memutar ulang
                setTimeout(playWeddingMusic, 300);
            }
        }
        
        function updateMusicControls() {
            const playPauseBtn = document.getElementById('playPauseBtn');
            if (isMusicPlaying) {
                playPauseBtn.innerHTML = '⏸️';
            } else {
                playPauseBtn.innerHTML = '▶️';
            }
        }
        
        // Event listeners untuk kontrol musik
        document.getElementById('playPauseBtn').addEventListener('click', toggleMusic);
        document.getElementById('stopBtn').addEventListener('click', stopWeddingMusic);
        document.getElementById('volumeBtn').addEventListener('click', toggleVolume);
        
        // Fallback: Jika user klik dimanapun di loading screen, langsung buka
        document.getElementById('loadingScreen').addEventListener('click', function(e) {
            if (e.target.className !== 'open-btn' && !e.target.closest('.audio-permission')) {
                userInteracted = true;
                openInvitation();
            }
        });
        
        // Interaksi dengan tombol buka undangan juga menandai user interaction
        document.querySelector('.open-btn').addEventListener('click', function() {
            userInteracted = true;
        });
    </script>
</body>
</html>
