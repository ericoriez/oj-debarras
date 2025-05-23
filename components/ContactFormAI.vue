<template>
  <div class="contact-container">
    <form @submit.prevent="handleSubmit" class="contact-form">

      <div class="form-inner">
        <div class="form-grid">
          <div class="form-group input-item">
            <label for="lastname">Nom</label>
            <input type="text" id="lastname" v-model="formData.lastname" required placeholder="Votre nom">
          </div>

          <div class="form-group input-item">
            <label for="firstname">Prénom</label>
            <input type="text" id="firstname" v-model="formData.firstname" required placeholder="Votre prénom">
          </div>

          <div class="form-group input-item">
            <label for="phone">Téléphone</label>
            <input type="tel" id="phone" v-model="formData.phone" required placeholder="Votre numéro">
          </div>

          <div class="form-group input-item">
            <label for="email">E-mail</label>
            <input type="email" id="email" v-model="formData.email" required placeholder="Votre email">
          </div>

          <div class="form-group input-item">
            <label for="typeClient">Type de client</label>
            <select id="typeClient" v-model="formData.clientType" required>
              <option value="">Sélectionnez</option>
              <option value="particulier">Particulier</option>
              <option value="entreprise">Entreprise</option>
            </select>
          </div>

          <div class="form-group input-item">
            <label for="intervention">Type d'intervention</label>
            <select id="intervention" v-model="formData.interventionType" required>
              <option value="">Sélectionnez</option>
              <option value="maison">Maison</option>
              <option value="appartement">Appartement</option>
              <option value="locaux commerciaux">Locaux commerciaux</option>
              <option value="bureaux">Bureaux</option>
              <option value="entrepot">Entrepôt / Usine</option>
              <option value="autres">Autres</option>
            </select>
          </div>

          <div class="form-group input-item">
            <label for="surface">Surface estimée (en m²)</label>
            <input type="number" id="surface" v-model="formData.surface" placeholder="Surface approximative">
          </div>

          <div class="form-group input-item">
            <label for="urgency">Degré d'urgence</label>
            <select id="urgency" v-model="formData.urgency" required>
              <option value="">Sélectionnez</option>
              <option value="peu urgent">Peu urgent</option>
              <option value="urgent">Urgent</option>
              <option value="très urgent">Très urgent</option>
            </select>
          </div>

        </div>

        <div class="form-group input-item full-width">
          <label for="message">Message</label>
          <textarea id="message" v-model="formData.message" required placeholder="Votre message" rows="6"></textarea>
        </div>

        <button type="submit" class="submit-btn input-item">
          Envoyer
        </button>
      </div>
      <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d369879.86766365287!2d6.126706954979967!3d45.82075956203162!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x478b8ffa1c0551c9%3A0x42781681620534ba!2sAnnecy!5e0!3m2!1sfr!2sfr!4v1747924735299!5m2!1sfr!2sfr"
          width="100%"
          height="300"
          style="border: 1px solid rgba(255, 255, 255, 0.2); border-radius: 4px; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"></iframe>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      formData: {
        lastname: '',
        firstname: '',
        phone: '',
        email: '',
        message: '',
        clientType: '',
        interventionType: '',
        surface: '',
        urgency: ''
      }
    }
  },
  methods: {
    async handleSubmit() {
      try {
        const requiredFields = ['lastname', 'firstname', 'phone', 'email', 'message', 'urgency'];
        for (const field of requiredFields) {
          if (!this.formData[field]) {
            alert('Veuillez remplir tous les champs obligatoires');
            return;
          }
        }

        const formData = new FormData();
        formData.append('access_key', 'cc706538-1781-4f64-be1b-374cddd8512d');
        formData.append('from_name', `${this.formData.firstname} ${this.formData.lastname}`);
        formData.append('email', this.formData.email);
        formData.append('subject', `Demande de Devis - ${this.formData.firstname} - ${this.formData.clientType} - ${this.formData.interventionType}`);
        formData.append('message', this.formData.message);
        formData.append('Téléphone', this.formData.phone);
        formData.append('Type de client', this.formData.clientType);
        formData.append("Type d'intervention", this.formData.interventionType);
        formData.append('Surface', `${this.formData.surface} m²`);
        formData.append("Urgence", this.formData.urgency);

        const response = await fetch('https://api.web3forms.com/submit', {
          method: 'POST',
          body: formData
        });

        const data = await response.json();
        if (data.success) {
          alert('Message envoyé avec succès!');
          this.formData = {
            lastname: '',
            firstname: '',
            phone: '',
            email: '',
            message: '',
            clientType: '',
            interventionType: '',
            surface: '',
            urgency: ''
          };
        } else {
          alert("Erreur lors de l'envoi : " + (data.message || 'Veuillez réessayer.'));
          console.error(data.message);
        }
      } catch (error) {
        alert('Une erreur est survenue. Veuillez réessayer.');
        console.error(error);
      }
    }
  }
}
</script>

<style scoped>

.contact-container {
  margin: 2% 5% 2% 5%;

}

.contact-form {
  background: #6DA48F80;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  border-radius: 4px;
  padding: 30px;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
  font-size: 24px;
  color: #25424C;
}

.form-grid {
  display: grid;
  gap: 20px;
  grid-template-columns: repeat(3, 1fr);
}

.full-width {
  grid-column: 1 / -1;
}

.form-group label {
  display: block;
  margin-bottom: 6px;
}


input, select, textarea {
  width: 100%;
  padding: 10px;
  border: none;
  border-radius: 4px;
  background: rgba(250, 236, 214, 1);
  color: inherit;
  box-sizing: border-box;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

input:focus,
textarea:focus,
select:focus {
  outline: none;
  border-color: rgba(36, 66, 74, 0.5);
}

.submit-btn {
  background: rgba(250, 236, 214, 1);
  border: 1px solid rgba(255, 255, 255, 0.2);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  border-radius: 4px;
  color: inherit;
  cursor: pointer;
  transition: background 0.3s ease, transform 0.5s ease;
  font-size: 24px;
  margin-top: 20px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  padding: 12px;
  font-weight: bold;

}

.submit-btn:hover {
    background: #D2B48C;
  transform: scale(1.05);
}

iframe {
  margin: 20px 0;
}

@media (max-width: 1024px) {
  .form-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .form-grid {
    grid-template-columns: 1fr;
  }
  .contact-form {
    padding: 10px;
  }
}
</style>
