<template>
  <section class="relative overflow-hidden">
    <!-- background glow -->
    <div class="pointer-events-none absolute inset-0">
      <div class="absolute -top-24 left-1/2 h-72 w-72 -translate-x-1/2 rounded-full bg-sky-500/10 blur-3xl"></div>
      <div class="absolute -bottom-24 right-10 h-72 w-72 rounded-full bg-indigo-500/10 blur-3xl"></div>
    </div>

    <div class="mx-auto w-full max-w-7xl px-6 lg:px-10 pt-16 pb-10">
      <!-- <div class="inline-flex items-center gap-2 rounded-full border border-white/10 bg-white/5 px-4 py-2 text-sm text-slate-300">
        <span class="h-2 w-2 rounded-full bg-emerald-400"></span>
        Available for freelance backend work
      </div> -->

      <h1 class="mt-6 text-4xl font-bold tracking-tight md:text-6xl">
        Backend Web Developer
      </h1>

      <p class="mt-4 max-w-2xl text-slate-300 leading-relaxed">
        I build secure backend systems and REST APIs using <span class="text-white font-medium">PHP/Laravel</span> and
        <span class="text-white font-medium">MySQL</span>. I also handle frontend integration using
        <span class="text-white font-medium">JavaScript / jQuery</span>.
      </p>

      <div class="mt-7 flex flex-wrap gap-3">
        <a href="#projects"
           class="rounded-xl bg-white text-slate-900 px-5 py-3 font-semibold hover:bg-slate-100 transition">
          View Projects
        </a>
        <a href="#contact"
           class="rounded-xl border border-white/15 bg-white/5 px-5 py-3 font-semibold text-white hover:bg-white/10 transition">
          Contact Me
        </a>
      </div>

      <div class="mt-10 grid gap-3 sm:grid-cols-3">
        <div class="rounded-2xl border border-white/10 bg-white/5 p-4">
          <p class="text-sm text-slate-400">Experience</p>
          <p class="mt-1 text-xl font-semibold">3+ years</p>
        </div>
        <div class="rounded-2xl border border-white/10 bg-white/5 p-4">
          <p class="text-sm text-slate-400">Focus</p>
          <p class="mt-1 text-xl font-semibold">APIs & Dashboards</p>
        </div>
        <div class="rounded-2xl border border-white/10 bg-white/5 p-4">
          <p class="text-sm text-slate-400">Stack</p>
          <p class="mt-1 text-xl font-semibold">PHP/Laravel • MySQL • JavaScript/jQuery/Vue</p>
        </div>
      </div>
    </div>
  </section>
</template>