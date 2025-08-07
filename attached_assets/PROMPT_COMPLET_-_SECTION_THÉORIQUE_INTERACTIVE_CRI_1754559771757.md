# PROMPT COMPLET - SECTION THÉORIQUE INTERACTIVE CRISIS TIMELINE

## OBJECTIF
Intégrer une section d'introduction théorique interactive avant la timeline existante, en respectant parfaitement la charte graphique rétro-pixelisée et l'architecture actuelle du site.

---

## 1. ARCHITECTURE ET INTÉGRATION

### 1.1 Position dans la page
```html
<!-- Structure existante conservée -->
<header>
  <!-- Navigation et titre existants -->
</header>

<!-- NOUVELLE SECTION À INSÉRER ICI -->
<section id="theoretical-framework" class="theoretical-section">
  <!-- Contenu théorique interactif -->
</section>

<!-- Section timeline existante -->
<section id="vulnerability-timeline" class="timeline-section">
  <!-- Timeline actuelle conservée -->
</section>
```

### 1.2 Charte graphique à respecter
- **Couleurs principales** : Rouge mat (#8B0000), jaune/orange (#FFD700, #FFA500), vert terminal (#00FF00)
- **Polices** : VT323 (monospace), Press Start 2P (titres pixelisés)
- **Style** : Bordures pixelisées, effet rétro, image-rendering: pixelated
- **Responsive** : Adaptation mobile avec grille verticale

---

## 2. SECTION A : QU'EST-CE QU'UNE CRISE ?

### 2.1 Structure HTML
```html
<div class="crisis-definition-container">
  <h2 class="pixel-title">Cadre Théorique : Définir la crise en partant du point de vue des acteurs</h2>
  
  <!-- Sélecteur de mode global -->
  <div class="mode-selector">
    <select id="crisis-mode" class="pixel-select">
      <option value="general">Mode Exploration Générale</option>
      <option value="specific">Mode Analyse Spécifique</option>
    </select>
    <select id="specific-crisis" class="pixel-select" style="display:none;">
      <option value="">Sélectionner une crise...</option>
      <!-- Options dynamiques depuis la timeline -->
    </select>
  </div>
  
  <!-- Texte théorique -->
  <div class="theoretical-text">
    <!-- Contenu textuel fourni -->
  </div>
</div>
```

### 2.2 Contenu textuel (style terminal vert)
```css
.theoretical-text {
  font-family: 'VT323', monospace;
  font-size: 18px;
  color: #00FF00;
  background: rgba(0, 0, 0, 0.8);
  border: 2px solid #00FF00;
  padding: 20px;
  margin: 20px 0;
  line-height: 1.4;
  image-rendering: pixelated;
}
```

**Texte intégral :** [Votre texte complet sur "Code is Law", le paradoxe des coiners, etc.]

---

## 3. MATRICE INTERACTIVE 2x2

### 3.1 Structure HTML
```html
<div class="matrix-container">
  <h3 class="matrix-title">Deux grandes familles de crises protocolaires</h3>
  
  <!-- Axes labels -->
  <div class="matrix-axes">
    <div class="axis-horizontal">
      <span class="axis-label-left">Le code ne permet pas...</span>
      <span class="axis-label-right">Le code permet...</span>
    </div>
    <div class="axis-vertical">
      <span class="axis-label-top">Situation normale</span>
      <span class="axis-label-bottom">Crise</span>
    </div>
  </div>
  
  <!-- Grille 2x2 -->
  <div class="matrix-grid">
    <div class="quadrant" data-quadrant="d" data-type="normal-restricted">
      <div class="quadrant-header">[d] Limitations Acceptées</div>
      <div class="quadrant-content">
        <div class="action">Action : Statu quo</div>
        <div class="examples" id="examples-d">
          <!-- Contenu dynamique -->
        </div>
      </div>
    </div>
    
    <div class="quadrant" data-quadrant="a" data-type="normal-allowed">
      <div class="quadrant-header">[a] Fonctionnement Standard</div>
      <div class="quadrant-content">
        <div class="action">Action : Statu quo</div>
        <div class="examples" id="examples-a">
          <!-- Contenu dynamique -->
        </div>
      </div>
    </div>
    
    <div class="quadrant crisis-vulnerability" data-quadrant="c" data-type="crisis-evolution">
      <div class="quadrant-header">[c] Crise d'Évolution</div>
      <div class="quadrant-content">
        <div class="action">Action : Application de nouvelles règles protocolaires</div>
        <div class="examples" id="examples-c">
          <!-- Contenu dynamique -->
        </div>
      </div>
    </div>
    
    <div class="quadrant crisis-vulnerability" data-quadrant="b" data-type="crisis-vulnerability">
      <div class="quadrant-header">[b] Crise de Vulnérabilité</div>
      <div class="quadrant-content">
        <div class="action">Action : Correction d'un bogue</div>
        <div class="examples" id="examples-b">
          <!-- Contenu dynamique -->
        </div>
      </div>
    </div>
  </div>
</div>
```

### 3.2 Styles CSS
```css
.matrix-container {
  position: relative;
  max-width: 800px;
  margin: 40px auto;
  font-family: 'VT323', monospace;
}

.matrix-title {
  font-family: 'Press Start 2P', monospace;
  font-size: 16px;
  color: #FFD700;
  text-align: center;
  margin-bottom: 30px;
  text-shadow: 2px 2px 0px #000;
}

.matrix-axes {
  position: relative;
  margin-bottom: 20px;
}

.axis-horizontal {
  display: flex;
  justify-content: space-between;
  margin-bottom: 10px;
}

.axis-vertical {
  position: absolute;
  left: -120px;
  top: 0;
  height: 400px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  writing-mode: vertical-rl;
  text-orientation: mixed;
}

.axis-label-left, .axis-label-right, .axis-label-top, .axis-label-bottom {
  font-size: 14px;
  color: #FFA500;
  font-weight: bold;
}

.matrix-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 4px;
  background: #000;
  border: 3px solid #FFD700;
  image-rendering: pixelated;
}

.quadrant {
  background: rgba(139, 0, 0, 0.8);
  border: 2px solid #FFD700;
  padding: 15px;
  cursor: pointer;
  transition: all 0.3s ease;
  min-height: 180px;
}

.quadrant:hover {
  background: rgba(139, 0, 0, 1);
  border-color: #FFA500;
  transform: scale(1.02);
}

.quadrant.crisis-vulnerability {
  background: rgba(255, 0, 0, 0.3);
}

.quadrant.crisis-evolution {
  background: rgba(255, 165, 0, 0.3);
}

.quadrant-header {
  font-family: 'Press Start 2P', monospace;
  font-size: 12px;
  color: #FFD700;
  margin-bottom: 10px;
  text-shadow: 1px 1px 0px #000;
}

.action {
  font-size: 14px;
  color: #00FF00;
  margin-bottom: 10px;
  font-style: italic;
}

.examples {
  font-size: 13px;
  color: #FFF;
  line-height: 1.3;
}

/* Responsive */
@media (max-width: 768px) {
  .matrix-grid {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, 1fr);
  }
  
  .axis-vertical {
    display: none;
  }
  
  .quadrant {
    min-height: 120px;
  }
}
```

### 3.3 Contenu dynamique par quadrant

**Mode Général :**
```javascript
const quadrantContent = {
  a: {
    title: "Fonctionnement Standard",
    examples: [
      "Contrôle de la double dépense",
      "Création monétaire selon l'échéancier prévu",
      "Validation des transactions légitimes",
      "Mécanismes de consensus fonctionnels"
    ],
    links: ["Voir exemples dans la timeline →"]
  },
  b: {
    title: "Crise de Vulnérabilité", 
    examples: [
      "CVE-2018-17144 : Inflation involontaire",
      "CVE-2010-5139 : Combined output overflow", 
      "CVE-2010-5141 : OP_RETURN spend vulnerability",
      "Correction de bogues pour restaurer les normes"
    ],
    links: ["Filtrer vulnérabilités →"]
  },
  c: {
    title: "Crise d'Évolution",
    examples: [
      "SegWit et le Scaling Debate",
      "The DAO hack et hard fork Ethereum",
      "Adoption de nouvelles règles protocolaires",
      "Réponse à une perte de légitimité"
    ],
    links: ["Voir évolutions majeures →"]
  },
  d: {
    title: "Limitations Acceptées",
    examples: [
      "Rejet automatique des doubles dépenses",
      "Invalidation des créations monétaires illégitimes",
      "Respect strict des règles de consensus",
      "Mécanismes de protection actifs"
    ],
    links: ["Voir mécanismes de sécurité →"]
  }
};
```

**Mode Crise Spécifique :**
```javascript
// Exemple pour CVE-2018-17144
const specificCrisisAnalysis = {
  a: "Mécanismes de validation qui fonctionnaient normalement",
  b: "Vulnérabilité permettant la double dépense → Correction immédiate",
  c: "N/A pour cette crise",
  d: "Protections qui ont limité l'impact"
};
```

---

## 4. SECTION B : TYPOLOGIE INTERACTIVE

### 4.1 Structure HTML
```html
<div class="crisis-typology">
  <h3 class="section-title">Typologie des Crises Interactive</h3>
  
  <!-- Filtres visuels -->
  <div class="crisis-filters">
    <button class="filter-btn active" data-filter="all">
      <span class="filter-icon">🔍</span>
      Toutes les crises
    </button>
    <button class="filter-btn" data-filter="vulnerability">
      <span class="filter-icon">🛡️</span>
      Crises de Vulnérabilité
    </button>
    <button class="filter-btn" data-filter="evolution">
      <span class="filter-icon">⬆️</span>
      Crises d'Évolution
    </button>
  </div>
  
  <!-- Basculeur Normal vs Crise -->
  <div class="context-toggle">
    <button class="toggle-btn active" data-context="crisis">
      Situations de Crise ([b] + [c])
    </button>
    <button class="toggle-btn" data-context="normal">
      Situations Normales ([a] + [d])
    </button>
  </div>
  
  <!-- Zone d'affichage dynamique -->
  <div class="typology-display" id="typology-content">
    <!-- Contenu mis à jour selon les filtres -->
  </div>
</div>
```

### 4.2 Styles pour la typologie
```css
.crisis-typology {
  margin: 40px 0;
  padding: 20px;
  background: rgba(0, 0, 0, 0.8);
  border: 2px solid #FFD700;
}

.filter-btn, .toggle-btn {
  font-family: 'VT323', monospace;
  font-size: 16px;
  background: #8B0000;
  color: #FFD700;
  border: 2px solid #FFD700;
  padding: 10px 15px;
  margin: 5px;
  cursor: pointer;
  image-rendering: pixelated;
}

.filter-btn:hover, .toggle-btn:hover {
  background: #FFD700;
  color: #8B0000;
}

.filter-btn.active, .toggle-btn.active {
  background: #00FF00;
  color: #000;
  border-color: #00FF00;
}

.filter-icon {
  margin-right: 8px;
}
```

---

## 5. FONCTIONNALITÉS JAVASCRIPT

### 5.1 Gestion des modes
```javascript
class TheoreticalFramework {
  constructor() {
    this.currentMode = 'general';
    this.selectedCrisis = null;
    this.init();
  }
  
  init() {
    this.bindEvents();
    this.loadTimelineData();
    this.renderMatrix();
  }
  
  bindEvents() {
    // Sélecteur de mode
    document.getElementById('crisis-mode').addEventListener('change', (e) => {
      this.switchMode(e.target.value);
    });
    
    // Quadrants cliquables
    document.querySelectorAll('.quadrant').forEach(quad => {
      quad.addEventListener('click', (e) => {
        this.handleQuadrantClick(e.currentTarget.dataset.quadrant);
      });
    });
    
    // Filtres de typologie
    document.querySelectorAll('.filter-btn').forEach(btn => {
      btn.addEventListener('click', (e) => {
        this.applyFilter(e.currentTarget.dataset.filter);
      });
    });
  }
  
  switchMode(mode) {
    this.currentMode = mode;
    const specificSelector = document.getElementById('specific-crisis');
    
    if (mode === 'specific') {
      specificSelector.style.display = 'block';
      this.populateCrisisSelector();
    } else {
      specificSelector.style.display = 'none';
      this.selectedCrisis = null;
    }
    
    this.renderMatrix();
  }
  
  handleQuadrantClick(quadrant) {
    if (this.currentMode === 'general') {
      // Afficher exemples multiples + liens vers timeline
      this.showGeneralExamples(quadrant);
    } else {
      // Afficher analyse spécifique de la crise sélectionnée
      this.showSpecificAnalysis(quadrant);
    }
  }
  
  // Connexion avec la timeline existante
  linkToTimeline(filter) {
    // Déclencher les filtres de la timeline existante
    const timelineSection = document.getElementById('vulnerability-timeline');
    timelineSection.scrollIntoView({ behavior: 'smooth' });
    
    // Appliquer le filtre correspondant
    if (window.timelineFilters) {
      window.timelineFilters.apply(filter);
    }
  }
}

// Initialisation
document.addEventListener('DOMContentLoaded', () => {
  new TheoreticalFramework();
});
```

---

## 6. INTÉGRATION AVEC LA TIMELINE EXISTANTE

### 6.1 Liens bidirectionnels
- **Depuis la matrice → Timeline** : Clic sur quadrant applique filtres correspondants
- **Depuis la timeline → Matrice** : Sélection d'une vulnérabilité active le mode spécifique

### 6.2 Données partagées
```javascript
// Utiliser les données existantes de la timeline
const vulnerabilityData = window.timelineData || [];

// Mapper les vulnérabilités selon la matrice
const mapToQuadrant = (vulnerability) => {
  const type = vulnerability.type;
  const severity = vulnerability.severity;
  
  if (['THEFT', 'INFLATION', 'DOS'].includes(type)) {
    return 'b'; // Crise de vulnérabilité
  } else if (['FAKE-CONF', 'NETWORK-SPLIT'].includes(type)) {
    return 'c'; // Crise d'évolution
  }
  // etc.
};
```

---

## 7. RESPONSIVE ET ACCESSIBILITÉ

### 7.1 Adaptation mobile
```css
@media (max-width: 768px) {
  .theoretical-section {
    padding: 10px;
  }
  
  .matrix-grid {
    grid-template-columns: 1fr;
    gap: 10px;
  }
  
  .crisis-filters {
    flex-direction: column;
  }
  
  .filter-btn, .toggle-btn {
    width: 100%;
    margin: 5px 0;
  }
}
```

### 7.2 Accessibilité
```html
<!-- ARIA labels pour les éléments interactifs -->
<div class="quadrant" 
     role="button" 
     tabindex="0"
     aria-label="Quadrant A: Fonctionnement Standard"
     data-quadrant="a">
```

---

## 8. ANIMATIONS ET TRANSITIONS

### 8.1 Transitions fluides
```css
.quadrant {
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.matrix-grid {
  animation: fadeIn 0.5s ease-in-out;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
```

### 8.2 Feedback visuel
```css
.quadrant.selected {
  box-shadow: 0 0 20px #FFD700;
  border-width: 4px;
}

.loading {
  position: relative;
}

.loading::after {
  content: "⟲";
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  animation: spin 1s linear infinite;
  color: #00FF00;
  font-size: 24px;
}
```

---

## RÉSULTAT ATTENDU

Cette implémentation créera une section théorique interactive parfaitement intégrée qui :

1. **Respecte la charte graphique** rétro-pixelisée existante
2. **S'intègre harmonieusement** avant la timeline actuelle
3. **Offre deux modes d'exploration** (général et spécifique)
4. **Connecte théorie et empirique** via des liens bidirectionnels
5. **Reste responsive** et accessible sur tous les appareils
6. **Enrichit l'expérience utilisateur** sans perturber l'existant

La section transformera votre cadre théorique en outil pédagogique interactif tout en conservant l'esthétique et la fonctionnalité de votre site actuel.

