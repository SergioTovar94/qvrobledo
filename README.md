# Queremos que vuelva Robledo


Landing page, de personas que queremos que vuelvan robledo al senado de la república.


**Para iniciar el repo:** 
```bash
git clone https://github.com/SergioTovar94/qvrobledo.git
```
### Nos ubicamos en la carpeta clonada

```bash
cd qvrobledo
```

### Luego instalamos los moduloes

```bash
npm install
```

### Pâra visualizar el repo:

```bash
npm run dev
```

## Estructura:

```text
└── 📁qvrobledo
    └── 📁public
        └── favicon.svg
    └── 📁src
        └── 📁assets
        └── 📁components
            └── Footer.astro
            └── GetInvolved.astro
            └── Header.astro
            └── HeroSection.astro
            └── JoinForm.astro
            └── WhatsAppCTA.astro
            └── WhyRobledo.astro
        └── 📁layouts
            └── Layout.astro
        └── 📁pages
            └── index.astro
        └── 📁styles
            └── global.css
    └── .gitignore
    └── astro.config.mjs
    └── package-lock.json
    └── package.json
    └── README.md
    └── tsconfig.json
```


```mermaid
graph TB
    User((User))

    subgraph "Landing Page System"
        subgraph "Frontend Container"
            WebApp["Web Application<br>(Astro.js)"]
            
            subgraph "Page Components"
                MainPage["Main Page<br>(index.astro)"]
                BaseLayout["Base Layout<br>(Layout.astro)"]
            end
            
            subgraph "UI Components"
                Header["Header Component<br>(Astro)"]
                Footer["Footer Component<br>(Astro)"]
                HeroSection["Hero Section<br>(Astro)"]
                WhyRobledo["Why Robledo Section<br>(Astro)"]
                GetInvolved["Get Involved Section<br>(Astro)"]
                JoinForm["Join Form<br>(Astro)"]
                WhatsAppCTA["WhatsApp CTA<br>(Astro)"]
            end
            
            subgraph "Static Assets"
                Styles["Global Styles<br>(CSS)"]
                Assets["Asset Files<br>(Images/Media)"]
                Favicon["Favicon<br>(SVG)"]
            end
        end
    end

    User -->|"Visits"| WebApp
    WebApp -->|"Renders"| MainPage
    MainPage -->|"Uses"| BaseLayout
    BaseLayout -->|"Includes"| Header
    BaseLayout -->|"Includes"| Footer
    MainPage -->|"Renders"| HeroSection
    MainPage -->|"Renders"| WhyRobledo
    MainPage -->|"Renders"| GetInvolved
    MainPage -->|"Renders"| JoinForm
    MainPage -->|"Renders"| WhatsAppCTA
    WebApp -->|"Loads"| Styles
    WebApp -->|"Loads"| Assets
    WebApp -->|"Loads"| Favicon
```