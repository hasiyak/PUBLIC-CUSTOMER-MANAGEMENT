<template>
  <q-page class="bg-black text-white">
    <!-- Hero Section -->
    <section class="hero-section relative-position flex flex-center text-center q-pa-md">
      <!-- Background elements for glow -->
      <div class="hero-bg-glow absolute"></div>

      <div class="content-wrapper" style="max-width: 900px; z-index: 1">
        <q-chip outline color="primary" class="q-mb-lg text-weight-bold" size="sm">
          NEXT GENERATION CRM
        </q-chip>

        <h1
          class="text-h2 text-md-h1 text-weight-bolder q-mb-md letter-spacing-tight"
          style="line-height: 1.1"
        >
          Manage Customers with <br />
          <span class="text-gradient">Absolute Precision</span>
        </h1>

        <p
          class="text-h6 text-grey-5 q-mb-xl text-weight-regular"
          style="max-width: 700px; margin-left: auto; margin-right: auto"
        >
          KGH CUSTO empowers your business with intelligent tracking, automated workflows, and
          comprehensive analytics. All in one beautifully simple platform.
        </p>

        <div class="row justify-center gap-4 q-mb-xl">
          <q-btn
            unelevated
            color="primary"
            label="Get Started Free"
            size="lg"
            class="q-px-xl text-weight-bold rounded-borders glow-btn"
          />
          <q-btn
            outline
            color="white"
            label="Learn More"
            size="lg"
            class="q-px-xl text-weight-bold rounded-borders hover-bg-light"
          />
        </div>

        <!-- Dashboard Mockup Graphic -->
        <div class="dashboard-mockup glass-panel q-mx-auto q-mt-xl relative-position">
          <!-- Using a subtle linear gradient to mimic a dashboard UI skeleton -->
          <div
            class="skeleton-ui column gap-3 q-pa-md"
            style="height: 400px; border-radius: 12px; background: rgba(20, 20, 20, 0.8)"
          >
            <div class="row items-center gap-3 q-mb-md">
              <div
                class="circle skeleton-bg"
                style="width: 40px; height: 40px; border-radius: 50%"
              ></div>
              <div class="skeleton-bg" style="height: 20px; width: 150px; border-radius: 4px"></div>
            </div>
            <div class="row q-col-gutter-md flex-1">
              <div class="col-8">
                <div class="skeleton-bg full-height" style="border-radius: 8px"></div>
              </div>
              <div class="col-4 column gap-3">
                <div class="skeleton-bg flex-1" style="border-radius: 8px"></div>
                <div class="skeleton-bg flex-1" style="border-radius: 8px"></div>
              </div>
            </div>
          </div>
          <div class="overlay-gradient absolute-full"></div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="q-py-xl q-px-md q-mt-xl" style="max-width: 1400px; margin: 0 auto">
      <div class="text-center q-mb-xl">
        <h2 class="text-h3 text-weight-bolder q-mb-sm">Powerful Core Features</h2>
        <p class="text-grey-5 text-subtitle1">
          Everything you need to manage your customer relationships effectively.
        </p>
      </div>

      <div class="row q-col-gutter-xl q-pt-md justify-center">
        <!-- Feature Cards -->
        <div class="col-12 col-sm-6 col-md-4" v-for="feature in features" :key="feature.title">
          <q-card
            class="glass-card full-height q-pa-lg hover-glow transition-main bg-transparent"
            flat
          >
            <div class="icon-wrap q-mb-md flex flex-center">
              <q-icon :name="feature.icon" size="32px" color="primary" />
            </div>
            <div class="text-h5 text-weight-bold q-mb-sm">{{ feature.title }}</div>
            <p class="text-grey-5" style="line-height: 1.6">{{ feature.desc }}</p>
          </q-card>
        </div>
      </div>
    </section>

    <!-- Education / Why Us Section -->
    <section class="q-py-xl q-px-md q-my-xl bg-dark-section">
      <div class="row items-center q-col-gutter-xl" style="max-width: 1400px; margin: 0 auto">
        <div class="col-12 col-md-6 q-pa-lg q-pa-md-xl">
          <h2 class="text-h3 text-weight-bolder q-mb-md">Built for Speed and Simplicity</h2>
          <p class="text-h6 text-grey-5 q-mb-lg text-weight-regular" style="line-height: 1.6">
            We removed the clutter so you can focus on what matters most: your customers. Unlike
            traditional CRMs that require weeks of training, KGH CUSTO is intuitive from day one.
          </p>
          <q-list class="q-mb-xl text-grey-4">
            <q-item v-for="point in benefits" :key="point" class="q-pa-none q-mb-sm">
              <q-item-section avatar min-width="40px">
                <q-icon name="check_circle" color="primary" size="24px" />
              </q-item-section>
              <q-item-section class="text-subtitle1">{{ point }}</q-item-section>
            </q-item>
          </q-list>
          <q-btn
            flat
            color="primary"
            no-caps
            label="See all capabilities"
            icon-right="arrow_forward"
            class="text-weight-bold q-px-none hover-white"
          />
        </div>
        <div class="col-12 col-md-6 flex flex-center q-py-xl">
          <!-- Abstract representation of speed/simplicity -->
          <div class="abstract-graphic relative-position">
            <div class="circle-1 bg-primary glow-red absolute"></div>
            <div class="circle-2 glass-panel absolute flex flex-center">
              <q-icon name="rocket_launch" size="80px" color="white" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Bottom -->
    <section class="q-py-xl q-px-md text-center q-my-xl">
      <div
        class="glass-panel q-pa-xl q-mx-auto rounded-borders text-center cta-box relative-position overflow-hidden"
        style="max-width: 1000px; border-color: rgba(255, 0, 0, 0.2)"
      >
        <div class="cta-glow absolute"></div>
        <div class="relative-position" style="z-index: 1">
          <h2 class="text-h3 text-weight-bolder q-mb-md text-white">
            Ready to scale your business?
          </h2>
          <p class="text-grey-5 text-h6 q-mb-xl">
            Join thousands of businesses managing millions of customers with KGH CUSTO.
          </p>
          <q-btn
            unelevated
            color="primary"
            label="Create Your Free Account"
            size="lg"
            class="q-px-xl text-weight-bold rounded-borders glow-btn"
          />
        </div>
      </div>
    </section>
  </q-page>
