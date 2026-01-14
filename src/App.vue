<script setup lang="ts">
import { ref } from 'vue'

const showPassword = ref(false)

function togglePassword() {
  showPassword.value = !showPassword.value
}

</script>

<template>
  <div class="container-fluid vh-100 bg-light position-relative overflow-hidden">
    <div class="row h-100 gx-4 p-4">

      <!-- LEFT PANEL -->
      <div class="col-lg-7 d-none d-lg-flex">
        <div class="left-panel text-white w-100 h-100 p-5 position-relative">

          <!-- Header -->
          <div class="d-flex align-items-center mb-5">
            <img
               src="./resources/image 6.png"
               alt="Logo"
               class="logo-img"
            />
            <div class="logo-divider mx-3"></div>
            <div class="fw-semibold fs-5 lh-sm">
             BKPSDM<br />KABUPATEN MUNA BARAT
            </div>
          </div>

          <!-- Title -->
          <div class="mb-4 text-center">
            <span class="badge bg-blue-700 px-5 py-3 fs-2 rounded-4">LIWU MOKESA</span>
          </div>

          <!-- Illustration placeholder -->
          <img
            src="./resources/intractive monitors 1.png"
            class="illustration-img"
          />

          <!-- Description -->
          <div class="mt-auto d-flex">
            <div class="w-60 ms-auto lh-lg">
              <div class="fw-bold mb-2">
                SIM ASN (Sistem Informasi Manajemen Aparatur Sipil Negara)
              </div>

              <div class="text-divider mb-2"></div>

              <div>
                adalah platform digital untuk memudahkan ASN dalam pelaporan aktivitas
                kinerja dan kehadiran kerja berbasis Website dan Mobile App.
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- RIGHT PANEL -->
      <div class="col-lg-5 d-flex align-items-center justify-content-center position-relative">
        <div class="w-75 px-4 position-relative">

          <!-- Logo -->
          <div class="text-center mb-5">
            <img
              src="./resources/Group 33742.svg"
              alt="SIM-ASN"
              class="login-logo mb-2"
            />
          </div>

          <!-- Form -->
          <h4 class="fw-bold mb-5 fs-1">Masuk Akun</h4>

          <div class="mb-4">
            <label class="form-label small fw-semibold">NOMOR INDUK PEGAWAI (NIP)</label>
            <div class="input-group">
              <input class="form-control form-control-lg" placeholder="Masukkan Username" />
              <button class="btn btn-outline-secondary" type="button">
                <i class="bi bi-person-fill"></i>
              </button>
            </div>
          </div>

          <div class="mb-5">
            <label class="form-label small fw-semibold">PASSWORD</label>
            <div class="input-group">
              <input :type="showPassword ? 'text' : 'password'" class="form-control form-control-lg" placeholder="Masukkan Password" />
              <button class="btn btn-outline-secondary" type="button" @click="togglePassword">
                <i class="bi" :class="showPassword ? 'bi-eye-fill' : 'bi-eye-slash-fill'"></i>
              </button>
            </div>
          </div>

          <button class="btn btn-warning text-white w-100 fw-semibold mb-5">
            Login
          </button>

          <!-- Store buttons -->
          <div class="d-flex justify-content-center gap-3 mb-5">
            <img
              src="./resources/Palystore.svg"
              alt="Play Store"
              class="store-btn"
            />
            <img
              src="./resources/Appstore.svg"
              alt="Play Store"
              class="store-btn"
            />
          </div>

          <!-- Footer -->
          <div class="d-flex align-items-center justify-content-center text-muted fs-5 gap-3 mt-4">
            <img
              src="./resources/Group.svg"
              alt="Afila Media Karya"
              class="footer-logo"
            />
            <span>
              Crafted by <span class="text-primary fw-semibold">Afila Media KW</span>
            </span>
          </div>
        </div>
      </div>

    </div>

    <!-- Decorative blobs -->
    <div class="blob blob-top"></div>
    <div class="blob blob-bottom"></div>
  </div>
</template>

<style scoped>

.form-control::placeholder {
  color: rgba(0, 0, 0, 0.3);
}

.w-60 {
  width: 60%;
}

.bg-blue-700 {
  background-color: #0B4EB5;
}

.left-panel {
  background: linear-gradient(
    135deg,
    rgba(50, 79, 159, 0.60) 0%,
    rgba(0, 68, 255, 0.70) 100%
  );
  border-radius: 24px;
  display: flex;
  flex-direction: column;
  position: relative;
  overflow: hidden;
}

.text-divider {
  width: 100%;
  height: 2px;
  background-color: rgba(255, 255, 255, 1);
}

.left-panel > * {
  position: relative;
  z-index: 2;
}

.logo-img {
  width: 50px;
  height: 50px;
  object-fit: contain;
}

.logo-divider {
  width: 4px;
  height: 44px;
  background-color: rgba(255, 255, 255, 1);
  border-radius: 2px;
}

.illustration-img {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 820px;
  max-width: 72%;
  z-index: 1;
  pointer-events: none;
}

.login-logo {
  height: 76px;
  width: auto;
}

.store-btn {
  min-width: 140px;
  width: 192px;
  height: 60px; 
  border-radius: 2px;  
  background: rgba(0,0,0,0);
}

.footer-logo {
  height: 26px;
  width: auto;
}

.blob {
  position: absolute;
  width: 260px;
  height: 260px;
  background: radial-gradient(circle, rgba(255,200,100,0.6), transparent 70%);
  filter: blur(40px);
  pointer-events: none;
}

.blob-top {
  top: -80px;
  right: -80px;
}

.blob-bottom {
  bottom: -80px;
  right: 120px;
}
</style>
