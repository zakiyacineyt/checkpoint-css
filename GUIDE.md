# 📋 Guide du Projet - Portefeuille Yacine HAMANI

## 🎯 Vue d'ensemble

Ce projet est un **portefeuille professionnel moderne** présenté avec un design épuré et professionnel. C'est une vitrine numérique de vos compétences et réalisations.

## 📂 Organisation du Projet

```
checkpoint-css/
├── 📄 index.html              ← Page principale
├── 📄 README.md              ← Documentation
├── 📄 package.json           ← Configuration
├── 📄 GUIDE.md              ← Ce fichier
│
├── assets/                    ← Ressources
│   ├── css/
│   │   └── styles.css        ← Tous les styles
│   └── images/
│       ├── profile/          ← Votre photo
│       └── projects/         ← Photos des projets
│
└── pages/                     ← Pages futures
```

## 🎨 Sections Principales

### 1️⃣ **Navbar**
```html
<nav class="navbar">
  <div class="navbar-logo"><h1>Yacine HAMANI</h1></div>
  <ul class="navbar-menu">
    <li><a href="#accueil">Accueil</a></li>
    <li><a href="#a-propos">À Propos</a></li>
    <li><a href="#projets">Projets</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>
```
- **Type** : Navigation sticky
- **Style** : Gradient sombre avec border accent
- **Fonction** : Navigation fluide avec underline animé

