<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="interests">
                <div class="my-auto">
                    <h2 class="mb-5">Intereses</h2>
                    <p>{{ interests.p1 }}</p>
                </div>
            </section>
</template>

<script>
export default {
  name: 'interests',
  props: ['interests']
}
</script>

<style scoped>

</style>
