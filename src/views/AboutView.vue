<template>
<div class="skills">
  <h1>À Propos</h1>
  <p>
    Étudiant en développement web et web mobile.<br/> Laissez-moi vous montrer un peu mon parcours...
  </p>
  <p>J'ai des compétences en : 
    <strong>HTML5</strong>, <strong>CSS</strong>, <strong>JavaScript</strong> (avec <strong>Vue.js</strong>, <strong>React.js</strong>), <strong>Node.js</strong>, <strong>PHP</strong> (avec <strong>Symfony</strong>), <strong>MySQL</strong>, <strong>MongoDB</strong>, <strong>Git</strong>, <strong>Wordpress</strong>.
  </p>
  <p>J'ai fait des études supérieures en :</p>
  <p>Licence 1 en Informatique - Université Sup-MTI</p>
  <p>Et maintenant un diplôme professionnel en Développement web et web mobile (En cours) - Centre Européen de Formation</p>
  <p>Je suis actuellement à la recherche d'un stage pour mettre à profit mes compétences et mes connaissances.</p>
</div>


 
</template>

<script>
export default {
  name: "À Propos", // Pour Contact, changez le name à "Contact"
  data() {
    return {
      title: "À Propos", // Pour Contact, changez le titre à "Contact"
    };
  },
};
</script>

<style scoped>
.skills{
  color:#fff;
  padding: 200px;
}
h1{
  font-family: 'Lora', serif;
  font-weight: 500; /* Poids 500 pour le gras */

}
</style>
