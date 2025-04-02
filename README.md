<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Discover {{Country Name}}</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    
    <style>
        /* Loader Styles */
        .loader-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #1e3a8a; /* Dark Blue */
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
        }

        .wrapper {
            width: 200px;
            height: 60px;
            position: relative;
        }

        .circle {
            width: 20px;
            height: 20px;
            position: absolute;
            border-radius: 50%;
            background-color: #fff;
            left: 15%;
            transform-origin: 50%;
            animation: circle7124 .5s alternate infinite ease;
        }

        @keyframes circle7124 {
            0% { top: 60px; height: 5px; border-radius: 50px 50px 25px 25px; transform: scaleX(1.7); }
            40% { height: 20px; border-radius: 50%; transform: scaleX(1); }
            100% { top: 0%; }
        }

        .circle:nth-child(2) { left: 45%; animation-delay: .2s; }
        .circle:nth-child(3) { left: auto; right: 15%; animation-delay: .3s; }

        .shadow {
            width: 20px;
            height: 4px;
            border-radius: 50%;
            background-color: rgba(0, 0, 0, 0.9);
            position: absolute;
            top: 62px;
            transform-origin: 50%;
            z-index: -1;
            left: 15%;
            filter: blur(1px);
            animation: shadow046 .5s alternate infinite ease;
        }

        @keyframes shadow046 {
            0% { transform: scaleX(1.5); }
            40% { transform: scaleX(1); opacity: .7; }
            100% { transform: scaleX(.2); opacity: .4; }
        }

        .shadow:nth-child(4) { left: 45%; animation-delay: .2s; }
        .shadow:nth-child(5) { left: auto; right: 15%; animation-delay: .3s; }

        /* Hide main content initially */
        .main-content {
            display: none;
        }
    </style>
</head>
<body class="bg-gray-100">
    
    <!-- Loader -->
    <div class="loader-container" id="loader">
        <div class="wrapper">
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="shadow"></div>
            <div class="shadow"></div>
            <div class="shadow"></div>
        </div>
    </div>

    <!-- Main Website Content -->
    <div class="main-content" id="main-content">
        <!-- Navbar -->
        <nav class="bg-blue-600 p-4 text-white flex justify-between">
            <h1 class="text-2xl font-bold">Discover {{Country Name}}</h1>
            <ul class="flex space-x-4">
                <li><a href="#about" class="hover:underline">About</a></li>
                <li><a href="#culture" class="hover:underline">Culture</a></li>
                <li><a href="#attractions" class="hover:underline">Attractions</a></li>
                <li><a href="#contact" class="hover:underline">Contact</a></li>
            </ul>
        </nav>

        <!-- Hero Section -->
        <section class="relative h-screen bg-cover bg-center" style="background-image: url('https://source.unsplash.com/1600x900/?nature,landscape')">
            <div class="absolute inset-0 bg-black bg-opacity-50 flex flex-col justify-center items-center text-white">
                <h2 class="text-5xl font-bold">Welcome to {{Country Name}}</h2>
                <p class="text-xl mt-2">Explore the beauty, culture, and history of our nation.</p>
            </div>
        </section>

        <!-- Other sections (About, Culture, Attractions, Contact) -->

        <!-- Footer -->
        <footer class="bg-gray-800 text-white p-4 text-center">
            <p>&copy; 2025 Discover {{Country Name}}. All rights reserved.</p>
        </footer>
    </div>

    <script>
        // Hide loader and show main content when page is fully loaded
        window.onload = function() {
            document.getElementById("loader").style.display = "none";
            document.getElementById("main-content").style.display = "block";
        };
    </script>
</body>
</html>
