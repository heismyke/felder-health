<script setup lang="ts">
import { ref } from "vue";
import {
    SparklesIcon,
    ShieldCheckIcon,
    ChartBarIcon,
    BellAlertIcon,
    BeakerIcon,
    ClockIcon,
    DevicePhoneMobileIcon,
    EnvelopeIcon,
    PhoneIcon,
} from "@heroicons/vue/24/outline";

const email = ref("");
const submitted = ref(false);

const features = [
    {
        icon: ChartBarIcon,
        title: "Diet Analysis",
        description:
            "Personalized nutrition recommendations tailored to your health goals",
    },
    {
        icon: ChartBarIcon,
        title: "Exercise Tracking",
        description:
            "Smart workout plans that adapt to your fitness level and progress",
    },
    {
        icon: ClockIcon,
        title: "Sleep Monitoring",
        description:
            "Track and optimize your sleep patterns for better health outcomes",
    },
    {
        icon: BeakerIcon,
        title: "Genetic Insights",
        description:
            "Health recommendations based on your unique genetic profile",
    },
    {
        icon: BellAlertIcon,
        title: "Early Warnings",
        description:
            "AI-powered alerts to detect and prevent health risks before they escalate",
    },
    {
        icon: ShieldCheckIcon,
        title: "Preventive Care",
        description:
            "Proactive health management through continuous monitoring and insights",
    },
];

const handleSubmit = () => {
    if (email.value) {
        submitted.value = true;
        setTimeout(() => {
            email.value = "";
            submitted.value = false;
        }, 3000);
    }
};
</script>

