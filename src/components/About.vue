<template>
    <section id="about" class="py-20">
        <div class="mx-auto max-w-7xl px-6 lg:px-10">

            <h2 class="text-3xl font-bold mb-10">About Me</h2>

            <div class="grid md:grid-cols-2 gap-12 items-start">

                <!-- PHOTO -->
                <div class="flex justify-center">
                    <img
                        :src="profileUrl"
                        alt="Profile"
                        class="w-64 h-74 object-cover rounded-2xl border border-white/10 shadow-lg"
                    />  
                </div>

                <!-- ABOUT INFO -->
                <div>

                    <p class="text-slate-300 leading-relaxed">
                        I am a backend web developer with 3+ years of experience specializing in 
                        PHP and MySQL. I develop web systems, monitoring systems, inventory 
                        systems, and admin dashboards.
                    </p>
                    <!-- INFO LIST -->
                    <div class="mt-6 space-y-3 text-slate-300">

                        <p>
                            <span class="text-white font-semibold">Name:</span> Diomedes E. Castillo Jr
                        </p>

                        <p>
                            <span class="text-white font-semibold">Experience:</span> 3+ years
                        </p>

                        <p>
                            <span class="text-white font-semibold">Specialization:</span> Backend Development
                        </p>

                        <p>
                            <span class="text-white font-semibold">Tech Stack:</span> PHP, MySQL, JavaScript, jQuery
                        </p>

                        <p>
                            <span class="text-white font-semibold">Location:</span> Cabuyao, Laguna, Philippines
                        </p>

                    </div>

                    <!-- EXPERIENCE -->
                    <div class="mt-8">

                        <h3 class="text-xl font-semibold mb-6">Experience</h3>

                        <div class="space-y-6">

                            <!-- JOB 1 -->
                            <div class="border-l border-white/10 pl-5">
                                <p class="font-semibold text-white">
                                    Backend Developer
                                </p>

                                <p class="text-slate-400 text-sm">
                                    Torres Technology • Apr 2021 – Oct 2021
                                </p>

                                <ul class="mt-2 text-slate-300 text-sm list-disc ml-4 space-y-1">
                                    <li>Contributed to development of a custom accounting system.</li>
                                    <li>Improved user interface and website structure.</li>
                                    <li>Implemented financial computations and report generation.</li>
                                </ul>
                            </div>

                            <!-- JOB 2 -->
                            <div class="border-l border-white/10 pl-5">
                                <p class="font-semibold text-white">
                                    Backend Developer
                                </p>

                                <p class="text-slate-400 text-sm">
                                    Umbra Digital Company • Apr 2022 – Jun 2025
                                </p>

                                <ul class="mt-2 text-slate-300 text-sm list-disc ml-4 space-y-1">
                                    <li>Developed monitoring and inventory systems.</li>
                                    <li>Built modules for order processing and stock tracking.</li>
                                    <li>Handled bug fixing and system maintenance.</li>
                                    <li>Implemented new features to improve workflow efficiency.</li>
                                </ul>
                            </div>

                        </div>
                    </div>

                </div>

            </div>

        </div>
    </section>
</template>

<script setup>
    const base = document.querySelector('base')?.href || window.location.origin + '/'
    const profileUrl = base + 'images/profile.jpg'
</script>
