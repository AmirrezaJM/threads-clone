<script setup>
    // const login  = async (prov) => {
    //     const {data,error} = await client.auth.signIn
    // }
    watchEffect(() => {
        if(user.value) {
            return navigateTo('/');
        }
    });
</script>

<template>
    <div id="AuthPage" class="w-full h-screen pt-32">
        <div class="w-full">
            <div class="w-full flex items-center justify-center gap-2.5 p-2">
                <img class="w-[35px]" src="/threads-logo.png" />
                <span class="font-bold text-2xl text-white">
                    Threads
                </span>
            </div>

            <div class="max-w-[350px] mx-auto px-2 text-white">
                <p class="text-center mb-6 mt-4">
                    Login/Register
                </p>
                <button class="flex items-center justify-center gap-3 p-1.5 w-full border rounded-full text-lg font-semibold">
                    <div class="flex items-center gap-2 justify-center">
                        <img class="w-full max-w-[30px] rounded-full" src="/github-logo.png" />
                    </div>
                </button>
            </div>
        </div>
    </div>
</template>