### 2️⃣ **Hero Section**
```html
<section id="accueil" class="hero">
  <div class="hero-content">
    <div class="hero-text">
      <p class="hero-name">Yacine HAMANI</p>
      <h1>Créateur de Solutions Web Modernes</h1>
      <p class="hero-subtitle">Développeur Web Full-Stack</p>
      <div class="hero-buttons">
        <a href="#projets" class="cta-button cta-primary">Découvrir mes projets</a>
        <a href="#contact" class="cta-button cta-secondary">Contactez-moi</a>
      </div>
    </div>
    <div class="hero-stats">
      <div class="stat-box">50+ Projets complétés</div>
      <div class="stat-box">30+ Clients satisfaits</div>
      <div class="stat-box">5+ Ans d'expérience</div>
    </div>
  </div>
</section>
```
- **Gradient** : Violet → Rose (#667eea → #764ba2)
- **Layout** : Flexbox (texte + stats)
- **Animations** : Fade-in-up à l'affichage

### 3️⃣ **About Section**
```html
<section id="a-propos" class="about">
  <div class="profile-section">
    <img src="assets/images/profile/profile.svg" alt="Yacine HAMANI">
  </div>
  <div class="about-text">
    <!-- Texte bio + features -->
  </div>
  <div class="skills-section">
    <!-- Barres de compétences -->
  </div>
</section>
```
- **Photo** : 280×350px dans un conteneur arrondi
- **Features** : 4 boîtes avec icônes (💡⚡🎨📱)
- **Compétences** : Front-End, Back-End, Outils & Frameworks

### 4️⃣ **Projects Section**
```html
<section id="projets" class="projects">
  <div class="projects-grid">
    <div class="project-card">
      <div class="project-image">
        <img src="assets/images/projects/projet-*.svg" alt="">
      </div>
      <div class="project-content">
        <h3>Titre du projet</h3>
        <p>Description...</p>
        <div class="project-tech">
          <span class="tech-tag">Technology</span>
        </div>
      </div>
    </div>
    <!-- 6 cartes au total -->
  </div>
</section>
```
- **Grille** : 3 colonnes (auto-fit responsive)
- **Cartes** : 320px min-width avec shadow et zoom
- **Overlay** : Bouton "Voir plus" au survol

### 5️⃣ **Contact Section**
```html
<section id="contact" class="contact">
  <div class="contact-info">
    <!-- Infos + liens sociaux -->
  </div>
  <form class="contact-form">
    <input type="text" placeholder="Votre nom">
    <input type="email" placeholder="Votre email">
    <input type="text" placeholder="Sujet">
    <textarea placeholder="Message">
    <button type="submit">Envoyer</button>
  </form>
</section>
```
- **Layout** : 2 colonnes (infos + formulaire)
- **Style** : Gradient primaire/secondaire
- **Formulaire** : Champs avec focus styles

### 6️⃣ **Footer**
```html
<footer class="footer">
  <div class="footer-content">
    <div class="footer-section">À Propos</div>
    <div class="footer-section">Navigation</div>
    <div class="footer-section">Réseaux sociaux</div>
  </div>
</footer>
```
- **Sections** : 3 colonnes responsives
- **Style** : Fond sombre avec border accent
- **Contenu** : À Propos, Navigation, Sociaux

## 🎨 Style et CSS

### Variables CSS (à personnaliser)
```css
:root {
  /* Couleurs */
  --primary-color: #667eea;      /* Violet */
  --secondary-color: #764ba2;    /* Rose */
  --accent-color: #3498db;       /* Bleu */
  
  /* Espacements */
  --spacing-md: 24px;
  --spacing-lg: 40px;
  --spacing-xl: 60px;
  
  /* Fonts */
  --font-main: 'Roboto', sans-serif;
  --font-heading: 'Poppins', sans-serif;
}
```

### Animations Clés
```css
/* Fade in général */
@keyframes fadeIn { from { opacity: 0; } }

/* Fade + movement */
@keyframes fadeInUp { from { opacity: 0; transform: translateY(40px); } }
@keyframes fadeInLeft { from { opacity: 0; transform: translateX(-40px); } }
```

## 📱 Responsive Design

### Desktop (1200px+)
- Navigation : Horizontale avec 40px gap
- Grille projets : 3 colonnes
- Layout : 2 colonnes (about, contact)

### Tablette (768px)
- Navigation : Centrée
- Grille projets : 2 colonnes
- Layout : 1 colonne adaptatif

### Mobile (480px)
- Navigation : Colonne verticale
- Grille projets : 1 colonne
- Menu complet : Stack vertical
- Boutons : Pleins (100% width)

## ✏️ Comment Modifier le Contenu

### 1. Changer le nom
Recherchez `Yacine HAMANI` et remplacez partout :
- `index.html` (3 occurrences)
- `assets/images/profile/profile.svg`

### 2. Modifier les projets
Chaque projet a cette structure :
```html
<div class="project-card">
  <div class="project-image">
    <img src="assets/images/projects/PROJECT_NAME.svg">
  </div>
  <h3 class="project-title">Titre</h3>
  <p class="project-description">Description...</p>
  <div class="project-tech">
    <span class="tech-tag">Tech1</span>
    <span class="tech-tag">Tech2</span>
  </div>
</div>
```

### 3. Modifier les compétences
```html
<div class="skill-item">
  <span class="skill-name">Compétence</span>
  <div class="progress-bar">
    <div class="progress-fill" style="width: 85%"></div>
  </div>
</div>
```

### 4. Ajouter des images
Placez vos images dans :
- **Profile** : `assets/images/profile/`
- **Projects** : `assets/images/projects/`

Puis changez le chemin dans le HTML

## 🚀 Optimisations Possible

- [ ] Ajouter un préprocesseur CSS (SASS)
- [ ] Minifier CSS et HTML
- [ ] Lazy loading pour les images
- [ ] Service Worker pour offline
- [ ] Lighthouse optimization
- [ ] SEO metadata
- [ ] Analytics

## 📞 Infos de Contact à Personnaliser

Dans le formulaire et le footer, mettez vos vrais infos :
- Email : `contact@example.com`
- Téléphone : `+33 6 12 34 56 78`
- Localisation : `Paris, France`
- LinkedIn/GitHub : Vos vrais profils

## 🎓 Apprentissage CSS

Concepts utilisés :
- **Flexbox** : Navigation, layouts
- **Grid** : Grille de projets
- **Variables CSS** : Personnalisation facile
- **Gradients** : Couleurs modernes
- **Transitions/Animations** : Effets fluides
- **Media Queries** : Responsive design
- **Pseudo-éléments** : Underlines, badges
- **Backdrop Filter** : Effets vitrés

## 📚 Ressources

- [MDN CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Color Palette Tools](https://coolors.co/)

---

**Créé par** : Yacine HAMANI  
**Date** : 9 Janvier 2026
