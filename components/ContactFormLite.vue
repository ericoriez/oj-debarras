<template>
  <div class="contact-container">

    <form @submit.prevent="handleSubmit" class="contact-form">
      <div class="form-inner">
        <div class="form-group input-item">
          <input type="text" id="name" v-model="formData.name" required placeholder="Nom*">
        </div>

        <div class="form-group input-item">
          <input type="email" id="email" v-model="formData.email" required placeholder="E-mail*">
        </div>

        <div class="form-group input-item">
          <input type="tel" id="phone" v-model="formData.phone" required placeholder="Telephone*">
        </div>

        <button type="submit" class="submit-btn input-item">
          Rappellez-moi !
        </button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      formData: {
        name: '',
        email: '',
        phone: ''
      }
    }
  },
  methods: {
    async handleSubmit() {
      try {
        // Vérification des required
        if (!this.formData.name || !this.formData.email || !this.formData.phone) {
          alert('Veuillez remplir tous les champs obligatoires');
          return;
        }

        const formData = new FormData();

        formData.append('access_key', 'cc706538-1781-4f64-be1b-374cddd8512d');
        formData.append('from_name', this.formData.name);
        formData.append('email', this.formData.email);
        formData.append('subject', `Site OJ-Debarras: Demande de Rappel de ${this.formData.name} - ${this.formData.phone}`);
        formData.append('message', `Bonjour, J'aurais besoin de renseignements pour un débarras.\nNuméro de téléphone : ${this.formData.phone}`);


        console.log('Envoi des données...', Object.fromEntries(formData));

        const response = await fetch('https://api.web3forms.com/submit', {
          method: 'POST',
          body: formData
        });

        const data = await response.json();
        console.log('Réponse:', data);

        if (data.success) {
          alert('Message envoyé avec succès!');
          this.formData = {
            name: '',
            phone: '',
            email: ''
          };
        } else {
          throw new Error(data.message || 'Erreur lors de l\'envoi');
        }
      } catch (error) {
        console.error('Erreur détaillée:', error);
        alert('Une erreur est survenue lors de l\'envoi du message. Veuillez réessayer.');
      }
    }
  }
}
</script>

<style scoped>
.contact-container {
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  box-sizing: border-box;
}

.contact-form {
  width: 100%;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 2px;
  border: 1px solid #6DA48F;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.1),
  0 0 0 1px rgba(255, 255, 255, 0.274);
  padding: 30px;
  box-sizing: border-box;
}

.form-inner {
  width: 100%;
  max-width: 600px;
  margin: 0 auto;
}

.form-group {
  width: 100%;
  margin-bottom: 20px;
  box-sizing: border-box;
}

label {
  display: block;
  margin-bottom: 8px;
  font-weight: bold;
}

label.optional::after {
  content: "";
}

label::after {
  content: " *";
  color: #ff4444;
}

input,
textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 4px;
  background: rgba(255, 255, 255, 0.1);
  color: inherit;
  box-sizing: border-box;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: rgba(255, 255, 255, 0.5);
}

.submit-btn {
  width: 100%;
  padding: 12px;
  background: rgba(254, 240, 193, 1);
  border: 1px solid rgba(255, 255, 255, 0.2);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
  border-radius: 4px;
  color: inherit;
  cursor: pointer;
  transition: transform 0.5s ease, background 0.3s ease;
  font-size: 24px;
}

.submit-btn:hover {
  background: rgba(210, 180, 140, 1) ;
  transform: scale(1.05);
}

</style>