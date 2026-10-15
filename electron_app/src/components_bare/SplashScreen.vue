@import '../assets/css/theme.css';
<template>
    <div class="splash_screen">
        <Transition name="fade">
            <div class="splash_content" v-if="show">
                <div class="splash_logo_box">
                    <svg width="64" height="64" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2L2 7L12 12L22 7L12 2Z" fill="url(#splash-brand-grad)" />
                        <path d="M2 17L12 22L22 17" stroke="url(#splash-brand-grad)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                        <path d="M2 12L12 17L22 12" stroke="url(#splash-brand-grad)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                        <defs>
                            <linearGradient id="splash-brand-grad" x1="2" y1="2" x2="22" y2="22" gradientUnits="userSpaceOnUse">
                                <stop offset="0%" stop-color="#2563eb" />
                                <stop offset="100%" stop-color="#06b6d4" />
                            </linearGradient>
                        </defs>
                    </svg>
                </div>
                <div class="splash_brand_title">Moderno <span class="splash_brand_diffusion">Diffusion</span></div>
                <div class="splash_brand_sub">Suite Creativa de Inteligencia Artificial Local</div>
                
                <div class="splash_loading_bar">
                    <div class="splash_loading_progress"></div>
                </div>
                <div class="splash_status">Iniciando motor neuronal y modelos locales...</div>
            </div>
        </Transition>
    </div>
</template>
<script>
export default {
    name: 'SplashScreen',
    props: {},
    components: {},
    mounted() {
        this.show = true;
    },
    data() {
        return {
            show:false
        };
    },
    methods: {

    },
}
</script>
<style>

.fade-enter-active,
.fade-leave-active {
  transition: opacity 2s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

</style>
<style scoped>
@import '../assets/css/theme.css';
.splash_screen {
    position: fixed;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    background: radial-gradient(circle at 50% 40%, #0f172a 0%, #030712 100%);
    display: flex;
    align-items: center;
    justify-content: center;
    -webkit-user-select: none;
    -webkit-app-region: drag;
    z-index: 99999;
}

.splash_content {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.splash_logo_box {
    width: 90px;
    height: 90px;
    border-radius: 22px;
    background: linear-gradient(135deg, rgba(37, 99, 235, 0.2), rgba(6, 182, 212, 0.15));
    border: 1px solid rgba(56, 189, 248, 0.35);
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 10px 30px rgba(37, 99, 235, 0.35), inset 0 1px 1px rgba(255, 255, 255, 0.3);
    margin-bottom: 24px;
    animation: splash-pulse 3s infinite ease-in-out;
}

@keyframes splash-pulse {
    0%, 100% { transform: scale(1); box-shadow: 0 10px 30px rgba(37, 99, 235, 0.35); }
    50% { transform: scale(1.04); box-shadow: 0 14px 40px rgba(6, 182, 212, 0.5); }
}

.splash_brand_title {
    font-size: 32px;
    font-weight: 800;
    letter-spacing: -0.5px;
    color: #ffffff;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    margin-bottom: 6px;
}

.splash_brand_diffusion {
    background: linear-gradient(135deg, #38bdf8 0%, #818cf8 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.splash_brand_sub {
    font-size: 14px;
    color: #94a3b8;
    font-weight: 500;
    margin-bottom: 32px;
}

.splash_loading_bar {
    width: 260px;
    height: 4px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 4px;
    overflow: hidden;
    position: relative;
    margin-bottom: 14px;
}

.splash_loading_progress {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 40%;
    background: linear-gradient(90deg, #2563eb, #00e5ff);
    border-radius: 4px;
    animation: splash-bar 1.6s infinite ease-in-out;
}

@keyframes splash-bar {
    0% { left: -40%; width: 30%; }
    50% { width: 50%; }
    100% { left: 100%; width: 30%; }
}

.splash_status {
    font-size: 12px;
    color: #64748b;
    letter-spacing: 0.2px;
}
</style>