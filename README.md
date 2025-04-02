/* Loading Animation */
        .wrapper {
            width: 200px;
            height: 60px;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 1000;
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
            0% {
                top: 60px;
                height: 5px;
                border-radius: 50px 50px 25px 25px;
                transform: scaleX(1.7);
            }
            40% {
                height: 20px;
                border-radius: 50%;
                transform: scaleX(1);
            }
            100% {
                top: 0%;
            }
        }

        .circle:nth-child(2) { left: 45%; animation-delay: .2s; }
        .circle:nth-child(3) { left: auto; right: 15%; animation-delay: .3s; }

        .shadow {
            width: 20px;
            height: 4px;
            border-radius: 50%;
            background-color: rgba(0,0,0,0.9);
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

        #content { display: none; }
    </style>
</head>
<body class="bg-gray-100">
    <!-- Loading Screen -->
    <div id="loading">
        <div class="wrapper">
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="shadow"></div>
            <div class="shadow"></div>
            <div class="shadow"></div>
        </div>
    </div>

    <!-- Main Content -->
    <div id="content">
        <!-- Navbar -->
        <nav class="bg-blue-600 p-4 text-white flex justify-between">
            <h1 class="text-2xl font-bold">Discover [Country Name]</h1>
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
                <h2 class="text-5xl font-bold">Welcome to [Country Name]</h2>
                <p class="text-xl mt-2">Explore the beauty, culture, and history of our nation.</p>
            </div>
        </section>
        
        <!-- About Section -->
        <section id="about" class="p-8 text-center">
            <h2 class="text-3xl font-bold">About [Country Name]</h2>
            <p class="mt-4 text-gray-700">[Add information about the country’s history, geography, and significance]</p>
        </section>
        
        <!-- Culture Section -->
        <section id="culture" class="bg-gray-200 p-8 text-center">
            <h2 class="text-3xl font-bold">Culture & Traditions</h2>
            <p class="mt-4 text-gray-700">[Highlight traditions, festivals, food, and more]</p>
        </section>
        
        <!-- Attractions Section -->
        <section id="attractions" class="p-8 text-center">
            <h2 class="text-3xl font-bold">Top Attractions</h2>
            <p class="mt-4 text-gray-700">[Describe famous places to visit]</p>
        </section>
        
        <!-- Contact Section -->
        <section id="contact" class="bg-blue-600 p-8 text-white text-center">
            <h2 class="text-3xl font-bold">Contact Us</h2>
            <p class="mt-4">Get in touch for more information.</p>
        </section>
        
        <!-- Footer -->
        <footer class="bg-gray-800 text-white p-4 text-center">
            <p>&copy; 2025 Discover [Country Name]. All rights reserved.</p>
        </footer>
    </div>
    
    <script>
        setTimeout(() => {
            document.getElementById('loading').style.display = 'none';
            document.getElementById('content').style.display = 'block';
        }, 5000);
    </script>
</body>
</html>
