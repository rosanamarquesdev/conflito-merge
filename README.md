Atividade: Simulação de Fluxo de Trabalho Git & GitHub

Este guia descreve o passo a passo para simular um fluxo de trabalho de desenvolvimento padrão, incluindo a criação de uma branch, a realização de um commit semântico e a abertura de um Pull Request (PR) para revisão.

Fase 1: Preparação Local (Na sua máquina)
Estes passos são feitos no seu terminal (Git Bash, PowerShell, etc.).

1. Clone o repositório
Baixe uma cópia exata do projeto do GitHub para o seu computador.

git clone [URL_DO_REPOSITORIO_AQUI]

Depois, entre na pasta do projeto:

cd [NOME_DO_PROJETO_CLONADO]

2. Crie sua nova branch
3. 
Crie uma "ramificação" nova para trabalhar, isolando suas alterações da main (principal). O nome deve seguir o padrão tipo/descrição (ex: feat/cria-erro-proposital).

git checkout -b feat/cria-erro-proposital

(Você será movido automaticamente para esta nova branch).

3. Faça a alteração (O erro proposital)

Abra o projeto no seu editor de código (como o VS Code).

Faça a alteração solicitada: apague um botão, remova uma linha de código importante, etc.

Salve o(s) arquivo(s) que você modificou.

Fase 2: Enviando as Mudanças (Terminal)

Agora, vamos "empacotar" e enviar suas alterações para o GitHub.

4. Adicione e "Comite" a alteração

Passo 4.1: Adicionar (Stage)

Informe ao Git quais arquivos você quer incluir no "pacote" de mudanças.

git add .

(O . significa "adicione todos os arquivos modificados nesta pasta e subpastas")

Passo 4.2: Commitar (Commit)

Crie o "pacote" (commit) com uma mensagem descritiva, seguindo o padrão de commit semântico.

git commit -m "feat: remove o botão de login da home"

5. Suba sua branch para o GitHub (Push)

Envie sua branch local (com seu commit) para o repositório remoto (GitHub).

git push origin feat/cria-erro-proposital

Nota: Se for a primeira vez que você sobe essa branch, o Git pode sugerir um comando um pouco mais longo (--set-upstream). Pode usar o que ele sugerir, que funciona da mesma forma.

Fase 3: Criando o Pull Request (Site do GitHub)
Esta parte é feita no repositorio remoto (site do GitHub)

6. Abra o Pull Request (PR)

Acesse a página do repositório no site do GitHub.

Assim que você subir sua branch (Passo 5), o GitHub mostrará um aviso amarelo/verde com o nome da sua branch e um botão: "Compare & pull request". Clique nele.

Se esse aviso não aparecer, vá manualmente para a aba "Pull requests" e clique no botão verde "New pull request".

Configure a comparação:

Base: main (ou master) <- É aqui que você quer que a mudança chegue.

Compare: feat/cria-erro-proposital <- É aqui que estão as suas mudanças.

Adicione o Reviewer (Revisor):

Na tela de criação do PR, olhe no menu à direita.

Encontre a seção "Reviewers".

Digite e selecione o usuário: rosanamarquesdev.

Adicione um título, uma breve descrição (se necessário) e clique em "Create pull request".

Pronto! A atividade está concluída e o PR está aguardando revisão.
