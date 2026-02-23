<template>
  <q-layout view="hHh lpR fff" class="system-layout">
    <!-- Navbar / Header -->
    <q-header class="glass-header q-py-sm" elevated>
      <q-toolbar class="q-px-lg q-px-md-xl window-width" style="max-width: 1400px; margin: 0 auto">
        <!-- Logo -->
        <div class="row items-center no-wrap cursor-pointer" @click="$router.push('/')">
          <!-- We can use a stylized icon as a logo -->
          <div class="logo-icon-wrap q-mr-sm row flex-center">
            <q-icon name="dashboard_customize" color="white" size="24px" />
          </div>
          <div class="text-h6 text-weight-bolder letter-spacing-1">
            KGH <span class="text-primary">CUSTO</span>
          </div>
        </div>

        <q-space />

        <!-- Desktop Navigation -->
        <div class="gt-sm row gap-4 items-center q-mr-xl">
          <q-btn flat no-caps label="Features" class="nav-btn text-weight-bold" />
          <q-btn flat no-caps label="How it works" class="nav-btn text-weight-bold" />
          <q-btn flat no-caps label="Testimonials" class="nav-btn text-weight-bold" />
          <q-btn flat no-caps label="Pricing" class="nav-btn text-weight-bold" />
        </div>

        <!-- Auth Buttons -->
        <div class="row items-center no-wrap gap-3">
          <q-btn flat no-caps label="Login" class="text-weight-bold nav-btn gt-xs" />
          <q-btn
            unelevated
            no-caps
            color="primary"
            label="Sign Up"
            class="q-px-md q-py-xs text-weight-bold rounded-borders glow-btn"
          />

          <!-- Mobile Menu -->
          <q-btn flat round dense icon="menu" class="lt-md q-ml-sm" />
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <!-- Footer -->
    <q-footer class="bg-black text-white border-top-dark q-py-xl q-mt-xl">
      <div class="q-px-lg q-px-md-xl" style="max-width: 1400px; margin: 0 auto">
        <div class="row q-col-gutter-xl">
          <!-- Brand & Info -->
          <div class="col-12 col-md-4">
            <div class="row items-center no-wrap q-mb-md">
              <div class="logo-icon-wrap-small q-mr-sm row flex-center">
                <q-icon name="dashboard_customize" color="white" size="18px" />
              </div>
              <div class="text-h6 text-weight-bolder">
                KGH <span class="text-primary">CUSTO</span>
              </div>
            </div>
            <p class="text-grey-5" style="max-width: 300px; line-height: 1.6">
              The ultimate customer management system designed for modern businesses to scale
              securely and efficiently.
            </p>
            <div class="row gap-2 q-mt-lg">
              <q-btn
                flat
                round
                dense
                icon="language"
                color="grey-6"
                class="hover-white bg-dark-hover"
              />
              <q-btn
                flat
                round
                dense
                icon="share"
                color="grey-6"
                class="hover-white bg-dark-hover"
              />
              <q-btn
                flat
                round
                dense
                icon="mail"
                color="grey-6"
                class="hover-white bg-dark-hover"
              />
            </div>
          </div>

          <!-- Links -->
          <div class="col-6 col-md-2">
            <div class="text-weight-bold q-mb-md text-white">Product</div>
            <div class="column gap-3">
              <a href="#" class="footer-link">Features</a>
              <a href="#" class="footer-link">Integrations</a>
              <a href="#" class="footer-link">Pricing</a>
              <a href="#" class="footer-link">Changelog</a>
            </div>
          </div>

          <div class="col-6 col-md-2">
            <div class="text-weight-bold q-mb-md text-white">Company</div>
            <div class="column gap-3">
              <a href="#" class="footer-link">About Us</a>
              <a href="#" class="footer-link">Careers</a>
              <a href="#" class="footer-link">Blog</a>
              <a href="#" class="footer-link">Contact</a>
            </div>
          </div>

          <!-- Newsletter -->
          <div class="col-12 col-md-4">
            <div class="text-weight-bold q-mb-md text-white">Subscribe to Newsletter</div>
            <p class="text-grey-5">Get the latest news and updates directly to your inbox.</p>
            <div class="row no-wrap q-mt-md">
              <q-input
                dark
                outlined
                dense
                color="primary"
                bg-color="dark"
                placeholder="Enter your email"
                class="col nav-input"
              />
              <q-btn
                unelevated
                color="primary"
                label="Subscribe"
                class="q-ml-sm rounded-borders text-weight-bold"
              />
            </div>
          </div>
        </div>

        <q-separator dark class="q-my-xl opacity-2" />

        <!-- Bottom Row -->
        <div class="row justify-between items-center text-grey-6 text-caption">
          <div>&copy; 2026 KGH CUSTO. All rights reserved.</div>
          <div class="row gap-4">
            <a href="#" class="footer-link text-caption">Privacy Policy</a>
            <a href="#" class="footer-link text-caption">Terms of Service</a>
          </div>
        </div>
      </div>
    </q-footer>
  </q-layout>
</template>

<script setup>
// Layout configured for KGH CUSTO Premium Landing Page
</script>

<style scoped lang="scss">
.system-layout {
  background-color: #050505;
}

.glass-header {
  background: rgba(5, 5, 5, 0.75) !important;
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.letter-spacing-1 {
  letter-spacing: 1px;
}

.logo-icon-wrap {
  width: 36px;
  height: 36px;
  background: linear-gradient(135deg, #ff0000 0%, #aa0000 100%);
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(255, 0, 0, 0.4);
}

.logo-icon-wrap-small {
  width: 28px;
  height: 28px;
  background: linear-gradient(135deg, #ff0000 0%, #aa0000 100%);
  border-radius: 6px;
  box-shadow: 0 4px 10px rgba(255, 0, 0, 0.3);
}

.nav-btn {
  color: #a0a0a0;
  transition: all 0.3s ease;
  font-size: 14px;
  &:hover {
    color: #ffffff;
  }
}

.glow-btn {
  box-shadow: 0 4px 15px rgba(255, 0, 0, 0.35);
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  &:hover {
    box-shadow: 0 6px 20px rgba(255, 0, 0, 0.6);
    transform: translateY(-2px);
  }
}

.bg-dark-hover {
  transition: all 0.3s ease;
  &:hover {
    background: rgba(255, 255, 255, 0.1) !important;
  }
}

.border-top-dark {
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}

.footer-link {
  color: #888888;
  text-decoration: none;
  transition: color 0.2s ease;
  font-size: 14px;
  &:hover {
    color: #ffffff;
  }
}

.hover-white {
  transition: color 0.2s ease;
  &:hover {
    color: #ffffff !important;
  }
}

.nav-input {
  :deep(.q-field__control) {
    border-radius: 6px;
  }
  :deep(.q-field__native) {
    color: white;
  }
}

.opacity-2 {
  opacity: 0.15;
}
</style>
