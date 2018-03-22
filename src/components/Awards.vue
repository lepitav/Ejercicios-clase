<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="awards">
                <div class="my-auto">
                    <h2 class="mb-5">Premios &amp; Certificados</h2>
                    <p>{{ awards.pa1 }}</p>
                </div>
            </section>
</template>

<script>
export default {
  name: 'awards',
  props: ['awards']
}
</script>

<style scoped>

</style>
