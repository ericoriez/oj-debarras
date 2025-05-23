# OJ-Débarras – Promotional Static Website

OJ-Débarras is a fast, responsive, and minimalistic promotional website designed for a local waste and clearance service. Its primary goal is to deliver key business information quickly and effectively, enabling users to understand the services offered and get in touch easily.

## 🧭 Project Objective

The website focuses on **simplicity**, **speed**, and **clarity**, aiming to:

- Present the business and its values clearly in just a few pages
- Provide a **quick contact form** for potential customers
- Ensure **mobile responsiveness** for easy access on any device
- Offer a solid, adaptable base for future styling and customization

## 🎯 Design Philosophy

This site has been built intentionally with **pure CSS** instead of utility frameworks like Tailwind or Bootstrap. The rationale behind this choice:

- **Full control** over every visual detail
- Easier to **refactor or redesign** the style layer in the future
- Avoid unnecessary bloat from unused utility classes or styles
- Aligns with the minimalist principle of the project: *lightweight and maintainable*

## 💡 Features

- Clean, mobile-first layout
- Fast load time with minimal dependencies
- Custom contact form integrated with [Web3Forms](https://web3forms.com/)
- Reusable Vue components for testimonials, cards, and more
- Designed to evolve without relying on external CSS frameworks

## 🛠️ Tech Stack

- **Vue.js 3**
- **Vite** as build tool
- **Vanilla CSS**
- **Web3Forms API** for contact form handling

## 📁 Project Structure
```bash
src/
├── assets/ # Images and icons
├── components/ # Vue components (ContactForm, Testimonials, etc.)
├── views/ # Main pages (Home, Contact, etc.)
├── App.vue # Main layout wrapper
└── main.js # Entry point
```

## 📱 Responsiveness

The site uses pure CSS media queries to adjust layout across devices, ensuring a good user experience on:

- Mobile phones
- Tablets
- Desktop screens

## 📬 Contact Handling

The contact form leverages **Web3Forms** to collect user submissions securely without a backend. All key fields are validated, and the form is styled to match the overall design aesthetic.

## 🚀 Getting Started

Clone the project and run locally:

```bash
git clone https://github.com/yourusername/oj-debarras.git
cd oj-debarras
npm install
npm run dev
```

# Install Nuxt

## Nuxt Minimal Starter

Look at the [Nuxt documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
