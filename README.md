🎓 Portal de Palestras | Gestão de Carreira - IFG

Uma Single Page Application (SPA) estática e orientada a dados, desenvolvida para gerir e acompanhar a agenda de palestras da disciplina de Gestão de Carreira do curso de Sistemas de Informação do IFG (Instituto Federal de Goiás).

Com uma arquitetura leve e um Design System inspirado no Neo-Brutalismo (que remete a pôsteres e zines clássicos de eventos), o portal foi projetado para ser 100% gerido através de um único arquivo de configuração JSON, dispensando a necessidade de editar o código HTML para adicionar novos eventos.

✨ Funcionalidades Principais

Arquitetura JSON-Driven: Todo o conteúdo da página (títulos, logotipos, palestrantes, datas e links) é gerado dinamicamente via JavaScript a partir do arquivo config.json.

Design Neo-Brutalista: Estética de alto impacto, com bordas grossas, alto contraste (fundo creme e elementos em preto sólido) e estrutura visual semelhante a bilhetes de shows impressos.

Gestão Inteligente de Links: Se um palestrante não tiver um link de material de apoio ou formulário de inscrição disponível, o botão é automaticamente renderizado, mas em estado desativado (disabled), mantendo a consistência do design.

Mobile-First e Responsivo: A interface foi construída para funcionar perfeitamente em telas de celulares, expandindo-se em um formato de grid organizado para tablets e computadores.

Zero Dependências: Construído inteiramente com HTML5, CSS3 e Vanilla JavaScript.

🛠️ Tecnologias Utilizadas

Frontend: HTML5, CSS3 (Variáveis, CSS Grid, Flexbox) e JavaScript puro (ES6+).

Hospedagem: GitHub Pages.

Estrutura de Dados: JSON.

⚙️ Como Atualizar o Portal (Para Administradores)

A principal vantagem deste projeto é que não precisa de conhecimentos avançados em programação para atualizar a agenda. Basta editar o arquivo config.json localizado na raiz do repositório.

Exemplo de como adicionar uma nova palestra:

{
  "id": "02",
  "titulo": "INOVAÇÃO EM STARTUPS TECNOLÓGICAS",
  "palestrante": {
    "nome": "CARLOS MENDES",
    "foto_url": "assets/carlos-mendes.jpg"
  },
  "tags": ["INOVAÇÃO", "STARTUP"],
  "data": "25 NOV",
  "dia_semana": "QUA.",
  "horario": "19:00",
  "links": {
    "inscricao": "https://link-do-formulario.com",
    "material": "" // Deixe vazio para desativar este botão no site
  }
}


Assim que o arquivo for atualizado no GitHub (via commit), a página do GitHub Pages irá refletir as alterações automaticamente após o build.

🚀 Como Executar Localmente

Como a aplicação faz uma requisição (fetch) para ler o arquivo JSON, será necessário abrir o projeto através de um servidor local para evitar bloqueios de segurança (CORS) no navegador.

Clone este repositório:
git clone https://github.com/seu-usuario/nome-do-repositorio.git

Abra a pasta do projeto no seu editor de código favorito (ex: VS Code).

Inicie um servidor local (Recomendação: extensão Live Server no VS Code).

O projeto estará rodando em http://127.0.0.1:5500/.

Desenvolvido para a disciplina de Gestão de Carreira (Sistemas de Informação) - Instituto Federal de Goiás (IFG) - Campus Goiânia.
