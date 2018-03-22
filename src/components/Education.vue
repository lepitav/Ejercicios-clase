<template>
  <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="education">
                <div class="my-auto">
                    <h2 class="mb-5">Education</h2>

                    <div class="resume-item d-flex flex-column flex-md-row mb-5">
                        <div class="resume-content mr-auto">
                            <h3 class="mb-0">{{ education.schoolname }}</h3>
                            <div class="subheading mb-3">{{ education.schooltitle }}</div>
                            <p>{{ education.schoolgpa }}</p>
                        </div>
                        <div class="resume-date text-md-right">
                            <span class="text-primary">{{ education.schooldate }}</span>
                        </div>
                    </div>
                </div>
            </section>
</template>

<script>
export default {
  name: 'education',
  props: ['education']
}
</script>

<style scoped>

</style>
