# 💸 App de Finanças Pessoais com Vibe Coding

# PRD REFINADO 

```markdown
# PRD – MVP de App de Finanças Pessoais Conversacional

## Contexto
Aplicativo que organiza finanças pessoais de forma prática e natural, usando **conversas** em vez de formulários ou planilhas.

## Problema
As pessoas muitas vezes deixam de fazer controle de finanças porque não têm habilidade para lidar com planilhas ou não têm tempo de preencher muitos formulários ou criar fórmulas complexas.  
O objetivo é oferecer uma experiência simples, personalizada e motivadora sem travar o fluxo inicial.

## Público-Alvo
- Pessoas iniciantes no controle financeiro.  
- Usuários que querem praticidade e não têm experiência com planilhas ou apps complexos.  

---

## Funcionalidades-Chave do MVP

### Tela Inicial (Login)
- Exibe login e informações sobre as facilidades de fazer a gestão financeira pelo aplicativo e o slogan "Disciplina é liberdade".  
- Deve conter uma **imagem muito realista, de uma mulher morena, de cabelos ondulados e longos, com cachos nas pontas, sentada em posição de meditação relaxada e sorrindo em algum local ao ar livre**, com **imagens de sonhos e planos realizados ao fundo** (ex.: a mulher em uma casa moderna, a mulher praticando atividade física, a mulher em uma praia com amigas, a mulher com roupa de executiva em um trabalho), transmitindo a ideia de que ela está no controle da sua vida e tem tempo para usufruir de outras coisas.  
- Após login, leva à **Tela Principal**.

### Tela Principal
- Mostra receitas e despesas que impactam o mês corrente.  
- **Chat do Assistente Financeiro** (canto inferior esquerdo): registrar gastos e receitas por conversa.  
  - Quando o usuário informar uma despesa parcelada (ex.: curso de inglês em 10 parcelas de R$ 200):  
    - O app deve perguntar **qual a forma de pagamento**.  
    - Se for **débito em conta, PIX ou boleto** → perguntar **qual conta será usada**.  
    - Se for **cartão de crédito** → perguntar **qual cartão foi usado**.  
    - O aplicativo deve **prever automaticamente as parcelas para os meses seguintes**, conforme o meio de pagamento informado.  
- **Quadro lateral de desempenho** (direita):  
  - Barras de progresso mostrando percentuais entre realizado e esperado para cada categoria de despesa e metas cadastradas.  
  - Se não houver metas ou expectativas de gastos cadastradas, exibe mensagem:  
    *“É importante cadastrar expectativas de gastos e metas para uma boa gestão financeira.”*  
- **Botões principais** (localizados juntos):  
  - **Relatórios e Extratos**: leva à tela de relatórios.  
  - **Manutenção**: leva à tela de manutenção, onde o usuário pode cadastrar contas, cartões, categorias, despesas/receitas fixas e metas.  
  - **Compartilhar Gestão Financeira**: permite compartilhar o controle financeiro com terceiros via e-mail, com diferentes níveis de acesso.  

### Tela Manutenção
Acessível apenas por botão na Tela Principal. Permite cadastrar e editar:  
1. **Contas**: apenas campo para nome da conta.  
2. **Cartões de crédito**: nome do cartão, data de vencimento da fatura, data de virada da fatura.  
3. **Categorias de despesas e receitas**:  
   - Campo para informar se é **Despesa** ou **Receita**.  
   - Campo para informar o **nome da categoria**.  
   - Campo para informar a **expectativa de valor** a ser gasto ou recebido naquele mês.  
   - Campo para abrir e cadastrar **subcategorias** relacionadas àquela categoria (ex.: Categoria “Filho João” → Subcategorias “Educação”, “Transporte”).  
4. **Despesas/Receitas Fixas**:  
   - Campo para informar se é **Despesa** ou **Receita**.  
   - Campo para informar o **valor**.  
   - Campo para informar a **data de vencimento ou recebimento**.  
   - Campo para informar em **quantas vezes** ainda será paga ou recebida, ou se é por **tempo indeterminado**.  
   - O aplicativo deve prever automaticamente esse gasto ou receita para os próximos meses conforme a quantidade de vezes informada, ou replicar indefinidamente até que o usuário ajuste como finalizada.  
5. **Metas financeiras**: valores a serem guardados para objetivos específicos.  

### Tela de Relatórios e Extratos
- Exibe gráficos e relatórios de todas as despesas e receitas do mês corrente.  
- Caixa de seleção para visualizar outros meses.  
- Opção de exportar relatórios em **PDF, Excel e formatos comuns**.  

### Compartilhamento de Controle Financeiro
- Usuário pode compartilhar acesso com terceiros via e-mail.  
- Tipos de acesso:  
  - **Consulta + Relatórios**.  
  - **Consulta + Edição/Manutenção + Relatórios**.  

---

## Validação Inicial
- Testar se usuários conseguem usar o chat para registrar transações parceladas com diferentes meios de pagamento.  
- Verificar se entendem a função da **Tela Manutenção** para cadastrar dados.  
- Avaliar clareza das barras de desempenho e relatórios.  
- Métrica básica: quantos usuários completam cadastro de pelo menos uma conta/cartão e registram transações na primeira semana.  

```

# INTERAÇÕES COM O LOVABLE

> /create-prd # PRD – MVP de App de Finanças Pessoais Conversacional

