<template>
  <section id="projects" class="py-26">
    <div class="mx-auto max-w-7xl px-6 lg:px-10">
      <h2 class="text-3xl font-bold mb-10">Project</h2>

      <div class="grid md:grid-cols-2 gap-12 items-start bg-white/5 border border-white/10 rounded-2xl p-8">

        <!-- SLIDER -->
        <div class="space-y-3">
          <div class="relative overflow-hidden rounded-xl border border-white/10 bg-slate-900">
            <img
                :src="images[current]"
                @click="openPreview(images[current])"
                class="w-full h-64 md:h-80 object-cover rounded-xl border border-white/10 cursor-pointer hover:opacity-90"
            />

            <!-- Prev / Next -->
            <button
              type="button"
              @click="prev"
              class="absolute left-3 top-1/2 -translate-y-1/2 rounded-full border border-white/10 bg-slate-950/60 backdrop-blur px-3 py-2 text-white hover:bg-slate-950/80 transition"
              aria-label="Previous image"
            >
              ‹
            </button>

            <button
              type="button"
              @click="next"
              class="absolute right-3 top-1/2 -translate-y-1/2 rounded-full border border-white/10 bg-slate-950/60 backdrop-blur px-3 py-2 text-white hover:bg-slate-950/80 transition"
              aria-label="Next image"
            >
              ›
            </button>

            <!-- Counter -->
            <div class="absolute bottom-3 right-3 rounded-full border border-white/10 bg-slate-950/60 backdrop-blur px-3 py-1 text-xs text-slate-200">
              {{ current + 1 }} / {{ images.length }}
            </div>
          </div>

          <!-- Thumbnails -->
          <div class="grid grid-cols-4 gap-2">
            <button
              v-for="(img, i) in images"
              :key="img"
              type="button"
              @click="go(i)"
              class="group overflow-hidden rounded-lg border border-white/10 bg-white/5 hover:bg-white/10 transition"
              :class="i === current ? 'ring-2 ring-white/30' : ''"
              aria-label="Select image"
            >
              <img :src="img" class="h-16 w-full object-cover opacity-90 group-hover:opacity-100" />
            </button>
          </div>

          <!-- Dots -->
          <div class="flex justify-center gap-2 pt-1">
            <button
              v-for="(_, i) in images"
              :key="i"
              type="button"
              @click="go(i)"
              class="h-2 w-2 rounded-full transition"
              :class="i === current ? 'bg-white' : 'bg-white/30 hover:bg-white/50'"
              aria-label="Go to image"
            />
          </div>
        </div>

        <!-- PROJECT INFO -->
        <div>
          <h3 class="text-2xl font-semibold text-white">
            Truck Delivery Monitoring System
          </h3>

          <p class="mt-4 text-slate-300 leading-relaxed">
            A web-based monitoring system used to track delivery transactions,
            drivers, and vehicles. The system helps administrators monitor
            operations, manage deliveries, and improve workflow efficiency.
          </p>

          <!-- TECH STACK -->
          <div class="mt-5 flex flex-wrap gap-2 text-slate-200">
            <span class="rounded-full border border-white/10 bg-white/5 px-3 py-1 text-xs">Laravel/PHP</span>
            <span class="rounded-full border border-white/10 bg-white/5 px-3 py-1 text-xs">MySQL</span>
            <span class="rounded-full border border-white/10 bg-white/5 px-3 py-1 text-xs">JavaScript</span>
            <span class="rounded-full border border-white/10 bg-white/5 px-3 py-1 text-xs">Alpine</span>
            <span class="rounded-full border border-white/10 bg-white/5 px-3 py-1 text-xs">Tailwind</span>
          </div>

          <!-- FEATURES -->
          <ul class="mt-6 space-y-2 text-slate-300 text-sm">
            <li>• Transaction and delivery monitoring</li>
            <li>• Driver and vehicle management</li>
            <li>• Role-based access (Admin / Driver)</li>
            <li>• Dashboard reporting and tracking</li>
            <li>• System maintenance and performance improvements</li>
          </ul>

          <!-- GITHUB LINK -->
            <div class="mt-6">
                <a
                    href="https://github.com/jayrcastillo007/truck-delivery-tracking-system"
                    target="_blank"
                    class="inline-flex items-center gap-2 rounded-lg border border-white/10 bg-white/5 px-4 py-2 text-sm font-semibold text-white hover:bg-white/10 transition"
                >
                    View Source Code
                </a>
            </div>
        </div>

        <div
            v-if="showPreview"
            class="fixed inset-0 bg-black/80 flex items-center justify-center z-50"
            @click="showPreview = false"
            >

            <img
            :src="previewImage"
            class="max-w-[90%] max-h-[90%] rounded-xl shadow-2xl"
            />

        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
    import { onMounted, onBeforeUnmount, ref } from 'vue'

    // import { ref } from "vue"

    const showPreview = ref(false)
    const previewImage = ref(null)

    function openPreview(img){
    previewImage.value = img
    showPreview.value = true
    }

    const images = [
        '/images/projects/track1.png',
        '/images/projects/track2.png',
        '/images/projects/track3.png',
        '/images/projects/track4.png',
        '/images/projects/track5.png',
        '/images/projects/track6.png',
        '/images/projects/track7.png',
        '/images/projects/track8.png',
    ]

    const current = ref(0)

    function go(i) {
        current.value = i
    }

    function next() {
        current.value = (current.value + 1) % images.length
    }

    function prev() {
        current.value = (current.value - 1 + images.length) % images.length
    }

    function onKey(e) {
        if (e.key === 'ArrowRight') next()
        if (e.key === 'ArrowLeft') prev()
    }

    onMounted(() => window.addEventListener('keydown', onKey))
    onBeforeUnmount(() => window.removeEventListener('keydown', onKey))
</script>