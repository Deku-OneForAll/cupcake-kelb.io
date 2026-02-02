# cupcake-kelb.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/feather-icons"></script>
    <script src="https://cdn.jsdelivr.net/npm/feather-icons/dist/feather.min.js"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#e11d48',
                        secondary: '#fb7185',
                    }
                }
            }
        }
    </script>
</head>
<body class="bg-gradient-to-br from-rose-100 via-pink-200 to-rose-300 min-h-screen overflow-hidden relative font-sans">

    <!-- Floating Hearts Background -->
    <div id="hearts-container" class="absolute inset-0 pointer-events-none overflow-hidden"></div>

    <!-- Main Content -->
    <div class="relative z-10 min-h-screen flex items-center justify-center p-4">
        <div class="bg-white/80 backdrop-blur-lg rounded-3xl shadow-2xl p-8 md:p-12 max-w-lg w-full border border-white/50 transform hover:scale-105 transition-transform duration-300">
            
            <!-- Header Icon -->
            <div class="flex justify-center mb-6">
                <div class="bg-primary/10 p-4 rounded-full animate-pulse">
                    <i data-feather="heart" class="w-12 h-12 text-primary fill-current"></i>
                </div>
            </div>

            <!-- Question -->
            <h1 class="text-3xl md:text-4xl font-bold text-center text-gray-800 mb-2 leading-tight">
                Would you be my <span class="text-primary">Valentine</span> forever?
            </h1>
            
            <p class="text-center text-gray-600 mb-8 italic">
                khmis f diwan (ila g3adt 3a9el)
            </p>

            <!-- Buttons Container -->
            <div class="relative h-32 flex items-center justify-center gap-6">
                <!-- Yes Button -->
                <button id="yes-btn" class="bg-primary hover:bg-rose-600 text-white font-bold py-4 px-8 rounded-full shadow-lg transform transition-all duration-200 hover:scale-110 hover:shadow-rose-500/50 flex items-center gap-2 group">
                    <span>Yes</span>
                    <i data-feather="check" class="w-5 h-5 group-hover:animate-bounce"></i>
                </button>

                <!-- No Button (The Elusive One) -->
                <button id="no-btn" class="bg-gray-400 hover:bg-gray-500 text-white font-bold py-4 px-8 rounded-full shadow-lg transition-all duration-150 absolute">
                    <span>No</span>
                </button>
            </div>

            <!-- Cute Footer -->
            <div class="mt-8 text-center text-sm text-gray-500 flex items-center justify-center gap-2">
                <i data-feather="lock" class="w-4 h-4"></i>
                <span>Secure connection to my heart</span>
            </div>
        </div>
    </div>

    <!-- Success Overlay (Hidden by default) -->
    <div id="success-overlay" class="fixed inset-0 bg-black z-50 hidden flex-col items-center justify-center">
        <div class="absolute inset-0 bg-gradient-to-t from-rose-900/80 to-black/60"></div>
        
        <div class="relative z-10 text-center p-4 max-w-4xl w-full">
            <h2 class="text-4xl md:text-6xl font-bold text-white mb-6 animate-bounce">
                Thank You! <span class="text-rose-400">❤️</span>
            </h2>
            
            <div class="relative w-full max-w-2xl mx-auto aspect-video rounded-2xl overflow-hidden shadow-2xl border-4 border-rose-400/50">
                <img 
                    src="https://media.giphy.com/media/75ZaxapnyMp2w/giphy.gif" 
                    alt="Celebration" 
                    class="w-full h-full object-cover"
                    id="success-gif"
                >
            </div>
            
            <p class="text-rose-200 mt-6 text-xl md:text-2xl font-light">
                Cupcake You are the luckiest person alive!
            </p>
            
            <button onclick="location.reload()" class="mt-8 bg-white/10 hover:bg-white/20 text-white border border-white/30 py-3 px-6 rounded-full transition-all flex items-center gap-2 mx-auto">
                <i data-feather="refresh-cw" class="w-4 h-4"></i>
                <span>Play Again</span>
            </button>
        </div>
    </div>

    <script src="script.js"></script>
    <script>feather.replace();</script>
</body>
</html>
