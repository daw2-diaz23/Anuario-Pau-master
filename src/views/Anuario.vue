
<template>
    <div>
      <main> 
          <div v-if="$route.params.id > 0">
              <div class="" v-for="item in AlumnosDaw" :key="item.id">
                      <div v-if="item.id == $route.params.id">
                          <DetalleAlumno :persona="item"/>
                      </div>
              </div>
              <div class="" v-for="item in ProfesoresDaw2" :key="item.id">
                      <div v-if="item.id == $route.params.id">
                          <DetalleAlumno :persona="item"/>
                      </div>
              </div>
          </div>
        <div v-else>
        <br>
        <div class="text-center fondo"> 
            <br>
            <h1 class="text-white">Promoción 2022/2023</h1>
            <h1 class="text-white">Desarollo de aplicacions web</h1>
            <h1 class="text-white">(DAW)</h1>
            <br>
        </div>
        <div class="mt-4" style="margin-left: 3%;">
          
          <h1>Profesores</h1>
        </div>
        <div class="d-flex justify-content-center ">
            <div v-for="item in ProfesoresDaw" :key="item.id">
                <fichaProfesor v-if="item.funcion == 'profesor'" :persona="item"/>
            </div>
        </div>
        <div style="margin-left: 3%;">
            <h1>Alumnos</h1>
        </div>    
            <div class="d-flex justify-content-center pb-5">
                <div v-for="item in AlumnosDaw" :key="item.id">
                    <div v-if="item.funcion == 'alumno'">
                        <fichaAlumno :persona="item"/>
                    </div>
                </div>
            </div>   
          </div>
      </main> 
    </div>
</template>

<style>

.fondo{
  background-color: #144c70;
}

h1{
  font-family: 'Bebas Neue', cursive;
}

</style>

<script>
import fichaProfesor from '../components/fichaProfesor.vue'
import DetalleAlumno from '../components/DetalleAlumno.vue';
import fichaAlumno from '../components/fichaAlumno.vue'


export default {
    name: 'Anuario',
    components:{
    fichaAlumno,
    DetalleAlumno,
    fichaProfesor
    
},
    
    data(){
        return{
            ProfesoresDaw: [
               
                {
                    id:1,
                    nombre: 'Carlos',
                    photo: 'carlos.png',
                    funcion: 'profesor'
                },
                {
                    id:2,
                    nombre: 'Ana Rovira',
                    photo: 'ana.jpg',
                    funcion: 'profesor'
                },
                 {
                    id:3,
                    nombre: 'Jordi',
                    photo: 'jordi.png',
                    funcion: 'profesor'
                },
                
                {
                    id:4,
                    nombre: 'Patricia Salinas',
                    photo: 'patricia.jpg',
                    funcion: 'profesor'
                }
                ,{
                    id:5,
                    nombre: 'Raul',
                    photo: 'raul.jpg',
                    funcion: 'profesor'
                }
            ],
            AlumnosDaw: [
                {
                    id:6,
                    nombre: 'Pablo',
                    photo: 'Pablo.jpg',
                    funcion: 'alumno',
                    estudios:['Bachillerato Social','Grado superior en Desarrollo de Aplicaciones Web(DAW)'],
                    trabajo:['Desarollador Web']
                },
                {
                    id:7,
                    nombre: 'Marta',
                    photo: 'Marta.avif',
                    funcion: 'alumno',
                    estudios:['Grado medio en Sistemas Microinformáticos y Redes','Grado superior en Desarrollo de Aplicaciones Web'],
                },
                {
                    id:8,
                    nombre: 'Juan',
                    photo: 'Juan.jpg',
                    funcion: 'alumno',
                    estudios:['Grado medio en Sistemas Microinformáticos y Redes' ,'Grado superior en Desarrollo de Aplicaciones Web'],
                    trabajo:['Repartidor de Pizza']
                },
                {
                    id:9,
                    nombre: 'David',
                    photo: 'david.avif',
                    funcion: 'alumno',
                    estudios:['Grado medio en Sistemas Microinformáticos y Redes','Grado superior en Desarrollo de Aplicaciones Web'],
                    trabajo:['Aparcador de coches']
                },
                {
                    id:10,
                    nombre: 'Alberto',
                    photo: 'alberto.jpg',
                    funcion: 'alumno',
                    estudios:['Grado medio en Sistemas Microinformáticos y Redes','Grado superior en Desarrollo de Aplicaciones Web'],
                    trabajo:['Diseño 3D']
                }
            ]
        }
    }
}
</script>