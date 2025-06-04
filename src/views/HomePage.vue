<script lang="ts">
import { ArrowRightFromLine, ArrowUpRight } from 'lucide-vue-next'

export default {
  components: {
    ArrowRightFromLine, ArrowUpRight
  }
}
</script>

<template>
    <!-- imagem em formato de circulo -->
    <section>
        <div>
            <img src="../assets/public/eduardo.webp" alt="Foto de perfil" class="profile-image">
        </div>

        <!-- textos de boas vindas -->
        <div>
        <h1>Bem-vindo aos meus links!</h1>
        <p>Olá! Eu sou Eduardo Brito, um desenvolvedor Front-End focado em criar soluções inovadoras.</p>
        <p>Explore meus projetos e entre em contato para colaborações!</p>
        </div>
    </section>

    <section>
    <div class="home">
        <!-- seção de links -->
        <div class="links">
            <ul class="link-list">
                <li><h1>Confira o meu WebSite!</h1>
                    <p>Confira mais sobre os meus projetos e mais informações sobre mim.</p>
                    <a href="https://eduardobrito.dev" target="_blank" class="link-item">Clique aqui   <ArrowUpRight :size="23"/></a>
                </li>

                <li><h1>Me acompanhe no GitHub!</h1>
                    <p>Acompanhe todos os meus projetos.</p>
                    <a href="https://github.com/Duduubas" target="_blank" class="link-item">Clique aqui  <ArrowUpRight :size="23"/></a>
                </li>

                <li><h1>Me siga no LinkedIn!</h1>
                    <p>Conecte-se comigo para oportunidades profissionais e networking.</p>
                    <a href="https://linkedin.com/in/eduardobritoo" target="_blank" class="link-item">Clique aqui   <ArrowUpRight :size="23"/></a>
                </li>

                <li><h1>Contate-me pelo Discord!</h1>
                    <p>Entre em contato comigo pelo Discord para conversarmos sobre projetos, dúvidas ou parcerias!</p>
                    <a href="https://discord.com/users/522531030834610211" target="_blank" class="link-item">Clique aqui   <ArrowUpRight :size="23"/></a>
                </li>

                <li><h1>Contate-me para parcerias e projetos!</h1>
                    <p>Interessado em colaborar? Entre em contato pelo e-mail para parcerias e projetos!</p>
                    <a href="mailto:contato@eduardobrito.dev" class="link-item">Clique aqui   <ArrowUpRight :size="23"/></a>
                </li>
            </ul>
        </div>
    </div>
    </section>
</template>

<style scoped>
/* Reset e configurações base */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Container principal */
.template {
  min-height: 100vh;
  background: linear-gradient(135deg, var(--color-black) 0%, #1a1a1a 100%);
  padding: 2rem 1rem;
  font-family: var(--font-montserrat);
  color: var(--color-white);
}

/* Seção do perfil */
section:first-child {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin-bottom: 3rem;
  animation: fadeInUp 0.8s ease-out;
}

/* Imagem de perfil */
.profile-image {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid var(--color-blue);
  box-shadow: 0 8px 24px rgba(0, 123, 255, 0.3);
  margin-bottom: 1.5rem;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  transform: scale(1.05);
  box-shadow: 0 12px 32px rgba(0, 123, 255, 0.4);
}

/* Textos de boas-vindas */
section:first-child h1 {
  font-family: var(--font-heading);
  font-size: 2.2rem;
  margin-bottom: 1rem;
  background: linear-gradient(45deg, var(--color-blue), var(--color-blue-hover));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

section:first-child p {
  font-size: 1.1rem;
  line-height: 1.6;
  color: var(--color-gray);
  font-family: var(--font-sans);
  margin-bottom: 0.5rem;
  max-width: 600px;
}

/* Container dos links */
.home {
  display: flex;
  justify-content: center;
  width: 100%;
}

.links {
  width: 100%;
  max-width: 500px;
}

/* Lista de links */
.link-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

/* Cada item da lista */
.link-list li {
  background: var(--color-cards);
  border-radius: 16px;
  padding: 1.5rem;
  border: 2px solid transparent;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
  animation: fadeInUp 0.6s ease-out;
  animation-fill-mode: both;
}

/* Animação escalonada para cada item */
.link-list li:nth-child(1) { animation-delay: 0.1s; }
.link-list li:nth-child(2) { animation-delay: 0.2s; }
.link-list li:nth-child(3) { animation-delay: 0.3s; }
.link-list li:nth-child(4) { animation-delay: 0.4s; }
.link-list li:nth-child(5) { animation-delay: 0.5s; }

/* Efeito hover nos itens */
.link-list li:hover {
  transform: translateY(-4px);
  border-color: var(--color-blue);
  box-shadow: 0 12px 32px rgba(0, 123, 255, 0.2);
}

/* Efeito de brilho ao passar o mouse */
.link-list li::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.05), transparent);
  transition: left 0.5s ease;
}

.link-list li:hover::before {
  left: 100%;
}

/* Títulos dos links */
.link-list h1 {
  font-family: var(--font-heading);
  font-size: 1.3rem;
  margin-bottom: 0.5rem;
  color: var(--color-white);
  font-weight: 600;
}

/* Descrições dos links */
.link-list p {
  font-size: 0.95rem;
  color: var(--color-gray);
  font-family: var(--font-sans);
  line-height: 1.5;
  margin-bottom: 1rem;
}


/* Botões/Links */
.link-item {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem; 
  background: linear-gradient(135deg, var(--color-blue), var(--color-blue-hover));
  color: var(--color-white);
  text-decoration: none;
  font-family: var(--font-sans);
  padding: 0.8rem 2rem;
  border-radius: 12px;
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.3s ease;
  box-shadow: 0 4px 16px rgba(0, 123, 255, 0.3);
  position: relative;
  overflow: hidden;
}

.link-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(0, 123, 255, 0.4);
  background: linear-gradient(135deg, var(--color-blue-hover), var(--color-blue));
}

.link-item:active {
  transform: translateY(0);
}

/* Animações */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Responsividade */
@media (max-width: 768px) {
  .template {
    padding: 1.5rem 1rem;
  }
  
  section:first-child h1 {
    font-size: 1.8rem;
  }
  
  section:first-child p {
    font-size: 1rem;
  }
  
  .profile-image {
    width: 100px;
    height: 100px;
  }
  
  .link-list li {
    padding: 1.2rem;
  }
  
  .link-list h1 {
    font-size: 1.1rem;
  }
  
  .link-item {
    padding: 0.7rem 1.5rem;
    font-size: 0.9rem;
  }
}

@media (max-width: 480px) {
  .template {
    padding: 1rem 0.5rem;
  }
  
  .links {
    max-width: 100%;
  }
  
  .link-list {
    gap: 1rem;
  }
  
  .link-list li {
    padding: 1rem;
  }
}

/* Efeito de pulse no botão de email */
.link-list li:last-child .link-item {
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0%, 100% {
    box-shadow: 0 4px 16px rgba(0, 123, 255, 0.3);
  }
  50% {
    box-shadow: 0 4px 16px rgba(0, 123, 255, 0.6);
  }
}
</style>