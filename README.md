<!DOCTYPE html>
<html>
<head>
  <title>Quiz sobre Sistemas Operacionais</title>
  <style>
    body {
      background-image: url("https://i.pinimg.com/originals/3f/7c/2e/3f7c2e51d5f75beabec6e5803551dc80.gif");
      background-size: cover;
      background-position: center;
      font-family: Calibri, Arial, sans-serif;
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      width: 500px;
      padding: 20px;
      background-color: rgba(0, 0, 0, 0.7);
      text-align: center;
      position: relative;
    }

    h1 {
      margin-top: 0;
      font-size: 24px;
    }

    #question {
      margin-bottom: 26px;
      font-size: 24px;
    }

    #options {
      text-align: left;
      margin-bottom: 24px;
    }

    label {
      display: block;
      margin-bottom: 14px;
      font-size: 18px;
    }

    #submit-btn,
    #next-btn {
      display: block;
      margin: 0 auto;
      width: 100px;
      padding: 10px;
      background-color: rgb(51, 8, 90);
      color: white;
      border: none;
      cursor: pointer;
    }

    #next-btn {
      display: none;
    }

    #result {
      font-weight: bold;
      display: none;
      margin-top: 20px;
      font-size: 20px;
    }

    #result.correct {
      color: green;
    }

    #result.incorrect {
      color: red;
    }

    /* Estilos para o rodapé */
    #footer {
      position: absolute;
      left: 0;
      right: 0;
      bottom: -30px; /* Ajuste a altura conforme necessário */
      margin: 0 auto;
      font-size: 14px;
      opacity: 0.5;
      transition: opacity 0.3s;
      text-align: center;
    }

    #footer:hover {
      opacity: 1;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Quiz sobre Sistemas Operacionais</h1>
    <div id="question"></div>
    <div id="options"></div>
    <button id="submit-btn">Responder</button>
    <button id="next-btn">Próxima Pergunta</button>
    <div id="result"></div>
    <div id="footer">
      Desenvolvido por Alex Oliveira
    </div>
  </div>

