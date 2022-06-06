<template>
    <div class="relative rounded-lg cursor-default">
        <img @mouseover="hover = true" @mouseleave="hover = false" :src="src" alt="" class="rounded-lg cursor-zoom-in">
        <div v-if="hover" class="absolute cursor-default bg-dark opacity-50 inset-0 w-full h-full rounded-lg"></div>
        <div v-if="hover" class="absolute cursor-default top-0 w-full h-full flex flex-col justify-between p-3">
            <div class="flex items-center justify-between">
                <button type="button" name="button" class="flex">
                    <p class="font-semibold text-white">{{ board }}</p>
                    <span class="material-icons text-white">expand_more</span>
                </button>
                <button type="button" name="button" class="bg-primary rounded-full text-white py-3 px-5 font-semibold">Save</button>
            </div>
            <div class="flex w-full">
                <button type="button" name="button" class="ml-auto mr-2 bg-white rounded-full w-8 h-8 text-dark opacity-80 hover:opacity-100 items-center flex justify-center">
                    <span class="material-icons font-semibold">upload</span>
                </button>
                <button type="button" name="button" class="bg-white rounded-full w-8 h-8 justify-center text-dark opacity-80 hover:opacity-100 items-center flex">
                    <span class="material-icons font-semibold">more_horiz</span>
                </button>
            </div>
        </div>
    </div>
</template>
 
<script>
export default {
    props: ['src', 'board'],
    data () {
        return {
            hover: false
        }
    }
}
</script>

<style>

</style>