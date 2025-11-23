<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Undangan Pernikahan - Huda & Desy</title>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Montserrat:wght@300;400;500&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: #fefaf5;
            color: #5a4a3a;
            overflow-y: auto;
            line-height: 1.6;
        }
        
        /* Background Batik */
        .batik-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Cpath fill='%238b7355' fill-opacity='0.15' d='M20,20 C40,0 60,0 80,20 C100,40 120,40 140,20 C160,0 180,0 180,20 C180,40 160,60 140,80 C120,100 100,100 80,80 C60,60 40,60 20,80 C0,100 0,80 0,60 C0,40 0,20 20,20 Z'/%3E%3Cpath fill='%238b7355' fill-opacity='0.15' d='M100,100 C120,80 140,80 160,100 C180,120 180,140 160,160 C140,180 120,180 100,160 C80,140 80,120 100,100 Z'/%3E%3C/svg%3E");
            background-size: 300px;
            z-index: -1;
            pointer-events: none;
        }
        
        /* ========== ORNAMENT DEKORATIF KOMPLIT ========== */
        /* Ornament corner - pojok halaman */
        .ornament-corner {
            position: fixed;
            width: 120px;
            height: 120px;
            z-index: 10;
            pointer-events: none;
            opacity: 0.4;
        }
        
        .ornament-top-left {
            top: 20px;
            left: 20px;
            border-top: 2px solid #8b7355;
            border-left: 2px solid #8b7355;
        }
        
        .ornament-top-right {
            top: 20px;
            right: 20px;
            border-top: 2px solid #8b7355;
            border-right: 2px solid #8b7355;
        }
        
        .ornament-bottom-left {
            bottom: 20px;
            left: 20px;
            border-bottom: 2px solid #8b7355;
            border-left: 2px solid #8b7355;
        }
        
        .ornament-bottom-right {
            bottom: 20px;
            right: 20px;
            border-bottom: 2px solid #8b7355;
            border-right: 2px solid #8b7355;
        }
        
        /* Ornament floral corner */
        .floral-corner {
            position: fixed;
            width: 80px;
            height: 80px;
            z-index: 10;
            pointer-events: none;
            opacity: 0.3;
        }
        
        .floral-top-left {
            top: 40px;
            left: 40px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Cpath fill='none' stroke='%238b7355' stroke-width='1.5' d='M30,30 Q50,10 70,30 Q90,50 70,70 Q50,90 30,70 Q10,50 30,30 Z'/%3E%3Ccircle cx='50' cy='50' r='8' fill='%238b7355' opacity='0.6'/%3E%3C/svg%3E");
        }
        
        .floral-top-right {
            top: 40px;
            right: 40px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Cpath fill='none' stroke='%238b7355' stroke-width='1.5' d='M30,30 Q50,10 70,30 Q90,50 70,70 Q50,90 30,70 Q10,50 30,30 Z'/%3E%3Ccircle cx='50' cy='50' r='8' fill='%238b7355' opacity='0.6'/%3E%3C/svg%3E");
        }
        
        .floral-bottom-left {
            bottom: 40px;
            left: 40px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Cpath fill='none' stroke='%238b7355' stroke-width='1.5' d='M30,30 Q50,10 70,30 Q90,50 70,70 Q50,90 30,70 Q10,50 30,30 Z'/%3E%3Ccircle cx='50' cy='50' r='8' fill='%238b7355' opacity='0.6'/%3E%3C/svg%3E");
        }
        
        .floral-bottom-right {
            bottom: 40px;
            right: 40px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Cpath fill='none' stroke='%238b7355' stroke-width='1.5' d='M30,30 Q50,10 70,30 Q90,50 70,70 Q50,90 30,70 Q10,50 30,30 Z'/%3E%3Ccircle cx='50' cy='50' r='8' fill='%238b7355' opacity='0.6'/%3E%3C/svg%3E");
        }
        
        /* Ornament divider floral */
        .divider-floral {
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 30px auto;
            width: 200px;
            height: 40px;
            position: relative;
        }
        
        .divider-floral::before,
        .divider-floral::after {
            content: '';
            flex: 1;
            height: 1px;
            background: #b8a58d;
        }
        
        .divider-floral::before {
            margin-right: 15px;
        }
        
        .divider-floral::after {
            margin-left: 15px;
        }
        
        .floral-center {
            width: 30px;
            height: 30px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 30 30'%3E%3Cpath fill='%238b7355' d='M15,5 C18,5 21,7 21,10 C21,13 18,15 15,15 C12,15 9,13 9,10 C9,7 12,5 15,5 Z M5,15 C8,15 11,17 11,20 C11,23 8,25 5,25 C2,25 -1,23 -1,20 C-1,17 2,15 5,15 Z M25,15 C28,15 31,17 31,20 C31,23 28,25 25,25 C22,25 19,23 19,20 C19,17 22,15 25,15 Z'/%3E%3C/svg%3E");
            opacity: 0.6;
        }
        
        /* Ornament section corners */
        .section-ornament {
            position: absolute;
            width: 40px;
            height: 40px;
            opacity: 0.3;
        }
        
        .section-top-left {
            top: 20px;
            left: 20px;
            border-top: 1px solid #8b7355;
            border-left: 1px solid #8b7355;
        }
        
        .section-top-right {
            top: 20px;
            right: 20px;
            border-top: 1px solid #8b7355;
            border-right: 1px solid #8b7355;
        }
        
        .section-bottom-left {
            bottom: 20px;
            left: 20px;
            border-bottom: 1px solid #8b7355;
            border-left: 1px solid #8b7355;
        }
        
        .section-bottom-right {
            bottom: 20px;
            right: 20px;
            border-bottom: 1px solid #8b7355;
            border-right: 1px solid #8b7355;
        }
        
        /* Ornament floating elements */
        .floating-ornament {
            position: fixed;
            z-index: 5;
            pointer-events: none;
            opacity: 0.1;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }
        
        .ornament-1 {
            top: 15%;
            left: 10%;
            width: 40px;
            height: 40px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 40 40'%3E%3Cpath fill='%238b7355' d='M20,5 C25,5 30,8 30,13 C30,18 25,21 20,21 C15,21 10,18 10,13 C10,8 15,5 20,5 Z M8,20 C12,20 16,23 16,27 C16,31 12,34 8,34 C4,34 0,31 0,27 C0,23 4,20 8,20 Z M32,20 C36,20 40,23 40,27 C40,31 36,34 32,34 C28,34 24,31 24,27 C24,23 28,20 32,20 Z'/%3E%3C/svg%3E");
        }
        
        .ornament-2 {
            top: 25%;
            right: 8%;
            width: 35px;
            height: 35px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 35 35'%3E%3Cpath fill='none' stroke='%238b7355' stroke-width='1.5' d='M17.5,5 C22,5 26,8 26,12 C26,16 22,19 17.5,19 C13,19 9,16 9,12 C9,8 13,5 17.5,5 Z M5,20 C9,20 13,23 13,27 C13,31 9,34 5,34 C1,34 -3,31 -3,27 C-3,23 1,20 5,20 Z M30,20 C34,20 38,23 38,27 C38,31 34,34 30,34 C26,34 22,31 22,27 C22,23 26,20 30,20 Z'/%3E%3C/svg%3E");
            animation-delay: 2s;
        }
        
        .ornament-3 {
            bottom: 30%;
            left: 5%;
            width: 30px;
            height: 30px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 30 30'%3E%3Ccircle cx='15' cy='15' r='12' fill='none' stroke='%238b7355' stroke-width='1.5'/%3E%3Ccircle cx='15' cy='15' r='6' fill='%238b7355' opacity='0.6'/%3E%3C/svg%3E");
            animation-delay: 4s;
        }

        .ornament-4 {
            bottom: 20%;
            right: 15%;
            width: 25px;
            height: 25px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 25 25'%3E%3Cpath fill='%238b7355' d='M12.5,2 C16,2 19,4 19,7 C19,10 16,12 12.5,12 C9,12 6,10 6,7 C6,4 9,2 12.5,2 Z M3,13 C6,13 9,15 9,18 C9,21 6,23 3,23 C0,23 -3,21 -3,18 C-3,15 0,13 3,13 Z M22,13 C25,13 28,15 28,18 C28,21 25,23 22,23 C19,23 16,21 16,18 C16,15 19,13 22,13 Z'/%3E%3C/svg%3E");
            animation-delay: 1s;
        }
        
        /* Ornament border untuk card */
        .ornament-card {
            position: relative;
            overflow: hidden;
        }
        
        .ornament-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 2px;
            background: linear-gradient(90deg, transparent, #8b7355, transparent);
            opacity: 0.3;
        }
        
        .ornament-card::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 2px;
            background: linear-gradient(90deg, transparent, #8b7355, transparent);
            opacity: 0.3;
        }

        /* Ornament header background pattern */
        .header-ornament {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 1;
            opacity: 0.05;
        }

        .header-ornament::before {
            content: '';
            position: absolute;
            top: 10%;
            left: 10%;
            width: 80%;
            height: 80%;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='100' viewBox='0 0 100 100'%3E%3Cpath fill='none' stroke='%23ffffff' stroke-width='0.5' d='M20,20 C40,0 60,0 80,20 C100,40 100,60 80,80 C60,100 40,100 20,80 C0,60 0,40 20,20 Z'/%3E%3C/svg%3E");
            background-size: 150px;
        }

        /* Ornament loading screen */
        .loading-ornament {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: -1;
            opacity: 0.1;
        }

        .loading-ornament::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 200px;
            height: 200px;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 200 200'%3E%3Cpath fill='none' stroke='%238b7355' stroke-width='2' d='M100,20 C140,20 170,50 170,90 C170,130 140,160 100,160 C60,160 30,130 30,90 C30,50 60,20 100,20 Z'/%3E%3Ccircle cx='100' cy='90' r='30' fill='none' stroke='%238b7355' stroke-width='1.5'/%3E%3C/svg%3E");
            background-size: contain;
            background-repeat: no-repeat;
        }

        /* Ornament button */
        .ornament-btn {
            position: relative;
            overflow: hidden;
        }

        .ornament-btn::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #8b7355, #b8a58d, #8b7355);
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: -1;
        }

        .ornament-btn:hover::before {
            opacity: 0.3;
        }

        /* Ornament gallery frame */
        .gallery-frame {
            position: relative;
            overflow: hidden;
            border: 1px solid #f0ebe4;
            background: #fcf9f5;
            transition: all 0.3s ease;
        }

        .gallery-frame::before {
            content: '';
            position: absolute;
            top: 8px;
            left: 8px;
            right: 8px;
            bottom: 8px;
            border: 1px solid rgba(139, 115, 85, 0.15);
            pointer-events: none;
            z-index: 2;
        }

        .gallery-frame:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(139,115,85,0.15);
        }

        /* Ornament countdown */
        .countdown-ornament {
            position: relative;
        }

        .countdown-ornament::before {
            content: '';
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 2px;
            background: linear-gradient(90deg, transparent, #8b7355, transparent);
        }

        /* Ornament music control */
        .music-ornament {
            position: relative;
        }

        .music-ornament::before {
            content: '♪';
            position: absolute;
            top: -25px;
            left: 50%;
            transform: translateX(-50%);
            color: #8b7355;
            opacity: 0.3;
            font-size: 16px;
        }

        /* Loading Screen */
        .loading-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #fefaf5;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            text-align: center;
            padding: 20px;
        }
        
        .couple-names {
            font-family: 'Cormorant Garamond', serif;
            font-size: 42px;
            color: #8b7355;
            margin-bottom: 15px;
            font-weight: 600;
            line-height: 1.2;
            letter-spacing: 1px;
        }
        
        .wedding-title {
            font-size: 16px;
            color: #a08c72;
            margin-bottom: 30px;
            letter-spacing: 3px;
            font-weight: 400;
            text-transform: uppercase;
        }
        
        .date-text {
            font-family: 'Cormorant Garamond', serif;
            font-size: 20px;
            color: #8b7355;
            margin-bottom: 20px;
            font-weight: 500;
            letter-spacing: 1px;
        }
        
        .loading-text {
            font-size: 15px;
            color: #7a6854;
            margin-bottom: 25px;
            max-width: 320px;
            line-height: 1.6;
            font-weight: 400;
        }
        
        .open-btn {
            padding: 16px 45px;
            font-size: 16px;
            background: #8b7355;
            color: white;
            border: none;
            border-radius: 2px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            letter-spacing: 2px;
            margin-top: 10px;
            text-transform: uppercase;
        }
        
        .open-btn:hover {
            background: #6d5a42;
        }
        
        .hidden {
            display: none;
        }
        
        /* Main Content */
        .wedding-invitation {
            max-width: 100%;
            margin: 0 auto;
            padding: 0;
            background: white;
            min-height: 100vh;
            position: relative;
        }
        
        /* Header dengan Background Foto Besar */
        .header-section {
            position: relative;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: center;
            text-align: center;
            color: white;
            overflow: hidden;
            padding-top: 8vh;
        }
        
        .header-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            z-index: 1;
            transition: background-image 0.5s ease;
        }
        
        .header-content {
            position: relative;
            z-index: 2;
            padding: 20px;
            max-width: 800px;
            margin-top: 4vh;
        }
        
        .main-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 7.5vw;
            color: #f9cb9c;
            margin-bottom: 25px;
            font-weight: 500;
            line-height: 1;
            letter-spacing: 3px;
            text-shadow: 2px 2px 12px rgba(0,0,0,0.8);
            text-transform: uppercase;
            font-style: italic;
            opacity: 0.95;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
        }
        
        .sub-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 2.5vw;
            color: rgba(255,255,255,0.95);
            margin-bottom: 60px;
            font-weight: 300;
            letter-spacing: 2px;
            font-style: italic;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.6);
            line-height: 1.3;
            opacity: 0.9;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease 0.2s;
        }
        
        .main-couple-names {
            font-family: 'Cormorant Garamond', serif;
            font-size: 4.5vw;
            color: rgba(255,255,255,0.95);
            margin-bottom: 30px;
            font-weight: 500;
            line-height: 1.1;
            letter-spacing: 2px;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.7);
            margin-top: 80px;
            opacity: 0.9;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease 0.4s;
        }
        
        .header-wedding-title {
            font-size: 1.8vw;
            color: rgba(255,255,255,0.9);
            margin-bottom: 25px;
            letter-spacing: 4px;
            font-weight: 300;
            text-transform: uppercase;
            opacity: 0.85;
            line-height: 1;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease 0.6s;
        }
        
        .header-date-text {
            font-family: 'Cormorant Garamond', serif;
            font-size: 2.5vw;
            color: rgba(255,255,255,0.95);
            margin-bottom: 60px;
            font-weight: 400;
            letter-spacing: 2px;
            text-shadow: 1px 1px 5px rgba(0,0,0,0.5);
            opacity: 0.9;
            line-height: 1;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease 0.8s;
        }
        
        /* Animasi saat elemen terlihat */
        .animate-in {
            transform: translateY(0);
            opacity: 1;
        }
        
        .section {
            margin: 0;
            padding: 80px 40px;
            background: white;
            border-bottom: 1px solid #f0ebe4;
            position: relative;
        }
        
        .section-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 32px;
            color: #8b7355;
            margin-bottom: 30px;
            text-align: center;
            position: relative;
            font-weight: 600;
            letter-spacing: 1px;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 40px;
            height: 1px;
            background: #b8a58d;
            margin: 15px auto;
        }
        
        .event-details {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }
        
        .event-card {
            background: #fcf9f5;
            padding: 30px 25px;
            border-radius: 0;
            text-align: center;
            border: 1px solid #f0ebe4;
            transition: transform 0.3s ease;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
        }
        
        .event-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(139,115,85,0.1);
        }
        
        .event-date {
            font-size: 18px;
            color: #8b7355;
            font-weight: 600;
            margin-bottom: 12px;
            font-family: 'Cormorant Garamond', serif;
        }
        
        .event-time {
            font-size: 16px;
            color: #a08c72;
            margin-bottom: 12px;
            font-weight: 500;
        }
        
        .event-location {
            font-size: 15px;
            color: #7a6854;
            line-height: 1.6;
        }
        
        .event-location strong {
            color: #8b7355;
            display: block;
            margin-bottom: 8px;
            font-size: 16px;
        }
        
        .location-btn {
            display: inline-block;
            margin-top: 15px;
            padding: 10px 20px;
            background: #8b7355;
            color: white;
            text-decoration: none;
            font-size: 14px;
            transition: all 0.3s ease;
        }
        
        .location-btn:hover {
            background: #6d5a42;
        }
        
        /* GALERI YANG DIPERBAIKI - TATA LETAK ATAS BAWAH */
        .gallery {
            display: flex;
            flex-direction: column;
            gap: 40px;
            margin-top: 25px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .gallery-item {
            background: transparent;
            border-radius: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: transform 0.3s ease;
            position: relative;
            overflow: hidden;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
            width: 100%;
            aspect-ratio: 4/5;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center;
            transition: transform 0.5s ease;
        }
        
        .gallery-item:hover img {
            transform: scale(1.03);
        }
        
        .rsvp-form {
            max-width: 500px;
            margin: 0 auto;
        }
        
        .form-group {
            margin-bottom: 25px;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
        }
        
        .form-input {
            width: 100%;
            padding: 15px 20px;
            border: 1px solid #e0d6c8;
            border-radius: 0;
            font-size: 16px;
            transition: border-color 0.3s ease;
            font-family: 'Montserrat', sans-serif;
            background: #fcf9f5;
            color: #5a4a3a;
        }
        
        .form-input:focus {
            outline: none;
            border-color: #8b7355;
        }
        
        .form-input::placeholder {
            color: #a08c72;
        }
        
        .submit-btn {
            background: #8b7355;
            color: white;
            border: none;
            padding: 18px 40px;
            border-radius: 0;
            font-size: 16px;
            cursor: pointer;
            width: 100%;
            font-weight: 500;
            transition: all 0.3s ease;
            letter-spacing: 1px;
            text-transform: uppercase;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
        }
        
        .submit-btn:hover {
            background: #6d5a42;
        }
        
        /* Gift Section */
        .gift-section {
            background: #fcf9f5;
            padding: 60px 30px;
        }
        
        .gift-section p {
            text-align: center;
            color: #7a6854 !important;
            margin-bottom: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            font-weight: 500;
            line-height: 1.6;
        }
        
        /* MODIFIKASI UNTUK PANEL REKENING YANG LEBIH RINGKAS */
        .compact-accounts {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .account-pair {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 20px;
        }
        
        .compact-account-card {
            background: white;
            padding: 20px;
            border-radius: 0;
            text-align: center;
            border: 1px solid #f0ebe4;
            transition: transform 0.3s ease;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
        }
        
        .compact-account-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(139,115,85,0.1);
        }
        
        .account-header {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .account-icon {
            font-size: 20px;
        }
        
        .account-type {
            font-size: 16px;
            color: #8b7355;
            font-weight: 600;
            font-family: 'Cormorant Garamond', serif;
        }
        
        .account-details {
            background: #fcf9f5;
            padding: 15px;
            margin: 10px 0;
            border: 1px solid #f0ebe4;
        }
        
        .account-number {
            font-size: 14px;
            color: #5a4a3a;
            font-weight: 600;
            margin-bottom: 8px;
            font-family: 'Montserrat', monospace;
        }
        
        .account-holder {
            font-size: 12px;
            color: #7a6854;
            margin-bottom: 10px;
        }
        
        .copy-btn {
            background: #8b7355;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 0;
            font-size: 12px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
        }
        
        .copy-btn:hover {
            background: #6d5a42;
        }
        
        .copy-btn.copied {
            background: #8b7355;
        }
        
        /* KARTU ALAMAT PENGIRIMAN HADIAH YANG LEBIH KECIL */
        .address-card {
            background: white;
            padding: 20px;
            border-radius: 0;
            text-align: center;
            border: 1px solid #f0ebe4;
            transition: transform 0.3s ease;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
            max-width: 500px;
            margin: 30px auto 0 auto;
        }
        
        .address-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(139,115,85,0.1);
        }
        
        .address-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 18px;
            color: #8b7355;
            margin-bottom: 10px;
            font-weight: 600;
        }
        
        .address-description {
            color: #7a6854;
            margin-bottom: 15px;
            font-style: italic;
            font-weight: 500;
            line-height: 1.6;
            font-size: 14px;
        }
        
        .address-details {
            background: #fcf9f5;
            padding: 15px;
            border: 1px solid #f0ebe4;
            margin: 15px 0;
            text-align: left;
        }
        
        .address-line {
            margin-bottom: 10px;
            display: flex;
            align-items: flex-start;
        }
        
        .address-line:last-child {
            margin-bottom: 0;
        }
        
        .address-label {
            font-weight: 600;
            color: #5a4a3a;
            min-width: 80px;
            text-align: left;
            font-size: 14px;
        }
        
        .address-value {
            color: #5a4a3a;
            font-weight: 500;
            flex: 1;
            text-align: left;
            line-height: 1.5;
            font-size: 14px;
        }
        
        /* Music Controls - Sederhana dan Minimalis */
        .music-controls {
            position: fixed;
            bottom: 25px;
            right: 25px;
            z-index: 10000;
            display: flex;
            gap: 10px;
            background: rgba(255, 248, 240, 0.95);
            padding: 10px 15px;
            border-radius: 0;
            box-shadow: 0 3px 10px rgba(139,115,85,0.2);
            border: 1px solid #f0ebe4;
        }
        
        .music-btn {
            width: 40px;
            height: 40px;
            border-radius: 0;
            border: none;
            background: #8b7355;
            color: white;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 14px;
            transition: all 0.3s ease;
        }
        
        .music-btn:hover {
            background: #6d5a42;
        }
        
        .divider {
            width: 80px;
            height: 1px;
            background: #b8a58d;
            margin: 20px auto;
        }
        
        .quote-text {
            font-style: italic;
            text-align: center;
            font-size: 16px;
            color: #7a6854;
            margin: 30px 0;
            padding: 0 20px;
            line-height: 1.8;
            font-family: 'Cormorant Garamond', serif;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
        }
        
        /* COUNTDOWN */
        .countdown {
            text-align: center;
            margin: 50px 0 30px 0;
            font-family: 'Cormorant Garamond', serif;
        }
        
        .countdown-title {
            font-size: 1.8vw;
            color: rgba(255,255,255,0.9);
            margin-bottom: 30px;
            text-transform: uppercase;
            letter-spacing: 2px;
            opacity: 0.85;
            line-height: 1;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease 1s;
        }
        
        .countdown-timer {
            display: flex;
            justify-content: center;
            gap: 30px;
        }
        
        .countdown-item {
            text-align: center;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
        }
        
        .countdown-number {
            font-size: 4vw;
            font-weight: 600;
            color: rgba(255,255,255,0.95);
            display: block;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.7);
            opacity: 0.9;
            line-height: 1;
        }
        
        .countdown-label {
            font-size: 1.2vw;
            color: rgba(255,255,255,0.85);
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-top: 10px;
            opacity: 0.8;
            line-height: 1;
        }
        
        .footer {
            text-align: center;
            padding: 40px 20px;
            background: #fcf9f5;
            color: #7a6854;
            font-size: 14px;
        }
        
        .thank-you {
            font-family: 'Cormorant Garamond', serif;
            font-size: 20px;
            margin-bottom: 10px;
            color: #8b7355;
        }

        /* Loading untuk foto */
        .photo-loading {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            height: 100%;
            background: #fcf9f5;
            color: #b8a58d;
            font-size: 16px;
            flex-direction: column;
            gap: 10px;
        }

        .loading-spinner {
            width: 30px;
            height: 30px;
            border: 3px solid #f3f3f3;
            border-top: 3px solid #b8a58d;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Style untuk nama orang tua */
        .parents-name {
            font-size: 16px;
            color: #7a6854;
            margin-top: 5px;
        }

        .alm {
            font-style: italic;
            color: #a08c72;
        }

        .tagline {
            font-family: 'Cormorant Garamond', serif;
            font-size: 18px;
            color: #8b7355;
            text-align: center;
            font-style: italic;
            margin: 40px 0;
            line-height: 1.6;
            padding: 0 20px;
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.8s ease;
        }

        /* Animasi saat elemen terlihat */
        .animate-in {
            transform: translateY(0);
            opacity: 1;
        }

        /* ========== KOMENTAR BUBBLE BESAR SCROLLABLE ========== */
        .bubble-comments-section {
            background: linear-gradient(135deg, #fef9f5 0%, #fdf6f0 100%);
            padding: 80px 30px;
            border-top: 1px solid #e8dfd1;
            border-bottom: 1px solid #e8dfd1;
            position: relative;
            overflow: hidden;
        }

        .bubble-comments-container {
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }

        .bubble-comments-header {
            text-align: center;
            margin-bottom: 50px;
        }

        .bubble-comments-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 38px;
            color: #7a6248;
            margin-bottom: 15px;
            font-weight: 600;
            letter-spacing: 1px;
            position: relative;
            display: inline-block;
        }

        .bubble-comments-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 2px;
            background: linear-gradient(90deg, #d4c8b5, #8b7355, #d4c8b5);
        }

        .bubble-comments-subtitle {
            font-size: 18px;
            color: #8b7355;
            max-width: 600px;
            margin: 25px auto 0;
            line-height: 1.6;
            font-style: italic;
        }

        /* Bubble Besar Scrollable */
        .big-bubble-container {
            background: white;
            border-radius: 20px;
            box-shadow: 0 8px 30px rgba(0,0,0,0.1);
            padding: 30px;
            margin: 40px auto;
            max-width: 800px;
            border: 1px solid #f0e9dd;
            position: relative;
            overflow: hidden;
        }

        .big-bubble-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, #8b7355, #d4c8b5, #8b7355);
        }

        .bubble-scroll-area {
            max-height: 400px;
            overflow-y: auto;
            padding-right: 15px;
            margin-bottom: 25px;
        }

        /* Scrollbar styling */
        .bubble-scroll-area::-webkit-scrollbar {
            width: 6px;
        }

        .bubble-scroll-area::-webkit-scrollbar-track {
            background: #f5f2ed;
            border-radius: 3px;
        }

        .bubble-scroll-area::-webkit-scrollbar-thumb {
            background: #d4c8b5;
            border-radius: 3px;
        }

        .bubble-scroll-area::-webkit-scrollbar-thumb:hover {
            background: #8b7355;
        }

        /* Individual Comment Styles */
        .comment-item {
            padding: 20px;
            margin-bottom: 20px;
            background: #fcf9f5;
            border-radius: 15px;
            border: 1px solid #f0ebe4;
            transition: all 0.3s ease;
            position: relative;
        }

        .comment-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(139,115,85,0.1);
        }

        .comment-item:last-child {
            margin-bottom: 0;
        }

        .comment-message {
            font-size: 14px;
            line-height: 1.6;
            color: #5a4a3a;
            margin-bottom: 12px;
            font-style: italic;
        }

        .comment-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 12px;
            color: #8b7355;
            border-top: 1px solid #f0ebe4;
            padding-top: 12px;
        }

        .comment-author {
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .comment-date {
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .empty-comments {
            text-align: center;
            padding: 60px 20px;
            color: #a08c72;
            font-style: italic;
        }

        .empty-comments-icon {
            font-size: 48px;
            margin-bottom: 15px;
            opacity: 0.6;
        }

        /* Bubble Form */
        .bubble-form-container {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            border: 1px solid #f0e9dd;
        }

        .bubble-input {
            width: 100%;
            padding: 14px 16px;
            border: 1px solid #e0e0e0;
            border-radius: 12px;
            font-size: 15px;
            margin-bottom: 15px;
            font-family: 'Montserrat', sans-serif;
            background: #fafafa;
            color: #5a4a3a;
            resize: vertical;
            min-height: 100px;
            transition: all 0.3s ease;
            line-height: 1.5;
        }

        .bubble-input:focus {
            outline: none;
            border-color: #8b7355;
            background: white;
        }

        .bubble-input::placeholder {
            color: #888;
        }

        .bubble-submit-btn {
            background: #8b7355;
            color: white;
            border: none;
            padding: 12px 28px;
            border-radius: 12px;
            font-size: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 8px;
            margin-left: auto;
        }

        .bubble-submit-btn:hover {
            background: #7a6248;
        }

        /* Response Message Styles */
        .response-message {
            margin-top: 20px;
            padding: 15px;
            border-radius: 5px;
            text-align: center;
            display: none;
            font-weight: 500;
            font-size: 14px;
        }

        .response-message.success {
            background: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
        }

        .response-message.error {
            background: #f8d7da;
            color: #721c24;
            border: 1px solid #f5c6cb;
        }

        /* Notifikasi Salin */
        .copy-notification {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #8b7355;
            color: white;
            padding: 15px 25px;
            border-radius: 0;
            z-index: 10001;
            font-size: 14px;
            box-shadow: 0 3px 10px rgba(139,115,85,0.3);
            transform: translateX(150%);
            transition: transform 0.3s ease;
        }
        
        .copy-notification.show {
            transform: translateX(0);
        }

        /* Responsive Design untuk Mobile */
        @media (max-width: 768px) {
            .header-section {
                padding-top: 6vh;
                height: 100vh;
            }
            
            .header-content {
                margin-top: 3vh;
                padding: 15px;
            }
            
            .main-title {
                font-size: 42px;
                margin-bottom: 20px;
                letter-spacing: 2px;
            }
            
            .sub-title {
                font-size: 18px;
                margin-bottom: 50px;
                letter-spacing: 1px;
                line-height: 1.3;
            }
            
            .main-couple-names {
                font-size: 28px;
                margin-bottom: 25px;
                margin-top: 60px;
                line-height: 1.1;
                letter-spacing: 1px;
            }
            
            .header-wedding-title {
                font-size: 14px;
                margin-bottom: 20px;
                letter-spacing: 2px;
                line-height: 1;
            }
            
            .header-date-text {
                font-size: 20px;
                margin-bottom: 50px;
                letter-spacing: 1px;
                line-height: 1;
            }
            
            .countdown {
                margin: 40px 0 25px 0;
            }
            
            .countdown-title {
                font-size: 14px;
                margin-bottom: 25px;
                letter-spacing: 1px;
            }
            
            .countdown-number {
                font-size: 28px;
            }
            
            .countdown-label {
                font-size: 10px;
                margin-top: 8px;
                letter-spacing: 0.5px;
            }
            
            .countdown-timer {
                gap: 25px;
            }
            
            .section {
                padding: 60px 20px;
            }
            
            .gallery {
                max-width: 100%;
                gap: 30px;
            }
            
            .gallery-item {
                aspect-ratio: 4/5;
            }
            
            .compact-accounts {
                grid-template-columns: 1fr;
                gap: 15px;
            }
            
            .account-pair {
                grid-template-columns: 1fr;
                gap: 15px;
            }

            .address-card {
                margin: 20px 10px 0 10px;
                max-width: 100%;
            }

            .address-line {
                flex-direction: column;
                align-items: flex-start;
            }

            .address-label {
                min-width: auto;
                margin-bottom: 5px;
            }

            /* Responsive untuk Bubble Komentar */
            .bubble-comments-section {
                padding: 60px 20px;
            }
            
            .bubble-comments-title {
                font-size: 32px;
            }
            
            .bubble-comments-subtitle {
                font-size: 16px;
            }
            
            .big-bubble-container {
                padding: 20px;
                margin: 30px auto;
            }
            
            .bubble-scroll-area {
                max-height: 350px;
            }
            
            .bubble-form-container {
                padding: 20px;
            }
            
            .bubble-input {
                padding: 12px;
                min-height: 80px;
            }

            /* Ornament responsive */
            .ornament-corner {
                width: 80px;
                height: 80px;
            }
            
            .floral-corner {
                width: 50px;
                height: 50px;
            }
            
            .floating-ornament {
                display: none;
            }
        }

        @media (max-width: 480px) {
            .header-section {
                padding-top: 5vh;
            }
            
            .header-content {
                margin-top: 2vh;
            }
            
            .main-title {
                font-size: 36px;
                margin-bottom: 15px;
            }
            
            .sub-title {
                font-size: 16px;
                margin-bottom: 40px;
            }
            
            .main-couple-names {
                font-size: 24px;
                margin-bottom: 20px;
                margin-top: 50px;
            }
            
            .countdown {
                margin: 35px 0 20px 0;
            }
            
            .countdown-timer {
                gap: 20px;
            }
            
            .countdown-number {
                font-size: 24px;
            }
            
            .gallery {
                gap: 25px;
            }
            
            .gallery-item {
                aspect-ratio: 4/5;
            }
            
            .comment-item {
                padding: 15px;
            }
            
            .comment-message {
                font-size: 13px;
            }
        }
    </style>
</head>
<body>
    <!-- Background Batik -->
    <div class="batik-background"></div>
    
    <!-- ========== ORNAMENT DEKORATIF KOMPLIT ========== -->
    <!-- Ornament Corner -->
    <div class="ornament-corner ornament-top-left"></div>
    <div class="ornament-corner ornament-top-right"></div>
    <div class="ornament-corner ornament-bottom-left"></div>
    <div class="ornament-corner ornament-bottom-right"></div>
    
    <!-- Floral Corner -->
    <div class="floral-corner floral-top-left"></div>
    <div class="floral-corner floral-top-right"></div>
    <div class="floral-corner floral-bottom-left"></div>
    <div class="floral-corner floral-bottom-right"></div>
    
    <!-- Floating Ornaments -->
    <div class="floating-ornament ornament-1"></div>
    <div class="floating-ornament ornament-2"></div>
    <div class="floating-ornament ornament-3"></div>
    <div class="floating-ornament ornament-4"></div>
    
    <!-- Loading Screen -->
    <div id="loadingScreen" class="loading-screen">
        <!-- Ornament loading screen -->
        <div class="loading-ornament"></div>
        
        <div class="couple-names">Huda Nurcahyo S<br>&<br>Desy Irmaya</div>
        
        <!-- Ornament divider di loading screen -->
        <div class="divider-floral">
            <div class="floral-center"></div>
        </div>
        
        <div class="wedding-title">The Wedding Celebration</div>
        <div class="date-text">14 Desember 2025</div>
        
        <div class="loading-text">
            Dengan penuh kebahagiaan, kami mengundang Anda untuk menyaksikan pernikahan kami.
        </div>
        
        <button class="open-btn ornament-btn" onclick="openInvitation()">
            Buka Undangan
        </button>
    </div>

    <!-- Konten Undangan Utama -->
    <div id="mainContent" class="hidden">
        <div class="wedding-invitation">
            <!-- Header dengan Background Foto Besar -->
            <div class="header-section">
                <!-- Ornament header -->
                <div class="header-ornament"></div>
                
                <div class="header-background" id="headerBackground">
                    <div class="photo-loading" id="photoLoading">
                        <div class="loading-spinner"></div>
                        Memuat Foto...
                    </div>
                </div>
                
                <div class="header-content">
                    <h1 class="main-title">Our Happily Ever After</h1>
                    <div class="sub-title">Our Destiny's Next Chapter: A Life Time As One</div>
                    
                    <!-- Spacing yang DITAMBAH -->
                    <div style="height: 80px;"></div>
                    
                    <div class="main-couple-names">Huda Nurcahyo S<br>&<br>Desy Irmaya</div>
                    <div class="header-wedding-title">Undangan Pernikahan</div>
                    <div class="header-date-text">14 Desember 2025</div>
                    
                    <!-- Countdown -->
                    <div class="countdown countdown-ornament">
                        <div class="countdown-title">Menuju Hari Bahagia</div>
                        <div class="countdown-timer">
                            <div class="countdown-item">
                                <span class="countdown-number" id="days">00</span>
                                <span class="countdown-label">Hari</span>
                            </div>
                            <div class="countdown-item">
                                <span class="countdown-number" id="hours">00</span>
                                <span class="countdown-label">Jam</span>
                            </div>
                            <div class="countdown-item">
                                <span class="countdown-number" id="minutes">00</span>
                                <span class="countdown-label">Menit</span>
                            </div>
                            <div class="countdown-item">
                                <span class="countdown-number" id="seconds">00</span>
                                <span class="countdown-label">Detik</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Sambutan -->
            <div class="section" style="position: relative;">
                <!-- Ornament section -->
                <div class="section-ornament section-top-left"></div>
                <div class="section-ornament section-top-right"></div>
                <div class="section-ornament section-bottom-left"></div>
                <div class="section-ornament section-bottom-right"></div>
                
                <h2 class="section-title">Assalamu'alaikum Warahmatullahi Wabarakatuh</h2>
                <p style="text-align: center; line-height: 1.8; font-size: 16px; color: #7a6854;">
                    Dengan memohon rahmat dan ridho Allah Subhanahu Wa Ta'ala, kami bermaksud menyelenggarakan 
                    resepsi pernikahan putra-putri kami. Tanpa mengurangi rasa hormat, kami mengundang Bapak/Ibu/Saudara/i 
                    untuk hadir dan memberikan do'a restu.
                </p>
                
                <!-- Ornament divider floral -->
                <div class="divider-floral">
                    <div class="floral-center"></div>
                </div>
                
                <div class="tagline">
                    "Fate Didn't Just Bring Us Together, It Started Our Forever"
                </div>
                
                <div style="text-align: center; margin: 40px 0;">
                    <h3 style="color: #8b7355; font-size: 22px; margin-bottom: 15px; font-family: 'Cormorant Garamond', serif;">
                        Huda Nurcahyo S
                    </h3>
                    <p class="parents-name">Putra dari</p>
                    <p class="parents-name">Bapak <strong>Rubino Fianto</strong></p>
                    <p class="parents-name">dan Ibu <strong class="alm">Almarhumah Kasini</strong></p>
                    
                    <!-- Ornament divider kecil -->
                    <div style="margin: 30px 0; display: flex; justify-content: center; align-items: center;">
                        <div style="width: 20px; height: 20px; background-image: url('data:image/svg+xml,%3Csvg xmlns=\'http://www.w3.org/2000/svg\' viewBox=\'0 0 20 20\'%3E%3Ccircle cx=\'10\' cy=\'10\' r=\'8\' fill=\'none\' stroke=\'%23b8a58d\' stroke-width=\'1\'/%3E%3C/svg%3E'); opacity: 0.5;"></div>
                    </div>
                    
                    <h3 style="color: #8b7355; font-size: 22px; margin-bottom: 15px; font-family: 'Cormorant Garamond', serif;">
                        Desy Irmaya
                    </h3>
                    <p class="parents-name">Putri dari</p>
                    <p class="parents-name">Bapak <strong>Muladi</strong></p>
                    <p class="parents-name">dan Ibu <strong>Sumini</strong></p>
                </div>
            </div>

            <!-- Acara -->
            <div class="section" style="position: relative;">
                <!-- Ornament section -->
                <div class="section-ornament section-top-left"></div>
                <div class="section-ornament section-top-right"></div>
                <div class="section-ornament section-bottom-left"></div>
                <div class="section-ornament section-bottom-right"></div>
                
                <h2 class="section-title">Jadwal Acara</h2>
                
                <!-- Ornament divider floral -->
                <div class="divider-floral">
                    <div class="floral-center"></div>
                </div>
                
                <div class="event-details">
                    <div class="event-card ornament-card">
                        <div class="event-date">Minggu, 14 Desember 2025</div>
                        <div class="event-time">08:00 - 12:00 WIB</div>
                        <div class="event-location">
                            <strong>Akad Nikah</strong>
                            Kantor Kalurahan Nglegi, Patuk, Gunungkidul<br>
                            Trukan, Nglegi, Kec. Patuk, Kabupaten Gunungkidul,<br>
                            Daerah Istimewa Yogyakarta 55862
                            <a href="https://maps.app.goo.gl/ctwb5nyjPKXw98Hv7" target="_blank" class="location-btn ornament-btn">
                                📍 Lihat Lokasi
                            </a>
                        </div>
                    </div>
                    <div class="event-card ornament-card">
                        <div class="event-date">Minggu, 14 Desember 2025</div>
                        <div class="event-time">18:00 - 21:00 WIB</div>
                        <div class="event-location">
                            <strong>Ngunduh Mantu</strong>
                            Rumah Keluarga Besar Bapak Rubino F.<br>
                            Grogol 2 No.002/002, Grogol II, Bejiharjo, Kec. Karangmojo,<br>
                            Yogyakarta, Daerah Istimewa Yogyakarta 55891
                            <a href="https://maps.app.goo.gl/VyiPVoBhiw8WKGRj9" target="_blank" class="location-btn ornament-btn">
                                📍 Lihat Lokasi
                            </a>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Gallery -->
            <div class="section" style="position: relative;">
                <!-- Ornament section -->
                <div class="section-ornament section-top-left"></div>
                <div class="section-ornament section-top-right"></div>
                <div class="section-ornament section-bottom-left"></div>
                <div class="section-ornament section-bottom-right"></div>
                
                <h2 class="section-title">Galeri Kenangan</h2>
                
                <!-- Ornament divider floral -->
                <div class="divider-floral">
                    <div class="floral-center"></div>
                </div>
                
                <div class="gallery">
                    <div class="gallery-item gallery-frame ornament-card">
                        <img src="https://drive.google.com/thumbnail?id=1qFlwcx460-Kyh7-wtunvNZYhk6UFepDV&sz=w2000" 
                             alt="Foto Kenangan Huda & Desy" 
                             loading="lazy"
                             onerror="this.src='https://images.unsplash.com/photo-1519225421980-715cb0215aed?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80'">
                    </div>
                    <div class="gallery-item gallery-frame ornament-card">
                        <img src="https://drive.google.com/thumbnail?id=12RSsFqzX7HewK-4_gpWdSQX1HpVlrfHI&sz=w2000" 
                             alt="Foto Kenangan Huda & Desy" 
                             loading="lazy"
                             onerror="this.src='https://images.unsplash.com/photo-1519225421980-715cb0215aed?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80'">
                    </div>
                </div>
            </div>

            <!-- RSVP DENGAN GOOGLE APPS SCRIPT -->
            <div class="section" style="position: relative;">
                <!-- Ornament section -->
                <div class="section-ornament section-top-left"></div>
                <div class="section-ornament section-top-right"></div>
                <div class="section-ornament section-bottom-left"></div>
                <div class="section-ornament section-bottom-right"></div>
                
                <h2 class="section-title">Konfirmasi Kehadiran</h2>
                
                <!-- Ornament divider floral -->
                <div class="divider-floral">
                    <div class="floral-center"></div>
                </div>
                
                <div style="background: #f0f8f0; border: 1px solid #4caf50; padding: 15px; margin: 20px 0; border-radius: 5px; text-align: center;">
                    <p style="color: #2e7d32; margin: 5px 0; font-size: 14px;">
                        <strong>📝 Konfirmasi via Form Online</strong>
                    </p>
                    <p style="color: #2e7d32; margin: 5px 0; font-size: 14px;">
                        Data akan langsung tersimpan ke Google Sheets kami secara otomatis
                    </p>
                </div>
                
                <div class="rsvp-form ornament-card" id="rsvpForm" style="padding: 20px;">
                    <div class="form-group">
                        <input type="text" class="form-input" id="rsvpNama" placeholder="Nama Lengkap *" required>
                    </div>
                    <div class="form-group">
                        <input type="email" class="form-input" id="rsvpEmail" placeholder="Email (opsional)">
                    </div>
                    <div class="form-group">
                        <input type="number" class="form-input" id="rsvpJumlahTamu" placeholder="Jumlah Tamu *" min="1" max="10" value="1" required>
                    </div>
                    <div class="form-group">
                        <select class="form-input" id="rsvpKehadiran" required>
                            <option value="">Pilih Kehadiran *</option>
                            <option value="Hadir di Akad & Ngunduh Mantu">Hadir di Akad & Ngunduh Mantu</option>
                            <option value="Hadir di Akad saja">Hadir di Akad saja</option>
                            <option value="Hadir di Ngunduh Mantu saja">Hadir di Ngunduh Mantu saja</option>
                            <option value="Berhalangan hadir">Berhalangan hadir</option>
                        </select>
                    </div>
                    <button class="submit-btn ornament-btn" onclick="submitRSVP()">
                        💌 Kirim Konfirmasi
                    </button>
                </div>
                
                <div id="rsvpResponse" class="response-message"></div>
            </div>

            <!-- ========== BUBBLE KOMENTAR BESAR SCROLLABLE ========== -->
            <div class="bubble-comments-section" style="position: relative;">
                <!-- Ornament section -->
                <div class="section-ornament section-top-left"></div>
                <div class="section-ornament section-top-right"></div>
                <div class="section-ornament section-bottom-left"></div>
                <div class="section-ornament section-bottom-right"></div>
                
                <div class="bubble-comments-container">
                    <div class="bubble-comments-header">
                        <h2 class="bubble-comments-title">Ucapan & Doa dari Tamu</h2>
                        
                        <!-- Ornament divider floral -->
                        <div class="divider-floral">
                            <div class="floral-center"></div>
                        </div>
                        
                        <p class="bubble-comments-subtitle">
                            Berbagi kebahagiaan melalui kata-kata indah dari para tamu undangan yang telah memberikan doa dan restu
                        </p>
                    </div>
                    
                    <!-- Bubble Besar Scrollable -->
                    <div class="big-bubble-container ornament-card">
                        <div class="bubble-scroll-area" id="bubbleCommentsDisplay">
                            <!-- Komentar akan ditampilkan di sini dalam satu bubble besar -->
                        </div>
                        
                        <div class="bubble-comments-count" style="text-align: center; color: #8b7355; font-size: 14px; margin-bottom: 15px;">
                            <span id="commentsCount">0</span> ucapan dan doa
                        </div>
                    </div>
                    
                    <!-- Bubble Form -->
                    <div class="bubble-form-container ornament-card">
                        <h3 style="color: #7a6248; margin-bottom: 20px; text-align: center; font-family: 'Cormorant Garamond', serif;">
                            Tambahkan Ucapan & Doa Anda
                        </h3>
                        <input type="text" class="form-input" id="bubbleCommentName" placeholder="Nama Anda (opsional)" style="margin-bottom: 20px; border-radius: 12px;">
                        <textarea class="bubble-input" id="bubbleCommentMessage" placeholder="Tuliskan ucapan dan doa terbaik Anda untuk mempelai..."></textarea>
                        <button class="bubble-submit-btn ornament-btn" onclick="submitBubbleComment()">
                            💌 Kirim Ucapan
                        </button>
                    </div>
                </div>
            </div>

            <!-- ========== WEDDING GIFT ========== -->
            <div class="gift-section" style="position: relative;">
                <!-- Ornament section -->
                <div class="section-ornament section-top-left"></div>
                <div class="section-ornament section-top-right"></div>
                <div class="section-ornament section-bottom-left"></div>
                <div class="section-ornament section-bottom-right"></div>
                
                <h2 class="section-title">Wedding Gift</h2>
                
                <!-- Ornament divider floral -->
                <div class="divider-floral">
                    <div class="floral-center"></div>
                </div>
                
                <p>
                    Kehadiran dan doa Anda adalah hadiah terindah bagi kami. Namun jika ingin memberikan tanda kasih, 
                    berikut informasi rekening dan dompet digital yang dapat digunakan:
                </p>
                
                <!-- LAYOUT REKENING YANG LEBIH RINGKAS -->
                <div class="compact-accounts">
                    <!-- BARIS ATAS: REKENING BANK -->
                    <div class="account-pair">
                        <!-- KIRI: REKENING HUDA -->
                        <div class="compact-account-card ornament-card">
                            <div class="account-header">
                                <div class="account-icon">🏦</div>
                                <div class="account-type">Bank BRI</div>
                            </div>
                            <div class="account-details">
                                <div class="account-number">6971 0100 3686 509</div>
                                <div class="account-holder">a.n. Huda Nurcahyo S</div>
                            </div>
                            <button class="copy-btn ornament-btn" onclick="copyToClipboard('697101003686509', this)">
                                📋 Salin Nomor
                            </button>
                        </div>
                        
                        <!-- KANAN: REKENING DESY -->
                        <div class="compact-account-card ornament-card">
                            <div class="account-header">
                                <div class="account-icon">🏦</div>
                                <div class="account-type">Bank BRI</div>
                            </div>
                            <div class="account-details">
                                <div class="account-number">7061 0100 6234 507</div>
                                <div class="account-holder">a.n. Desy Irmaya</div>
                            </div>
                            <button class="copy-btn ornament-btn" onclick="copyToClipboard('706101006234507', this)">
                                📋 Salin Nomor
                            </button>
                        </div>
                    </div>
                    
                    <!-- BARIS BAWAH: DOMPET DIGITAL -->
                    <div class="account-pair">
                        <!-- KIRI: DANA HUDA -->
                        <div class="compact-account-card ornament-card">
                            <div class="account-header">
                                <div class="account-icon">💜</div>
                                <div class="account-type">DANA</div>
                            </div>
                            <div class="account-details">
                                <div class="account-number">083838665700</div>
                                <div class="account-holder">a.n. Huda Nurcahyo S</div>
                            </div>
                            <button class="copy-btn ornament-btn" onclick="copyToClipboard('083838665700', this)">
                                📋 Salin Nomor
                            </button>
                        </div>
                        
                        <!-- KANAN: SHOPEEPAY DESY -->
                        <div class="compact-account-card ornament-card">
                            <div class="account-header">
                                <div class="account-icon">🛍️</div>
                                <div class="account-type">ShopeePay</div>
                            </div>
                            <div class="account-details">
                                <div class="account-number">088238320769</div>
                                <div class="account-holder">a.n. Desy Irmaya</div>
                            </div>
                            <button class="copy-btn ornament-btn" onclick="copyToClipboard('088238320769', this)">
                                📋 Salin Nomor
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- KARTU ALAMAT PENGIRIMAN HADIAH -->
                <div class="address-card ornament-card">
                    <div class="address-title">Alamat Pengiriman Hadiah</div>
                    <p class="address-description">
                        Bagi yang ingin memberikan hadiah, silahkan dikirim ke alamat berikut:
                    </p>
                    <div class="address-details">
                        <div class="address-line">
                            <span class="address-label">Penerima:</span>
                            <span class="address-value">Desy Irmaya</span>
                        </div>
                        <div class="address-line">
                            <span class="address-label">Alamat:</span>
                            <span class="address-value">Nglegi No.011/003, Nglegi, Nglegi, Patuk, Gunungkidul</span>
                        </div>
                    </div>
                    <button class="copy-btn ornament-btn" onclick="copyAddressToClipboard(this)" style="margin-top: 15px;">
                        📋 Salin Alamat
                    </button>
                </div>
            </div>

            <!-- Penutup -->
            <div class="section" style="text-align: center; background: transparent; border-bottom: none; position: relative;">
                <!-- Ornament section -->
                <div class="section-ornament section-top-left"></div>
                <div class="section-ornament section-top-right"></div>
                <div class="section-ornament section-bottom-left"></div>
                <div class="section-ornament section-bottom-right"></div>
                
                <!-- Ornament divider floral -->
                <div class="divider-floral">
                    <div class="floral-center"></div>
                </div>
                
                <div class="quote-text">
                    "Dan di antara tanda-tanda kekuasaan-Nya ialah Dia menciptakan untukmu istri-istri 
                    dari jenismu sendiri, supaya kamu cenderung dan merasa tenteram kepadanya, dan dijadikan-Nya 
                    di antaramu rasa kasih dan sayang." (QS. Ar-Rum: 21)
                </div>
                <p style="font-size: 16px; color: #7a6854; margin-top: 20px;">
                    Merupakan suatu kehormatan dan kebahagiaan bagi kami apabila Bapak/Ibu/Saudara/i 
                    berkenan hadir untuk memberikan do'a restu.
                </p>
            </div>
            
            <!-- Footer -->
            <div class="footer" style="position: relative;">
                <!-- Ornament section -->
                <div class="section-ornament section-top-left"></div>
                <div class="section-ornament section-top-right"></div>
                
                <div class="thank-you">Terima Kasih</div>
                <p>Kami yang berbahagia,<br><strong>Keluarga Besar Huda & Desy</strong></p>
            </div>
        </div>
    </div>

    <!-- Kontrol Musik - Minimalis -->
    <div id="musicControls" class="music-controls hidden music-ornament">
        <button id="playPauseBtn" class="music-btn">⏸️</button>
        <button id="stopBtn" class="music-btn">⏹️</button>
    </div>

    <!-- Notifikasi Salin -->
    <div id="copyNotification" class="copy-notification">
        ✅ Berhasil disalin ke clipboard
    </div>

    <script>
        // ========== KONFIGURASI YANG DIPERBAIKI ==========
        const YOUTUBE_VIDEO_ID = 'Ph94XLpDKm0';
        const WEDDING_DATE = new Date('December 14, 2025 00:00:00').getTime();
        
        // URL Google Apps Script YANG BARU - SESUAI PERMINTAAN ANDA
        const RSVP_SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbw7cs6A703qUueElvfir6qWr6mZKDtJzPtSi5SO7_cr2s69JGH6ZYvB3i1DLMiIJ7ScpQ/exec';
        
        const PHOTO_URLS = [
            'https://drive.google.com/thumbnail?id=10b3WE_Qcr6kaNw2WbQjziTW9BrIF5qkP&sz=w2000',
            'https://images.unsplash.com/photo-1519225421980-715cb0215aed?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80'
        ];
        
        let musicPlayer = null;
        let isMusicPlaying = false;

        // Data komentar contoh
        const sampleComments = [
            {
                id: 1,
                name: "Keluarga Besar",
                message: "Selamat menempuh hidup baru. Semoga menjadi keluarga yang sakinah, mawaddah, warahmah.",
                date: "12 Des 2023"
            },
            {
                id: 2,
                name: "Sahabat Mempelai",
                message: "Akhirnya hari bahagia kalian tiba! Semoga pernikahan ini membawa kebahagiaan tak terhingga.",
                date: "11 Des 2023"
            },
            {
                id: 3,
                name: "Teman Kerja",
                message: "Congratulations! Semoga pernikahan kalian penuh berkah dan kebahagiaan selalu.",
                date: "10 Des 2023"
            },
            {
                id: 4,
                name: "Saudara",
                message: "Selamat atas pernikahannya. Semoga langgeng hingga akhir hayat. ❤️",
                date: "9 Des 2023"
            }
        ];

        // ========== SISTEM RSVP YANG DIPERBAIKI (TANPA PESAN) ==========
        async function submitRSVP() {
            console.log('=== MULAI SUBMIT RSVP ===');
            
            const nama = document.getElementById('rsvpNama').value.trim();
            const email = document.getElementById('rsvpEmail').value.trim();
            const jumlahTamu = document.getElementById('rsvpJumlahTamu').value;
            const kehadiran = document.getElementById('rsvpKehadiran').value;
            const submitBtn = document.querySelector('.submit-btn');
            const responseDiv = document.getElementById('rsvpResponse');

            // Validasi
            if (!nama || !jumlahTamu || !kehadiran) {
                showResponseMessage('❌ Harap isi semua field yang wajib diisi!', 'error');
                return;
            }

            if (nama.length < 2) {
                showResponseMessage('❌ Nama harus minimal 2 karakter!', 'error');
                return;
            }

            // Validasi jumlah tamu
            if (jumlahTamu < 1 || jumlahTamu > 10) {
                showResponseMessage('❌ Jumlah tamu harus antara 1-10!', 'error');
                return;
            }

            // Tampilkan loading
            const originalText = submitBtn.innerHTML;
            submitBtn.innerHTML = '🔄 Mengirim...';
            submitBtn.disabled = true;

            try {
                // Format data yang sederhana dan jelas - TANPA PESAN
                const formData = new URLSearchParams();
                formData.append('nama', nama);
                formData.append('email', email || 'Tidak diisi');
                formData.append('jumlahTamu', jumlahTamu);
                formData.append('kehadiran', kehadiran);

                console.log('Data yang dikirim:', {
                    nama: nama,
                    email: email || 'Tidak diisi',
                    jumlahTamu: jumlahTamu,
                    kehadiran: kehadiran
                });

                // Kirim ke Google Apps Script - PASTIKAN METHOD POST
                const response = await fetch(RSVP_SCRIPT_URL, {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/x-www-form-urlencoded; charset=UTF-8'
                    },
                    body: formData
                });

                console.log('Response status:', response.status);

                // Handle response
                let result;
                try {
                    result = await response.json();
                    console.log('Response JSON:', result);
                } catch (jsonError) {
                    const textResponse = await response.text();
                    console.log('Response TEXT:', textResponse);
                    throw new Error('Response bukan format JSON: ' + textResponse);
                }

                if (result.success) {
                    showResponseMessage(
                        '🎉 Terima kasih! Konfirmasi kehadiran Anda berhasil tercatat. ' +
                        `<br><strong>${result.data.nama}</strong> - ${result.data.jumlahTamu} tamu - ${result.data.kehadiran}` +
                        '<br>Kami tidak sabar bertemu dengan Anda! ❤️', 
                        'success'
                    );
                    resetRSVPForm();
                    
                    // Auto-hide pesan sukses setelah 8 detik
                    setTimeout(() => {
                        hideResponseMessage();
                    }, 8000);
                } else {
                    throw new Error(result.error || 'Terjadi kesalahan tidak diketahui');
                }

            } catch (error) {
                console.error('Error details:', error);
                showResponseMessage(
                    '❌ Maaf, terjadi kesalahan sistem. ' +
                    'Silakan coba lagi atau hubungi kami via WhatsApp: Huda 085910651074' +
                    '<br><small>Error: ' + error.message + '</small>', 
                    'error'
                );
            } finally {
                // Reset tombol
                submitBtn.innerHTML = '💌 Kirim Konfirmasi';
                submitBtn.disabled = false;
            }
        }

        function showResponseMessage(message, type) {
            const responseDiv = document.getElementById('rsvpResponse');
            if (responseDiv) {
                responseDiv.innerHTML = message;
                responseDiv.className = `response-message ${type}`;
                responseDiv.style.display = 'block';
                
                // Scroll ke response message
                responseDiv.scrollIntoView({ 
                    behavior: 'smooth',
                    block: 'center'
                });
            }
        }

        function hideResponseMessage() {
            const responseDiv = document.getElementById('rsvpResponse');
            if (responseDiv) {
                responseDiv.style.display = 'none';
            }
        }

        function resetRSVPForm() {
            document.getElementById('rsvpNama').value = '';
            document.getElementById('rsvpEmail').value = '';
            document.getElementById('rsvpJumlahTamu').value = '1';
            document.getElementById('rsvpKehadiran').value = '';
        }

        // ========== SISTEM KOMENTAR BUBBLE BESAR SCROLLABLE ==========
        function displayBubbleComments() {
            const bubbleCommentsDisplay = document.getElementById('bubbleCommentsDisplay');
            const commentsCount = document.getElementById('commentsCount');
            
            if (!bubbleCommentsDisplay || !commentsCount) return;
            
            // Ambil komentar dari localStorage atau gunakan contoh
            const comments = getComments();
            
            // Update jumlah komentar
            commentsCount.textContent = comments.length;
            
            if (comments.length === 0) {
                bubbleCommentsDisplay.innerHTML = `
                    <div class="empty-comments">
                        <div class="empty-comments-icon">💌</div>
                        <p>Belum ada ucapan dan doa.</p>
                        <p>Jadilah yang pertama memberikan doa restu!</p>
                    </div>
                `;
                return;
            }
            
            bubbleCommentsDisplay.innerHTML = '';
            
            // TAMPILKAN KOMENTAR DENGAN URUTAN: LAMA DI ATAS, BARU DI BAWAH
            comments.forEach((comment, index) => {
                const commentItem = document.createElement('div');
                commentItem.className = 'comment-item';
                commentItem.style.animationDelay = `${index * 0.1}s`;
                
                commentItem.innerHTML = `
                    <div class="comment-message">${comment.message}</div>
                    <div class="comment-footer">
                        <div class="comment-author">👤 ${comment.name}</div>
                        <div class="comment-date">📅 ${comment.date}</div>
                    </div>
                `;
                
                bubbleCommentsDisplay.appendChild(commentItem);
            });
            
            // SCROLL KE ATAS untuk menampilkan komentar lama terlebih dahulu
            bubbleCommentsDisplay.scrollTop = 0;
        }

        function submitBubbleComment() {
            const nameInput = document.getElementById('bubbleCommentName');
            const messageInput = document.getElementById('bubbleCommentMessage');
            
            if (!nameInput || !messageInput) return;
            
            const name = nameInput.value.trim();
            const message = messageInput.value.trim();
            
            if (!message) {
                alert('Silakan tulis ucapan dan doa terlebih dahulu.');
                return;
            }
            
            // Jika nama kosong, gunakan "Tamu Undangan"
            const guestName = name || 'Tamu Undangan';
            
            const newComment = {
                id: Date.now(),
                name: guestName,
                message: message,
                date: new Date().toLocaleDateString('id-ID', {
                    day: 'numeric',
                    month: 'short',
                    year: 'numeric'
                })
            };
            
            const comments = getComments();
            // TAMBAHKAN DI AKHIR ARRAY (bukan di awal) agar komentar terbaru muncul di bawah
            comments.push(newComment);
            saveComments(comments);
            
            // Reset form
            nameInput.value = '';
            messageInput.value = '';
            
            // Refresh tampilan
            displayBubbleComments();
            
            // Tampilkan notifikasi
            showBubbleCommentNotification();
            
            // Scroll ke bagian komentar
            setTimeout(() => {
                const bubbleSection = document.querySelector('.bubble-comments-section');
                if (bubbleSection) {
                    bubbleSection.scrollIntoView({ 
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            }, 500);
        }

        function showBubbleCommentNotification() {
            const notification = document.createElement('div');
            notification.innerHTML = `
                <div style="
                    position: fixed;
                    top: 20px;
                    right: 20px;
                    background: #8b7355;
                    color: white;
                    padding: 12px 20px;
                    border-radius: 8px;
                    z-index: 1000;
                    font-size: 14px;
                    box-shadow: 0 3px 10px rgba(0,0,0,0.2);
                ">
                    Terima kasih atas ucapan dan doanya!
                </div>
            `;
            
            document.body.appendChild(notification);
            
            setTimeout(() => {
                if (notification.parentNode) {
                    notification.parentNode.removeChild(notification);
                }
            }, 3000);
        }

        // Simpan komentar di localStorage
        function getComments() {
            try {
                const comments = localStorage.getItem('weddingGuestComments');
                return comments ? JSON.parse(comments) : sampleComments;
            } catch (error) {
                console.error('Error membaca komentar:', error);
                return sampleComments;
            }
        }
        
        function saveComments(comments) {
            try {
                localStorage.setItem('weddingGuestComments', JSON.stringify(comments));
            } catch (error) {
                console.error('Error menyimpan komentar:', error);
            }
        }

        // ========== FUNGSI UTAMA ==========
        function openInvitation() {
            console.log('Membuka undangan...');
            
            const loadingScreen = document.getElementById('loadingScreen');
            const mainContent = document.getElementById('mainContent');
            const musicControls = document.getElementById('musicControls');
            
            // Sembunyikan loading screen
            if (loadingScreen) {
                loadingScreen.style.display = 'none';
            }
            
            // Tampilkan konten utama
            if (mainContent) {
                mainContent.classList.remove('hidden');
            }
            
            // Tampilkan kontrol musik
            if (musicControls) {
                musicControls.classList.remove('hidden');
            }
            
            // Mulai musik
            setTimeout(() => {
                playWeddingMusic();
            }, 500);
            
            // Preload foto
            preloadPhoto();
            
            // Animasi header
            setTimeout(() => {
                animateHeaderElements();
            }, 300);
            
            // Setup scroll animation
            setTimeout(() => {
                setupScrollAnimation();
            }, 500);
            
            // Tampilkan komentar bubble
            setTimeout(() => {
                displayBubbleComments();
            }, 700);
            
            console.log('Undangan berhasil dibuka');
        }

        // ========== FUNGSI LAINNYA ==========
        function setupScrollAnimation() {
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('animate-in');
                    }
                });
            }, {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            });
            
            // Observer untuk elemen lainnya
            document.querySelectorAll('.section-title, .event-card, .gallery-item, .form-group, .submit-btn, .compact-account-card, .copy-btn, .quote-text, .tagline, .address-card, .big-bubble-container, .comment-item').forEach(el => {
                observer.observe(el);
            });
            
            document.querySelectorAll('.countdown-item').forEach((item, index) => {
                setTimeout(() => {
                    item.classList.add('animate-in');
                }, 1500 + (index * 200));
            });
        }
        
        function animateHeaderElements() {
            const headerElements = document.querySelectorAll('.header-section .main-title, .header-section .sub-title, .header-section .main-couple-names, .header-section .header-wedding-title, .header-section .header-date-text, .header-section .countdown-title');
            
            headerElements.forEach(el => {
                el.classList.add('animate-in');
            });
        }
        
        function preloadPhoto() {
            const headerBackground = document.getElementById('headerBackground');
            const photoLoading = document.getElementById('photoLoading');
            
            if (!headerBackground) return;
            
            headerBackground.style.background = 'linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), #fcf9f5';
            tryLoadPhoto(0);
        }
        
        function tryLoadPhoto(index) {
            if (index >= PHOTO_URLS.length) {
                showPhotoError();
                return;
            }
            
            const headerBackground = document.getElementById('headerBackground');
            const photoLoading = document.getElementById('photoLoading');
            const currentUrl = PHOTO_URLS[index];
            
            if (!headerBackground) return;
            
            const img = new Image();
            
            img.onload = function() {
                headerBackground.style.background = `linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), url('${currentUrl}')`;
                headerBackground.style.backgroundSize = 'cover';
                headerBackground.style.backgroundPosition = 'center';
                headerBackground.style.backgroundRepeat = 'no-repeat';
                
                if (photoLoading) {
                    photoLoading.style.display = 'none';
                }
            };
            
            img.onerror = function() {
                setTimeout(() => {
                    tryLoadPhoto(index + 1);
                }, 500);
            };
            
            setTimeout(() => {
                if (!img.complete) {
                    img.onerror();
                }
            }, 5000);
            
            img.src = currentUrl;
        }
        
        function showPhotoError() {
            const headerBackground = document.getElementById('headerBackground');
            const photoLoading = document.getElementById('photoLoading');
            
            if (!headerBackground) return;
            
            headerBackground.style.background = 'linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), #fcf9f5';
            
            if (photoLoading) {
                photoLoading.innerHTML = `
                    <div>📷</div>
                    <div>Foto tidak dapat dimuat</div>
                    <small>Menggunakan background default</small>
                `;
                photoLoading.style.color = '#b8a58d';
            }
        }
        
        function playWeddingMusic() {
            try {
                // Hentikan player lama jika ada
                if (musicPlayer) {
                    try {
                        musicPlayer.src = 'about:blank';
                        if (musicPlayer.parentNode) {
                            musicPlayer.parentNode.removeChild(musicPlayer);
                        }
                    } catch (e) {
                        console.log('Error membersihkan player lama:', e);
                    }
                }

                // Buat player baru
                musicPlayer = document.createElement('iframe');
                musicPlayer.id = 'youtubePlayer';
                musicPlayer.src = `https://www.youtube.com/embed/${YOUTUBE_VIDEO_ID}?autoplay=1&loop=1&playlist=${YOUTUBE_VIDEO_ID}&enablejsapi=1&rel=0&mute=0`;
                musicPlayer.width = '0';
                musicPlayer.height = '0';
                musicPlayer.style.display = 'none';
                musicPlayer.allow = 'autoplay; encrypted-media; accelerometer; gyroscope';
                musicPlayer.allowFullscreen = false;
                
                document.body.appendChild(musicPlayer);
                
                isMusicPlaying = true;
                updateMusicControls();
                
                console.log('Musik wedding dimulai');
                
            } catch (error) {
                console.error('Error memutar musik:', error);
            }
        }
        
        function stopWeddingMusic() {
            if (musicPlayer) {
                try {
                    musicPlayer.src = 'about:blank';
                    isMusicPlaying = false;
                    updateMusicControls();
                } catch (error) {
                    console.error('Error menghentikan musik:', error);
                }
            }
        }
        
        function toggleMusic() {
            if (isMusicPlaying) {
                stopWeddingMusic();
            } else {
                playWeddingMusic();
            }
        }
        
        function updateMusicControls() {
            const playPauseBtn = document.getElementById('playPauseBtn');
            if (playPauseBtn) {
                if (isMusicPlaying) {
                    playPauseBtn.innerHTML = '⏸️';
                    playPauseBtn.title = 'Pause Musik';
                } else {
                    playPauseBtn.innerHTML = '▶️';
                    playPauseBtn.title = 'Play Musik';
                }
            }
        }

        // ========== FUNGSI SALIN ==========
        function copyToClipboard(text, buttonElement = null) {
            if (navigator.clipboard && window.isSecureContext) {
                navigator.clipboard.writeText(text).then(() => {
                    showCopySuccess(buttonElement);
                }).catch(err => {
                    fallbackCopyTextToClipboard(text, buttonElement);
                });
            } else {
                fallbackCopyTextToClipboard(text, buttonElement);
            }
        }

        function fallbackCopyTextToClipboard(text, buttonElement = null) {
            const textArea = document.createElement("textarea");
            textArea.value = text;
            textArea.style.top = "0";
            textArea.style.left = "0";
            textArea.style.position = "fixed";
            textArea.style.opacity = "0";
            
            document.body.appendChild(textArea);
            textArea.focus();
            textArea.select();
            
            try {
                const successful = document.execCommand('copy');
                if (successful) {
                    showCopySuccess(buttonElement);
                } else {
                    showCopyError();
                }
            } catch (err) {
                showCopyError();
            }
            
            document.body.removeChild(textArea);
        }

        function copyAddressToClipboard(buttonElement) {
            const address = "Desy Irmaya\nNglegi No.011/003, Nglegi, Nglegi, Patuk, Gunungkidul";
            copyToClipboard(address, buttonElement);
        }

        function showCopySuccess(buttonElement = null) {
            if (buttonElement) {
                const originalText = buttonElement.innerHTML;
                buttonElement.innerHTML = '✅ Tersalin!';
                buttonElement.classList.add('copied');
                
                setTimeout(() => {
                    buttonElement.innerHTML = originalText;
                    buttonElement.classList.remove('copied');
                }, 2000);
            }
            
            const notification = document.getElementById('copyNotification');
            if (notification) {
                notification.classList.add('show');
                
                setTimeout(() => {
                    notification.classList.remove('show');
                }, 2000);
            }
        }

        function showCopyError() {
            alert('Gagal menyalin teks. Silahkan salin secara manual.');
        }
        
        // Countdown Timer
        function updateCountdown() {
            const now = new Date().getTime();
            const distance = WEDDING_DATE - now;
            
            if (distance < 0) {
                const daysEl = document.getElementById('days');
                const hoursEl = document.getElementById('hours');
                const minutesEl = document.getElementById('minutes');
                const secondsEl = document.getElementById('seconds');
                
                if (daysEl) daysEl.innerText = '00';
                if (hoursEl) hoursEl.innerText = '00';
                if (minutesEl) minutesEl.innerText = '00';
                if (secondsEl) secondsEl.innerText = '00';
                return;
            }
            
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
            
            const daysEl = document.getElementById('days');
            const hoursEl = document.getElementById('hours');
            const minutesEl = document.getElementById('minutes');
            const secondsEl = document.getElementById('seconds');
            
            if (daysEl) daysEl.innerText = days.toString().padStart(2, '0');
            if (hoursEl) hoursEl.innerText = hours.toString().padStart(2, '0');
            if (minutesEl) minutesEl.innerText = minutes.toString().padStart(2, '0');
            if (secondsEl) secondsEl.innerText = seconds.toString().padStart(2, '0');
        }
        
        // Event listeners
        document.addEventListener('DOMContentLoaded', function() {
            // Setup event listeners untuk tombol musik
            const playPauseBtn = document.getElementById('playPauseBtn');
            const stopBtn = document.getElementById('stopBtn');
            
            if (playPauseBtn) {
                playPauseBtn.addEventListener('click', toggleMusic);
            }
            
            if (stopBtn) {
                stopBtn.addEventListener('click', stopWeddingMusic);
            }
            
            // Mulai countdown
            updateCountdown();
            setInterval(updateCountdown, 1000);
            
            console.log('Undangan siap dibuka');
        });
    </script>
</body>
</html>
