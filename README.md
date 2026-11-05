##🎓 Portal de Palestras | Gestão de Carreira - IFG
Uma Single Page Application (SPA) estática e orientada a dados, desenvolvida para gerir e acompanhar a agenda de palestras da disciplina de Gestão de Carreira do curso de Sistemas de Informação do IFG (Instituto Federal de Goiás).

Com uma arquitetura leve e um Design System inspirado no Neo-Brutalismo (que remete a pósteres e zines clássicos de eventos), o portal foi projetado para ser 100% gerido através de um único ficheiro de configuração JSON, dispensando a necessidade de editar o código HTML para adicionar novos eventos.

##✨ Funcionalidades Principais
Arquitetura JSON-Driven: Todo o conteúdo da página (títulos, logótipos, palestrantes, datas e links) é gerado dinamicamente via JavaScript a partir do ficheiro config.json.

Design Neo-Brutalista: Estética de alto impacto, com bordas grossas, alto contraste (fundo creme e elementos em preto sólido) e estrutura visual semelhante a bilhetes de concertos impressos.

Gestão Inteligente de Links: Se um palestrante não tiver um link de material de apoio ou formulário de inscrição disponível, o botão é automaticamente renderizado, mas em estado desativado (disabled), mantendo a consistência do design.

Mobile-First e Responsivo: A interface foi construída para funcionar perfeitamente em ecrãs de telemóveis, expandindo-se num formato de grelha (Grid) organizado para tablets e computadores.

Zero Dependências: Construído inteiramente com HTML5, CSS3 e Vanilla JavaScript.

##🛠️ Tecnologias Utilizadas
Frontend: HTML5, CSS3 (Variáveis, CSS Grid, Flexbox) e JavaScript puro (ES6+).

Alojamento (Hospedagem): GitHub Pages.

Estrutura de Dados: JSON.

##⚙️ Como Atualizar o Portal (Para Administradores)
A principal vantagem deste projeto é que não precisa de conhecimentos avançados em programação para atualizar a agenda. Basta editar o ficheiro config.json localizado na raiz do repositório.

Exemplo de como adicionar uma nova palestra:

JSON
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
Assim que o ficheiro for atualizado no GitHub, a página irá refletir as alterações automaticamente.

##🚀 Como Executar Localmente
Como a aplicação faz uma requisição (fetch) para ler o ficheiro JSON, será necessário abrir o projeto através de um servidor local para evitar erros de CORS no navegador.

Clone este repositório:git clone [https://github.com/seu-usuario/nome-do-repositorio.git](https://github.com/seu-usuario/nome-do-repositorio.git)

Abra a pasta do projeto no seu editor (ex: VS Code).

Inicie um servidor local (Recomendação: extensão Live Server no VS Code).

O projeto estará a correr em [http://127.0.0.1:5500/](http://127.0.0.1:5500/).

Desenvolvido para a disciplina de Gestão de Carreira (Sistemas de Informação) - Instituto Federal de Goiás (IFG).
