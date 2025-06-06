# WG-Aereo
trabalho da umc M2

WG Aéreo – Sistema Web de Reservas de Voos
WG Aéreo é um sistema web completo para simular o cadastro de passageiros, escolha de destinos e reservas de voos. Desenvolvido com Spring Boot no backend e HTML/CSS/JavaScript no frontend, o projeto segue a arquitetura MVC e implementa diversos padrões de projeto reconhecidos.

Objetivo
Este projeto visa o desenvolvimento de um sistema educacional que integra tecnologias Java no backend e frontend moderno para simular uma aplicação de reservas aéreas. Foi projetado para demonstrar a integração entre camadas da aplicação e boas práticas de desenvolvimento web.

Backend (Java + Spring Boot)
• Java 17
• Spring Boot 3.x
• Spring Web
• Spring Data JPA
• MySQL
• Padrões de projeto: DAO, Facade, Singleton, Builder
Frontend (Web)
• HTML5 + CSS3
• JavaScript ES6
• Fetch API
• Google Fonts (Poppins)
• CSS Flexbox para responsividade
 Estrutura do Projeto
bash
CopiarEditar
wgAeroporto/
├── backend/
│ ├── controller/ # Controladores REST
│ ├── model/entity/ # Entidades JPA
│ ├── repository/ # Interfaces JPA
│ ├── service/ # Regras de negócio
│ └── facade/ # Fachada de serviços
├── frontend/
│ ├── index.html # Página inicial
│ ├── cadastro.html # Cadastro de passageiro
│ ├── consultar.html # Consulta de reservas
│ ├── voo.html # Associação de voos
│ ├── css/ # Estilos customizados
│ └── js/ # Scripts JS (fetch etc.)
└── docs/
 └── db_wgAereo.sql # Script do banco de dados
 Como Executar o Projeto
 Banco de Dados (MySQL)
1. Crie um banco chamado wg_aeroporto.
2. Importe o script SQL localizado em: /docs/db_wgAereo.sql.
3. Configure o arquivo application.properties no backend:
properties
CopiarEditar
spring.datasource.url=jdbc:mysql://localhost:3306/wg_aeroporto
spring.datasource.username=root
spring.datasource.password=SUASENHA
spring.jpa.hibernate.ddl-auto=update
 Rodando o Backend
bash
CopiarEditar
cd backend
./mvnw spring-boot:run
Ou com Maven instalado:
bash
CopiarEditar
mvn spring-boot:run
 Executando o Frontend
• Basta abrir o arquivo index.html diretamente no navegador.
• Para uma experiência mais completa, recomenda-se configurar um
servidor local (ex: Live Server no VSCode).
 Teste Rápido
1. Acesse index.html.
2. Selecione um destino.
3. Preencha o formulário com os dados do passageiro.
4. Clique em Cadastrar.
5. Salve o voo.
6. Vá até consultar.html para visualizar as reservas feitas.
 Autor
Desenvolvido por Gabriel e Weslley Viana
 Projeto didático com foco em prática de Java Web e frontend moderno.
 Licença
Este projeto é livre para fins educacionais e não possui restrições de uso para
aprendizado.
