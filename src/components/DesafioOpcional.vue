<template>
    <div class="container text-light">
      <div class="row">
        <!-- Columna para el formulario -->
        <div class="col-md-6">
          <form>
            <!-- Input Text para el título -->
            <div class="form-group">
              <label for="title">Titulo:</label>
              <input type="text" id="title" class="form-control" v-model="title" />
            </div>
  
            <!-- Dropdown para seleccionar un emoji -->
            <div class="form-group">
              <label for="emoji">Emoji:</label>
              <select id="emoji" class="form-control" v-model="emoji">
                  <option value="🧑🏻‍💻">🧑🏻‍💻</option>
                  <option value="😱">😱</option>
                  <option value="🤘🏻">🤘🏻</option>
                  <option value="💣">💣</option>

            </select>
            </div>
  
            <!-- Escala de opciones -->
            <div class="form-group">
              <label>Apreciacion:</label><br />
              <div class="form-check form-check-inline">
                <input type="radio" id="regular" value="Regular" v-model="scale" class="form-check-input" />
                <label for="regular" class="form-check-label">Regular</label>
              </div>
              <div class="form-check form-check-inline">
                <input type="radio" id="good" value="Bien" v-model="scale" class="form-check-input" />
                <label for="good" class="form-check-label">Bien</label>
              </div>
              <div class="form-check form-check-inline">
                <input type="radio" id="very_good" value="Muy bien" v-model="scale" class="form-check-input" />
                <label for="very_good" class="form-check-label">Muy bien</label>
              </div>
              <div class="form-check form-check-inline">
                <input type="radio" id="amazing" value="Increíble" v-model="scale" class="form-check-input" />
                <label for="amazing" class="form-check-label">Increíble</label>
              </div>
            </div>
  
            <!-- Habilidades con checkboxes -->
            <div class="form-group">
              <label>Competencias aprendidas:</label><br />
              <div class="form-check">
                <input type="checkbox" id="morfologia" value="Morfología de un componente" v-model="skills" class="form-check-input" />
                <label for="morfologia" class="form-check-label">Morfología de un componente</label>
              </div>
              <div class="form-check">
                <input type="checkbox" id="directives" value="Directivas" v-model="skills" class="form-check-input" />
                <label for="directives" class="form-check-label">Directivas</label>
              </div>
              <div class="form-check">
                <input type="checkbox" id="one_way" value="One Way Data Binding" v-model="skills" class="form-check-input" />
                <label for="one_way" class="form-check-label">One Way Data Binding</label>
              </div>
              <div class="form-check">
                <input type="checkbox" id="two_way" value="Two Way Data Binding" v-model="skills" class="form-check-input" />
                <label for="two_way" class="form-check-label">Two Way Data Binding</label>
              </div>
              <div class="form-check">
                <input type="checkbox" id="mvvm" value="MVVM (Model-View-ViewModel)" v-model="skills" class="form-check-input" />
                <label for="mvvm" class="form-check-label">MVVM (Model-View-ViewModel)</label>
              </div>
              <div class="form-check">
                <input type="checkbox" id="state" value="Estado" v-model="skills" class="form-check-input" />
                <label for="state" class="form-check-label">Estado</label>
              </div>
            </div>
  
            <!-- Opinión con textarea -->
            <div class="form-group">
              <label for="opinion">Opinion:</label>
              <textarea id="opinion" class="form-control" v-model="opinion"></textarea>
            </div>
          </form>
        </div>
  
        <!-- Columna para mostrar la información -->
        <div class="col-md-6">
          <h2 class="titulo">{{ title }} {{ emoji }}</h2>
          <p>Y me parece {{ scale }}</p>
          <h2>He aprendido:</h2>
          <p>{{ skills.join(", ") }}</p>
          <h2>Mi opinion del framework es:</h2>
          <p>{{ opinion }}</p>
        </div>
      </div>
    </div>


  </template>
  
  <script>
  export default {
    name: "DesafioOpcional",
    data() {
      return {
        title: "",
        emoji: "",
        scale: "",
        skills: [],
        opinion: "",
      };
    },
  };
  </script>
  
  <style scoped>
  div {
    margin-bottom: 10px;
  }
  label {
    margin-right: 10px;
  }
  .titulo {
  word-wrap: break-word;
  white-space: normal;
  max-width: 100%;
  }

  </style>
  