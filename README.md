<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abylaikhan | AI/ML Developer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        zinc: { 950: '#09090b' }
                    }
                }
            }
        }
    </script>
</head>
<body class="bg-zinc-950 text-zinc-200 antialiased selection:bg-indigo-500/30">

    <!-- Header -->
    <header class="fixed top-0 w-full z-50 backdrop-blur-md bg-zinc-950/80 border-b border-zinc-800">
        <nav class="max-w-5xl mx-auto px-6 py-4 flex items-center justify-between">
            <a href="#" class="text-lg font-semibold text-white">Abylaikhan</a>
            <div class="flex items-center gap-6 text-sm">
                <a href="#about" class="hover:text-white transition-colors">About</a>
                <a href="#projects" class="hover:text-white transition-colors">Projects</a>
                <a href="#contact" class="hover:text-white transition-colors">Contact</a>
                <a href="#" class="px-3 py-1 rounded-full border border-zinc-700 hover:bg-zinc-800 transition-all">CV</a>
            </div>
        </nav>
    </header>

    <main class="max-w-5xl mx-auto px-6 pt-32 pb-20">
        
        <!-- Hero Section -->
        <section id="about" class="mb-24">
            <h1 class="text-5xl font-bold text-white mb-6 tracking-tight">Hi, I'm Abylaikhan.<br><span class="text-zinc-400">Building Intelligent Systems with Python & ML.</span></h1>
            <p class="text-xl text-zinc-400 max-w-2xl mb-8 leading-relaxed">
                I engineer high-performance solutions at the intersection of AI, Computer Vision, and Data Retrieval. Focused on scalable architecture and production-grade intelligent systems.
            </p>
            <div class="flex gap-4">
                <a href="#projects" class="px-6 py-3 bg-indigo-600 text-white rounded-lg font-medium hover:bg-indigo-500 transition-all">View Projects</a>
                <a href="#" class="px-6 py-3 border border-zinc-700 text-white rounded-lg font-medium hover:bg-zinc-800 transition-all">Read CV</a>
            </div>
        </section>

        <!-- Projects -->
        <section id="projects" class="mb-24">
            <h2 class="text-2xl font-semibold text-white mb-8">Featured Projects</h2>
            <div class="grid md:grid-cols-2 gap-6">
                <!-- Project 1 -->
                <div class="border border-zinc-800 rounded-xl p-6 hover:border-zinc-700 hover:bg-zinc-900 transition-all group">
                    <h3 class="text-lg font-semibold text-white mb-2">Semantic & Hybrid Search Engine</h3>
                    <p class="text-zinc-400 text-sm mb-4">Python-based engine combining vector embeddings and BM25. Implemented Float32 to Int8 quantization reducing memory by 75%, with NumPy optimizations for <15ms latency. RAG-pipeline integrated with local Gemma via Ollama.</p>
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span class="px-2 py-1 bg-zinc-900 rounded text-xs text-zinc-300">Python</span>
                        <span class="px-2 py-1 bg-zinc-900 rounded text-xs text-zinc-300">NumPy</span>
                        <span class="px-2 py-1 bg-zinc-900 rounded text-xs text-zinc-300">RAG</span>
                    </div>
                    <a href="#" class="text-indigo-400 text-sm hover:text-indigo-300">GitHub →</a>
                </div>
                <!-- Project 2 -->
                <div class="border border-zinc-800 rounded-xl p-6 hover:border-zinc-700 hover:bg-zinc-900 transition-all group">
                    <h3 class="text-lg font-semibold text-white mb-2">GestureControl Interface</h3>
                    <p class="text-zinc-400 text-sm mb-4">Touchless OS control using computer vision. Built with Python and MediaPipe Hand Tracking. Custom geometric logic enables precise real-time gesture recognition (clicks, scrolls, volume control).</p>
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span class="px-2 py-1 bg-zinc-900 rounded text-xs text-zinc-300">Python</span>
                        <span class="px-2 py-1 bg-zinc-900 rounded text-xs text-zinc-300">MediaPipe</span>
                    </div>
                    <a href="#" class="text-indigo-400 text-sm hover:text-indigo-300">GitHub →</a>
                </div>
                <!-- Project 3 -->
                <div class="border border-zinc-800 rounded-xl p-6 hover:border-zinc-700 hover:bg-zinc-900 transition-all group">
                    <h3 class="text-lg font-semibold text-white mb-2">AI Content Summary Bot</h3>
                    <p class="text-zinc-400 text-sm mb-4">Telegram bot using aiogram 3.x for automated summarization and sentiment analysis of text/video content. Asynchronous architecture integrated with LLMs via OpenRouter/OpenAI API.</p>
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span class="px-2 py-1 bg-zinc-900 rounded text-xs text-zinc-300">Python</span>
                        <span class="px-2 py-1 bg-zinc-900 rounded text-xs text-zinc-300">aiogram</span>
                        <span class="px-2 py-1 bg-zinc-900 rounded text-xs text-zinc-300">OpenAI API</span>
                    </div>
                    <a href="#" class="text-indigo-400 text-sm hover:text-indigo-300">GitHub →</a>
                </div>
            </div>
        </section>

        <!-- Skills -->
        <section id="skills" class="mb-24">
            <h2 class="text-2xl font-semibold text-white mb-8">Technical Stack</h2>
            <div class="space-y-6">
                <div>
                    <h4 class="text-zinc-500 text-sm uppercase tracking-wider mb-3">Languages</h4>
                    <div class="flex flex-wrap gap-2"><span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">Python (Core, OOP)</span></div>
                </div>
                <div>
                    <h4 class="text-zinc-500 text-sm uppercase tracking-wider mb-3">AI/ML & Data</h4>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">NumPy</span>
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">MediaPipe</span>
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">RAG</span>
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">Vector Embeddings</span>
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">Prompt Engineering</span>
                    </div>
                </div>
                <div>
                    <h4 class="text-zinc-500 text-sm uppercase tracking-wider mb-3">Backend & Tools</h4>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">SQLite</span>
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">Git</span>
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">API Integration</span>
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">aiogram</span>
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">dotenv</span>
                        <span class="px-3 py-1 bg-zinc-900 rounded-md text-sm">venv</span>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer id="contact" class="border-t border-zinc-800 py-12">
        <div class="max-w-5xl mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-6">
            <p class="text-zinc-500 text-sm">© 2026 Abylaikhan. All rights reserved.</p>
            <div class="flex gap-6 text-sm text-zinc-400">
                <a href="#" class="hover:text-white">Email</a>
                <a href="#" class="hover:text-white">GitHub</a>
                <a href="#" class="hover:text-white">LinkedIn</a>
                <a href="#" class="hover:text-white">Telegram</a>
            </div>
        </div>
    </footer>

</body>
</html>
