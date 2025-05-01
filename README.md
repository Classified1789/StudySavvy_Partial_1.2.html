<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StudySavvy - Your Learning Companion</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        body {
            background-color: #222222;
            color: #ffffff;
        }
        .blue-gradient {
            background: linear-gradient(135deg, #0055A4 0%, #003b72 100%);
        }
        .red-gradient {
            background: linear-gradient(135deg, #DC143C 0%, #a01030 100%);
        }
        .green-gradient {
            background: linear-gradient(135deg, #117C13 0%, #0a5c0c 100%);
        }
        .orange-gradient {
            background: linear-gradient(135deg, #DA7756 0%, #b65a3e 100%);
        }
        .purple-gradient {
            background: linear-gradient(135deg, #8A2BE2 0%, #5a1c96 100%);
        }
        .yellow-text {
            color: #eded3e;
        }
        .card-hover {
            transition: transform 0.2s;
        }
        .card-hover:hover {
            transform: translateY(-4px);
        }
        .sidebar-item {
            border-left: 4px solid transparent;
        }
        .sidebar-item.active {
            border-left: 4px solid #0055A4;
            background-color: #333333;
        }
        .sidebar-item:hover:not(.active) {
            background-color: #333333;
        }
        .section {
            display: none;
        }
        .section.active {
            display: block;
        }
    </style>
</head>
<body>
    <div class="fixed h-full w-64 bg-[#333333] shadow-lg">
        <div class="p-6">
            <div class="flex items-center space-x-2">
                <div class="w-8 h-8 blue-gradient rounded-lg"></div>
                <h1 class="text-2xl font-bold text-[#eded3e]">StudySavvy</h1>
            </div>
        </div>

        <nav class="mt-6">
            <a href="#" class="block px-6 py-3 sidebar-item active text-white" data-section="dashboard">
                Dashboard
            </a>
            <a href="#" class="block px-6 py-3 sidebar-item text-gray-300 hover:text-white" data-section="courses">
                My Courses
            </a>
            <a href="#" class="block px-6 py-3 sidebar-item text-gray-300 hover:text-white" data-section="planner">
                Study Planner
            </a>
            <a href="#" class="block px-6 py-3 sidebar-item text-gray-300 hover:text-white" data-section="resources">
                Resources
            </a>
            <a href="#" class="block px-6 py-3 sidebar-item text-gray-300 hover:text-white" data-section="analytics">
                Analytics
            </a>
        </nav>
    </div>

    <div class="ml-64 p-8">
        <header class="flex justify-between items-center mb-8">
            <div>
                <h2 class="text-2xl font-bold text-white">Welcome back, Alex!</h2>
                <p class="text-gray-400">Let's continue your learning journey</p>
            </div>

            <div class="flex items-center space-x-4">
                <button class="p-2 rounded-full bg-[#444444] hover:bg-[#555555]">
                    <i class="fas fa-bell text-[#eded3e]"></i>
                </button>
                <div class="flex items-center space-x-2">
                    <div class="w-10 h-10 blue-gradient rounded-full flex items-center justify-center text-white font-bold">
                        AMJ
                    </div>
                    <span class="text-gray-300">Alex M. Johnson</span>
                </div>
            </div>
        </header>

        <section id="dashboard" class="section active">
            <div class="grid grid-cols-4 gap-6 mb-8">
                <div class="bg-[#333333] p-6 rounded-xl shadow-lg card-hover">
                    <div class="flex items-center justify-between mb-4">
                        <h3 class="text-gray-400">Study Hours</h3>
                        <div class="w-8 h-8 blue-gradient rounded-lg"></div>
                    </div>
                    <p class="text-2xl font-bold text-white">24.5</p>
                    <p class="text-green-400 text-sm">+2.5 from last week</p>
                </div>

                <div class="bg-[#333333] p-6 rounded-xl shadow-lg card-hover">
                    <div class="flex items-center justify-between mb-4">
                        <h3 class="text-gray-400">Tasks Complete</h3>
                        <div class="w-8 h-8 red-gradient rounded-lg"></div>
                    </div>
                    <p class="text-2xl font-bold text-white">18/20</p>
                    <p class="text-green-400 text-sm">90% completion rate</p>
                </div>

                <div class="bg-[#333333] p-6 rounded-xl shadow-lg card-hover">
                    <div class="flex items-center justify-between mb-4">
                        <h3 class="text-gray-400">Active Courses</h3>
                        <div class="w-8 h-8 green-gradient rounded-lg"></div>
                    </div>
                    <p class="text-2xl font-bold text-white">5</p>
                    <p class="text-blue-400 text-sm">2 due this week</p>
                </div>

                <div class="bg-[#333333] p-6 rounded-xl shadow-lg card-hover">
                    <div class="flex items-center justify-between mb-4">
                        <h3 class="text-gray-400">Study Streak</h3>
                        <div class="w-8 h-8 orange-gradient rounded-lg"></div>
                    </div>
                    <p class="text-2xl font-bold text-white">7 days</p>
                    <p class="yellow-text text-sm">Personal best!</p>
                </div>
            </div>

            <div class="grid grid-cols-3 gap-6">
                <div class="col-span-2 bg-[#333333] p-6 rounded-xl shadow-lg">
                    <h3 class="text-xl font-bold mb-4 text-white">Current Focus</h3>
                    <div class="space-y-4">
                        <div class="p-4 bg-[#444444] rounded-lg">
                            <div class="flex items-center justify-between mb-2">
                                <h4 class="font-semibold text-[#0055A4]">Mathematics</h4>
                                <span class="text-sm text-[#0055A4]">Chapter 7</span>
                            </div>
                            <div class="w-full bg-[#555555] rounded-full h-2">
                                <div class="blue-gradient h-2 rounded-full" style="width: 75%"></div>
                            </div>
                        </div>

                        <div class="p-4 bg-[#444444] rounded-lg">
                            <div class="flex items-center justify-between mb-2">
                                <h4 class="font-semibold text-[#DC143C]">Physics</h4>
                                <span class="text-sm text-[#DC143C]">Unit 4</span>
                            </div>
                            <div class="w-full bg-[#555555] rounded-full h-2">
                                <div class="red-gradient h-2 rounded-full" style="width: 60%"></div>
                            </div>
                        </div>

                        <div class="p-4 bg-[#444444] rounded-lg">
                            <div class="flex items-center justify-between mb-2">
                                <h4 class="font-semibold text-[#117C13]">Biology</h4>
                                <span class="text-sm text-[#117C13]">Section 3</span>
                            </div>
                            <div class="w-full bg-[#555555] rounded-full h-2">
                                <div class="green-gradient h-2 rounded-full" style="width: 45%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="bg-[#333333] p-6 rounded-xl shadow-lg">
                    <h3 class="text-xl font-bold mb-4 text-white">Upcoming Tasks</h3>
                    <div class="space-y-4">
                        <div class="flex items-center p-3 bg-[#444444] rounded-lg">
                            <div class="w-2 h-2 bg-[#DC143C] rounded-full mr-3"></div>
                            <div>
                                <p class="font-medium text-white">Math Assignment</p>
                                <p class="text-sm text-gray-400">Due in 2 hours</p>
                            </div>
                        </div>

                        <div class="flex items-center p-3 bg-[#444444] rounded-lg">
                            <div class="w-2 h-2 bg-[#eded3e] rounded-full mr-3"></div>
                            <div>
                                <p class="font-medium text-white">Physics Quiz</p>
                                <p class="text-sm text-gray-400">Tomorrow, 10:00 AM</p>
                            </div>
                        </div>

                        <div class="flex items-center p-3 bg-[#444444] rounded-lg">
                            <div class="w-2 h-2 bg-[#117C13] rounded-full mr-3"></div>
                            <div>
                                <p class="font-medium text-white">Group Study</p>
                                <p class="text-sm text-gray-400">Friday, 3:00 PM</p>
                            </div>
                        </div>

                        <div class="flex items-center p-3 bg-[#444444] rounded-lg">
                            <div class="w-2 h-2 bg-[#DA7756] rounded-full mr-3"></div>
                            <div>
                                <p class="font-medium text-white">Literature Essay</p>
                                <p class="text-sm text-gray-400">Monday, 9:00 AM</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="courses" class="section">
            <h2 class="text-2xl font-bold mb-6 text-white">My Courses</h2>

            <div class="grid grid-cols-3 gap-6 mb-8">
                <div class="bg-[#333333] rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-32 blue-gradient flex items-center justify-center">
                        <i class="fas fa-square-root-alt text-4xl text-white"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white mb-2">Advanced Mathematics</h3>
                        <p class="text-gray-400 mb-4">Prof. Johnson • MWF 9:00-10:30 AM</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-sm text-gray-400">Progress</span>
                                <div class="w-24 bg-[#555555] rounded-full h-2 mt-1">
                                    <div class="blue-gradient h-2 rounded-full" style="width: 75%"></div>
                                </div>
                            </div>
                            <button class="px-4 py-2 rounded-lg blue-gradient text-white text-sm font-medium">
                                Continue
                            </button>
                        </div>
                    </div>
                </div>

                <div class="bg-[#333333] rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-32 red-gradient flex items-center justify-center">
                        <i class="fas fa-atom text-4xl text-white"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white mb-2">Physics 201</h3>
                        <p class="text-gray-400 mb-4">Dr. Reynolds • TR 1:00-2:30 PM</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-sm text-gray-400">Progress</span>
                                <div class="w-24 bg-[#555555] rounded-full h-2 mt-1">
                                    <div class="red-gradient h-2 rounded-full" style="width: 60%"></div>
                                </div>
                            </div>
                            <button class="px-4 py-2 rounded-lg red-gradient text-white text-sm font-medium">
                                Continue
                            </button>
                        </div>
                    </div>
                </div>

                <div class="bg-[#333333] rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-32 green-gradient flex items-center justify-center">
                        <i class="fas fa-dna text-4xl text-white"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white mb-2">Biology 102</h3>
                        <p class="text-gray-400 mb-4">Prof. Martinez • TR 10:00-11:30 AM</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-sm text-gray-400">Progress</span>
                                <div class="w-24 bg-[#555555] rounded-full h-2 mt-1">
                                    <div class="green-gradient h-2 rounded-full" style="width: 45%"></div>
                                </div>
                            </div>
                            <button class="px-4 py-2 rounded-lg green-gradient text-white text-sm font-medium">
                                Continue
                            </button>
                        </div>
                    </div>
                </div>

                <div class="bg-[#333333] rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-32 orange-gradient flex items-center justify-center">
                        <i class="fas fa-book text-4xl text-white"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white mb-2">English Literature</h3>
                        <p class="text-gray-400 mb-4">Dr. Williams • MWF 2:00-3:30 PM</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-sm text-gray-400">Progress</span>
                                <div class="w-24 bg-[#555555] rounded-full h-2 mt-1">
                                    <div class="orange-gradient h-2 rounded-full" style="width: 30%"></div>
                                </div>
                            </div>
                            <button class="px-4 py-2 rounded-lg orange-gradient text-white text-sm font-medium">
                                Continue
                            </button>
                        </div>
                    </div>
                </div>

                <div class="bg-[#333333] rounded-xl shadow-lg overflow-hidden card-hover">
                    <div class="h-32 purple-gradient flex items-center justify-center">
                        <i class="fas fa-laptop-code text-4xl text-white"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white mb-2">Computer Science</h3>
                        <p class="text-gray-400 mb-4">Prof. Chen • TR 3:00-4:30 PM</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="text-sm text-gray-400">Progress</span>
                                <div class="w-24 bg-[#555555] rounded-full h-2 mt-1">
                                    <div class="purple-gradient h-2 rounded-full" style="width: 85%"></div>
                                </div>
                            </div>
                            <button class="px-4 py-2 rounded-lg purple-gradient text-white text-sm font-medium">
                                Continue
                            </button>
                        </div>
                    </div>
                </div>

                <div class="bg-[#333333] rounded-xl shadow-lg overflow-hidden flex items-center justify-center h-64 border-2 border-dashed border-gray-500 card-hover">
                    <div class="text-center">
                        <div class="w-12 h-12 bg-[#444444] mx-auto rounded-full flex items-center justify-center mb-2">
                            <i class="fas fa-plus text-gray-300"></i>
                        </div>
                        <p class="text-gray-400">Add New Course</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="planner" class="section">
            <h2 class="text-2xl font-bold mb-6 text-white">Study Planner</h2>

            <div class="grid grid-cols-3 gap-6">
                <div class="col-span-2 bg-[#333333] p-6 rounded-xl shadow-lg">
                    <div class="flex justify-between items-center mb-6">
                        <h3 class="text-xl font-bold text-white">April 2025</h3>
                        <div class="flex space-x-2">
                            <button class="p-2 rounded-lg bg-[#444444] hover:bg-[#555555]">
                                <i class="fas fa-chevron-left text-gray-300"></i>
                            </button>
                            <button class="p-2 rounded-lg bg-[#444444] hover:bg-[#555555]">
                                <i class="fas fa-chevron-right text-gray-300"></i>
                            </button>
                        </div>
                    </div>

                    <div class="grid grid-cols-7 gap-1">
                        <div class="text-center text-gray-400 py-2">Sun</div>
                        <div class="text-center text-gray-400 py-2">Mon</div>
                        <div class="text-center text-gray-400 py-2">Tue</div>
                        <div class="text-center text-gray-400 py-2">Wed</div>
                        <div class="text-center text-gray-400 py-2">Thu</div>
                        <div class="text-center text-gray-400 py-2">Fri</div>
                        <div class="text-center text-gray-400 py-2">Sat</div>

                        <div class="text-center py-4 text-gray-500">30</div>
                        <div class="text-center py-4 text-gray-500">31</div>
                        <div class="text-center py-4">1</div>
                        <div class="text-center py-4">2</div>
                        <div class="text-center py-4">3</div>
                        <div class="text-center py-4">4</div>
                        <div class="text-center py-4">5</div>

                        <div class="text-center py-4">6</div>
                        <div class="text-center py-4">7</div>
                        <div class="text-center py-4">8</div>
                        <div class="text-center py-4">9</div>
                        <div class="text-center py-4">10</div>
                        <div class="text-center py-4">11</div>
                        <div class="text-center py-4">12</div>

                        <div class="text-center py-4">13</div>
                        <div class="text-center py-4">14</div>
                        <div class="text-center py-4">15</div>
                        <div class="text-center py-4">16</div>
                        <div class="text-center py-4">17</div>
                        <div class="text-center py-4">18</div>
                        <div class="text-center py-4">19</div>

                        <div class="text-center py-4">20</div>
                        <div class="text-center py-4 relative bg-blue-500 rounded-lg font-bold">
                            21
                            <div class="absolute bottom-1 left-1/2 transform -translate-x-1/2 w-1 h-1 bg-red-500 rounded-full"></div>
                        </div>
                        <div class="text-center py-4 relative">
                            22
                            <div class="absolute bottom-1 left-1/2 transform -translate-x-1/2 w-1 h-1 bg-green-500 rounded-full"></div>
                        </div>
                        <div class="text-center py-4">23</div>
                        <div class="text-center py-4">24</div>
                        <div class="text-center py-4 relative">
                            25
                            <div class="absolute bottom-1 left-1/2 transform -translate-x-1/2 w-1 h-1 bg-purple-500 rounded-full"></div>
                        </div>
                        <div class="text-center py-4">26</div>

                        <div class="text-center py-4">27</div>
                        <div class="text-center py-4">28</div>
                        <div class="text-center py-4">29</div>
                        <div class="text-center py-4">30</div>
                        <div class="text-center py-4 text-gray-500">1</div>
                        <div class="text-center py-4 text-gray-500">2</div>
                        <div class="text-center py-4 text-gray-500">3</div>
                    </div>
                </div>

                <div class="bg-[#333333] p-6 rounded-xl shadow-lg">
                    <h3 class="text-xl font-bold mb-4 text-white">Study Schedule</h3>
                    <div class="space-y-4">
                        <div class="flex items-center p-3 bg-[#444444] rounded-lg">
                            <div class="w-2 h-full bg-blue-500 rounded-full mr-3"></div>
                            <div class="w-full">
                                <div class="flex justify-between">
                                    <p class="font-medium text-white">Mathematics</p>
                                    <p class="text-sm text-gray-400">2 hrs</p>
                                </div>
                                <p class="text-sm text-gray-400">9:00 AM - 11:00 AM</p>
                            </div>
                        </div>

                        <div class="flex items-center p-3 bg-[#444444] rounded-lg">
                            <div class="w-2 h-full bg-red-500 rounded-full mr-3"></div>
                            <div class="w-full">
                                <div class="flex justify-between">
                                    <p class="font-medium text-white">Physics</p>
                                    <p class="text-sm text-gray-400">1.5 hrs</p>
                                </div>
                                <p class="text-sm text-gray-400">1:00 PM - 2:30 PM</p>
                            </div>
                        </div>

                        <div class="flex items-center p-3 bg-[#444444] rounded-lg">
                            <div class="w-2 h-full bg-green-500 rounded-full mr-3"></div>
                            <div class="w-full">
                                <div class="flex justify-between">
                                    <p class="font-medium text-white">Biology</p>
                                    <p class="text-sm text-gray-400">1 hr</p>
                                </div>
                                <p class="text-sm text-gray-400">3:00 PM - 4:00 PM</p>
                            </div>
                        </div>

                        <div class="flex items-center p-3 bg-[#444444] rounded-lg">
                            <div class="w-2 h-full bg-orange-500 rounded-full mr-3"></div>
                            <div class="w-full">
                                <div class="flex justify-between">
                                    <p class="font-medium text-white">English</p>
                                    <p class="text-sm text-gray-400">1 hr</p>
                                </div>
                                <p class="text-sm text-gray-400">5:00 PM - 6:00 PM</p>
                            </div>
                        </div>

                        <button class="w-full py-3 mt-4 rounded-lg blue-gradient text-white font-medium">
                            Add Study Block
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <section id="resources" class="section">
            <h2 class="text-2xl font-bold mb-6 text-white">Resources</h2>
            <div class="grid grid-cols-12 gap-6">
                <div class="col-span-3">
                    <div class="bg-[#333333] p-4 rounded-xl shadow-lg mb-6">
                        <h3 class="text-lg font-bold text-white mb-3">Categories</h3>

                        <div class="space-y-2">
                            <button class="w-full text-left p-2 rounded bg-[#0055A4] text-white font-medium">
                                <i class="fas fa-users mr-2"></i>Peer Tutoring
                            </button>
                            <button class="w-full text-left p-2 rounded hover:bg-[#444444] text-gray-300">
                                <i class="fas fa-book mr-2"></i>Study Guides
                            </button>
                            <button class="w-full text-left p-2 rounded hover:bg-[#444444] text-gray-300">
                                <i class="fas fa-file-pdf mr-2"></i>Course Materials
                            </button>
                            <button class="w-full text-left p-2 rounded hover:bg-[#444444] text-gray-300">
                                <i class="fas fa-video mr-2"></i>Video Tutorials
                            </button>
                            <button class="w-full text-left p-2 rounded hover:bg-[#444444] text-gray-300">
                                <i class="fas fa-clipboard-list mr-2"></i>Practice Tests
                            </button>
                            <button class="w-full text-left p-2 rounded hover:bg-[#444444] text-gray-300">
                                <i class="fas fa-link mr-2"></i>External Resources
                            </button>
                        </div>
                    </div>

                    <div class="bg-[#333333] p-4 rounded-xl shadow-lg">
                        <h3 class="text-lg font-bold text-white mb-3">Filters</h3>

                        <div class="mb-4">
                            <label class="block text-gray-400 text-sm mb-2">Subject</label>
                            <select class="w-full bg-[#444444] text-white rounded p-2 border border-[#555555]">
                                <option>All Subjects</option>
                                <option>Mathematics</option>
                                <option>Physics</option>
                                <option>Biology</option>
                                <option>English Literature</option>
                                <option>Computer Science</option>
                            </select>
                        </div>

                        <div class="mb-4">
                            <label class="block text-gray-400 text-sm mb-2">Resource Type</label>
                            <select class="w-full bg-[#444444] text-white rounded p-2 border border-[#555555]">
                                <option>All Types</option>
                                <option>Documents</option>
                                <option>Videos</option>
                                <option>Interactive</option>
                                <option>People</option>
                            </select>
                        </div>

                        <div class="mb-4">
                            <label class="block text-gray-400 text-sm mb-2">Rating</label>
                            <div class="flex items-center">
                                <i class="fas fa-star text-[#eded3e]"></i>
                                <i class="fas fa-star text-[#eded3e]"></i>
                                <i class="fas fa-star text-[#eded3e]"></i>
                                <i class="fas fa-star text-gray-500"></i>
                                <i class="fas fa-star text-gray-500"></i>
                                <span class="text-gray-400 ml-2">& above</span>
                            </div>
                        </div>

                        <button class="w-full py-2 mt-4 rounded-lg bg-[#444444] text-white font-medium hover:bg-[#555555]">
                            Apply Filters
                        </button>
                    </div>
                </div>

                <div class="col-span-9">
                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg mb-6">
                        <div class="flex justify-between items-center mb-4">
                            <h3 class="text-xl font-bold text-white">Available Peer Tutors</h3>
                            <button class="px-4 py-2 rounded-lg blue-gradient text-white text-sm font-medium">
                                Become a Tutor
                            </button>
                        </div>

                        <div class="grid grid-cols-3 gap-4 mb-4">
                            <div class="bg-[#444444] p-4 rounded-lg flex items-start space-x-3 card-hover">
                                <div class="w-12 h-12 red-gradient rounded-full flex items-center justify-center text-white font-bold flex-shrink-0">
                                    JS
                                </div>
                                <div>
                                    <h4 class="font-medium text-white">James Smith</h4>
                                    <p class="text-sm text-gray-400">Mathematics, Physics</p>
                                    <div class="flex text-xs text-[#eded3e] mt-1">
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star-half-alt"></i>
                                        <span class="text-gray-400 ml-1">(4.5)</span>
                                    </div>
                                    <button class="mt-2 px-3 py-1 rounded text-xs red-gradient text-white">
                                        Schedule
                                    </button>
                                </div>
                            </div>

                            <div class="bg-[#444444] p-4 rounded-lg flex items-start space-x-3 card-hover">
                                <div class="w-12 h-12 green-gradient rounded-full flex items-center justify-center text-white font-bold flex-shrink-0">
                                    EJ
                                </div>
                                <div>
                                    <h4 class="font-medium text-white">Emma Johnson</h4>
                                    <p class="text-sm text-gray-400">Biology, Chemistry</p>
                                    <div class="flex text-xs text-[#eded3e] mt-1">
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <span class="text-gray-400 ml-1">(5.0)</span>
                                    </div>
                                    <button class="mt-2 px-3 py-1 rounded text-xs green-gradient text-white">
                                        Schedule
                                    </button>
                                </div>
                            </div>

                            <div class="bg-[#444444] p-4 rounded-lg flex items-start space-x-3 card-hover">
                                <div class="w-12 h-12 blue-gradient rounded-full flex items-center justify-center text-white font-bold flex-shrink-0">
                                    MP
                                </div>
                                <div>
                                    <h4 class="font-medium text-white">Michael Patel</h4>
                                    <p class="text-sm text-gray-400">Computer Science</p>
                                    <div class="flex text-xs text-[#eded3e] mt-1">
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="fas fa-star"></i>
                                        <i class="far fa-star"></i>
                                        <span class="text-gray-400 ml-1">(4.0)</span>
                                    </div>
                                    <button class="mt-2 px-3 py-1 rounded text-xs blue-gradient text-white">
                                        Schedule
                                    </button>
                                </div>
                            </div>
                        </div>

                        <div class="text-center">
                            <button class="text-[#0055A4] hover:underline">
                                View All Tutors <i class="fas fa-chevron-right ml-1"></i>
                            </button>
                        </div>
                    </div>

                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg mb-6">
                        <div class="flex justify-between items-center mb-4">
                            <h3 class="text-xl font-bold text-white">Recommended Study Materials</h3>
                            <div class="flex space-x-2">
                                <button class="p-2 rounded-lg bg-[#444444] hover:bg-[#555555]">
                                    <i class="fas fa-th-large text-gray-300"></i>
                                </button>
                                <button class="p-2 rounded-lg bg-[#444444] hover:bg-[#555555]">
                                    <i class="fas fa-list text-gray-300"></i>
                                </button>
                            </div>
                        </div>

                        <div class="grid grid-cols-2 gap-4">
                            <div class="bg-[#444444] p-4 rounded-lg flex space-x-4 card-hover">
                                <div class="w-12 h-12 bg-[#555555] rounded flex items-center justify-center flex-shrink-0">
                                    <i class="fas fa-file-pdf text-[#DC143C] text-xl"></i>
                                </div>
                                <div class="flex-grow">
                                    <div class="flex justify-between">
                                        <h4 class="font-medium text-white">Calculus Formulas Cheatsheet</h4>
                                        <span class="text-xs text-[#0055A4]">PDF</span>
                                    </div>
                                    <p class="text-sm text-gray-400 mt-1">Complete guide to calculus formulas and theorems</p>
                                    <div class="flex justify-between items-center mt-2">
                                        <div class="flex text-xs text-[#eded3e]">
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="far fa-star"></i>
                                        </div>
                                        <button class="text-sm text-[#0055A4]">
                                            <i class="fas fa-download"></i>
                                        </button>
                                    </div>
                                </div>
                            </div>

                            <div class="bg-[#444444] p-4 rounded-lg flex space-x-4 card-hover">
                                <div class="w-12 h-12 bg-[#555555] rounded flex items-center justify-center flex-shrink-0">
                                    <i class="fas fa-video text-[#117C13] text-xl"></i>
                                </div>
                                <div class="flex-grow">
                                    <div class="flex justify-between">
                                        <h4 class="font-medium text-white">Physics - Motion Explained</h4>
                                        <span class="text-xs text-[#117C13]">VIDEO</span>
                                    </div>
                                    <p class="text-sm text-gray-400 mt-1">Clear explanation of Newton's laws of motion</p>
                                    <div class="flex justify-between items-center mt-2">
                                        <div class="flex text-xs text-[#eded3e]">
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star-half-alt"></i>
                                        </div>
                                        <button class="text-sm text-[#117C13]">
                                            <i class="fas fa-play"></i>
                                        </button>
                                    </div>
                                </div>
                            </div>

                            <div class="bg-[#444444] p-4 rounded-lg flex space-x-4 card-hover">
                                <div class="w-12 h-12 bg-[#555555] rounded flex items-center justify-center flex-shrink-0">
                                    <i class="fas fa-clipboard-list text-[#DA7756] text-xl"></i>
                                </div>
                                <div class="flex-grow">
                                    <div class="flex justify-between">
                                        <h4 class="font-medium text-white">Biology Practice Quiz</h4>
                                        <span class="text-xs text-[#DA7756]">QUIZ</span>
                                    </div>
                                    <p class="text-sm text-gray-400 mt-1">Test your knowledge of cellular biology</p>
                                    <div class="flex justify-between items-center mt-2">
                                        <div class="flex text-xs text-[#eded3e]">
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="far fa-star"></i>
                                        </div>
                                        <button class="text-sm text-[#DA7756]">
                                            <i class="fas fa-pen"></i>
                                        </button>
                                    </div>
                                </div>
                            </div>

                            <div class="bg-[#444444] p-4 rounded-lg flex space-x-4 card-hover">
                                <div class="w-12 h-12 bg-[#555555] rounded flex items-center justify-center flex-shrink-0">
                                    <i class="fas fa-laptop-code text-[#8A2BE2] text-xl"></i>
                                </div>
                                <div class="flex-grow">
                                    <div class="flex justify-between">
                                        <h4 class="font-medium text-white">Intro to Python Programming</h4>
                                        <span class="text-xs text-[#8A2BE2]">INTERACTIVE</span>
                                    </div>
                                    <p class="text-sm text-gray-400 mt-1">Learn Python basics with interactive exercises</p>
                                    <div class="flex justify-between items-center mt-2">
                                        <div class="flex text-xs text-[#eded3e]">
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                        </div>
                                        <button class="text-sm text-[#8A2BE2]">
                                            <i class="fas fa-code"></i>
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="text-center mt-4">
                            <button class="text-[#0055A4] hover:underline">
                                View All Materials <i class="fas fa-chevron-right ml-1"></i>
                            </button>
                        </div>
                    </div>

                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg">
                        <h3 class="text-xl font-bold text-white mb-4">Upcoming Group Study Sessions</h3>

                        <div class="space-y-4">
                            <div class="bg-[#444444] p-4 rounded-lg card-hover">
                                <div class="flex justify-between items-center mb-2">
                                    <h4 class="font-medium text-white">Advanced Calculus Study Group</h4>
                                    <span class="text-sm px-2 py-1 bg-[#0055A4] rounded-full text-white">Math</span>
                                </div>
                                <p class="text-sm text-gray-400 mb-3">Hosted by James Smith • Sunday, April 20, 3:00 PM</p>
                                <div class="flex justify-between items-center">
                                    <div class="flex -space-x-2">
                                        <div class="w-8 h-8 blue-gradient rounded-full border-2 border-[#444444] flex items-center justify-center text-white text-xs">
                                            JS
                                        </div>
                                        <div class="w-8 h-8 red-gradient rounded-full border-2 border-[#444444] flex items-center justify-center text-white text-xs">
                                            KL
                                        </div>
                                        <div class="w-8 h-8 green-gradient rounded-full border-2 border-[#444444] flex items-center justify-center text-white text-xs">
                                            AW
                                        </div>
                                        <div class="w-8 h-8 bg-[#555555] rounded-full border-2 border-[#444444] flex items-center justify-center text-white text-xs">
                                            +2
                                        </div>
                                    </div>
                                    <button class="px-3 py-1 rounded blue-gradient text-white text-sm">
                                        Join Session
                                    </button>
                                </div>
                            </div>

                            <div class="bg-[#444444] p-4 rounded-lg card-hover">
                                <div class="flex justify-between items-center mb-2">
                                    <h4 class="font-medium text-white">Physics Exam Prep</h4>
                                    <span class="text-sm px-2 py-1 bg-[#DC143C] rounded-full text-white">Physics</span>
                                </div>
                                <p class="text-sm text-gray-400 mb-3">Hosted by Dr. Reynolds • Monday, April 21, 5:00 PM</p>
                                <div class="flex justify-between items-center">
                                    <div class="flex -space-x-2">
                                        <div class="w-8 h-8 purple-gradient rounded-full border-2 border-[#444444] flex items-center justify-center text-white text-xs">
                                            DR
                                        </div>
                                        <div class="w-8 h-8 orange-gradient rounded-full border-2 border-[#444444] flex items-center justify-center text-white text-xs">
                                            MP
                                        </div>
                                        <div class="w-8 h-8 bg-[#555555] rounded-full border-2 border-[#444444] flex items-center justify-center text-white text-xs">
                                            +7
                                        </div>
                                    </div>
                                    <button class="px-3 py-1 rounded red-gradient text-white text-sm">
                                        Join Session
                                    </button>
                                </div>
                            </div>

                            <div class="bg-[#444444] p-4 rounded-lg card-hover">
                                <div class="flex justify-between items-center mb-2">
                                    <h4 class="font-medium text-white">Biology Study Group</h4>
                                    <span class="text-sm px-2 py-1 bg-[#117C13] rounded-full text-white">Biology</span>
                                </div>
                                <p class="text-sm text-gray-400 mb-3">Hosted by Emma Johnson • Wednesday, April 23, 4:00 PM</p>
                                <div class="flex justify-between items-center">
                                    <div class="flex -space-x-2">
                                        <div class="w-8 h-8 green-gradient rounded-full border-2 border-[#444444] flex items-center justify-center text-white text-xs">
                                            EJ
                                        </div>
                                        <div class="w-8 h-8 blue-gradient rounded-full border-2 border-[#444444] flex items-center justify-center text-white text-xs">
                                            LT
                                        </div>
                                        <div class="w-8 h-8 bg-[#555555] rounded-full border-2 border-[#444444] flex items-center justify-center text-white text-xs">
                                            +4
                                        </div>
                                    </div>
                                    <button class="px-3 py-1 rounded green-gradient text-white text-sm">
                                        Join Session
                                    </button>
                                </div>
                            </div>
                        </div>

                        <div class="mt-4 text-center">
                            <button class="px-4 py-2 rounded-lg border border-[#0055A4] text-[#0055A4] text-sm font-medium hover:bg-[#0055A4] hover:bg-opacity-20">
                                Create Study Group
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <script>
                document.addEventListener('DOMContentLoaded', function() {
                    // Add functionality for resource category buttons
                    const categoryButtons = document.querySelectorAll('#resources .col-span-3 button');
                    categoryButtons.forEach(button => {
                        button.addEventListener('click', function() {
                            // Remove active class from all buttons
                            categoryButtons.forEach(btn => {
                                btn.classList.remove('bg-[#0055A4]', 'text-white');
                                btn.classList.add('hover:bg-[#444444]', 'text-gray-300');
                            });

                            // Add active class to clicked button
                            this.classList.remove('hover:bg-[#444444]', 'text-gray-300');
                            this.classList.add('bg-[#0055A4]', 'text-white');

                            // Here you would normally filter content based on the selected category
                            // This is just a visual demo for now
                        });
                    });
                    // Add hover effects to cards
                    const cards = document.querySelectorAll('.card-hover');
                    cards.forEach(card => {
                        card.addEventListener('mouseenter', function() {
                            this.style.transform = 'translateY(-4px)';
                            this.style.transition = 'transform 0.3s ease';
                        });

                        card.addEventListener('mouseleave', function() {
                            this.style.transform = 'translateY(0)';
                        });
                    });
                });
            </script>
        </section>

        <section id="analytics" class="section">
                <h2 class="text-2xl font-bold mb-6 text-white">Analytics</h2>

                <div class="grid grid-cols-4 gap-6 mb-8">
                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg card-hover">
                        <div class="flex items-center justify-between mb-4">
                            <h3 class="text-gray-400">Total Study Time</h3>
                            <div class="w-8 h-8 purple-gradient rounded-lg"></div>
                        </div>
                        <p class="text-2xl font-bold text-white">147.5 hrs</p>
                        <p class="text-green-400 text-sm">+12.5 from last month</p>
                    </div>

                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg card-hover">
                        <div class="flex items-center justify-between mb-4">
                            <h3 class="text-gray-400">Assignment Score</h3>
                            <div class="w-8 h-8 blue-gradient rounded-lg"></div>
                        </div>
                        <p class="text-2xl font-bold text-white">92%</p>
                        <p class="text-green-400 text-sm">+5% from last semester</p>
                    </div>

                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg card-hover">
                        <div class="flex items-center justify-between mb-4">
                            <h3 class="text-gray-400">Courses Active</h3>
                            <div class="w-8 h-8 orange-gradient rounded-lg"></div>
                        </div>
                        <p class="text-2xl font-bold text-white">5/7</p>
                        <p class="text-blue-400 text-sm">2 completed this term</p>
                    </div>

                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg card-hover">
                        <div class="flex items-center justify-between mb-4">
                            <h3 class="text-gray-400">Productivity Score</h3>
                            <div class="w-8 h-8 green-gradient rounded-lg"></div>
                        </div>
                        <p class="text-2xl font-bold text-white">87/100</p>
                        <p class="yellow-text text-sm">Top 15% of users!</p>
                    </div>
                </div>

                <div class="grid grid-cols-3 gap-6 mb-8">
                    <div class="col-span-2 bg-[#333333] p-6 rounded-xl shadow-lg">
                        <div class="flex justify-between items-center mb-6">
                            <h3 class="text-xl font-bold text-white">Study Time Analysis</h3>
                            <div class="flex space-x-2">
                                <button class="px-3 py-1 rounded bg-[#0055A4] text-white text-sm">Week</button>
                                <button class="px-3 py-1 rounded bg-[#444444] hover:bg-[#555555] text-gray-300 text-sm">Month</button>
                                <button class="px-3 py-1 rounded bg-[#444444] hover:bg-[#555555] text-gray-300 text-sm">Semester</button>
                            </div>
                        </div>

                        <div class="h-64 flex items-end justify-between space-x-2">
                            <div class="flex flex-col items-center w-full">
                                <div class="blue-gradient w-full rounded-t-sm" style="height: 35%"></div>
                                <p class="text-xs text-gray-400 mt-2">Mon</p>
                            </div>
                            <div class="flex flex-col items-center w-full">
                                <div class="blue-gradient w-full rounded-t-sm" style="height: 65%"></div>
                                <p class="text-xs text-gray-400 mt-2">Tue</p>
                            </div>
                            <div class="flex flex-col items-center w-full">
                                <div class="blue-gradient w-full rounded-t-sm" style="height: 45%"></div>
                                <p class="text-xs text-gray-400 mt-2">Wed</p>
                            </div>
                            <div class="flex flex-col items-center w-full">
                                <div class="blue-gradient w-full rounded-t-sm" style="height: 80%"></div>
                                <p class="text-xs text-gray-400 mt-2">Thu</p>
                            </div>
                            <div class="flex flex-col items-center w-full">
                                <div class="blue-gradient w-full rounded-t-sm" style="height: 50%"></div>
                                <p class="text-xs text-gray-400 mt-2">Fri</p>
                            </div>
                            <div class="flex flex-col items-center w-full">
                                <div class="blue-gradient w-full rounded-t-sm" style="height: 30%"></div>
                                <p class="text-xs text-gray-400 mt-2">Sat</p>
                            </div>
                            <div class="flex flex-col items-center w-full">
                                <div class="blue-gradient w-full rounded-t-sm" style="height: 20%"></div>
                                <p class="text-xs text-gray-400 mt-2">Sun</p>
                            </div>
                        </div>

                        <div class="flex justify-between mt-8">
                            <div>
                                <p class="text-sm text-gray-400">Average Daily</p>
                                <p class="text-xl font-bold text-white">3.5 hrs</p>
                            </div>
                            <div>
                                <p class="text-sm text-gray-400">Most Productive</p>
                                <p class="text-xl font-bold text-white">Thursday</p>
                            </div>
                            <div>
                                <p class="text-sm text-gray-400">Total Weekly</p>
                                <p class="text-xl font-bold text-white">24.5 hrs</p>
                            </div>
                        </div>
                    </div>

                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg">
                        <h3 class="text-xl font-bold text-white mb-4">Time Distribution</h3>
                        <div class="space-y-6">
                            <div>
                                <div class="flex justify-between text-sm mb-1">
                                    <span class="text-[#0055A4]">Mathematics</span>
                                    <span class="text-gray-400">8.5 hrs (35%)</span>
                                </div>
                                <div class="w-full bg-[#444444] rounded-full h-2">
                                    <div class="blue-gradient h-2 rounded-full" style="width: 35%"></div>
                                </div>
                            </div>

                            <div>
                                <div class="flex justify-between text-sm mb-1">
                                    <span class="text-[#DC143C]">Physics</span>
                                    <span class="text-gray-400">6 hrs (24%)</span>
                                </div>
                                <div class="w-full bg-[#444444] rounded-full h-2">
                                    <div class="red-gradient h-2 rounded-full" style="width: 24%"></div>
                                </div>
                            </div>

                            <div>
                                <div class="flex justify-between text-sm mb-1">
                                    <span class="text-[#117C13]">Biology</span>
                                    <span class="text-gray-400">4.5 hrs (18%)</span>
                                </div>
                                <div class="w-full bg-[#444444] rounded-full h-2">
                                    <div class="green-gradient h-2 rounded-full" style="width: 18%"></div>
                                </div>
                            </div>

                            <div>
                                <div class="flex justify-between text-sm mb-1">
                                    <span class="text-[#DA7756]">English</span>
                                    <span class="text-gray-400">3 hrs (12%)</span>
                                </div>
                                <div class="w-full bg-[#444444] rounded-full h-2">
                                    <div class="orange-gradient h-2 rounded-full" style="width: 12%"></div>
                                </div>
                            </div>

                            <div>
                                <div class="flex justify-between text-sm mb-1">
                                    <span class="text-[#8A2BE2]">Computer Science</span>
                                    <span class="text-gray-400">2.5 hrs (10%)</span>
                                </div>
                                <div class="w-full bg-[#444444] rounded-full h-2">
                                    <div class="purple-gradient h-2 rounded-full" style="width: 10%"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="grid grid-cols-3 gap-6">
                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg">
                        <h3 class="text-xl font-bold text-white mb-4">Performance Metrics</h3>

                        <div class="space-y-4">
                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex justify-between mb-1">
                                    <h4 class="font-medium text-white">Assignment Completion</h4>
                                    <span class="text-green-400">95%</span>
                                </div>
                                <div class="w-full bg-[#555555] rounded-full h-2">
                                    <div class="green-gradient h-2 rounded-full" style="width: 95%"></div>
                                </div>
                            </div>

                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex justify-between mb-1">
                                    <h4 class="font-medium text-white">Quiz Average</h4>
                                    <span class="text-blue-400">87%</span>
                                </div>
                                <div class="w-full bg-[#555555] rounded-full h-2">
                                    <div class="blue-gradient h-2 rounded-full" style="width: 87%"></div>
                                </div>
                            </div>

                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex justify-between mb-1">
                                    <h4 class="font-medium text-white">Attendance</h4>
                                    <span class="yellow-text">100%</span>
                                </div>
                                <div class="w-full bg-[#555555] rounded-full h-2">
                                    <div style="background: linear-gradient(135deg, #eded3e 0%, #b5b52f 100%)" class="h-2 rounded-full w-full"></div>
                                </div>
                            </div>

                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex justify-between mb-1">
                                    <h4 class="font-medium text-white">Study Efficiency</h4>
                                    <span class="text-orange-400">82%</span>
                                </div>
                                <div class="w-full bg-[#555555] rounded-full h-2">
                                    <div class="orange-gradient h-2 rounded-full" style="width: 82%"></div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg">
                        <div class="flex justify-between items-center mb-4">
                            <h3 class="text-xl font-bold text-white">Study Goals</h3>
                            <button class="p-2 rounded-full bg-[#444444] hover:bg-[#555555]">
                                <i class="fas fa-plus text-gray-300"></i>
                            </button>
                        </div>

                        <div class="space-y-4">
                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex justify-between items-start">
                                    <div>
                                        <h4 class="font-medium text-white">30 hours weekly study time</h4>
                                        <p class="text-sm text-gray-400 mt-1">24.5/30 hours completed</p>
                                    </div>
                                    <span class="text-sm bg-[#0055A4] text-white px-2 py-1 rounded-full">82%</span>
                                </div>
                                <div class="w-full bg-[#555555] rounded-full h-2 mt-3">
                                    <div class="blue-gradient h-2 rounded-full" style="width: 82%"></div>
                                </div>
                            </div>

                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex justify-between items-start">
                                    <div>
                                        <h4 class="font-medium text-white">Complete Physics project</h4>
                                        <p class="text-sm text-gray-400 mt-1">Due in 5 days</p>
                                    </div>
                                    <span class="text-sm bg-[#DC143C] text-white px-2 py-1 rounded-full">60%</span>
                                </div>
                                <div class="w-full bg-[#555555] rounded-full h-2 mt-3">
                                    <div class="red-gradient h-2 rounded-full" style="width: 60%"></div>
                                </div>
                            </div>

                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex justify-between items-start">
                                    <div>
                                        <h4 class="font-medium text-white">Improve quiz scores to 90%</h4>
                                        <p class="text-sm text-gray-400 mt-1">Current: 87%</p>
                                    </div>
                                    <span class="text-sm bg-[#117C13] text-white px-2 py-1 rounded-full">97%</span>
                                </div>
                                <div class="w-full bg-[#555555] rounded-full h-2 mt-3">
                                    <div class="green-gradient h-2 rounded-full" style="width: 97%"></div>
                                </div>
                            </div>

                            <div class="text-center mt-2">
                                <button class="text-[#0055A4] hover:underline text-sm">
                                    View All Goals <i class="fas fa-chevron-right ml-1"></i>
                                </button>
                            </div>
                        </div>
                    </div>

                    <div class="bg-[#333333] p-6 rounded-xl shadow-lg">
                        <h3 class="text-xl font-bold text-white mb-4">Learning Insights</h3>

                        <div class="space-y-4">
                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex items-center space-x-3">
                                    <div class="w-8 h-8 blue-gradient rounded-full flex items-center justify-center">
                                        <i class="fas fa-lightbulb text-white text-sm"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-medium text-white">Peak Productivity</h4>
                                        <p class="text-sm text-gray-400">You focus best between 9AM-11AM</p>
                                    </div>
                                </div>
                            </div>

                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex items-center space-x-3">
                                    <div class="w-8 h-8 red-gradient rounded-full flex items-center justify-center">
                                        <i class="fas fa-exclamation text-white text-sm"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-medium text-white">Focus Area</h4>
                                        <p class="text-sm text-gray-400">Physics needs more attention</p>
                                    </div>
                                </div>
                            </div>

                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex items-center space-x-3">
                                    <div class="w-8 h-8 green-gradient rounded-full flex items-center justify-center">
                                        <i class="fas fa-check text-white text-sm"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-medium text-white">Strong Subject</h4>
                                        <p class="text-sm text-gray-400">Computer Science (95% average)</p>
                                    </div>
                                </div>
                            </div>

                            <div class="p-4 bg-[#444444] rounded-lg">
                                <div class="flex items-center space-x-3">
                                    <div class="w-8 h-8 purple-gradient rounded-full flex items-center justify-center">
                                        <i class="fas fa-trophy text-white text-sm"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-medium text-white">Achievement</h4>
                                        <p class="text-sm text-gray-400">7-day study streak! Keep it up!</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="mt-8 flex justify-center">
                    <button class="px-6 py-3 rounded-lg blue-gradient text-white font-medium">
                        <i class="fas fa-download mr-2"></i>Generate Progress Report
                    </button>
                </div>
            </section>

            <script>
                document.addEventListener('DOMContentLoaded', function() {
                    // Time analysis period switcher
                    const periodButtons = document.querySelectorAll('#analytics .col-span-2 button');
                    periodButtons.forEach(button => {
                        button.addEventListener('click', function() {
                            // Remove active class from all buttons
                            periodButtons.forEach(btn => {
                                btn.classList.remove('bg-[#0055A4]', 'text-white');
                                btn.classList.add('bg-[#444444]', 'hover:bg-[#555555]', 'text-gray-300');
                            });

                            // Add active class to clicked button
                            this.classList.remove('bg-[#444444]', 'hover:bg-[#555555]', 'text-gray-300');
                            this.classList.add('bg-[#0055A4]', 'text-white');

                            // In a real application, you would update the chart data here
                        });
                    });

                    // Make chart columns interactive
                    const chartColumns = document.querySelectorAll('#analytics .h-64 .flex-col');
                    chartColumns.forEach(column => {
                        column.addEventListener('mouseenter', function() {
                            const bar = this.querySelector('div');
                            bar.style.opacity = '0.8';

                            // Create and show tooltip (simplified implementation)
                            const day = this.querySelector('p').textContent;
                            const height = parseFloat(bar.style.height);
                            const hours = (height / 100 * 8).toFixed(1);

                            const tooltip = document.createElement('div');
                            tooltip.classList.add('bg-[#222222]', 'text-white', 'p-2', 'rounded', 'absolute', 'text-xs');
                            tooltip.style.bottom = `calc(${height}% + 20px)`;
                            tooltip.style.left = '50%';
                            tooltip.style.transform = 'translateX(-50%)';
                            tooltip.style.zIndex = '10';
                            tooltip.textContent = `${day}: ${hours} hrs`;

                            this.style.position = 'relative';
                            this.appendChild(tooltip);
                        });
                        column.addEventListener('mouseleave', function() {
                            const bar = this.querySelector('div');
                            bar.style.opacity = '1';

                            // Remove tooltip
                            const tooltip = this.querySelector('div.absolute');
                            if (tooltip) {
                                this.removeChild(tooltip);
                            }
                        });
                    });
                });
            </script>

    <script>
        // Navigation functionality
        document.addEventListener('DOMContentLoaded', function() {
            const sidebarItems = document.querySelectorAll('.sidebar-item');
            const sections = document.querySelectorAll('.section');

            sidebarItems.forEach(item => {
                item.addEventListener('click', function(e) {
                    e.preventDefault();

                    // Remove active class from all sidebar items
                    sidebarItems.forEach(sidebarItem => {
                        sidebarItem.classList.remove('active');
                    });

                    // Add active class to clicked item
                    this.classList.add('active');

                    // Show corresponding section
                    const targetSection = this.getAttribute('data-section');

                    // Hide all sections
                    sections.forEach(section => {
                        section.classList.remove('active');
                    });

                    // Show target section
                    document.getElementById(targetSection).classList.add('active');
                });
            });
        });
    </script>
</body>
</html>
