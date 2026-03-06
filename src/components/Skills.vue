<template>
  <section id="skills" class="py-16">
    <div class="flex items-end justify-between gap-4">
      <div>
        <h2 class="text-3xl font-bold">Skills</h2>
        <p class="mt-2 text-slate-300">What I use to build production-ready web apps.</p>
      </div>
    </div>

    <div class="mt-8 grid gap-4 md:grid-cols-3">
      <div class="rounded-2xl border border-white/10 bg-white/5 p-6 hover:bg-white/10 transition">
        <p class="text-sm text-slate-400">Backend</p>
        <h3 class="mt-2 font-semibold text-lg">Laravel / PHP</h3>
        <p class="mt-2 text-slate-300 text-sm">REST APIs, auth, roles, admin systems.</p>
        <div class="mt-4 flex flex-wrap gap-2">
            <span class="rounded-full border border-white/10 bg-white/5 px-3 py-1 text-xs text-slate-200">Laravel</span>
            <span class="rounded-full border border-white/10 bg-white/5 px-3 py-1 text-xs text-slate-200">PHP</span>
            <span class="rounded-full border border-white/10 bg-white/5 px-3 py-1 text-xs text-slate-200">REST API</span>
        </div>
      </div>

      <div class="rounded-2xl border border-white/10 bg-white/5 p-6 hover:bg-white/10 transition">
        <p class="text-sm text-slate-400">Database</p>
        <h3 class="mt-2 font-semibold text-lg">MySQL</h3>
        <p class="mt-2 text-slate-300 text-sm">Schema design, queries, optimization.</p>
        <div class="mt-4 flex flex-wrap gap-2">
          <span class="tag">MySQL</span>
          <span class="tag">Eloquent</span>
          <span class="tag">Migrations</span>
        </div>
      </div>

      <div class="rounded-2xl border border-white/10 bg-white/5 p-6 hover:bg-white/10 transition">
        <p class="text-sm text-slate-400">Frontend</p>
        <h3 class="mt-2 font-semibold text-lg">jQuery / Vue / Tailwind / Bootstrap</h3>
        <p class="mt-2 text-slate-300 text-sm">Components, UI, responsive pages.</p>
        <div class="mt-4 flex flex-wrap gap-2">
          <span class="tag">Vue</span>
          <span class="tag">Tailwind</span>
          <span class="tag">jQuery</span>
        </div>
      </div>
    </div>
  </section>
</template>
