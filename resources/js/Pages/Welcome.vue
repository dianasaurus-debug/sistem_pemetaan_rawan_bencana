<template>
    <inertia-head>
        <title>
            EWARN BOJONEGORO
        </title>
    </inertia-head>
    <div class="relative flex items-top justify-center min-h-screen bg-cover bg-center sm:items-center sm:pt-0" style="background-image: url('/assets/images/bg-welcome.jpg');">
        <div class="hidden fixed top-0 left-0 px-6 py-4 sm:block">
            <inertia-link :href="route('dashboard')" class="font-bold text-lg">
                EWARN BOJONEGORO
            </inertia-link>

        </div>
        <div v-if="canLogin" class="hidden fixed top-0 right-0 px-6 py-4 sm:block font-bold text-lg">
            <inertia-link v-if="$page.props.user" href="/dashboard">
                Dashboard
            </inertia-link>

            <template v-else>
                <inertia-link :href="route('login')">
                    Log in
                </inertia-link>

                <inertia-link v-if="canRegister" :href="route('register')" class="ml-4">
                    Register
                </inertia-link>
            </template>
        </div>

        <div class="max-w-6xl mx-auto sm:px-6 lg:px-8">

            <div class="mt-8 overflow-hidden text-center">
                <span class="font-extrabold text-white text-6xl">EWARN BOJONEGORO</span>
                <p class=" font-bold text-white text-2xl max-w-screen-sm mt-4">
                    Selamat datang di Sistem Informasi Bencana Hidrometeorologi Kabupaten Bojonegoro
                </p>
            </div>

        </div>
    </div>
</template>

<style scoped>
    .bg-gray-100 {
        background-color: #f7fafc;
        background-color: rgba(247, 250, 252, var(--tw-bg-opacity));
    }

    .border-gray-200 {
        border-color: #edf2f7;
        border-color: rgba(237, 242, 247, var(--tw-border-opacity));
    }

    .text-gray-400 {
        color: #cbd5e0;
        color: rgba(203, 213, 224, var(--tw-text-opacity));
    }

    .text-gray-500 {
        color: #a0aec0;
        color: rgba(160, 174, 192, var(--tw-text-opacity));
    }

    .text-gray-600 {
        color: #718096;
        color: rgba(113, 128, 150, var(--tw-text-opacity));
    }

    .text-gray-700 {
        color: #4a5568;
        color: rgba(74, 85, 104, var(--tw-text-opacity));
    }

    .text-gray-900 {
        color: #1a202c;
        color: rgba(26, 32, 44, var(--tw-text-opacity));
    }

    @media (prefers-color-scheme: dark) {
        .dark\:bg-gray-800 {
            background-color: #2d3748;
            background-color: rgba(45, 55, 72, var(--tw-bg-opacity));
        }

        .dark\:bg-gray-900 {
            background-color: #1a202c;
            background-color: rgba(26, 32, 44, var(--tw-bg-opacity));
        }

        .dark\:border-gray-700 {
            border-color: #4a5568;
            border-color: rgba(74, 85, 104, var(--tw-border-opacity));
        }

        .dark\:text-white {
            color: #fff;
            color: rgba(255, 255, 255, var(--tw-text-opacity));
        }

        .dark\:text-gray-400 {
            color: #cbd5e0;
            color: rgba(203, 213, 224, var(--tw-text-opacity));
        }
    }
</style>

<script>
        export default {
        props: {
            canLogin: Boolean,
            canRegister: Boolean,
            laravelVersion: String,
            phpVersion: String,
        }
    }
</script>