</template>

<script setup>
const features = [
  {
    icon: 'groups',
    title: 'Client Tracking',
    desc: 'Maintain complete profiles of every customer, interaction history, and future follow-ups effortlessly.',
  },
  {
    icon: 'analytics',
    title: 'Smart Analytics',
    desc: 'Gain beautiful, actionable insights into your sales pipeline and customer retention metrics.',
  },
  {
    icon: 'bolt',
    title: 'Automated Workflows',
    desc: 'Save hours every week by automating repetitive tasks, emails, and important client reminders.',
  },
  {
    icon: 'security',
    title: 'Bank-grade Security',
    desc: 'Your customer data is encrypted and backed up daily across multiple secure global regions.',
  },
  {
    icon: 'receipt_long',
    title: 'Seamless Invoicing',
    desc: 'Generate and send professional, branded invoices directly from your CRM workspace.',
  },
  {
    icon: 'forum',
    title: 'Omnichannel Comm',
    desc: 'Communicate with clients via email, SMS, and WhatsApp directly from one unified dashboard.',
  },
]

const benefits = [
  'Zero learning curve – start tracking immediately',
  'Lightning-fast interface built on modern tech',
  'Fully customizable to match your workflow',
  '24/7 dedicated priority technical support',
]
</script>

<style scoped lang="scss">
.hero-section {
  min-height: 90vh;
  padding-top: 100px;
  overflow: hidden;
}

.hero-bg-glow {
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(255, 0, 0, 0.15) 0%, rgba(0, 0, 0, 0) 70%);
  top: -100px;
  left: 50%;
  transform: translateX(-50%);
  pointer-events: none;
  z-index: 0;
}

.letter-spacing-tight {
  letter-spacing: -1.5px;
}

.hover-bg-light {
  transition: all 0.3s ease;
  &:hover {
    background: rgba(255, 255, 255, 0.1);
  }
}

.dashboard-mockup {
  border-radius: 12px;
  padding: 8px;
  border: 1px solid rgba(255, 0, 0, 0.3);
  box-shadow:
    0 20px 50px rgba(0, 0, 0, 0.5),
    0 0 40px rgba(255, 0, 0, 0.15);
  transform: perspective(1000px) rotateX(10deg) scale(0.95);
  transition: transform 0.6s cubic-bezier(0.25, 0.8, 0.25, 1);

  &:hover {
    transform: perspective(1000px) rotateX(0deg) scale(1);
  }

  .overlay-gradient {
    background: linear-gradient(to bottom, rgba(5, 5, 5, 0) 0%, #050505 100%);
    pointer-events: none;
    border-radius: 8px;
  }
}

.skeleton-bg {
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.02);
}

.flex-1 {
  flex: 1;
}

.glass-card {
  background: rgba(15, 15, 15, 0.6) !important;
  border: 1px solid rgba(255, 255, 255, 0.05);
  border-radius: 16px;

  .icon-wrap {
    width: 64px;
    height: 64px;
    border-radius: 12px;
    background: rgba(255, 0, 0, 0.1);
    border: 1px solid rgba(255, 0, 0, 0.2);
  }
}

.bg-dark-section {
  background: linear-gradient(to bottom, #050505, #0a0a0a, #050505);
  border-top: 1px solid rgba(255, 255, 255, 0.02);
  border-bottom: 1px solid rgba(255, 255, 255, 0.02);
}

.abstract-graphic {
  width: 300px;
  height: 300px;

  .circle-1 {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    filter: blur(40px);
    opacity: 0.5;
    animation: pulse 4s infinite alternate;
  }

  .circle-2 {
    width: 160px;
    height: 160px;
    border-radius: 50%;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border: 1px solid rgba(255, 0, 0, 0.3);
    z-index: 2;
  }
}

.cta-box {
  .cta-glow {
    width: 100%;
    height: 100%;
    background: radial-gradient(circle, rgba(255, 0, 0, 0.1) 0%, rgba(0, 0, 0, 0) 80%);
    top: 0;
    left: 0;
    pointer-events: none;
  }
}

@keyframes pulse {
  0% {
    transform: translate(-50%, -50%) scale(1);
    opacity: 0.4;
  }
  100% {
    transform: translate(-50%, -50%) scale(1.3);
    opacity: 0.7;
  }
}

@media (max-width: 768px) {
  .hero-section {
    padding-top: 60px;
  }
  .text-md-h1 {
    font-size: 3rem !important;
    line-height: 1.2 !important;
  }
}
</style>
