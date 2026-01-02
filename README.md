🚗 DriveMax

DriveMax é uma landing page fictícia de consultoria automotiva, desenvolvida com foco em UI consistente, hierarquia visual clara e boas práticas de front-end moderno.

O projeto simula uma empresa que auxilia clientes na escolha e compra segura de veículos, servindo como estudo prático e peça de portfólio.

🔗 Demo:
https://codigopratico.github.io/drivemax/

🎯 Objetivo do Projeto

Este projeto foi criado para:

Consolidar fundamentos de Vue 3 (Composition API)

Aplicar padronização de design tokens (cores, tipografia, espaçamentos)

Trabalhar componentização realista, como em projetos profissionais

Implementar animações baseadas em rolagem (IntersectionObserver)

Simular um produto real, não apenas telas soltas

🧱 Estrutura da Aplicação

A aplicação é organizada por seções semânticas, cada uma isolada em seu próprio componente:

HomeSection – Hero principal e proposta de valor

ServicesSection – Processo de consultoria

ReviewSection – Depoimentos de clientes

SecuritySection – Confiança e segurança na compra

DecisionPainSection – Dores do usuário e identificação

ContactSection – Chamada para ação + rodapé

Essa separação segue um padrão Section-based, evitando componentes genéricos e confusos.

🎨 Design System

O projeto utiliza CSS Variables como design tokens, centralizando decisões visuais:

Cores

Brand primária (laranja)

Fundos escuros e claros bem definidos

Cards sempre em fundo branco para contraste

Texto separado por função (primary, dark, muted)

Tipografia

Escalas tipográficas padronizadas (heading, subtitle, body, button)

Uso extensivo de clamp() para responsividade real

Fonte base: Inter

Isso evita CSS inconsistente e facilita manutenção.

✨ Animações

As seções utilizam IntersectionObserver para ativar animações ao entrar na viewport:

Melhora a percepção de qualidade

Evita animações desnecessárias

Não depende de bibliotecas externas

Implementação simples e performática.

🛠️ Tecnologias Utilizadas

Vue 3

Vite

Composition API

CSS moderno (clamp, variables, flexbox)

GitHub Pages

Nenhuma dependência desnecessária.

📁 Organização
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

⚠️ Observações Importantes

Este é um projeto fictício, criado exclusivamente para fins educacionais.

Nenhuma informação de contato é real.

O foco está em arquitetura, organização e clareza, não em backend.

📌 Status do Projeto

✔ Estrutura sólida
✔ Design consistente
✔ Pronto para portfólio
✔ Base escalável para projetos maiores

👨‍💻 Autor

Kauan Gabriel  
Desenvolvedor Front-end — CódigoPrático
