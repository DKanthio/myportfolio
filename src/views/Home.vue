<template>
  <div class="home-view full-width">
    <div class="content">
    <div class="image">
    <div class="text">
          <h1 class="custom-heading">Bonjour, je suis <br/> Kanthio</h1>
          <h2>Développeuse web </h2>
    </div>
    <img src="@/assets/images/photo.jpeg" alt="Mon image" class="profile-image" />
    </div>
    <AboutView/>
    <div class="text-before-projects">
        <h1>Mes Créations</h1>
        <h2>Ceux ci sont mes différents projets réalisés </h2>
    </div>
    <div class="projets">
    <div v-for="projet in projets" :key="projet.id" class="projet">
          <img :src="projet.image" :alt="projet.title" @click="openModal(projet)" />
          <h3>{{ projet.title }}</h3>
    </div>
    </div>
     
    </div>
    <Modal :projet="selectedProject" v-if="selectedProject" @close="selectedProject = null" />
    <Contact />
  </div>
</template>

<script>
import Contact from "@/views/Contact.vue";
import AboutView from "@/views/AboutView.vue";
import Modal from "@/components/Modal.vue";

export default {
  name: "Home",
  components: {
    Contact,
    AboutView,
    Modal,
  },
  data() {
    return {
      projets: [
        
          {
            id: 1,
            title: "Mon Cv",
            date: "02/10/2023",
            technologies: "HTML, CSS",
            github: "https://github.com/DKanthio/devoir-Cv",
            image: "/assets/images/creation1.png",
            link: "/assets/cv/index.html", // Utilisez un chemin absolu
        },

        {
          id: 2,
          title: "Cahier Des Charges",
          date: "05/10/2023",
          technologies: "Powerpoint",
          image: "/assets/images/creation1.png",
          link: "/assets/CDC.pdf",
        },
        {
          id: 3,
          title: "Dynamiser un espace commentaire",
          date: "31/10/2023",
          technologies: "HTML, CSS, Javascript",
          github: "https://github.com/DKanthio/commentaire",
          image: "/assets/images/creation1.png",
          link: "/assets/commentaire/index.html",
        },
        {
          id: 4,
          title: "Trouve ton artisan",
          date: "07/02/2024",
          technologies: "HTML, CSS, Angular",
          github: "https://github.com/DKanthio/Trouve-ton-artisan",
          image: "/assets/images/creation1.png",
          link: "https://trouve-ton-artisan-three.vercel.app/",
        },
        {
          id: 5,
          title: "Au petit village",
          date: "25/01/2024",
          technologies: "HTML, CSS, Angular",
          github: "https://github.com/DKanthio/Au-petit-village",
          image: "/assets/images/creation1.png",
          link: "/assets/aupetitvillage/Au_petit_village.pdf",
        },
        {
          id: 6,
          title: "Knowledge",
          date: "11-06-2024",
          technologies: "HTML, CSS,Symfony",
          github: "https://github.com/DKanthio/knowledge",
          image: "/assets/images/creation1.png",
          link: "/assets/learning.pdf",
        },
        {
          id: 7,
          title: "Mediatheque",
          date: "07-03-2024",
          technologies: "HTML,Python",
          github: "https://github.com/DKanthio/gestion_mediatheque",
          image: "/assets/images/creation1.png",
          link: "/assets/mediatheque.pdf",
        },
      ],
      selectedProject: null,
    };
  },
  methods: {
    openModal(projet) {
      this.selectedProject = projet;
    },
  },
};
</script>


  
<style scoped>
  h1, h2 {
              font-family: 'Lora', serif;
              font-weight: 500; /* Poids 500 pour le gras */
          }
  .custom-heading{
    color: #fff;
  }
   h2 ,p {
    color: #fff;
   }
  .image {
    display: flex;
    align-items: center;
  }
  
  .text {
    display: flex;
    flex-direction: column;
    color: #fff;
  }
  
  .profile-image {
    width: 500px;
    height: 600px;
    margin-left: 20px;
  }
  
  h1{
    color:#fff;
  }
  .image {
    margin-left: 20px;
  }
  
  .projets {
  display: flex;
  justify-content: center;
}

.projet {
  margin: 20px;
  max-width: 200px;
  text-align: center;
  color: #fff;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.projet img {
  max-width: 100%;
  border-radius: 5px;
  transition: box-shadow 0.3s;
  width: 900px;
  height: 300px;
}
.projet:hover img {
  box-shadow: 4px 4px 12px rgba(128, 0, 128, 0.5); /* Ombre violette en bas à droite */
}

.projet-details {
  margin-top: 10px;
  text-align: center;
}

.projet a {
  color: #007bff;
  text-decoration: none;
  display: block;
  margin-top: 10px;
}
  
  .home-view {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    padding: 20px;
  }
  
  .content {
    max-width: 800px;
    text-align: center;
  }
  .full-width {
    width: 100%;
  }
  
  
  .contact-form {
    max-width: 600px;
    margin: 0 auto;
  }
  </style>
  
