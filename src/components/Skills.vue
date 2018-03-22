<template>
    <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="skills">
        <div class="my-auto">
            <h2 class="mb-5">Habilidades</h2>

            <div class="subheading mb-3">{{ skills.heading }}</div>
                <ul class="list-inline list-icons">
                    <li class="list-inline-item">
                        <i class="devicons devicons-html5"></i>
                    </li>
                    <li class="list-inline-item">
                        <i class="devicons devicons-css3"></i>
                     </li>
                    <li class="list-inline-item">
                        <i class="devicons devicons-javascript"></i>
                    </li>
                    <li class="list-inline-item">
                        <i class="devicons devicons-bootstrap"></i>
                     </li>
                     <li class="list-inline-item">
                        <i class="devicons devicons-npm"></i>
                      </li>
                      <li class="list-inline-item">
                        <i class="devicon-photoshop-plain"></i>
                     </li> 
                </ul>

                    <div class="subheading mb-3">{{ skills.heading2 }}</div>
                    <ul class="fa-ul mb-0">
                        <li>
                            <i class="fa-li fa fa-check"></i>
                            {{ skills.idiomas }}
                        </li>
                        <li>
                            <i class="fa-li fa fa-check"></i>
                            {{ skills.art }}
                        </li>
                    </ul>
        </div>
    </section>
</template>

<script>
export default {
  name: 'skills',
  props: ['skills']
}
</script>

<style scoped>

</style>

