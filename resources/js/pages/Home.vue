
<template>

    <Layout>
        <main>

            <div class="flex">
                <div class="w-1/2 px-2 md:max-w-xxl rounded-lg bg-white shadow-lg dashboard-card ">
                    <div class="p-6 justify-start">
                        <h5 class="text-gray-900 text-xl font-medium mb-2">Card title</h5>
                        <p class="text-gray-700 text-base mb-4">
                            This is a wider card with supporting text below as a natural lead-in to additional
                            content. This content is a little bit longer.
                        </p>
                        <p class="text-gray-600 text-xs">Last updated 3 mins ago</p>
                    </div>
                </div>
                <div class=" w-1/2 px-2 md:max-w-xxl rounded-lg bg-white shadow-lg dashboard-card ">
                    <div class="p-6  justify-start">
                        <h5 class="text-gray-900 text-xl font-medium mb-2">Card title</h5>
                        <p class="text-gray-700 text-base mb-4">
                            This is a wider card with supporting text below as a natural lead-in to additional
                            content. This content is a little bit longer.
                        </p>
                        <p class="text-gray-600 text-xs">Last updated 3 mins ago</p>
                    </div>
                </div>
            </div>
            <div class="flex">
                <div class="w-1/2  px-2 md:max-w-xxl rounded-lg bg-white shadow-lg dashboard-card ">
                    <div class="p-6 justify-start">
                        <h5 class="text-gray-900 text-xl font-medium mb-2">Card title</h5>
                        <p class="text-gray-700 text-base mb-4">
                            This is a wider card with supporting text below as a natural lead-in to additional
                            content. This content is a little bit longer.
                        </p>
                        <p class="text-gray-600 text-xs">Last updated 3 mins ago</p>
                    </div>
                </div>
                <div class=" w-1/2 px-2 md:max-w-xxl rounded-lg bg-white shadow-lg dashboard-card ">
                    <div class="p-6  justify-start">
                        <h5 class="text-gray-900 text-xl font-medium mb-2">Card title</h5>
                        <p class="text-gray-700 text-base mb-4">
                            This is a wider card with supporting text below as a natural lead-in to additional
                            content. This content is a little bit longer.
                        </p>
                        <p class="text-gray-600 text-xs">Last updated 3 mins ago</p>
                    </div>
                </div>
            </div>

        </main>
    </Layout>


</template>

<script>
import Layout from "../components/Layout.vue";

export default {
    components: { Layout }
};


</script>

<style lang="scss">


.dashboard-card {
    margin:1rem;
    padding:1rem;
}

</style>
