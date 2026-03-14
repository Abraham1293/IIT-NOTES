# IIT-NOTES
Free IIT preparation notes for Physics, Chemistry and Maths
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IITian Notes | Premium Study Material for JEE & Engineering</title>
    
    <!-- Tailwind CSS for Styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Tailwind Configuration -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#4f46e5', // Indigo 600
                        secondary: '#0f172a', // Slate 900
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8fafc;
        }
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        ::-webkit-scrollbar-thumb {
            background: #c7c7cc;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #a1a1aa;
        }
        
        /* Toast Animation */
        @keyframes slideIn {
            from { transform: translateX(100%); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        @keyframes fadeOut {
            from { opacity: 1; }
            to { opacity: 0; }
        }
        .toast-enter {
            animation: slideIn 0.3s ease-out forwards;
        }
        .toast-exit {
            animation: fadeOut 0.3s ease-out forwards;
        }
    </style>
</head>
<body class="text-slate-800 antialiased flex flex-col min-h-screen">

    <!-- Toast Notification Container -->
    <div id="toast-container" class="fixed bottom-4 right-4 z-50 flex flex-col gap-2"></div>

    <!-- Navbar -->
    <header class="bg-white/80 backdrop-blur-md sticky top-0 z-40 border-b border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo -->
                <div class="flex items-center gap-2 cursor-pointer">
                    <div class="bg-primary text-white p-2 rounded-lg">
                        <i data-lucide="graduation-cap" class="w-6 h-6"></i>
                    </div>
                    <span class="font-bold text-xl tracking-tight text-secondary">IITian<span class="text-primary">Notes</span></span>
                </div>
                
                <!-- Desktop Navigation -->
                <nav class="hidden md:flex space-x-8">
                    <a href="#" class="text-slate-600 hover:text-primary font-medium transition-colors">Home</a>
                    <a href="#subjects" class="text-slate-600 hover:text-primary font-medium transition-colors">Subjects</a>
                    <a href="#materials" class="text-slate-600 hover:text-primary font-medium transition-colors">Study Material</a>
                    <a href="#pyq" class="text-slate-600 hover:text-primary font-medium transition-colors">PYQs</a>
                </nav>

                <!-- CTA Button -->
                <div class="hidden md:flex">
                    <button class="bg-primary hover:bg-indigo-700 text-white px-5 py-2 rounded-full font-medium transition-all shadow-md shadow-indigo-200">
                        Join Community
                    </button>
                </div>

                <!-- Mobile menu button -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" class="text-slate-500 hover:text-slate-700 focus:outline-none">
                        <i data-lucide="menu" class="w-6 h-6"></i>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile Navigation -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-t border-slate-200">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="#" class="block px-3 py-2 rounded-md text-base font-medium text-slate-700 hover:text-primary hover:bg-slate-50">Home</a>
                <a href="#subjects" class="block px-3 py-2 rounded-md text-base font-medium text-slate-700 hover:text-primary hover:bg-slate-50">Subjects</a>
                <a href="#materials" class="block px-3 py-2 rounded-md text-base font-medium text-slate-700 hover:text-primary hover:bg-slate-50">Study Material</a>
                <button class="w-full text-left px-3 py-2 mt-2 bg-primary text-white rounded-md font-medium">Join Community</button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative pt-20 pb-24 overflow-hidden">
        <!-- Background decorative elements -->
        <div class="absolute inset-0 z-0 opacity-30">
            <div class="absolute top-0 left-1/4 w-96 h-96 bg-indigo-300 rounded-full mix-blend-multiply filter blur-3xl animate-blob"></div>
            <div class="absolute top-0 right-1/4 w-96 h-96 bg-cyan-300 rounded-full mix-blend-multiply filter blur-3xl animate-blob animation-delay-2000"></div>
            <div class="absolute -bottom-8 left-1/3 w-96 h-96 bg-purple-300 rounded-full mix-blend-multiply filter blur-3xl animate-blob animation-delay-4000"></div>
        </div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10 text-center">
            <span class="inline-block py-1 px-3 rounded-full bg-indigo-50 border border-indigo-100 text-indigo-600 text-sm font-semibold mb-6">
                🔥 Updated for 2026-2027 Syllabus
            </span>
            <h1 class="text-5xl md:text-6xl font-extrabold text-secondary tracking-tight mb-6 leading-tight">
                Ace Your IIT Journey With <br class="hidden md:block" />
                <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-cyan-500">Topper's Handwritten Notes</span>
            </h1>
            <p class="mt-4 max-w-2xl mx-auto text-lg text-slate-600 mb-10">
                Access meticulously curated study materials, formula sheets, and previous year questions designed specifically for JEE Main, JEE Advanced, and Engineering Semester exams.
            </p>
            
            <!-- Search Bar -->
            <div class="max-w-2xl mx-auto bg-white p-2 rounded-full shadow-lg border border-slate-100 flex items-center">
                <div class="pl-4 text-slate-400">
                    <i data-lucide="search" class="w-5 h-5"></i>
                </div>
                <input 
                    type="text" 
                    id="global-search"
                    placeholder="Search for 'Rotational Dynamics', 'Organic Chemistry'..." 
                    class="w-full py-3 px-4 outline-none bg-transparent text-slate-700 placeholder-slate-400"
                >
                <button onclick="scrollToMaterials()" class="bg-primary hover:bg-indigo-700 text-white px-6 py-3 rounded-full font-medium transition-colors">
                    Search
                </button>
            </div>
            
            <div class="mt-10 flex flex-wrap justify-center gap-6 text-sm text-slate-500 font-medium">
                <div class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-green-500"></i> Free PDF Downloads</div>
                <div class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-green-500"></i> High-Quality Scans</div>
                <div class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-green-500"></i> Chapter-wise Sorted</div>
            </div>
        </div>
    </section>

    <!-- Subjects Section -->
    <section id="subjects" class="py-16 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-secondary">Browse by Subject</h2>
                <p class="mt-4 text-slate-600">Select a subject to view specialized study materials</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Physics Card -->
                <div onclick="filterSubject('Physics')" class="group cursor-pointer bg-slate-50 rounded-2xl p-8 border border-slate-100 hover:border-indigo-200 hover:shadow-xl hover:shadow-indigo-100 transition-all duration-300 hover:-translate-y-1">
                    <div class="w-14 h-14 bg-blue-100 text-blue-600 rounded-xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                        <i data-lucide="atom" class="w-8 h-8"></i>
                    </div>
                    <h3 class="text-xl font-bold text-secondary mb-2">Physics</h3>
                    <p class="text-slate-600 mb-4">Mechanics, Electromagnetism, Optics, Modern Physics & Thermodynamics.</p>
                    <span class="text-primary font-medium flex items-center gap-1 group-hover:gap-2 transition-all">
                        View Notes <i data-lucide="arrow-right" class="w-4 h-4"></i>
                    </span>
                </div>

                <!-- Chemistry Card -->
                <div onclick="filterSubject('Chemistry')" class="group cursor-pointer bg-slate-50 rounded-2xl p-8 border border-slate-100 hover:border-indigo-200 hover:shadow-xl hover:shadow-indigo-100 transition-all duration-300 hover:-translate-y-1">
                    <div class="w-14 h-14 bg-emerald-100 text-emerald-600 rounded-xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                        <i data-lucide="flask-conical" class="w-8 h-8"></i>
                    </div>
                    <h3 class="text-xl font-bold text-secondary mb-2">Chemistry</h3>
                    <p class="text-slate-600 mb-4">Physical Chemistry, Organic Reactions, and Inorganic block elements.</p>
                    <span class="text-primary font-medium flex items-center gap-1 group-hover:gap-2 transition-all">
                        View Notes <i data-lucide="arrow-right" class="w-4 h-4"></i>
                    </span>
                </div>

                <!-- Mathematics Card -->
                <div onclick="filterSubject('Mathematics')" class="group cursor-pointer bg-slate-50 rounded-2xl p-8 border border-slate-100 hover:border-indigo-200 hover:shadow-xl hover:shadow-indigo-100 transition-all duration-300 hover:-translate-y-1">
                    <div class="w-14 h-14 bg-purple-100 text-purple-600 rounded-xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                        <i data-lucide="calculator" class="w-8 h-8"></i>
                    </div>
                    <h3 class="text-xl font-bold text-secondary mb-2">Mathematics</h3>
                    <p class="text-slate-600 mb-4">Calculus, Algebra, Coordinate Geometry, Trigonometry & Vectors.</p>
                    <span class="text-primary font-medium flex items-center gap-1 group-hover:gap-2 transition-all">
                        View Notes <i data-lucide="arrow-right" class="w-4 h-4"></i>
                    </span>
                </div>
            </div>
        </div>
    </section>

    <!-- Notes Repository Section -->
    <section id="materials" class="py-16 bg-slate-50 flex-grow">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center mb-8 gap-4">
                <div>
                    <h2 class="text-3xl font-bold text-secondary">Study Materials Repository</h2>
                    <p class="text-slate-600 mt-2">Download high-quality notes in PDF format</p>
                </div>
                
                <!-- Category Filters -->
                <div class="flex bg-white rounded-lg p-1 border border-slate-200 shadow-sm overflow-x-auto w-full md:w-auto">
                    <button onclick="setFilter('All')" id="btn-All" class="filter-btn active px-4 py-2 rounded-md text-sm font-medium transition-colors bg-primary text-white">All</button>
                    <button onclick="setFilter('Physics')" id="btn-Physics" class="filter-btn px-4 py-2 rounded-md text-sm font-medium text-slate-600 hover:bg-slate-100 transition-colors">Physics</button>
                    <button onclick="setFilter('Chemistry')" id="btn-Chemistry" class="filter-btn px-4 py-2 rounded-md text-sm font-medium text-slate-600 hover:bg-slate-100 transition-colors">Chemistry</button>
                    <button onclick="setFilter('Mathematics')" id="btn-Mathematics" class="filter-btn px-4 py-2 rounded-md text-sm font-medium text-slate-600 hover:bg-slate-100 transition-colors">Maths</button>
                </div>
            </div>

            <!-- Notes List Container -->
            <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden">
                <div class="grid grid-cols-1 divide-y divide-slate-100" id="notes-container">
                    <!-- Notes will be injected here via JS -->
                </div>
                
                <!-- Empty State (Hidden by default) -->
                <div id="empty-state" class="hidden py-16 text-center">
                    <div class="inline-flex items-center justify-center w-16 h-16 rounded-full bg-slate-100 mb-4">
                        <i data-lucide="search-x" class="w-8 h-8 text-slate-400"></i>
                    </div>
                    <h3 class="text-lg font-medium text-secondary">No materials found</h3>
                    <p class="text-slate-500 mt-1">Try adjusting your search or filter criteria.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Newsletter/Motivation Section -->
    <section class="py-16 bg-secondary text-white relative overflow-hidden">
        <div class="absolute inset-0 z-0 opacity-10">
             <svg class="absolute left-0 top-0 h-full w-full" viewBox="0 0 100 100" preserveAspectRatio="none">
                <path d="M0,100 C20,0 50,0 100,100 Z" fill="#ffffff" />
            </svg>
        </div>
        <div class="max-w-4xl mx-auto px-4 relative z-10 text-center">
            <h2 class="text-3xl font-bold mb-4">"Success is not a destination, it's a journey."</h2>
            <p class="text-slate-300 text-lg mb-8">Get notified whenever new topper notes or formula sheets are uploaded. No spam, just pure value.</p>
            <div class="flex flex-col sm:flex-row gap-3 justify-center max-w-md mx-auto">
                <input type="email" placeholder="Enter your email address" class="px-4 py-3 rounded-lg flex-grow text-slate-800 focus:outline-none focus:ring-2 focus:ring-primary">
                <button onclick="showToast('Subscribed successfully!', 'success')" class="bg-primary hover:bg-indigo-600 px-6 py-3 rounded-lg font-medium transition-colors whitespace-nowrap">
                    Subscribe Now
                </button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-white border-t border-slate-200 pt-12 pb-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
                <div class="col-span-1 md:col-span-2">
                    <div class="flex items-center gap-2 mb-4">
                        <div class="bg-primary text-white p-1.5 rounded-md">
                            <i data-lucide="graduation-cap" class="w-5 h-5"></i>
                        </div>
                        <span class="font-bold text-lg text-secondary">IITian<span class="text-primary">Notes</span></span>
                    </div>
                    <p class="text-slate-500 text-sm max-w-sm mb-4">
                        The ultimate destination for JEE aspirants and engineering students to find structured, high-quality, and free study materials.
                    </p>
                    <div class="flex space-x-4 text-slate-400">
                        <a href="#" class="hover:text-primary transition-colors"><i data-lucide="twitter" class="w-5 h-5"></i></a>
                        <a href="#" class="hover:text-primary transition-colors"><i data-lucide="youtube" class="w-5 h-5"></i></a>
                        <a href="#" class="hover:text-primary transition-colors"><i data-lucide="instagram" class="w-5 h-5"></i></a>
                    </div>
                </div>
                
                <div>
                    <h4 class="font-semibold text-secondary mb-4">Quick Links</h4>
                    <ul class="space-y-2 text-sm text-slate-500">
                        <li><a href="#" class="hover:text-primary transition-colors">About Us</a></li>
                        <li><a href="#" class="hover:text-primary transition-colors">Syllabus</a></li>
                        <li><a href="#" class="hover:text-primary transition-colors">Mock Tests</a></li>
                        <li><a href="#" class="hover:text-primary transition-colors">Contribute Notes</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="font-semibold text-secondary mb-4">Legal</h4>
                    <ul class="space-y-2 text-sm text-slate-500">
                        <li><a href="#" class="hover:text-primary transition-colors">Privacy Policy</a></li>
                        <li><a href="#" class="hover:text-primary transition-colors">Terms of Service</a></li>
                        <li><a href="#" class="hover:text-primary transition-colors">Copyright Info</a></li>
                        <li><a href="#" class="hover:text-primary transition-colors">Contact Support</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-slate-200 pt-8 flex flex-col md:flex-row justify-between items-center gap-4 text-sm text-slate-500">
                <p>&copy; 2026 IITianNotes. All rights reserved.</p>
                <p>Made with <i data-lucide="heart" class="w-4 h-4 inline text-red-500 mx-1 fill-current"></i> for Students</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript Application Logic -->
    <script>
        // Initialize Lucide Icons
        lucide.createIcons();

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Mock Database for Notes
        const notesDatabase = [
            { id: 1, title: 'Kinematics & 1D Motion', subject: 'Physics', author: 'AIR 145', size: '3.2 MB', downloads: '12k', date: 'New', type: 'PDF' },
            { id: 2, title: 'Laws of Motion & Friction', subject: 'Physics', author: 'Allen Star Batch', size: '4.5 MB', downloads: '8.5k', date: 'Jan 2026', type: 'PDF' },
            { id: 3, title: 'General Organic Chemistry (GOC)', subject: 'Chemistry', author: 'Fiitjee Notes', size: '6.1 MB', downloads: '25k', date: 'New', type: 'PDF' },
            { id: 4, title: 'Coordination Compounds', subject: 'Chemistry', author: 'AIR 42', size: '2.8 MB', downloads: '9k', date: 'Feb 2026', type: 'PDF' },
            { id: 5, title: 'Differential Calculus Complete', subject: 'Mathematics', author: 'Super 30', size: '8.4 MB', downloads: '18k', date: 'New', type: 'PDF' },
            { id: 6, title: 'Vectors & 3D Geometry', subject: 'Mathematics', author: 'Bansal Classes', size: '4.1 MB', downloads: '14k', date: 'Dec 2025', type: 'PDF' },
            { id: 7, title: 'Electrostatics & Capacitance', subject: 'Physics', author: 'Resonance', size: '5.5 MB', downloads: '11k', date: 'Mar 2026', type: 'PDF' },
            { id: 8, title: 'Chemical Thermodynamics', subject: 'Chemistry', author: 'Self Study', size: '3.9 MB', downloads: '6k', date: 'Jan 2026', type: 'PDF' },
        ];

        let currentFilter = 'All';
        let searchQuery = '';

        // DOM Elements
        const notesContainer = document.getElementById('notes-container');
        const emptyState = document.getElementById('empty-state');
        const searchInput = document.getElementById('global-search');

        // Subject colors for badges
        const subjectColors = {
            'Physics': 'bg-blue-100 text-blue-700 border-blue-200',
            'Chemistry': 'bg-emerald-100 text-emerald-700 border-emerald-200',
            'Mathematics': 'bg-purple-100 text-purple-700 border-purple-200'
        };

        // Render Notes Function
        function renderNotes() {
            // Filter logic
            const filteredNotes = notesDatabase.filter(note => {
                const matchesFilter = currentFilter === 'All' || note.subject === currentFilter;
                const matchesSearch = note.title.toLowerCase().includes(searchQuery.toLowerCase()) || 
                                      note.subject.toLowerCase().includes(searchQuery.toLowerCase());
                return matchesFilter && matchesSearch;
            });

            // Update UI
            notesContainer.innerHTML = '';

            if (filteredNotes.length === 0) {
                notesContainer.classList.add('hidden');
                emptyState.classList.remove('hidden');
                return;
            }

            notesContainer.classList.remove('hidden');
            emptyState.classList.add('hidden');

            filteredNotes.forEach(note => {
                const isNew = note.date === 'New';
                
                const noteElement = document.createElement('div');
                noteElement.className = 'p-4 sm:p-6 hover:bg-slate-50 transition-colors flex flex-col sm:flex-row gap-4 sm:items-center justify-between group';
                
                noteElement.innerHTML = `
                    <div class="flex items-start gap-4">
                        <div class="mt-1 flex-shrink-0 w-12 h-12 rounded-lg bg-red-50 text-red-500 flex items-center justify-center border border-red-100">
                            <i data-lucide="file-text" class="w-6 h-6"></i>
                        </div>
                        <div>
                            <div class="flex items-center gap-2 mb-1">
                                <h4 class="font-semibold text-secondary text-lg group-hover:text-primary transition-colors">${note.title}</h4>
                                ${isNew ? '<span class="px-2 py-0.5 rounded text-[10px] font-bold bg-amber-100 text-amber-700 uppercase tracking-wider">New</span>' : ''}
                            </div>
                            <div class="flex flex-wrap items-center gap-3 text-sm text-slate-500">
                                <span class="px-2.5 py-0.5 rounded-full border text-xs font-medium ${subjectColors[note.subject]}">
                                    ${note.subject}
                                </span>
                                <span class="flex items-center gap-1"><i data-lucide="user" class="w-3.5 h-3.5"></i> ${note.author}</span>
                                <span class="flex items-center gap-1"><i data-lucide="hard-drive" class="w-3.5 h-3.5"></i> ${note.size}</span>
                                <span class="flex items-center gap-1"><i data-lucide="download" class="w-3.5 h-3.5"></i> ${note.downloads}</span>
                            </div>
                        </div>
                    </div>
                    <div class="flex sm:flex-col md:flex-row gap-2 mt-4 sm:mt-0 w-full sm:w-auto">
                        <button onclick="handlePreview('${note.title}')" class="flex-1 sm:flex-none px-4 py-2 rounded-lg border border-slate-200 text-slate-600 font-medium hover:bg-slate-100 hover:text-secondary transition-colors text-sm flex items-center justify-center gap-2">
                            <i data-lucide="eye" class="w-4 h-4"></i> Preview
                        </button>
                        <button onclick="handleDownload('${note.title}')" class="flex-1 sm:flex-none px-4 py-2 rounded-lg bg-primary text-white font-medium hover:bg-indigo-700 shadow-sm shadow-indigo-200 transition-colors text-sm flex items-center justify-center gap-2">
                            <i data-lucide="download-cloud" class="w-4 h-4"></i> Download
                        </button>
                    </div>
                `;
                notesContainer.appendChild(noteElement);
            });

            // Re-initialize icons for newly added DOM elements
            lucide.createIcons();
        }

        // Handle Filter Clicks
        function setFilter(subject) {
            currentFilter = subject;
            
            // Update button styles
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.classList.remove('bg-primary', 'text-white');
                btn.classList.add('text-slate-600', 'hover:bg-slate-100');
            });
            
            const activeBtn = document.getElementById(`btn-${subject}`);
            activeBtn.classList.remove('text-slate-600', 'hover:bg-slate-100');
            activeBtn.classList.add('bg-primary', 'text-white');

            renderNotes();
        }

        // Wrapper to navigate from hero cards
        function filterSubject(subject) {
            scrollToMaterials();
            setFilter(subject);
        }

        // Handle Search Input
        searchInput.addEventListener('input', (e) => {
            searchQuery = e.target.value;
            renderNotes();
        });

        // Scroll helper
        function scrollToMaterials() {
            document.getElementById('materials').scrollIntoView({ behavior: 'smooth' });
        }

        // Interaction Handlers (Mock logic using Toast instead of annoying alerts)
        function handleDownload(title) {
            showToast(`Started downloading: ${title}`, 'success');
        }

        function handlePreview(title) {
            showToast(`Opening preview for: ${title}`, 'info');
        }

        // Custom Toast Notification System
        function showToast(message, type = 'info') {
            const container = document.getElementById('toast-container');
            const toast = document.createElement('div');
            
            // Icon based on type
            const icon = type === 'success' 
                ? '<i data-lucide="check-circle-2" class="w-5 h-5 text-green-500"></i>'
                : '<i data-lucide="info" class="w-5 h-5 text-blue-500"></i>';

            toast.className = `bg-white border border-slate-200 shadow-lg rounded-lg p-4 flex items-center gap-3 w-80 toast-enter`;
            toast.innerHTML = `
                ${icon}
                <p class="text-sm font-medium text-slate-700 flex-grow">${message}</p>
                <button onclick="this.parentElement.remove()" class="text-slate-400 hover:text-slate-600">
                    <i data-lucide="x" class="w-4 h-4"></i>
                </button>
            `;
            
            container.appendChild(toast);
            lucide.createIcons(); // render icons in toast

            // Auto remove after 3 seconds
            setTimeout(() => {
                toast.classList.remove('toast-enter');
                toast.classList.add('toast-exit');
                setTimeout(() => toast.remove(), 300); // wait for animation to finish
            }, 3000);
        }

        // Initial Render
        renderNotes();
    </script>
</body>
</html>
