<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'

const openReadmeInEditor = () => fetch('/__open-in-editor?file=README.md')
</script>

<template>
  <div class="demo-page">
    <div class="hero">
      <span class="badge"> Branche DEMO</span>

      <h1>Bienvenue sur la version de démonstration</h1>

      <p>
        Cette version est déployée automatiquement par Vercel depuis la branche
        <strong>feature/demo</strong>.
      </p>

      <div class="buttons">
        <button>Voir le tableau de bord</button>
        <button class="secondary">Documentation</button>
      </div>
    </div>

    <div class="cards">
      <div class="card">
        <h3>⚡ Déploiement</h3>
        <p>Chaque push crée automatiquement un aperçu de l'application.</p>
      </div>

      <div class="card">
        <h3>🌿 Git Branches</h3>
        <p>Chaque collaborateur possède sa propre URL de prévisualisation.</p>
      </div>

      <div class="card">
        <h3>🔄 CI/CD</h3>
        <p>Les Pull Requests sont testées avant leur fusion dans la production.</p>
      </div>

      <div class="card">
        <h3>👥 Collaboration</h3>
        <p>L'équipe peut consulter le travail de chacun directement sur Vercel.</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.demo-page{
    padding:50px;
    max-width:1200px;
    margin:auto;
    font-family:Arial, Helvetica, sans-serif;
}

.hero{
    text-align:center;
    margin-bottom:50px;
}

.badge{
    background:#42b883;
    color:white;
    padding:8px 18px;
    border-radius:20px;
    font-size:14px;
    display:inline-block;
    margin-bottom:20px;
}

.hero h1{
    font-size:48px;
    margin-bottom:20px;
}

.hero p{
    color:#666;
    font-size:18px;
}

.buttons{
    margin-top:35px;
}

button{
    background:#42b883;
    color:white;
    border:none;
    padding:14px 28px;
    border-radius:8px;
    cursor:pointer;
    margin:8px;
    font-size:16px;
}

.secondary{
    background:#35495e;
}

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
    gap:25px;
}

.card{
    background:white;
    border-radius:14px;
    padding:25px;
    box-shadow:0 10px 25px rgba(0,0,0,.08);
    transition:.3s;
}

.card:hover{
    transform:translateY(-6px);
}

.card h3{
    margin-bottom:15px;
}

.card p{
    color:#666;
}
</style>