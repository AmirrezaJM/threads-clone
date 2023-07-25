<script setup>
    import { useUserStore } from "~/stores/user";

    // -- variables
    const userStore = useUserStore();
    const posts = ref([])
    const isPosts = ref(false);
    const isLoading = ref(false);
    

    // -- lifeCycle
    onBeforeMount(() => {
        posts.value = [
            {
                id: 1,
                name: "Amirreza Jolani",
                image: "https://placehold.co/100",
                text: "I'm back guys",
                picture: "https://placehold.co/100",
            }
        ]
    })

    // -- pageMeta Nuxt
    definePageMeta({
        layout: "main"
    });
    
</script>

<template>
    <main id="IndexPage" class="w-full overflow-auto">
        <div class="mx-auto max-w-[500px] overflow-hidden">
            <div id="posts" class="px-4 max-w-[600px] mx-auto">
                <div v-if="posts">
                    <div class="text-white" v-for="post in posts" :key="post.id">
                        <Post :post="post" @isDeleted="posts = []" />
                        <Post :post="post" @isDeleted="posts = []" />
                        <Post :post="post" @isDeleted="posts = []" />
                        <Post :post="post" @isDeleted="posts = []" />
                        <Post :post="post" @isDeleted="posts = []" />
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>