> Na TELA MANUTENÇÃO, na parte de despesas e receitas fixas, acrescentar campo referente à conta ou cartão em que a despesa ou receita é gerada, para que a ferramenta insira no controle de contas e cartões. Nos relatórios e extratos deve ter opção de gerar relatório por tipo de conta ou de cartão e por período, podendo ser selecionado mais de um tipo de conta ou de cartão ou de um período (substituir a lista por marcadores que podem ser selecionados ou não). No assistente financeiro, se a conta ou cartão de pagamento ou de recebimento não estiver cadastrada, ele deve perguntar se o usuário deseja cadastrar e perguntar os mesmos dados que existem nos campos da tela manutenção, salvando a nova conta ou cartão. O nome do aplicativo deve ser alterado para LibertA. (//ele havia alterado o nome para FinanZen).

> Na parte do relatório, ao mudar o filtro, ele não está atualizando os relatórios. Inserir um botão para atualizar os relatórios em frente ao nome "Filtros de relatório", para que o relatório seja atualizado com os filtros que foram selecionados. E um botão "Limpar filtros". Se nenhum filtro tiver selecionado, os relatórios considerarão como se todos estivesse selecionados.

> Inclua a opção de "Editar" as contas, cartões, categorias, fixos e metas, para que não seja necessário excluir e reincluir.

> Quanto à expectativa de gastos e de receitas, é importante saber que é a expectativa mensal. Na tela inicial, deve ser considerada a expectativa x realidade do mês em curso ou do mês que foi selecionado no filtro. Na parte superior da tela inicial, onde está sendo exibido o mês e ano, deve ser exibido filtro para escolher qualquer mês e ano, para avaliar o desempenho. Outro erro que está acontecendo é que quando alteramos qualquer coisa na tela de manutenção ele não salva definitivamente. Depois que saímos e entramos de novo na tela, ele volta para os parâmetros iniciais, e não salva as alterações. Qualquer informações que for inserida na tela principal, no assistente ou na tela de manutenção deve atualizar todas as telas da ferramenta, todas as informações devem ser compartilháveis entre todas as telas: manutenção, relatórios e tela principal. Quanto aos filtros do relatório, mudar a concepção: só exibir as informações para as opções que estiverem marcadas. Ao clicar em limpar filtros, ele deve voltar para a marcação padrão, que é marcar todos os campos.

Resultado final no Lovable: https://libertapp.lovable.app/

# RESUMO DAS FUNCIONALIDADES DO APP

O app de gestão financeira permite a inclusão de receitas e despesas de forma automática por interação de texto ou voz com um chat. 

Ele possui uma tela de login com uma imagem que remete à tranquilidade de estar no controle das finanças pessoais e algumas referências ao que o aplicativo faz:

<img width="1900" height="876" alt="image" src="https://github.com/user-attachments/assets/e10c3ee1-1fdb-468d-9954-4f08994e70ea" />

Após o login, há uma uma tela principal onde está o chat assistente e onde são exibidas as informações principais de receitas e despesas e um monitor de gastos, receitas e metas previstas x realizadas para o mês corrente ou para outro mês de escolha do usuário, conforme filtro na parte superior, bem como três botões para telas acessórias:

<img width="1183" height="858" alt="image" src="https://github.com/user-attachments/assets/6562538d-9604-44d5-9d0e-d0950473e703" />
Nesta tela é necessário aprimorar as soluções e respostas para algumas perguntas do Chat Assistente, pois nem sempre ele sabe o que fazer e não dá uma solução adequada.

Na Tela Manutenção é possível parametrizar as contas, cartões, despesas e receitas fixas, categorias de receitas e despesas, com subcategorias e previsão de despesas ou gastos em cada categoria, e metas com valores e prazos, conforme a realidade do usuário:

<img width="1041" height="472" alt="image" src="https://github.com/user-attachments/assets/a82b97bc-aeb1-48a4-899a-b1a0b8bb3b89" />

Na Tela Relatórios e Extratos há gráficos e relatórios de acompanhamento com filtros personalizáveis por contas, cartões e períodos:

<img width="893" height="865" alt="image" src="https://github.com/user-attachments/assets/b5a4b249-e4d8-4ebb-a7b7-89003847f3b1" />

Necessário aprimoramento da parte do extrato para possibilitar a edição ou exclusão de receitas ou despesas lançadas, e também a parte dos filtros.

Na Tela de Compartilhamento deveria ser possível compartilhar o aplicativo com terceiros, que podem ter acesso somente de consulta ou acesso de colaboração, para inclusão de informações, manutenção e emissão de relatórios. Todavia não funcionou, sendo necessários ajustes no Lovable.

# REFLEXÃO SOBRE O PROCESSO

## O que funcionou bem? 
O Lovable entendeu bem a ideia e criou as telas conforme solicitado, mas foi fundamental ter refinado antes no Copilot, pois o Lovable possui muito poucos créditos.

## O que não funcionou como o esperado? 
Alguns detalhes precisarem ser bem melhor explicados para que e fossem aprimorados, de modo que compreendi que a especificação precisa ser muito bem detalhada e refinada várias vezes até obter o resultado esperado.

## O que aprendeu sobre conversar com IAs? 
É necessário especificar com muitos detalhes e que é necessário testar e refinar muitas vezes até ser possível obter o resultado desejado.