</body>
</html>
  <script>
    var questions = [
      {
        question: "1. Qual é o objetivo principal de um sistema operacional?",
        options: [
          "a) Tornar a utilização do computador mais simples",
          "b) Tornar a utilização do computador mais rápida",
          "c) Tornar a utilização do computador mais segura",
          "d) Todas as alternativas anteriores",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 3
      },
      {
        question: "2. O que é um sistema operacional?",
        options: [
          "a) Um conjunto de rotinas executado pelo processador",
          "b) Um conjunto de utilitários para facilitar a interação do usuário com o computador",
          "c) Uma interface gráfica para acessar os recursos do computador",
          "d) Um dispositivo de entrada e saída",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 0
      },
      {
        question: "3. Qual é a principal função de um sistema operacional?",
        options: [
          "a) Controlar o funcionamento do computador",
          "b) Gerenciar os recursos do computador",
          "c) Facilitar a interação do usuário com o computador",
          "d) Todas as alternativas anteriores",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 3
      },
      {
        question: "4. O que são utilitários em um sistema operacional?",
        options: [
          "a) Programas utilizados para facilitar a interação do usuário com o computador",
          "b) Conjuntos de rotinas executadas pelo processador",
          "c) Dispositivos de entrada e saída do computador",
          "d) Componentes de hardware essenciais para o funcionamento do sistema operacional",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 0
      },
      {
        question: "5. Por que é importante controlar o uso concorrente de recursos em um sistema operacional?",
        options: [
          "a) Para garantir a segurança dos recursos do sistema",
          "b) Para evitar conflitos entre diferentes usuários",
          "c) Para otimizar o compartilhamento de recursos e reduzir custos",
          "d) Todas as alternativas anteriores",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 3
      },
      {
        question: "6. O que significa o termo 'máquina de camada' em sistemas operacionais?",
        options: [
          "a) Programação realizada em linguagem de máquina",
          "b) Programação realizada em linguagem de alto nível",
          "c) Necessidade de conhecimento detalhado da arquitetura do hardware",
          "d) Facilidade de programação em sistemas modernos",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 2
      },
      {
        question: "7. Quais são os recursos comuns de um sistema computacional?",
        options: [
          "a) Monitores de vídeo, impressoras, unidades de CD/DVD, discos e fitas magnéticas",
          "b) Compiladores, linkers, bibliotecas e depuradores",
          "c) Linhas de comunicação e dispositivos de entrada e saída",
          "d) Todos os dispositivos conectados à internet",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 0
      },
      {
        question: "8. O que é compartilhamento de recursos em um sistema operacional?",
        options: [
          "a) A utilização simultânea de recursos por vários usuários",
          "b) A divisão de recursos entre diferentes sistemas operacionais",
          "c) O acesso exclusivo de recursos por um único usuário",
          "d) A criação de recursos virtuais para cada usuário",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 0
      },
      {
        question: "9. Quais são as funções básicas de um sistema operacional?",
        options: [
          "a) Controlar o funcionamento do computador e gerenciar os recursos",
          "b) Facilitar a interação do usuário com o computador",
          "c) Controlar o uso concorrente de recursos",
          "d) Todas as alternativas anteriores",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 3
      },
      {
        question: "10. Quais são os benefícios do compartilhamento de recursos em um sistema operacional?",
        options: [
          "a) Redução de custos",
          "b) Uso mais eficiente dos recursos",
          "c) Melhor aproveitamento das facilidades concorrentes",
          "d) Todas as alternativas anteriores",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 3
      },
      {
        question: "11. Quais foram as principais características de hardware na década de 2000?",
        options: [
          "a) Integração de componentes em alta escala",
          "b) Miniaturização dos equipamentos",
          "c) Redução de custos dos computadores",
          "d) Todas as alternativas anteriores",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 3
      },
      {
        question: "12. O que tornou os computadores mais acessíveis a diversas camadas da população na década de 2000??",
        options: [
          "a) Evolução dos processadores",
          "b) Evolução dos equipamentos de comunicação",
          "c) Redução de custos dos computadores",
          "d) Todas as alternativas anteriores",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 2
      },
      {
        question: "13. Quais dispositivos móveis se popularizaram na década de 2000?",
        options: [
          "a) Notebooks",
          "b) Netbooks",
          "c) PDAs",
          "d) Todos os dispositivos mencionados acima",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 3
      },
      {
        question: "14. Como os sistemas operacionais evoluíram na década de 2000 em relação à interação com o usuário?",
        options: [
          "a) Tornaram-se mais intuitivos",
          "b) Estiveram presentes em dispositivos móveis como telefones celulares",
          "c) Desenvolveram novas interfaces",
          "d) Todas as alternativas anteriores",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 3
      },
      {
        question: "15. Quais características foram incorporadas pelos sistemas operacionais na década de 2000 para torná-los mais eficientes? I Mecanismos automáticos para recuperação de erro II Atualização de correções e novas versões de forma automática III Proatividade no sistema                     Quais a alternativas verdadeiras!",
        options: [
          "a) II apenas",
          "b) II e III",
          "c) I, II e III",
          "d) I apenas",
          "e) todas são falsas"
        ],
        answer: 2
      },
      {
        question: "16. O que marcou o início da década de 2010 em termos de modelos computacionais? I Consolidação dos modelos computacionais em nuvem II Popularização de smartphones e tablets III Integração de componentes em alta escala               Quais afirmativas são verdadeiras  ??",
        options: [
          "a) I apenas",
          "b) II apenas",
          "c) III apenas",
          "d) I e II",
          "e) II e III"
        ],
        answer: 3
      },
      {
        question: "17. Uma aplicação que deseja chamar uma rotina do sistema operacional é o  mecanismo de ___________ ?",
        options: [
          "a) tempo de acesso",
          "b) system call",
          "c) sistema operacional",
          "d) terminal",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 1
      },
      {
        question: "18. Nos sistemas monoprogramáveis somente um programa pode estar em execução por vez, permanecendo o _________ dedicado, exclusivamente, a essa tarefa.",
        options: [
          "a) GPU",
          "b) Thread",
          "c) Sistema Operacional",
          "d) Disco Rígido",
          "e) Processador"
        ],
        answer: 4
      },{
        question: "19. Qual foi a tendência observada na década de 2010 em relação à computação em nuvem?",
        options: [
          "a) Maior adoção de modelos computacionais em nuvem",
          "b) Popularização de serviços de armazenamento em nuvem",
          "c) Integração de aplicativos e serviços baseados em nuvem nos sistemas operacionais",
          "d) Todas as alternativas anteriores",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 3
      },
      {
        question: "20. Nos primeiros computadores, a programação era realizada em _____________________, em painéis através de fios, exigindo, consequentemente, um grande conhecimento da arquitetura do hardware. Isso era uma grande dificuldade para os programadores da época?",
        options: [
          "a) JavaScript",
          "b) memória cache",
          "c) linguagem de máquina",
          "d) computação de nuvem ",
          "e) modo de acesso "
        ],
        answer: 2
      },
      {
        question: "21. Quem são os fundadores da Microsoft?",
        options: [
          "a) Bill Gates e Paul Allen",
          "b) Mark Zuckerberg e Eduardo Saverin",
          "c) Larry Page e Sergey Brin",
          "d) Steve Jobs e Steve Wozniak ",
          "e)  Jeff Bezos e Elon Musk"
        ],
        answer: 0
      },
      {
        question: "22. Qual foi a ordem de lançamento dos Windows a seguir I Windows 95 II Windows XP  III Windows 1 IV Windows 7 V Windows 10? ?",
        options: [
          "a) I, II, V, III, IV",
          "b) III, I, II, V, IV",
          "c) II, I, IV, V, III",
          "d) I, IV, V, III, II",
          "e) III, I, II, IV, V"
        ],
        answer: 4
      },
      {
        question: "23. Analise as afirmações a seguir I A primeira versão do Windows foi muito popular II Uma das principais críticas era que o sistema era “pesado”,  quais alternativas são verdadeiras ?",
        options: [
          "a) I apenas",
          "b) II apenas",
          "c) Todas são verdadeiras",
          "d) Todas são falsas ",
          "e) I é verdadeira e a II justifica a primeira"
        ],
        answer: 1
      },
      {
        question: "24. Qual é o sistema operacional mais utilizado entre pessoas em geral ?",
        options: [
          "a) Linux",
          "b) MacOS",
          "c) Unix",
          "d) IBM",
          "e) Windows"
        ],
        answer: 4
      },
      {
        question: "25. Qual versão do Windows foi lançada em 1990?",
        options: [
          "a) Windows 3",
          "b) Windows ME",
          "c) Windows XP",
          "d) Windows 1",
          "e) Windows Vista"
        ],
        answer: 0
      },
      {
        question: "26. Quais são os sistemas operacionais da Microsoft que foram lançados antes do Windows 10?",
        options: [
          "a) Windows 7, Windows 8 e Windows 8.1",
          "b) Windows Vista, Windows 7 e Windows 8",
          "c) Windows 95, Windows 98 e Windows ME",
          "d) Windows XP, Windows Vista e Windows 7",
          "e) Windows 2000, Windows XP e Windows Vista"
        ],
        answer: 0
      },
      {
        question: "27. Qual é o sistema operacional mais utilizado para servidores?",
        options: [
          "a) Windows ",
          "b) Linux",
          "c) macOS ",
          "d) Unix",
          "e) FreeBSD"
        ],
        answer: 1
      },
      {
        question: "28. Quais são as principais vantangens do Linux?",
        options: [
          "a) Instabilidade, Segurança, Compatibilidade com Hardware, Liberdade, Alto Custo",
          "b) Instabilidade, Insegurança, Compatibilidade com Hardware, Liberdade, Baixo Custo",
          "c) Escalabilidade, Segurança, Compatibilidade com Hardware, Liberdade, Baixo Custo",
          "d) Estabilidade, Segurança, Compatibilidade com Hardware, Liberdade, Baixo Custo",
          "e) Estabilidade, Segurança, Compatibilidade com Hardware, Liberdade, Alto Custo"
        ],
        answer: 3
      },
      {
        question: "29. O que é uma característica do Linux em termos de compatibilidade com hardware?",
        options: [
          "a) Funciona apenas em computadores modernos",
          "b) Requer especificações de hardware avançadas",
          "c) Funciona apenas em processadores Intel",
          "d) Funciona em praticamente todos os computadores, independentemente do modelo ou processador",
          "e) Oferece melhor suporte a dispositivos externos"
        ],
        answer: 3
      },
      {
        question: "30. Qual empresa famosa utiliza o sistema Linux?",
        options: [
          "a) Apple",
          "b) Microsoft",
          "c) Facebook",
          "d) Amazon",
          "e) Google"
        ],
        answer: 4
      },{
        question: "31. Qual foi o primeiro sistema operacional lançado pela Microsoft com interface gráfica?",
        options: [
          "a) Windows 1.0",
          "b) Windows 2.0",
          "c) Windows 3.0",
          "d) Windows 95",
          "e) Windows 10"
        ],
        answer: 0
      },
      {
        question: "32. Qual foi a primeira versão do Windows capaz de sobrepor janelas de aplicativos?",
        options: [
          "a) Windows 1.0",
          "b) Windows 2.0",
          "c) Windows 3.x",
          "d) Windows 95",
          "e) Windows 8"
        ],
        answer: 1
      },
      {
        question: "33. Quais recursos NÃO foram introduzidos no Windows 95?",
        options: [
          "a) Menu Iniciar e Barra de Tarefas",
          "b) Gerenciador de Programas e File Explorerr",
          "c) capacidade de tirar proveito do poder de processamento das CPUS",
          "d) Interface gráfica e mouse",
          "e) Tecnologia Plug & Play e upgrades fáceis"
        ],
        answer: 2
      },
      {
        question: "34. Qual versão do Windows a ser um sucesso de crítica e público, com elogios à sua capacidade de multitarefa e facilidade de uso ?",
        options: [
          "a) Windows 1.0",
          "b) Windows 2.0",
          "c) Windows 3.x",
          "d) Windows XP",
          "e) Windows 95"
        ],
        answer: 2
      },
      {
        question: "35. Qual era a principal elemento interface da primeira versão do Windows?",
        options: [
          "a) barra de tarafas",
          "b) gerenciador de arquivos",
          "c) Painel de controle",
          "d) Atalhos de teclado",
          "e) Unidade central de processamento"
        ],
        answer: 1
      },
      {
        question: "36. Qual foi o sistema operacional da Microsoft apoiado por uma grande campanha de marketing envolvendo uma musica dos Rolling Stones e atores da série Friends ?",
        options: [
          "a) Windows 1.0",
          "b) Windows 2.0",
          "c) Windows 3.x",
          "d) Windows 95",
          "e) Windows XP"
        ],
        answer: 4
      },
      {
        question: "37. Quais conceitos estrearam no Windows 95 tão diferentes para a época que gerou uma indústria de cursos sobre Windows 95?",
        options: [
          "a) Menu Iniciar e Barra de Tarefas",
          "b) Barra de Tarefas e gerenciador de arquivos",
          "c) Multitarefa e capacidade de armazenamento",
          "d) Interface gráfica e monotarefa",
          "e) Plug & Play e sobreposição de janelas"
        ],
        answer: 0
      },
      {
        question: "38. Qual versão do Windows prometia facilitar o upgrade do computador com tecnologia Plug & Play??",
        options: [
          "a) Windows 1.0",
          "b) Windows 2.0",
          "c) Windows 3.0",
          "d) Windows 95",
          "e) Windows XP"
        ],
        answer: 3
      },
      {
        question: "39. Quais aplicativos estavam presentes no Windows 1.0?",
        options: [
          "a) Paint, calculadora, agenda, editor de texto, Reversi",
          "b) Gerenciador de Programas, File Explorer, Paint, Reversi",
          "c) Menu Iniciar, Barra de Tarefas, Paint, editor de texto",
          "d) Multitarefa, facilidade de uso, agenda, calculadora",
          "e) Interface gráfica, mouse, jogos, calculadora"
        ],
        answer: 0
      },
      {
        question: "40. Qual foi a primeira versão do Windows a rodar sobre o MS-DOS e não ser um sistema operacional completo?",
        options: [
          "a) Windows 1.0",
          "b) Windows 2.0",
          "c) Windows 3.0",
          "d) Windows 95",
          "e) Windows XP"
        ],
        answer: 0
      },
      {
        question: "41. Sobre o Linux é correto afirmar?",
        options: [
          "a) Um sistema operacional pago, mas com estabilidade e segurança",
          "b) A plataforma é conhecida por ser adotada mais por servidores do que por usuários finais o que dá a ela a fama de ser difícil",
          "c) Um fato que muitos sabem é que o Linux é bem menos seguro que o Windows",
          "d) Não funciona normalmente em todos os computadores",
          "e) Nenhuma das alternativas anteriores"
        ],
        answer: 1
      },
      {
        question: "42. O que é destacado como uma das características do Linux?",
        options: [
          "a) Estabilidade",
          "b) Compatibilidade com Hardware",
          "c) Liberdade",
          "d) Segurança",
          "e) Todas as alternativas"
        ],
        answer: 4
      },
      {
        question: "43. Qual usuário precisa aprovar as instalações ou alterações necessárias no sistema Linux?",
        options: [
          "a) Root ou Superusuário",
          "b) Admin",
          "c) Usuário comum",
          "d) Todos os usuários",
          "e) Usuário primário"
        ],
        answer: 0
      },
      {
        question: "44. Qual sistema operacional é conhecido por ser adotado mais por servidores do que por usuários finais??",
        options: [
          "a) Windows",
          "b) Linux",
          "c) macOS X",
          "d) Windows e macOS X",
          "e) Linux e macOS X"
        ],
        answer: 1
      },
      {
        question: "45. Qual é uma das vantagens do Linux em termos de compatibilidade com hardware?",
        options: [
          "a) Funciona normalmente em praticamente todos os computadores",
          "b) Funciona apenas em computadores mais antigos",
          "c) Possui restrições quanto aos modelos de computadores suportados",
          "d) Requer um processador específico para funcionar corretamente",
          "e) Nenhuma das opções está correta"
        ],
        answer: 0
      },{
        question: "46. Por que o Linux é considerado de baixo custo?",
        options: [
          "a) Por ser um sistema open source",
          "b) Por ter programas livres",
          "c) Por não precisar de licenças de software",
          "d) Por ser gratuito para copiar e instalar",
          "e) Todas as opções estão corretas"
        ],
        answer: 4
      },
      {
        question: "47. Quais são algumas das funções do núcleo do sistema operacional?",
        options: [
          "a) Tratamento de interrupções e exceções",
          "b) Um conjunto de utilitários para facilitar a interação do usuário com o computador",
          "c) Criação e eliminação de processos e threads",
          "d) Gerência do sistema de arquivos",
          "e) Todas as alternativas anteriores"
        ],
        answer: 4
      },
      {
        question: "48. Uma das principais características da multiprogramação é permitir que vários programas compartilhem o _____________. O ________________ deve ser responsável pelo controle da utilização da__________.",
        options: [
          "a) Processo, Usuário, placa-mãe",
          "b) Escalonamento, controle, memória ",
          "c) Núcleo, Processador, UCP",
          "d) Processador, Sistema Operacional, UCP",
          "e) Sistema operacional,  processo, memória"
        ],
        answer: 3
      },
      {
        question: "49. Muitas das principais implementações de segurança de um sistema operacional utilizam um mecanismo presente no hardware dos processadores, é conhecido como? ",
        options: [
          "a) Sincronização",
          "b) Escalonamento",
          "c) Gerência de memória",
          "d) Contabilização do uso do sistema",
          "e) Modo de acesso"
        ],
        answer: 4
      },
      {
        question: "50. Em geral, os processadores possuem dois modos de acesso, quai são eles?",
        options: [
          "a) Modo análago, modo usuário",
          "b) Modo usuário, modo kernel",
          "c) modo kernel, modo multivalorado",
          "d) modo usuário, modo Scram",
          "e) modo kernel, modo de instrução"
        ],
        answer: 1
      },
      {
        question: "51. Qual função do núcleo do sistema operacional lida com a detecção de possíveis ameaças??",
        options: [
          "a) Auditoria e segurança do sistema",
          "b) Sincronização e comunicação entre processos e threads",
          "c) Gerência de segurança do hardware",
          "d) Tratamento de interrupções e exceções",
          "e) Segurança e gerência de dispositivos de E/S"
        ],
        answer: 0
      },
      {
        question: "52. Qual dessas funções abaixo não é uma das responsabilidades do sistema operacional?",
        options: [
          "a) Tratamento de interrupções e exceções",
          "b) Gerenciamento da memórias",
          "c) Controlar o acesso aos dispositivos de entrada e saída",
          "d) Suporte a redes locais e distribuídas",
          "e) Interface gráfica do usuário"
        ],
        answer: 4
      },
      {
        question: "53. O que ocorre se uma aplicação tenta executar uma instrução privilegiada diretamente sem utilizar uma rotina do sistema operacional ??",
        options: [
          "a) O próprio hardware do processador sinalizará com um erro.",
          "b) Uma aplicação deve assim ser sempre executada com o processador em modo usuário.",
          "c) Uma exceção é gerada e a execução do programa é interrompida, protegendo o núcleo do sistema",
          "d) O mecanismo de proteção por hardware garantirá a segurança do sistema.",
          "e) Todas as alternativas anteriores"
        ],
        answer: 4
      },
      {
        question: "54. Em um sistema multiprogramável, qual é a principal função do sistema operacional em relação ao uso da Unidade Central de Processamento (UCP)?",
        options: [
          "a) Permitir que um programa monopolize o uso da UCP",
          "b) Gerenciar o compartilhamento da UCP entre os programas",
          "c) Aumentar a capacidade de processamento da UCP",
          "d) Impedir o acesso dos programas à UCP",
          "e) Otimizar a velocidade de processamento da UCP"
        ],
        answer: 1
      },
      {
        question: "55. Qual é o modo de acesso do processador que permite que uma aplicação execute instruções não privilegiadas?",
        options: [
          "a) Modo de execução limitada",
          "b) Modo kernel",
          "c) Modo privativo",
          "d) Modo de acesso restrito",
          "e) Modo usuário"
        ],
        answer: 4
      },
      {
        question: "56. Em sistemas monoprogramáveis, quantos programas podem estar em execução simultaneamente?",
        options: [
          "a) Apenas um programa",
          "b) Dois programas",
          "c) Três programas",
          "d) Vários programas",
          "e) Todos os programas disponíveis"
        ],
        answer: 0
      },
      {
        question: "57. O que é um buffer no contexto de um sistema de computador?",
        options: [
          "a) Um espaço de memória para armazenar dados temporariamente?",
          "b) Um dispositivo de armazenamento permanente de dados",
          "c) Um componente de hardware que melhora o desempenho do processador",
          "d) Um software de segurança para proteger os dados do sistema",
          "e) Um espaço de memória para armazenar dados permanentemente"
        ],
        answer: 0
      },
      {
        question: "58. Qual é a principal finalidade do armazenamento em cache no sistema operacional?",
        options: [
          "a) Reduzir o tempo de acesso a dispositivos de entrada e saída",
          "b) Aumentar a capacidade de armazenamento da memória principal",
          "c) Gerenciar o compartilhamento de recursos entre os programas",
          "d) Acelerar o acesso a dados frequentemente utilizados",
          "e) Melhorar a segurança dos dados do usuário"
        ],
        answer: 3
      },
      {
        question: "59. O buffering é usado para lidar com a diferença de velocidade entre o recebimento e o processamento de dados. Onde os dados são armazenados temporariamente durante o buffering?",
        options: [
          "a) Memória Cache",
          "b) Registradores",
          "c) Memória principal",
          "d) Disco rígido",
          "e) Buffer de entrada/saída"
        ],
        answer: 4
      },
      {
        question: "60. Qual é uma memória implementada no processador que armazena a cópia dos dados originais?",
        options: [
          "a) Buffering",
          "b) Caching",
          "c) Memória Ram",
          "d) Memória Secundária",
          "e) todas as alternativas estão incorretas"
        ],
        answer: 1
      },{
        question: "61. Qual é a diferença fundamental entre buffering e caching?",
        options: [
          "a) O buffering é usado para armazenar dados temporariamente, enquanto o caching é usado para armazenar dados frequentemente utilizados.",
          "b) O buffering é usado para melhorar o desempenho do sistema, enquanto o caching é usado para lidar com a diferença de velocidade entre o recebimento e o processamento de dados.",
          "c) O buffering armazena dados em cache, enquanto o caching armazena dados em um dispositivo de armazenamento externo",
          "d) O buffering é aplicado em sistemas monoprogramáveis, enquanto o caching é aplicado em sistemas multiprogramáveis",
          "e) O buffering é uma técnica de hardware, enquanto o caching é uma técnica de software"
        ],
        answer: 0
      },
      {
        question: "62.O que o sistema operacional deve garantir em relação à execução concorrente de programas e à integridade do sistema operacional?",
        options: [
          "a) A confiabilidade do hardware",
          "b) A segurança dos dados do usuário",
          "c) A exclusividade do uso da UCP por um único programa",
          "d) O compartilhamento equitativo dos recursos entre os programas",
          "e) Todas as alternativas"
        ],
        answer: 4
      },
      {
        question: "63. O que é buffering num conceito de sistema operacional?",
        options: [
          "a) Armazenamento temporário de dados que são repetidamente visitados",
          "b) Armazenamento de dados em um disco de velocidade rápida",
          "c) Correção da diferença de velocidade entre dispositivos de comunicação",
          "d) Armazenamento de cópias dos dados originais",
          "e) Memória implementada no processador para acesso rápido"
        ],
        answer: 2
      },
      {
        question: "64. Sobre o buffer é correto afirmar que eles são do tipo?",
        options: [
          "a) Hardware apenas",
          "b) Software apenas",
          "c) Hardware ou Solftware",
          "d) Hardware ou software, mas em geral o buffer de software é amplamente mais utilizado. ",
          "e) Hardware ou software, mas em geral o buffer de hardware é amplamente mais utilizado. "
        ],
        answer: 3
      },
      {
        question: "65. Sobre a finalidade do caching é correto afirmar que o caching deve??",
        options: [
          "a) Evitar o tráfico de rede",
          "b) Armazenar temporariamente os dados que são repetidamente visitados",
          "c) Armazenar cópias dos dados originais para acesso rápido",
          "d) Armazenar dados em um disco de velocidade rápida",
          "e) Todas as afirmações acima estão corretas"
        ],
        answer: 4
      },
      {
        question: "66. Onde ocorre o buffering?",
        options: [
          "a) Na memória cache",
          "b) No processador",
          "c) Na mémoria RAM",
          "d) No disco rígido",
          "e) Na memória secundária"
        ],
        answer: 2
      },
      {
        question: "67. O que são chamadas de sistema (system calls)?",
        options: [
          "a) Funções específicas que invocam o sistema operacional para realizar tarefas complexas",
          "b) Tarefas executadas pelo sistema operacional para gerenciar recursos de hardware",
          "c) Ações realizadas pelo usuário para acessar arquivos e pastas",
          "d) Rotinas do sistema operacional para proteger o núcleo do sistema",
          "e) Instruções privilegiadas executadas diretamente pela aplicação"
        ],
        answer: 0
      },
      {
        question: "68. Qual é a consequência de uma aplicação tentar executar uma instrução privilegiada diretamente, sem utilizar uma chamada de sistema?",
        options: [
          "a) O sistema operacional executará a instrução com privilégios reduzidos",
          "b) O sistema operacional interromperá a execução do programa e gerará uma exceção",
          "c) A aplicação receberá um aviso de erro, mas continuará sua execução",
          "d) A aplicação não será interrompida nem encerrada pelo sistema operacional",
          "e) A instrução será executada normalmente, sem causar problemas"
        ],
        answer: 1
      },
      {
        question: "69. Como o sistema operacional garante a execução segura das chamadas de sistema?",
        options: [
          "a) Verificando se a aplicação possui privilégios necessários antes de permitir a execução da rotina",
          "b) Atribuindo privilégios especiais a todas as aplicações",
          "c) Limitando o número de chamadas de sistema que uma aplicação pode fazer",
          "d) Bloqueando todas as chamadas de sistema e permitindo apenas o acesso a recursos de hardware",
          "e) Permitindo que todas as aplicações executem instruções privilegiadas diretamente"
        ],
        answer: 0
      },
      {
        question: "70. Qual é a finalidade do modo kernel em um processador?",
        options: [
          "a) Permite que uma aplicação acesse um conjunto reduzido de instruções do processador",
          "b) Restringe o acesso da aplicação às instruções do processador",
          "c) Define o conjunto total de instruções que uma aplicação pode executar",
          "d) Determina a localização do buffer na memória RAM",
          "e) Permite que uma aplicação acesse o conjunto total de instruções do processador"
        ],
        answer: 4
      },
      {
        question: "71. Podemos definir chamadas de sistemas como funções, porém, são funções específicas que invocam o sistema operacional para que este faça algo, como a criação de um __________?",
        options: [
          "a) Processo",
          "b) Processador",
          "c) Sistema multiprogramável",
          "d) Disco rígido",
          "e) Conjunto de instruções"
        ],
        answer: 0
      },
      {
        question: "72. Diferente do buffer que acontece na Memória RAM onde ocorre o caching?",
        options: [
          "a) Evolução dos processadores",
          "b) Processador ou em disco",
          "c) Arquivos de paginação ",
          "d) Memória virtual ou processador ",
          "e) Dispositivos de armazenamento externo"
        ],
        answer: 1
      },
      {
        question: "73. O que são system calls?",
        options: [
          "a) Instruções de acesso direto à memória RAM",
          "b) Rotinas do sistema operacional para manipulação de dispositivos de entrada e saída",
          "c) Funções específicas que invocam o sistema operacional para realizar tarefas complexas",
          "d) Protocolos de comunicação entre diferentes processos do sistema operacional",
          "e) Instruções de acesso direto ao processador"
        ],
        answer: 2
      },
      {
        question: "74. Sobre as afirmaçoes a seguir sobre system call quais são verdadeiras ?:  I O sistema operacional verificará se a aplicação possui privilégios necessários para executar a rotina desejada. II Em caso negativo, o sistema operacional não consegue impedir o desvio para a rotina.III Este é um mecanismo de proteção por software. IV Garante que as aplicações só poderão executar rotinas autorizadas",
        options: [
          "a) I apenas",
          "b) I, II e III",
          "c) I, II e IV",
          "d) I, III, e IV",
          "e) I, II, III e IV"
        ],
        answer: 3
      },
      {
        question: "75. Quais características foram incorporadas pelos sistemas operacionais na década de 2000 para torná-los mais eficientes? I Mecanismos automáticos para recuperação de erro II Atualização de correções e novas versões de forma automática III Proatividade no sistema                     Quais a alternativas verdadeiras!",
        options: [
          "a) II apenas",
          "b) II e III",
          "c) I, II e III",
          "d) I apenas",
          "e) todas são falsas"
        ],
        answer: 2
      },
      {
        question: "76. Quais das afirmaçoes abaixo é um possíveis impactos caso uma aplicação comprometa a integridade do núcleo do sistema operacional?",
        options: [
          "a) O sistema pode ficar inoperante",
          "b) A aplicação pode ser instalada automaticamente",
          "c) O desempenho de outros aplicativos podem ser melhorados",
          "d) O sistema pode exigir uma permissão do especifica do processador",
          "e) As configurações do sistema podem ser bloqueadas e apagadas da mémoria"
        ],
        answer: 0
      },
      {
        question: "77. O que é uma preocupação nos projetos de sistemas operacionais em relação à integridade do núcleo e acesso aos seus serviços??",
        options: [
          "a) A compatibilidade com diferentes dispositivos externos",
          "b) A alocação eficiente de recursos de hardware",
          "c) A otimização de desempenho do sistema",
          "d) A interface gráfica do usuário",
          "e) A implementação de mecanismos de proteção"
        ],
        answer: 4
      },
      {
        question: "78. Quando o processador trabalha no modo usuário, uma aplicação só́ pode executar instruções conhecidas como ?",
        options: [
          "a) Instruções de alto desempenho",
          "b) Instruções não privilegiadas",
          "c) Instruções de baixo nível",
          "d) Instruções de acesso restrito",
          "e) Instruções de controle do sistema"
        ],
        answer: 1
      },
      {
        question: "79. Qual é o objetivo das chamadas de sistemas (system calls) em relação aos usuários comuns?",
        options: [
          "a) Permitir que realizem tarefas complexas de baixo nível no sistema",
          "b) Conceder permissões especiais aos usuários comuns",
          "c) Simplificar a interação com o sistema operacional",
          "d) Controlar as configurações de segurança do sistema operacional",
          "e) Controlar as configurações de segurança do sistema operacional"
        ],
        answer: 2
      }
    ];

    var currentQuestion = 0;
    var score = 0;

    var questionElement = document.getElementById("question");
    var optionsElement = document.getElementById("options");
    var submitButton = document.getElementById("submit-btn");
    var nextButton = document.getElementById("next-btn");
    var resultElement = document.getElementById("result");

    function showQuestion() {
      var question = questions[currentQuestion];
      questionElement.textContent = question.question;

      var options = question.options;
      optionsElement.innerHTML = "";

      for (var i = 0; i < options.length; i++) {
        var option = options[i];
        var label = document.createElement("label");
        var input = document.createElement("input");
        input.type = "radio";
        input.name = "answer";
        input.value = i;
        label.appendChild(input);
        label.appendChild(document.createTextNode(option));
        optionsElement.appendChild(label);
      }
    }

    function showResult() {
      var question = questions[currentQuestion];
      var selectedOption = document.querySelector('input[name="answer"]:checked');
      var answerIndex = selectedOption ? parseInt(selectedOption.value) : -1;

      var correctAnswer = question.options[question.answer];
      var userAnswer = question.options[answerIndex];

      var resultMessage = document.createElement("div");

      if (answerIndex === question.answer) {
        resultMessage.textContent = "Você acertou!";
        resultMessage.classList.add("correct");
        resultMessage.style.color = "green";
        score++;
      } else {
        resultMessage.textContent = "Você errou!";
        resultMessage.classList.add("incorrect");
        resultMessage.style.color = "red";
      }

      var correctAnswerElement = document.createElement("div");
      correctAnswerElement.textContent = "Resposta correta: " + correctAnswer;

      var userAnswerElement = document.createElement("div");
      userAnswerElement.textContent = "Sua resposta: " + userAnswer;

      resultElement.innerHTML = "";
      resultElement.appendChild(resultMessage);
      resultElement.appendChild(correctAnswerElement);
      resultElement.appendChild(userAnswerElement);

      resultElement.style.display = "block";
    }

    function nextQuestion() {
      currentQuestion++;
      if (currentQuestion === questions.length - 1) {
        nextButton.textContent = "Finalizar";
      }
      if (currentQuestion === questions.length) {
        showResult();
        submitButton.style.display = "none";
        nextButton.style.display = "none";
      } else {
        showQuestion();
        submitButton.style.display = "block";
        nextButton.style.display = "none";
        resultElement.textContent = "";
        resultElement.style.display = "none";
        resultElement.classList.remove("correct");
        resultElement.classList.remove("incorrect");
      }
    }

    showQuestion();

    submitButton.addEventListener("click", function() {
      showResult();
      submitButton.style.display = "none";
      nextButton.style.display = "block";
    });

    nextButton.addEventListener("click", nextQuestion);
  </script>
</body>
</html>
