<template>
    <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="experience">
        <div class="my-auto">
            <h2 class="mb-5">Experiencia</h2>
            <div>
                {{ experiences.experience }}
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "experiences",
        props: ['experiences']
        }
</script>

<style scoped>

</style>