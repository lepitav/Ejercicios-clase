<template>
    <div id="app">
        <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
            <a class="navbar-brand js-scroll-trigger" href="#page-top">
                <span class="d-block d-lg-none">Start Bootstrap</span>
                <span class="d-none d-lg-block">
          <img class="img-fluid img-profile rounded-circle mx-auto mb-2" src="./assets/img/profile.jpg" alt="">
        </span>
            </a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
                    aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link js-scroll-trigger" href="#about">Datos</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link js-scroll-trigger" href="#experience">Experiencia</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link js-scroll-trigger" href="#education">Educación</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link js-scroll-trigger" href="#skills">Habilidades</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link js-scroll-trigger" href="#interests">Intereses</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link js-scroll-trigger" href="#awards">Premios</a>
                    </li>
                </ul>
            </div>
        </nav>

        <div class="container-fluid p-0">

            <about :about="misdatos"></about>

            <experiences :experiences="experiences"></experiences>

            <education :education="education"></education>

            <skills :skills="skills"></skills>

            <interests :interests="interests"></interests>

            <awards :awards="awards"></awards>

        </div>
    </div>
</template>

<script>
    import About from './components/About.vue'
    import Experiences from './components/Experiences.vue'
    import Education from './components/Education.vue'
    import Skills from './components/Skills.vue'
    import Interests from './components/Interests.vue'
    import Awards from './components/Awards.vue'
    import axios from 'axios'

    export default {
        name: "app",
        mounted(){
            console.log("Componente Cargado...")
            this.prueba()
        },
        components: {
            'about': About,
            'experiences': Experiences,
            'education': Education,
            'skills': Skills,
            'interests': Interests,
            'awards': Awards
        },
        data() {
            return {
                misdatos: {
                    name: 'Luis E.',
                    lastname: 'Pita V.',
                    address: 'Colinas de la California · Calle San José, Residencias San José',
                    phone: '(424) 193-6674',
                    email: 'luiseduardopita@hotmail.com',
                    description: '',
                    facebook: 'https://facebook.com/',
                    twitter: 'https://twitter.com/',
                    linkedin: 'https://linkedin.com/in/',
                    github: 'https://github.com/lepitav'
                },
                experiences: {
                    experience: 'No posee experiencia laboral.'
                },
                education: {
                    schoolname: 'U.E. Colegio Yale',
                    schooltitle: 'Bachiller en Ciencias',
                    schooldate: 'Septiembre 2005 - Julio 2016',
                    schoolgpa: 'GPA: 2.6'
                },
                skills: {
                    idiomas: 'Bilingüe: Inglés y Español.',
                    art: 'Artista. Dibujar, hacer lineart, inking y pintar dichos dibujos.',
                    heading: 'Herramientas y Software',
                    heading2: 'Habilidades Especificas'
                },
                interests: {
                    p1: 'Paso mayor parte de mi tiempo en casa. Me gusta disfrutar de una gran variedad de shows de ciencia ficción y suspenso. Soy fanático de los videojuegos, en casi todos los géneros. También me gusta dibujar y pintar digitalmente.'
                },
                awards: {
                    pa1: 'Hasta la fecha, no se le ha otrogado ningun certificado o premio.'
                }
            }
        },
        methods: {
            prueba(){
                axios.get('https://swapi.co/api/people').then(response => {
                    console.log(response)
                })
                .catch(error => {
                    console.log(error)
                });
            }
        }
    };
</script>

<style>

</style>
