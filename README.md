# matrix-website
a simple matrix-inspired website project
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to the World - Matrix Style</title>
    <style>
        /* Reset default margins and padding */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Courier New', Courier, monospace;
        }

        /* Full screen black background */
        body {
            background-color: black;
            color: #00FF00;  /* Green text, like Matrix code */
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            text-align: center;
        }

        /* Welcome message styling */
        .welcome-message {
            font-size: 40px;
            color: white;
            text-shadow: 0 0 15px #00FF00, 0 0 30px #00FF00;
            margin-bottom: 20px;
            z-index: 2;
        }

        .sub-message {
            font-size: 20px;
            color: white;
            text-shadow: 0 0 15px #00FF00, 0 0 30px #00FF00;
            margin-top: 10px;
            z-index: 2;
        }

        /* Matrix Effect */
        .matrix {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;  /* Make the effect not interfere with clicking or interaction */
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .matrix-line {
            font-size: 30px;
            letter-spacing: 2px;
            color: #00FF00;
            position: absolute;
            top: -100%;
            animation: drop 2s infinite linear;
            opacity: 0;
        }

        /* Keyframes for the matrix effect - falling code animation */
        @keyframes drop {
            0% {
                top: -100%;
                opacity: 0;
            }
            50% {
                top: 50%;
                opacity: 1;
            }
            100% {
                top: 100%;
                opacity: 0;
            }
        }

        /* Make the lines appear randomly in time and position */
        .matrix-line:nth-child(1) { animation-duration: 1.5s; animation-delay: 0s; }
        .matrix-line:nth-child(2) { animation-duration: 1.7s; animation-delay: 0.2s; }
        .matrix-line:nth-child(3) { animation-duration: 1.9s; animation-delay: 0.4s; }
        .matrix-line:nth-child(4) { animation-duration: 2.1s; animation-delay: 0.6s; }
        .matrix-line:nth-child(5) { animation-duration: 1.6s; animation-delay: 0.8s; }
        .matrix-line:nth-child(6) { animation-duration: 2.3s; animation-delay: 1s; }
        .matrix-line:nth-child(7) { animation-duration: 1.8s; animation-delay: 1.2s; }
        .matrix-line:nth-child(8) { animation-duration: 2.0s; animation-delay: 1.4s; }
    </style>
</head>
<body>
    <!-- Welcome Message -->
    <div class="welcome-message">
        <h1>Welcome to the World</h1>
        <p class="sub-message">A jaw-dropping world of possibilities</p>
    </div>

    <!-- Matrix Animation -->
    <div class="matrix">
        <div class="matrix-line">1</div>
        <div class="matrix-line">0</div>
        <div class="matrix-line">1</div>
        <div class="matrix-line">1</div>
        <div class="matrix-line">0</div>
        <div class="matrix-line">1</div>
        <div class="matrix-line">1</div>
        <div class="matrix-line">0</div>
    </div>
</body>
</html>
