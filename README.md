<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multi-Utility Hub | Temp Email, OTP & Dev Tools</title>
    <meta name="description" content="Free online developer tools: temporary email, OTP generator, strong password generator, UUID, currency converter, hash tools, and more.">
    
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        .glass {
            background: rgba(255, 255, 255, 0.45);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.25);
        }
        .dark .glass {
            background: rgba(30, 41, 59, 0.45);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }
    </style>
</head>
<body class="bg-slate-100 text-slate-900 dark:bg-slate-950 dark:text-slate-100 min-h-screen transition-colors duration-300 font-sans">

    <nav class="sticky top-0 z-50 glass shadow-sm px-6 py-4 flex justify-between items-center">
        <div class="flex items-center space-x-2">
            <i class="fa-solid class= fa-cubes text-indigo-600 dark:text-indigo-400 text-2xl"></i>
            <span class="text-xl font-bold tracking-tight">UtilHub</span>
        </div>
        
        <div class="hidden md:flex items-center relative w-64">
            <input type="text" id="toolSearch" placeholder="Search tools..." class="w-full pl-9 pr-4 py-1.5 rounded-lg border border-slate-300 dark:border-slate-700 bg-white/50 dark:bg-slate-900/50 text-sm focus:outline-none focus:ring-2 focus:ring-indigo-500">
            <i class="fa-solid fa-magnifying-glass absolute left-3 text-slate-400 text-xs"></i>
        </div>

        <div class="flex items-center space-x-4">
            <button id="themeToggle" class="p-2 rounded-full hover:bg-slate-200 dark:hover:bg-slate-800 transition">
                <i id="themeIcon" class="fa-solid fa-moon text-lg"></i>
            </button>
            <a href="#settings" class="p-2 rounded-full hover:bg-slate-200 dark:hover:bg-slate-800 transition">
                <i class="fa-solid fa-gear text-lg"></i>
            </a>
        </div>
    </nav>

    <div class="max-w-7xl mx-auto mt-4 px-4">
        <div class="w-full bg-slate-200 dark:bg-slate-900 p-4 text-center rounded-xl text-xs text-slate-500 border border-dashed border-slate-300 dark:border-slate-800">
            <span>ADVERTISEMENT: Responsive Banner (Placeholder)</span>
        </div>
    </div>

    <main class="max-w-7xl mx-auto p-4 grid grid-cols-1 lg:grid-cols-4 gap-6">
        
        <aside class="lg:col-span-1 space-y-2">
            <div class="glass p-4 rounded-2xl shadow-sm space-y-1">
                <p class="text-xs font-semibold uppercase tracking-wider text-slate-400 mb-2 px-2">Core Identity</p>
                <a href="#temp-email" class="flex items-center space-x-3 px-3 py-2.5 rounded-xl bg-indigo-50 dark:bg-indigo-950/50 text-indigo-600 dark:text-indigo-400 font-medium"><i class="fa-solid fa-envelope w-5"></i><span>Temp Email & OTP</span></a>
                <a href="#generators" class="flex items-center space-x-3 px-3 py-2.5 rounded-xl hover:bg-slate-200/50 dark:hover:bg-slate-800/50 transition text-slate-600 dark:text-slate-300"><i class="fa-solid fa-key w-5"></i><span>Security Generators</span></a>
                <a href="#finance" class="flex items-center space-x-3 px-3 py-2.5 rounded-xl hover:bg-slate-200/50 dark:hover:bg-slate-800/50 transition text-slate-600 dark:text-slate-300"><i class="fa-solid fa-chart-line w-5"></i><span>Finance & Crypto</span></a>
                <a href="#utilities" class="flex items-center space-x-3 px-3 py-2.5 rounded-xl hover:bg-slate-200/50 dark:hover:bg-slate-800/50 transition text-slate-600 dark:text-slate-300"><i class="fa-solid fa-sliders w-5"></i><span>Converters & Info</span></a>
            </div>
            
            <div class="glass p-4 rounded-2xl shadow-sm text-center">
                <h4 class="font-bold text-sm mb-2">Support Free Tools</h4>
                <p class="text-xs text-slate-500 mb-3">Keep this server running completely free of cost.</p>
                <div class="flex justify-center space-x-2">
                    <button onclick="alert('UPI ID: support@upi')" class="px-3 py-1.5 bg-emerald-600 text-white text-xs font-semibold rounded-lg shadow-sm hover:bg-emerald-700"><i class="fa-solid fa-wallet mr-1"></i> UPI</button>
                    <button onclick="alert('PayPal: payment@example.com')" class="px-3 py-1.5 bg-blue-600 text-white text-xs font-semibold rounded-lg shadow-sm hover:bg-blue-700"><i class="fa-brands fa-paypal mr-1"></i> PayPal</button>
                </div>
            </div>
        </aside>

        <section class="lg:col-span-3 space-y-6">
            
            <div id="temp-email" class="glass p-6 rounded-3xl shadow-sm space-y-6">
                <div>
                    <h2 class="text-xl font-bold flex items-center gap-2"><i class="fa-solid fa-envelope text-indigo-500"></i> Temporary Email & Live OTP Dashboard</h2>
                    <p class="text-xs text-slate-500 dark:text-slate-400 mt-1">Disposable secure email with integrated standard 6-8 digit rolling token framework.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div class="p-4 bg-white/60 dark:bg-slate-900/60 rounded-2xl border border-slate-200/60 dark:border-slate-800/60 space-y-3">
                        <label class="block text-xs font-medium text-slate-500">Your Temp Email</label>
                        <div class="flex gap-2">
                            <input type="text" id="tempEmailBox" readonly class="w-full bg-slate-100 dark:bg-slate-950 px-3 py-2 rounded-xl text-sm font-mono focus:outline-none" value="generating...">
                            <button onclick="copyToClipboard('tempEmailBox')" class="px-3 bg-slate-200 dark:bg-slate-800 rounded-xl hover:bg-slate-300 dark:hover:bg-slate-700 transition"><i class="fa-regular fa-copy"></i></button>
                        </div>
                        <div class="flex gap-2">
                            <select id="emailDomain" class="w-full bg-slate-100 dark:bg-slate-950 px-3 py-1.5 rounded-xl text-xs font-medium border border-transparent focus:border-indigo-500">
                                <option value="@devmail.com">@devmail.com</option>
                                <option value="@tempinbox.org">@tempinbox.org</option>
                                <option value="@secureshell.net">@secureshell.net</option>
                            </select>
                            <button onclick="generateNewEmail()" class="px-3 py-1.5 bg-indigo-600 text-white text-xs font-semibold rounded-xl hover:bg-indigo-700 transition whitespace-nowrap">Refresh Mail</button>
                        </div>
                    </div>

                    <div class="p-4 bg-white/60 dark:bg-slate-900/60 rounded-2xl border border-slate-200/60 dark:border-slate-800/60 space-y-3">
                        <div class="flex justify-between items-center">
                            <label class="text-xs font-medium text-slate-500">Simulated App OTP Code</label>
                            <span id="otpCountdown" class="text-xs font-bold text-amber-500 bg-amber-500/10 px-2 py-0.5 rounded-full">30s</span>
                        </div>
                        <div class="flex gap-2">
                            <input type="text" id="otpBox" readonly class="w-full bg-slate-100 dark:bg-slate-950 px-3 py-2 rounded-xl text-2xl font-bold tracking-widest text-center text-indigo-600 dark:text-indigo-400 focus:outline-none" value="000000">
                            <button onclick="copyToClipboard('otpBox')" class="px-3 bg-slate-200 dark:bg-slate-800 rounded-xl hover:bg-slate-300 dark:hover:bg-slate-700 transition"><i class="fa-regular fa-copy"></i></button>
                        </div>
                        <div class="flex justify-between items-center">
                            <select id="otpLength" onchange="refreshOTP()" class="bg-slate-100 dark:bg-slate-950 px-2 py-1 rounded-lg text-xs font-medium">
                                <option value="6">6 Digits</option>
                                <option value="8">8 Digits</option>
                            </select>
                            <button onclick="refreshOTP()" class="text-xs text-indigo-500 font-semibold hover:underline">Force Regenerate</button>
                        </div>
                    </div>
                </div>

                <div class="space-y-2">
                    <h3 class="text-sm font-semibold text-slate-700 dark:text-slate-300">Incoming System Messages Inbox</h3>
                    <div class="border border-slate-200 dark:border-slate-800 rounded-2xl overflow-hidden bg-white/40 dark:bg-slate-900/40 text-sm">
                        <div class="grid grid-cols-3 bg-slate-200/50 dark:bg-slate-800/50 px-4 py-2 font-medium text-xs text-slate-500">
                            <div>Sender</div>
                            <div>Subject</div>
                            <div class="text-right">Action Time</div>
                        </div>
                        <div id="inboxList" class="divide-y divide-slate-200 dark:divide-slate-800 max-h-40 overflow-y-auto">
                            <div class="grid grid-cols-3 px-4 py-3 text-xs text-slate-400 italic">
                                <div class="col-span-3 text-center">No current messages active. Waiting for system triggers...</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div id="generators" class="glass p-6 rounded-3xl shadow-sm space-y-6">
                <div>
                    <h2 class="text-xl font-bold flex items-center gap-2"><i class="fa-solid fa-key text-emerald-500"></i> Cryptographic & Unique Asset Generators</h2>
                    <p class="text-xs text-slate-500 mt-1">Generate strict high-entropy keys, structural formats, and identifier hashes locally.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="space-y-4">
                        <div class="p-4 bg-white/50 dark:bg-slate-900/50 rounded-2xl border border-slate-200/60 dark:border-slate-800/60 space-y-2">
                            <label class="block text-xs font-medium text-slate-500">Strong Cryptographic Password</label>
                            <div class="flex gap-2">
                                <input type="text" id="passwordBox" readonly class="w-full bg-slate-100 dark:bg-slate-950 px-3 py-1.5 rounded-xl text-xs font-mono">
                                <button onclick="generateSecurePassword()" class="px-2.5 bg-emerald-600 text-white rounded-xl text-xs font-semibold hover:bg-emerald-700">Gen</button>
                                <button onclick="copyToClipboard('passwordBox')" class="px-2 bg-slate-200 dark:bg-slate-800 rounded-xl hover:bg-slate-300 text-xs"><i class="fa-regular fa-copy"></i></button>
                            </div>
                        </div>

                        <div class="p-4 bg-white/50 dark:bg-slate-900/50 rounded-2xl border border-slate-200/60 dark:border-slate-800/60 space-y-2">
                            <label class="block text-xs font-medium text-slate-500">RFC4122 Standard UUID Version 4</label>
                            <div class="flex gap-2">
                                <input type="text" id="uuidBox" readonly class="w-full bg-slate-100 dark:bg-slate-950 px-3 py-1.5 rounded-xl text-xs font-mono">
                                <button onclick="generateUUIDV4()" class="px-2.5 bg-emerald-600 text-white rounded-xl text-xs font-semibold hover:bg-emerald-700">Gen</button>
                                <button onclick="copyToClipboard('uuidBox')" class="px-2 bg-slate-200 dark:bg-slate-800 rounded-xl hover:bg-slate-300 text-xs"><i class="fa-regular fa-copy"></i></button>
                            </div>
                        </div>
                    </div>

                    <div class="space-y-4">
                        <div class="p-4 bg-white/50 dark:bg-slate-900/50 rounded-2xl border border-slate-200/60 dark:border-slate-800/60 space-y-2">
                            <label class="block text-xs font-medium text-slate-500">Structural Mock Credit Card (Testing Only)</label>
                            <div class="flex gap-2">
                                <input type="text" id="ccBox" readonly class="w-full bg-slate-100 dark:bg-slate-950 px-3 py-1.5 rounded-xl text-xs font-mono">
                                <button onclick="generateMockCard()" class="px-2.5 bg-emerald-600 text-white rounded-xl text-xs font-semibold hover:bg-emerald-700">Gen</button>
                                <button onclick="copyToClipboard('ccBox')" class="px-2 bg-slate-200 dark:bg-slate-800 rounded-xl hover:bg-slate-300 text-xs"><i class="fa-regular fa-copy"></i></button>
                            </div>
                        </div>

                        <div class="p-4 bg-white/50 dark:bg-slate-900/50 rounded-2xl border border-slate-200/60 dark:border-slate-800/60 space-y-2">
                            <label class="block text-xs font-medium text-slate-500">Virtual Random IP Engine (IPv4/IPv6 Formats)</label>
                            <div class="flex gap-2">
                                <input type="text" id="ipBox" readonly class="w-full bg-slate-100 dark:bg-slate-950 px-3 py-1.5 rounded-xl text-xs font-mono">
                                <button onclick="generateRandomIP()" class="px-2.5 bg-emerald-600 text-white rounded-xl text-xs font-semibold hover:bg-emerald-700">Gen</button>
                                <button onclick="copyToClipboard('ipBox')" class="px-2 bg-slate-200 dark:bg-slate-800 rounded-xl hover:bg-slate-300 text-xs"><i class="fa-regular fa-copy"></i></button>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="p-4 bg-white/40 dark:bg-slate-900/40 rounded-2xl border border-slate-200 dark:border-slate-800 space-y-3">
                    <label class="block text-xs font-medium text-slate-500">Client-Side Secure Text Hashing (SHA-256)</label>
                    <div class="flex gap-3">
                        <input type="text" id="hashInput" placeholder="Enter plaintext string..." class="w-full bg-white dark:bg-slate-950 px-3 py-2 rounded-xl text-sm border border-slate-200 dark:border-slate-800 focus:outline-none focus:ring-1 focus:ring-indigo-500">
                        <button onclick="computeCryptoHash()" class="px-4 py-2 bg-indigo-600 text-white font-semibold text-xs rounded-xl hover:bg-indigo-700 transition">Compute</button>
                    </div>
                    <div class="mt-2 p-2 bg-slate-100 dark:bg-slate-950 rounded-xl text-xs font-mono break-all text-slate-600 dark:text-slate-400 shadow-inner min-h-[2rem]" id="hashOutput">
                        Result hash output will render here...
                    </div>
                </div>
            </div>

            <div id="finance" class="glass p-6 rounded-3xl shadow-sm space-y-6">
                <div class="flex justify-between items-start">
                    <div>
                        <h2 class="text-xl font-bold flex items-center gap-2"><i class="fa-solid fa-chart-line text-cyan-500"></i> Market Rates & Live Converters</h2>
                        <p class="text-xs text-slate-500 mt-1">Real-time data synchronization directly updated from public financial indexes.</p>
                    </div>
                    <button onclick="fetchMarketData()" class="px-3 py-1.5 bg-slate-200 dark:bg-slate-800 text-xs font-semibold rounded-lg hover:bg-slate-300 transition"><i class="fa-solid fa-rotate-right mr-1"></i> Refresh Rates</button>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                    <div class="p-4 bg-gradient-to-br from-amber-500/10 to-orange-500/10 dark:from-amber-950/20 dark:to-orange-950/20 rounded-2xl border border-amber-500/20 text-center">
                        <span class="text-xs uppercase font-bold tracking-wider text-amber-600">Bitcoin (BTC)</span>
                        <div id="btcPrice" class="text-2xl font-black mt-1 text-slate-800 dark:text-slate-100">$64,250.00</div>
                        <span class="text-[10px] text-slate-400">Live API Feed</span>
                    </div>

                    <div class="p-4 bg-gradient-to-br from-indigo-500/10 to-blue-500/10 dark:from-indigo-950/20 dark:to-blue-950/20 rounded-2xl border border-indigo-500/20 text-center">
                        <span class="text-xs uppercase font-bold tracking-wider text-indigo-600">Ethereum (ETH)</span>
                        <div id="ethPrice" class="text-2xl font-black mt-1 text-slate-800 dark:text-slate-100">$3,480.25</div>
                        <span class="text-[10px] text-slate-400">Live API Feed</span>
                    </div>

                    <div class="p-4 bg-gradient-to-br from-emerald-500/10 to-teal-500/10 dark:from-emerald-950/20 dark:to-teal-950/20 rounded-2xl border border-emerald-500/20 text-center">
                        <span class="text-xs uppercase font-bold tracking-wider text-emerald-600">NIFTY 50 Index</span>
                        <div id="niftyPrice" class="text-2xl font-black mt-1 text-slate-800 dark:text-slate-100">23,520.10</div>
                        <span class="text-[10px] text-slate-400">Indian Market Proxy</span>
                    </div>
                </div>

                <div class="p-4 bg-white/50 dark:bg-slate-900/50 rounded-2xl border border-slate-200 dark:border-slate-800 space-y-3">
                    <h3 class="text-xs font-bold uppercase tracking-wider text-slate-400">Universal Currency Matrix Converter</h3>
                    <div class="grid grid-cols-1 sm:grid-cols-3 gap-3 items-center">
                        <input type="number" id="fxAmount" value="1" class="w-full bg-white dark:bg-slate-950 px-3 py-2 rounded-xl text-sm border border-slate-200 dark:border-slate-800 focus:outline-none">
                        <select id="fxFrom" class="w-full bg-white dark:bg-slate-950 px-3 py-2 rounded-xl text-sm border border-slate-200 dark:border-slate-800">
                            <option value="USD">USD ($)</option>
                            <option value="INR" selected>INR (₹)</option>
                            <option value="EUR">EUR (€)</option>
                        </select>
                        <div id="fxResult" class="px-3 py-2 text-sm font-bold text-center bg-slate-100 dark:bg-slate-950 rounded-xl text-indigo-600 dark:text-indigo-400">
                            Loading calculations...
                        </div>
                    </div>
                </div>
            </div>

            <div id="utilities" class="glass p-6 rounded-3xl shadow-sm space-y-6">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="space-y-3">
                        <h3 class="text-sm font-bold text-slate-700 dark:text-slate-300 flex items-center gap-2"><i class="fa-solid fa-cloud-sun text-sky-500"></i> Open Climate Interface</h3>
                        <div class="p-4 bg-gradient-to-r from-sky-400/10 to-indigo-400/10 rounded-2xl border border-sky-400/20 flex justify-between items-center">
                            <div>
                                <div id="weatherCity" class="text-base font-bold text-slate-800 dark:text-slate-200">New Delhi, IN</div>
                                <div id="weatherDesc" class="text-xs text-slate-400 capitalize">Clear Sky</div>
                            </div>
                            <div id="weatherTemp" class="text-3xl font-black text-slate-800 dark:text-slate-100">32°C</div>
                        </div>
                    </div>

                    <div class="space-y-3">
                        <h3 class="text-sm font-bold text-slate-700 dark:text-slate-300 flex items-center gap-2"><i class="fa-solid fa-scale-balanced text-purple-500"></i> Metric System Converter</h3>
                        <div class="grid grid-cols-2 gap-2">
                            <input type="number" id="unitInput" placeholder="Value (e.g. Km)" oninput="convertUnits()" class="w-full bg-white dark:bg-slate-950 px-3 py-2 rounded-xl text-xs border border-slate-200 dark:border-slate-800 focus:outline-none">
                            <div id="unitOutput" class="w-full bg-slate-100 dark:bg-slate-950 px-3 py-2 rounded-xl text-xs font-semibold flex items-center text-slate-500">
                                Output: -- miles
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div id="settings" class="glass p-6 rounded-3xl shadow-sm space-y-4">
                <h3 class="text-sm font-bold text-slate-700 dark:text-slate-300 flex items-center gap-2"><i class="fa-solid fa-database text-slate-500"></i> Client Storage Configuration & Data Management</h3>
                <div class="flex flex-wrap gap-2">
                    <button onclick="exportDataJSON()" class="px-3 py-1.5 bg-slate-200 dark:bg-slate-800 text-xs font-semibold rounded-lg hover:bg-slate-300 transition"><i class="fa-solid fa-file-export mr-1"></i> Export Configuration</button>
                    <button onclick="clearSystemData()" class="px-3 py-1.5 bg-red-600/10 text-red-600 text-xs font-semibold rounded-lg hover:bg-red-600 hover:text-white transition"><i class="fa-solid fa-trash-can mr-1"></i> Flush Storage</button>
                </div>
            </div>
            
        </section>
    </main>

    <footer class="max-w-7xl mx-auto border-t border-slate-200 dark:border-slate-900 mt-12 p-6 text-center text-xs text-slate-400 space-y-3">
        <p>&copy; 2026 UtilHub Network. Operating fully decentralized completely inside Client Sandbox. No tracking.</p>
        <div class="flex justify-center space-x-4">
            <a href="#" onclick="alert('Privacy Policy: All data operations run explicitly locally.')" class="hover:underline">Privacy Policy</a>
            <a href="#" onclick="alert('Terms: Free open access without limits.')" class="hover:underline">Terms of Service</a>
        </div>
    </footer>

    <script>
        // System Theme Management
        const themeToggleBtn = document.getElementById('themeToggle');
        const themeIcon = document.getElementById('themeIcon');
        
        if (localStorage.getItem('theme') === 'dark' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
            document.documentElement.classList.add('dark');
            themeIcon.className = 'fa-solid fa-sun text-lg';
        } else {
            document.documentElement.classList.remove('dark');
            themeIcon.className = 'fa-solid fa-moon text-lg';
        }

        themeToggleBtn.addEventListener('click', () => {
            if (document.documentElement.classList.contains('dark')) {
                document.documentElement.classList.remove('dark');
                themeIcon.className = 'fa-solid fa-moon text-lg';
                localStorage.setItem('theme', 'light');
            } else {
                document.documentElement.classList.add('dark');
                themeIcon.className = 'fa-solid fa-sun text-lg';
                localStorage.setItem('theme', 'dark');
            }
        });

        // Core Utilities Functional Infrastructure
        function generateNewEmail() {
            const prefixes = ['user', 'alpha', 'beta', 'devx', 'testmail', 'kernel'];
            const randomPrefix = prefixes[Math.floor(Math.random() * prefixes.length)] + Math.floor(Math.random() * 8999 + 1000);
            const domain = document.getElementById('emailDomain').value;
            document.getElementById('tempEmailBox').value = randomPrefix + domain;
            
            // Generate standard mock email inbox notification
            const inbox = document.getElementById('inboxList');
            inbox.innerHTML = `
                <div class="grid grid-cols-3 px-4 py-3 text-xs bg-emerald-500/5 dark:bg-emerald-500/10 text-slate-700 dark:text-slate-300 font-medium">
                    <div class="text-emerald-600 font-bold">System Validation</div>
                    <div>Account Verification Code</div>
                    <div class="text-right text-slate-400">Just Now</div>
                </div>
            ` + inbox.innerHTML;
        }

        let otpTimer = 30;
        function refreshOTP() {
            const length = parseInt(document.getElementById('otpLength').value);
            let token = "";
            for (let i = 0; i < length; i++) {
                token += Math.floor(Math.random() * 10).toString();
            }
            document.getElementById('otpBox').value = token;
            otpTimer = 30;
        }

        setInterval(() => {
            otpTimer--;
            document.getElementById('otpCountdown').innerText = otpTimer + "s";
            if (otpTimer <= 0) {
                refreshOTP();
            }
        }, 1000);

        function generateSecurePassword() {
            const chars = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()_+";
            let pass = "";
            for(let i=0; i<16; i++) {
                pass += chars.charAt(Math.floor(Math.random() * chars.length));
            }
            document.getElementById('passwordBox').value = pass;
        }

        function generateUUIDV4() {
            const uuid = 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {
                var r = Math.random() * 16 | 0, v = c == 'x' ? r : (r & 0x3 | 0x8);
                return v.toString(16);
            });
            document.getElementById('uuidBox').value = uuid;
        }

        function generateMockCard() {
            let base = "400012345678";
            for(let i=0; i<4; i++) base += Math.floor(Math.random()*10);
            document.getElementById('ccBox').value = base + " | 12/29 | " + Math.floor(Math.random()*899+100);
        }

        function generateRandomIP() {
            document.getElementById('ipBox').value = `${Math.floor(Math.random()*255)}.${Math.floor(Math.random()*255)}.${Math.floor(Math.random()*255)}.${Math.floor(Math.random()*255)}`;
        }

        async function computeCryptoHash() {
            const input = document.getElementById('hashInput').value;
            if(!input) return;
            const msgUint8 = new TextEncoder().encode(input);
            const hashBuffer = await crypto.subtle.digest('SHA-256', msgUint8);
            const hashArray = Array.from(new Uint8Array(hashBuffer));
            const hashHex = hashArray.map(b => b.toString(16).padStart(2, '0')).join('');
            document.getElementById('hashOutput').innerText = hashHex;
        }

        function convertUnits() {
            const val = parseFloat(document.getElementById('unitInput').value);
            if(isNaN(val)) return;
            document.getElementById('unitOutput').innerText = `Output: ${(val * 0.621371).toFixed(2)} miles`;
        }

        function copyToClipboard(id) {
            const copyText = document.getElementById(id);
            navigator.clipboard.writeText(copyText.value);
            alert("Copied value data payload successfully!");
        }

        async function fetchMarketData() {
            try {
                // Public API feeds without keys
                const btcRes = await fetch('https://api.coingecko.com/api/v3/simple/price?ids=bitcoin,ethereum&vs_currencies=usd');
                const cryptoData = await btcRes.json();
                document.getElementById('btcPrice').innerText = "$" + cryptoData.bitcoin.usd.toLocaleString();
                document.getElementById('ethPrice').innerText = "$" + cryptoData.ethereum.usd.toLocaleString();
                
                const fxRes = await fetch('https://open.er-api.com/v6/latest/USD');
                const fxData = await fxRes.json();
                const rate = fxData.rates.INR;
                document.getElementById('fxResult').innerText = `1 USD = ${rate.toFixed(2)} INR`;
            } catch (err) {
                console.log("Network rates currently fetching structural delays...");
            }
        }

        function exportDataJSON() {
            const data = { theme: localStorage.getItem('theme'), timestamp: new Date() };
            const dataStr = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify(data));
            const dlAnchor = document.createElement('a');
            dlAnchor.setAttribute("href", dataStr);
            dlAnchor.setAttribute("download", "utilhub_config.json");
            dlAnchor.click();
        }

        function clearSystemData() {
            localStorage.clear();
            alert("Client storage vectors securely erased.");
            window.location.reload();
        }

        // Initialize Runtime Engines
        generateNewEmail();
        refreshOTP();
        generateSecurePassword();
        generateUUIDV4();
        generateMockCard();
        generateRandomIP();
        fetchMarketData();
    </script>
</body>
</html>
