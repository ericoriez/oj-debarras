

<template>
  <div class="hero-section">
    <img src="@/assets/images/ex-img-1.png" alt="hero-images" class="background-image"/>
    <div class="hero-content">
      <img class="logo" src="@/assets/images/logo-OJDeb.png" alt="Logo"/>
      <h1>Nos Prestations</h1>
    </div>
  </div>


  <div class="intro-section">
    <h2>Pour quelles interventions ?</h2>
    <p>OJ Débarras : Votre partenaire pour un débarras écologique et responsable !
      <br>Nous vidons maisons, bureaux, garages et greniers, même lors de successions,
      avec un engagement fort pour l’écologie. Recyclage, revalorisation
      et tarifs compétitifs sont au cœur de notre mission : offrir un service rapide, fiable et respectueux de
      l’environnement.
      <br>Simplifiez vos débarras, contactez-nous dès aujourd'hui pour un devis gratuit !</p>
  </div>

  <div class="cards-container">
    <BaseDetailedCard
        v-for="(card, index) in cards"
        :key="index"
        :title="card.title"
        :imageSrc="card.imageSrc"
        :text="card.text"
        :imageWidth="imageWidth"
    />
  </div>

  <ExampleSection/>
  <BaselogoLite/>
</template>

<script>
import BaseDetailedCard from "~/components/BaseCard.vue";

import maison from "@/assets/images/maison.png";
import appartement from "@/assets/images/appartement.png";
import locaux from "@/assets/images/locaux.png";
import bureaux from "@/assets/images/bureaux.png";
import entrepots from "@/assets/images/entrepots.png";

export default {
  components: {
    BaseDetailedCard
  },
  data() {
    return {
      imageWidth: '250px',
      cards: [
        {
          title: 'Maison',
          imageSrc: maison,
          text: 'Nous intervenons pour vider complètement ou partiellement votre maison, que ce soit à la suite d’un déménagement, d’une succession ou d’une rénovation. Nous assurons un tri écoresponsable et un recyclage optimal des objets et encombrants.'
        },
        {
          title: 'Appartement',
          imageSrc: appartement,
          text: 'Débarras d’appartements en étage avec ou sans ascenseur. Nous prenons en charge l’évacuation de meubles, électroménagers et déchets, tout en respectant les parties communes et la copropriété.'
        },
        {
          title: 'Locaux Commerciaux',
          imageSrc: locaux,
          text: 'Nous proposons un service rapide et efficace de débarras pour vos magasins, boutiques ou espaces commerciaux, que ce soit avant une fermeture, une reprise ou une rénovation. Valorisation du mobilier possible.'
        },
        {
          title: 'Bureaux',
          imageSrc: bureaux,
          text: 'Débarras de bureaux professionnels, open spaces ou salles de réunion. Nous assurons le démontage du mobilier, le recyclage du matériel informatique et le respect des délais pour ne pas perturber votre activité.'
        },
        {
          title: 'Entrepôt / Usine',
          imageSrc: entrepots,
          text: 'Intervention sur des sites industriels ou entrepôts pour évacuer machines, palettes, archives, gravats ou encombrants divers. Nous proposons également un service de tri, recyclage et destruction sécurisée.'
        }
      ]
    }
  }
}
</script>

<style scoped>

.hero-section {
  position: relative;
  width: 100%;
  height: 80vh;
  overflow: hidden;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
}

.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: 1;
  opacity: 0.5;
}

.hero-content {
  position: relative;
  z-index: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  height: 100%;
  padding: 5rem;
  overflow-y: auto;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
  gap: 5%;

}

.logo {
  filter: contrast(200%);
}

h1 {
  font-size: 5rem;
  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
}

h2 {
  font-size: 3rem;

  font-family: 'Alkatra', sans-serif;
  font-weight: 200;
}

button {
  background-color: #B6D0C5;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  padding: 1rem 2rem;
  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
  border-radius: 5px;
  border: none;
  margin-bottom: 3rem;
}

button:hover {
  background-color: #A0BDAF;
  opacity: 1;
}

.intro-section {
  font-family: 'Inter', sans-serif;
  color: #25424C;
  font-size: 24px;
  background-color: White;
  padding: 5% 20%;
  gap: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.cards-container {
  background-color: #6DA48F80;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 40px;
  padding-top: 2%;
  margin-bottom: 5%;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

@media (max-width: 768px) {
  .hero-content {
    padding: 2rem;
    gap: 2rem;
  }

  .intro-section {
    padding: 5% 5%;
  }
}
</style>