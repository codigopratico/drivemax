# 🚗 DriveMax

**DriveMax** é uma landing page fictícia de **consultoria automotiva**, desenvolvida com foco em **UI consistente**, **hierarquia visual clara** e **boas práticas de front-end moderno**.

O projeto simula uma empresa que auxilia clientes na escolha e compra segura de veículos, servindo como **estudo prático** e **peça de portfólio**.

🔗 **Demo:**  
[https://codigopratico.github.io/drivemax/](https://codigopratico.github.io/drivemax/)

---

## 🎯 Objetivo do Projeto

Este projeto foi criado para:

- Consolidar fundamentos do **Vue 3 (Composition API)**
- Aplicar **design tokens** (cores, tipografia e espaçamentos)
- Trabalhar **componentização realista**, como em projetos profissionais
- Implementar animações baseadas em rolagem com **IntersectionObserver**
- Simular um **produto real**, e não apenas telas isoladas

---

## 🧱 Estrutura da Aplicação

A aplicação segue um padrão **Section-based**, onde cada seção da landing page é isolada em seu próprio componente, evitando componentes genéricos e confusos.

### Seções

- **HomeSection** — Hero principal e proposta de valor  
- **ServicesSection** — Processo de consultoria  
- **ReviewSection** — Depoimentos de clientes  
- **SecuritySection** — Confiança e segurança na compra  
- **DecisionPainSection** — Dores do usuário e identificação  
- **ContactSection** — Chamada para ação e rodapé  

---

## 🎨 Design System

O projeto utiliza **CSS Variables** como design tokens, centralizando decisões visuais e garantindo consistência.

### 🎨 Cores
- Brand primária (laranja)
- Fundos claros e escuros bem definidos
- Cards sempre em fundo branco para melhor contraste
- Cores de texto separadas por função (primary, dark, muted)

### 🔤 Tipografia
- Escalas tipográficas padronizadas (heading, subtitle, body, button)
- Uso extensivo de `clamp()` para responsividade real
- Fonte base: **Inter**

Essa abordagem reduz inconsistências visuais e facilita a manutenção do CSS.

---

## ✨ Animações

As animações são ativadas quando as seções entram na viewport, utilizando **IntersectionObserver**:

- Melhora a percepção de qualidade da interface
- Evita animações desnecessárias fora da tela
- Não depende de bibliotecas externas
- Implementação simples e performática

---

## 🛠️ Tecnologias Utilizadas

- **Vue 3**
- **Vite**
- **Composition API**
- **CSS moderno** (Variables, `clamp()`, Flexbox)
- **GitHub Pages**

> Nenhuma dependência desnecessária foi utilizada.

---

## 📁 Organização de Pastas

```txt
src/
├─ components/
│  ├─ HomeSection.vue
│  ├─ ServicesSection.vue
│  ├─ ReviewSection.vue
│  ├─ SecuritySection.vue
│  ├─ DecisionPainSection.vue
│  └─ ContactSection.vue
│
├─ assets/
│  └─ img/
│
├─ styles/
│  ├─ base.css
│  └─ main.css
```
---

## ⚠️ Observações Importantes

- Este é um **projeto fictício**, criado exclusivamente para fins educacionais.
- Nenhuma informação de contato apresentada é real.
- O foco do projeto está em **arquitetura, organização e clareza de código**, não em backend.

---

## 📌 Status do Projeto

- ✔ Estrutura sólida  
- ✔ Design consistente  
- ✔ Pronto para portfólio  
- ✔ Base escalável para projetos maiores  

---

## 👨‍💻 Autor

**Kauan Gabriel**  
Desenvolvedor Front-end — **CódigoPrático**