<template>
    <div class="min-h-screen bg-white font-sans">
        <!-- Navigation -->
        <nav
            class="fixed top-0 left-0 right-0 bg-white/80 backdrop-blur-md z-50 border-b border-sky-50"
        >
            <div class="max-w-7xl mx-auto px-6 lg:px-8">
                <div class="flex items-center justify-between h-20">
                    <div class="flex items-center space-x-3">
                        <div
                            class="w-10 h-10 bg-gradient-to-br from-sky-200 to-sky-300 rounded-xl flex items-center justify-center"
                        >
                            <!-- Abstract minimal logo -->
                            <svg
                                class="w-6 h-6"
                                viewBox="0 0 24 24"
                                fill="none"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <circle
                                    cx="12"
                                    cy="8"
                                    r="3"
                                    stroke="currentColor"
                                    stroke-width="1.5"
                                    class="text-sky-600"
                                />
                                <path
                                    d="M6 20C6 16.6863 8.68629 14 12 14C15.3137 14 18 16.6863 18 20"
                                    stroke="currentColor"
                                    stroke-width="1.5"
                                    stroke-linecap="round"
                                    class="text-sky-600"
                                />
                                <circle
                                    cx="12"
                                    cy="12"
                                    r="10"
                                    stroke="currentColor"
                                    stroke-width="1.5"
                                    class="text-sky-500"
                                    opacity="0.3"
                                />
                            </svg>
                        </div>
                        <span
                            class="text-2xl font-light bg-gradient-to-r from-sky-400 to-sky-500 bg-clip-text text-transparent"
                        >
                            Feldor Health
                        </span>
                    </div>
                    <div class="flex items-center gap-3">
                        <!-- WhatsApp Button -->
                        <a
                            href="https://wa.me/2349158272790"
                            target="_blank"
                            class="hidden sm:flex items-center gap-2 px-5 py-2.5 bg-green-100 text-green-700 rounded-full hover:bg-green-200 transition-all duration-300 font-light shadow-sm"
                        >
                            <svg
                                class="w-4 h-4"
                                fill="currentColor"
                                viewBox="0 0 24 24"
                            >
                                <path
                                    d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"
                                />
                            </svg>
                            <span class="text-sm">WhatsApp</span>
                        </a>

                        <!-- Contact Button -->
                        <a
                            href="tel:+2349158272790"
                            class="px-6 py-2.5 bg-sky-300 text-sky-700 rounded-full hover:bg-sky-400 transition-all duration-300 font-light shadow-sm flex items-center gap-2"
                        >
                            <PhoneIcon class="w-4 h-4" />
                            <span class="hidden sm:inline">Contact</span>
                        </a>
                    </div>
                </div>
            </div>
        </nav>

        <!-- Hero Section -->
        <section class="pt-32 pb-20 px-6 relative overflow-hidden">
            <!-- Abstract Background Elements -->
            <div
                class="absolute top-20 right-10 w-72 h-72 bg-sky-50 rounded-full blur-3xl opacity-70"
            ></div>
            <div
                class="absolute bottom-20 left-10 w-96 h-96 bg-blue-50 rounded-full blur-3xl opacity-60"
            ></div>

            <div class="max-w-7xl mx-auto relative z-10">
                <div class="text-center max-w-4xl mx-auto">
                    <div
                        class="inline-flex items-center space-x-2 bg-sky-50 px-5 py-2.5 rounded-full mb-8 border border-sky-100"
                    >
                        <SparklesIcon class="w-5 h-5 text-sky-400" />
                        <span class="text-sky-600 font-light text-sm"
                            >AI-Powered Health Assistant</span
                        >
                    </div>

                    <h1
                        class="text-6xl lg:text-7xl font-extralight mb-6 bg-gradient-to-r from-sky-400 via-sky-500 to-sky-600 bg-clip-text text-transparent leading-tight tracking-tight"
                    >
                        Your Health,
                        <br />
                        <span class="text-slate-700 font-light"
                            >Empowered by AI</span
                        >
                    </h1>

                    <p
                        class="text-xl text-slate-500 mb-12 max-w-2xl mx-auto leading-relaxed font-light"
                    >
                        Integrating diet, exercise, sleep, and genetic data to
                        deliver personalized health insights. Preventive
                        healthcare made accessible, personalized, and effective.
                    </p>

                    <!-- Email Signup -->
                    <div class="max-w-md mx-auto mb-8">
                        <form
                            @submit.prevent="handleSubmit"
                            class="flex flex-col sm:flex-row gap-3"
                        >
                            <input
                                v-model="email"
                                type="email"
                                placeholder="Enter your email"
                                required
                                class="flex-1 px-6 py-4 rounded-full border border-sky-200 focus:border-sky-300 focus:outline-none text-slate-600 bg-white shadow-sm font-light"
                            />
                            <button
                                type="submit"
                                class="px-8 py-4 bg-gradient-to-r from-sky-300 to-sky-400 text-sky-800 rounded-full hover:shadow-lg hover:shadow-sky-300/50 transition-all duration-300 font-normal whitespace-nowrap"
                            >
                                Join Waitlist
                            </button>
                        </form>
                        <p
                            v-if="submitted"
                            class="mt-3 text-green-500 font-light animate-pulse"
                        >
                            Thanks! We'll notify you when we launch.
                        </p>
                    </div>

                    <!-- Stats -->
                    <div class="flex flex-wrap justify-center gap-8 mt-16">
                        <div class="text-center">
                            <div class="text-4xl font-light text-sky-400">
                                AI
                            </div>
                            <div class="text-sm text-slate-500 mt-1 font-light">
                                Powered Insights
                            </div>
                        </div>
                        <div class="text-center">
                            <div class="text-4xl font-light text-sky-400">
                                24/7
                            </div>
                            <div class="text-sm text-slate-500 mt-1 font-light">
                                Health Monitoring
                            </div>
                        </div>
                        <div class="text-center">
                            <div class="text-4xl font-light text-sky-400">
                                100%
                            </div>
                            <div class="text-sm text-slate-500 mt-1 font-light">
                                Personalized
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Features Grid -->
        <section class="py-20 px-6 bg-gradient-to-b from-white to-sky-25">
            <div class="max-w-7xl mx-auto">
                <div class="text-center mb-16">
                    <h2
                        class="text-4xl lg:text-5xl font-light text-slate-700 mb-4"
                    >
                        Comprehensive Health Management
                    </h2>
                    <p
                        class="text-lg text-slate-500 max-w-2xl mx-auto font-light"
                    >
                        Everything you need to take control of your health in
                        one intelligent platform
                    </p>
                </div>

                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <div
                        v-for="(feature, index) in features"
                        :key="index"
                        class="group bg-white p-8 rounded-2xl border border-sky-100 hover:border-sky-200 hover:shadow-lg transition-all duration-300 cursor-pointer"
                    >
                        <div
                            class="w-14 h-14 bg-gradient-to-br from-sky-50 to-sky-100 rounded-xl flex items-center justify-center mb-5 group-hover:scale-110 transition-transform duration-300"
                        >
                            <component
                                :is="feature.icon"
                                class="w-7 h-7 text-sky-400"
                            />
                        </div>
                        <h3 class="text-xl font-normal text-slate-700 mb-3">
                            {{ feature.title }}
                        </h3>
                        <p class="text-slate-500 leading-relaxed font-light">
                            {{ feature.description }}
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- How It Works -->
        <section class="py-20 px-6 bg-white">
            <div class="max-w-7xl mx-auto">
                <div class="text-center mb-16">
                    <h2
                        class="text-4xl lg:text-5xl font-light text-slate-700 mb-4"
                    >
                        How It Works
                    </h2>
                    <p
                        class="text-lg text-slate-500 max-w-2xl mx-auto font-light"
                    >
                        Simple, seamless, and personalized for you
                    </p>
                </div>

                <div class="grid lg:grid-cols-4 gap-8">
                    <div class="text-center">
                        <div
                            class="w-16 h-16 bg-gradient-to-br from-sky-300 to-sky-400 text-white rounded-2xl flex items-center justify-center text-2xl font-light mx-auto mb-5 shadow-sm"
                        >
                            1
                        </div>
                        <h3 class="text-xl font-normal text-slate-700 mb-3">
                            Connect Your Data
                        </h3>
                        <p class="text-slate-500 font-light">
                            Sync your fitness devices, upload genetic data, and
                            log your daily activities
                        </p>
                    </div>

                    <div class="text-center">
                        <div
                            class="w-16 h-16 bg-gradient-to-br from-sky-300 to-sky-400 text-white rounded-2xl flex items-center justify-center text-2xl font-light mx-auto mb-5 shadow-sm"
                        >
                            2
                        </div>
                        <h3 class="text-xl font-normal text-slate-700 mb-3">
                            AI Analysis
                        </h3>
                        <p class="text-slate-500 font-light">
                            Our AI processes your data to identify patterns and
                            potential health risks
                        </p>
                    </div>

                    <div class="text-center">
                        <div
                            class="w-16 h-16 bg-gradient-to-br from-sky-300 to-sky-400 text-white rounded-2xl flex items-center justify-center text-2xl font-light mx-auto mb-5 shadow-sm"
                        >
                            3
                        </div>
                        <h3 class="text-xl font-normal text-slate-700 mb-3">
                            Get Insights
                        </h3>
                        <p class="text-slate-500 font-light">
                            Receive personalized recommendations and early
                            warning alerts
                        </p>
                    </div>

                    <div class="text-center">
                        <div
                            class="w-16 h-16 bg-gradient-to-br from-sky-300 to-sky-400 text-white rounded-2xl flex items-center justify-center text-2xl font-light mx-auto mb-5 shadow-sm"
                        >
                            4
                        </div>
                        <h3 class="text-xl font-normal text-slate-700 mb-3">
                            Take Action
                        </h3>
                        <p class="text-slate-500 font-light">
                            Follow actionable steps to improve your health and
                            prevent diseases
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- CEO Section -->
        <section class="py-16 px-6 bg-white">
            <div class="max-w-4xl mx-auto text-center">
                <div class="inline-block">
                    <div class="flex flex-col items-center">
                        <!-- CEO Profile Picture - Replace src with your image -->
                        <div class="relative mb-4">
                            <div
                                class="w-20 h-20 rounded-full overflow-hidden border-2 border-sky-200 shadow-lg"
                            >
                                <img
                                    src="/ceo-profile.jpg"
                                    alt="CEO Profile"
                                    class="w-full h-full object-cover"
                                />
                            </div>
                        </div>

                        <!-- CEO Info -->
                        <div>
                            <h3 class="text-lg font-normal text-slate-700 mb-1">
                                Ayibiowu simisola Elvis
                            </h3>
                            <p class="text-sm text-slate-500 font-light mb-3">
                                Founder & CEO
                            </p>
                            <p
                                class="text-sm text-slate-600 font-light max-w-md mx-auto italic"
                            >
                                "Building the future of preventive healthcare
                                for Africa"
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Coming Soon Banner -->
        <section
            class="py-20 px-6 bg-gradient-to-br from-sky-200 via-sky-300 to-blue-300 relative overflow-hidden"
        >
            <div class="absolute inset-0 opacity-20">
                <div
                    class="absolute top-10 left-10 w-64 h-64 bg-white rounded-full blur-3xl"
                ></div>
                <div
                    class="absolute bottom-10 right-10 w-96 h-96 bg-white rounded-full blur-3xl"
                ></div>
            </div>

            <div class="max-w-4xl mx-auto text-center relative z-10">
                <DevicePhoneMobileIcon
                    class="w-20 h-20 text-sky-600 mx-auto mb-6"
                />
                <h2 class="text-4xl lg:text-5xl font-light text-sky-800 mb-6">
                    Coming Soon to Africa
                </h2>
                <p
                    class="text-xl text-sky-700 mb-8 max-w-2xl mx-auto font-light"
                >
                    Be among the first to experience the future of preventive
                    healthcare. Join our waitlist and get exclusive early access
                    when we launch.
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <button
                        class="px-10 py-4 bg-white text-sky-600 rounded-full hover:bg-sky-50 transition-all duration-300 font-normal text-lg shadow-lg"
                    >
                        Join Waitlist
                    </button>
                    <button
                        class="px-10 py-4 bg-transparent border border-white text-white rounded-full hover:bg-white/10 transition-all duration-300 font-light text-lg"
                    >
                        Learn More
                    </button>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="bg-sky-50 text-slate-600 py-12 px-6">
            <div class="max-w-7xl mx-auto">
                <div
                    class="flex flex-col md:flex-row justify-between items-center"
                >
                    <div class="flex items-center space-x-3 mb-6 md:mb-0">
                        <div
                            class="w-10 h-10 bg-gradient-to-br from-sky-200 to-sky-300 rounded-xl flex items-center justify-center"
                        >
                            <!-- Abstract minimal logo -->
                            <svg
                                class="w-6 h-6"
                                viewBox="0 0 24 24"
                                fill="none"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <circle
                                    cx="12"
                                    cy="8"
                                    r="3"
                                    stroke="currentColor"
                                    stroke-width="1.5"
                                    class="text-sky-600"
                                />
                                <path
                                    d="M6 20C6 16.6863 8.68629 14 12 14C15.3137 14 18 16.6863 18 20"
                                    stroke="currentColor"
                                    stroke-width="1.5"
                                    stroke-linecap="round"
                                    class="text-sky-600"
                                />
                                <circle
                                    cx="12"
                                    cy="12"
                                    r="10"
                                    stroke="currentColor"
                                    stroke-width="1.5"
                                    class="text-sky-500"
                                    opacity="0.3"
                                />
                            </svg>
                        </div>
                        <span class="text-xl font-light text-sky-700">
                            Feldor Health
                        </span>
                    </div>

                    <div class="text-center md:text-right">
                        <div
                            class="flex flex-col sm:flex-row gap-4 mb-4 justify-center md:justify-end"
                        >
                            <!-- Email -->
                            <a
                                href="mailto:ayibiowusimisola@gmail.com"
                                class="flex items-center gap-2 text-sm text-slate-600 hover:text-sky-600 transition-colors font-light"
                            >
                                <EnvelopeIcon class="w-4 h-4" />
                                <span>ayibiowusimisola@gmail.com</span>
                            </a>

                            <!-- Phone -->
                            <a
                                href="tel:+2349158272790"
                                class="flex items-center gap-2 text-sm text-slate-600 hover:text-sky-600 transition-colors font-light"
                            >
                                <PhoneIcon class="w-4 h-4" />
                                <span>+234 915 827 2790</span>
                            </a>
                        </div>

                        <p class="text-sm font-light">
                            © 2025 Feldor Health. Making preventive healthcare
                            accessible to Africa.
                        </p>
                        <p class="text-xs mt-2 text-slate-500 font-light">
                            Powered by AI · Built for the Future
                        </p>
                    </div>
                </div>
            </div>
        </footer>
    </div>
</template>

<style scoped>
@keyframes pulse {
    0%,
    100% {
        opacity: 1;
    }
    50% {
        opacity: 0.7;
    }
}

.animate-pulse {
    animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}
</style>
