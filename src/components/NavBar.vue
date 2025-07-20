<template>
    <header class="sticky-top bg-white border-bottom shadow-sm">
      <nav class="container d-flex justify-content-between py-2">
        <span class="fw-bold">Gustavo Silva</span>
        <ul class="nav">
          <li class="nav-item"><a href="#contact" class="nav-link px-2">Contact</a></li>
          <li class="nav-item"><a href="#experience" class="nav-link px-2">Experience</a></li>
          <li class="nav-item"><a href="#education" class="nav-link px-2">Education</a></li>
          <li class="nav-item"><a href="#skills" class="nav-link px-2">Skills</a></li>
          <li class="nav-item"><a href="#projects" class="nav-link px-2">Projects</a></li>
          <li class="nav-item"><a href="#languages" class="nav-link px-2">Languages</a></li>
          <li class="nav-item">
            <div class="form-check form-switch">
                <input class="form-check-input" type="checkbox" role="switch" id="switchCheckDefault" v-model.lazy="darkMode" :aria-checked="darkMode" @changed="darkMode = !darkMode" switch>
                <label class="form-check-label" for="switchCheckDefault">{{ darkMode ? 'Light Mode' : 'Dark Mode' }}</label>
            </div>
          </li>
          <li class="nav-item">
            <button class="btn btn-sm btn-outline-primary ms-3" @click="printCV">Print CV</button>
          </li>
        </ul>
      </nav>
    </header>
</template>

<script setup>
    import { ref, watch } from 'vue'

    const darkMode = ref(false)

    watch(darkMode, (val) => {
        document.body.classList.toggle('bg-dark', val)
        document.body.classList.toggle('text-light', val)
    })

    function printCV() {
        window.print()
    }
</script>