# Proposta de Roteiro de Testes

Tester: Lucas Carvalho Flores

### Considerações Iniciais

Me parece sensato assumir que seja necessário ter uma conta cadastrada para usar esse serviço a partir do aplicativo mobile.

Não sei que tipo de telas estão ou estarão presentes na aplicação, então o roteiro somente pode ser montado de forma conceitual.

## Roteiro

1. A primeira etapa seria testar as funcionalidades mais fundamentais, de criação de novo usuário, login e logout.

2. Em seguida, tentar usar funcionalizades protegidas por tráz de autenticação sem estar autenticado. Se isso não for possível diretamente pelo aplicativo mobile, eu vou ler o tipo de pauload utilizado pelo React Native para a tela a sendo testada, e então montar o mesmo payload manualmente via linha de comando e enviar sem credenciais (ou com credenciais inválidas) de autenticação, para verificar a segurança do sistema.
Por exemplo, se após a autenticação eu recebo um token de segurança, vou replicar manualmente um payload e trocar um caracter no token a ser enviado, tornando o token inválido. O sistema deve rejeitar esse payload e qualquer ação solicitada nele, respondendo apenas com um erro de acesso não autorizado ou similar, à discrição da equipe de desenvolvimento.
Testes desse tipo devem ser realizados para todos os endpoints do sistema que são protegidos por autenticação.

3. Após os testes de tentar usar funções protegidas sem estar devidamente autenticado, eu prossigo para testar uma a uma as funcionalidades fornecidas pela aplicação.
Se entendi corretamente o que o sistema oferece, os próximos testes serão especificamente para as funcionalidades que dependem de tirar as fotos das questões resolvidas no papel, resolvidas por humanos, para submissão ao sistema para serem analisadas e corrigidas.

4. Fazer uma reunição rápida em algum momento da semana para se alinhar sobre quais assuntos e tipos de problemas o sistema está implemetnado para conseguir reconhecer e resolver no estado atual do desenvolvimento do sistema.
Vamos chamar cada assunto que o sistema pode ser capaz de reconhecer, resolver e corrigir, de "competência".

5. Organizar estas competências em uma lista, separada por áreas e em ordem crescente de complexidade, como se eu fosse ensiar esses assuntos a estudantes.

6. Para cada competência do sistema a ser testada e verificada, eu vou consultar um livro didático adequado (definido previamente por consulta e orientação de professores do IM daqui da Ufal) para revisar o assunto para o qual vou elaborar os testes, e escolher questões da lista de questões do livro para a competência a ser testada.

7. Agora vou resolver uma lista de questões, onde vou propositalmente acertar algumas questões e errar outras.
Os erros serão divididos em três tipos diferentes de erros:
      1. Erros aritméticos.
      2. Erros algébricos.
      3. Erros de aplicação de teoremas e provas.  
      Suponho que erros do tipo 3 sejam os mais desafiadores para o sistema detectar e corrigir, e vou adorar acompanhar a evolução no sistema nesse e nos outros aspectos.

4. Ainda para cada competência, após elaborado e resolvido (com os erros propositais planejados) a lista de questões, vou fotografar uma a uma no aplicativo e registar o resultado respondido pelo sistema, com prints e anotações pessoais, incluindo as questões que errei propositalmente, onde errei, e qual seria uma forma correta de ter feito.
Vale notar que podem haver mais de uma forma correta de resolver um mesmo problema.

5. Os resultados desses testes devem então serem submetidos no Trello, Jira, YouTrack, Discord ou seja lá qual for a plataforma que a equipe do projeto estiver utilizando para organização e gestão do projeto e da equipe do projeto, com as devidas menções dos integrantes da equipe responsáveis por fazer uso dos resultados dos testes e informando quanto tempo foi gasto em cada atividade.
