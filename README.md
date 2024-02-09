# Power Track

O Power Track é um sistema de rastreamento e gerenciamento de incidentes e solicitações de serviço projetado para atender às necessidades de diversas áreas de uma organização. Proporcionando flexibilidade e funcionalidades abrangentes, o Power Track permite o registro eficiente, monitoramento e resolução de uma ampla gama de solicitações e incidentes.

## Funcionalidades Principais

- **Gerenciamento de Grupos e Usuários:** Crie, adicione usuários e designe administradores para grupos, facilitando o gerenciamento interno.
- **Registro e Monitoramento de Atividades:** Mantenha um registro completo de todas as interações e atividades para fins de auditoria.
- **Vinculação com Bases de Conhecimento:** Acesse uma base de conhecimento integrada para soluções rápidas e eficazes.
- **Abertura de Chamados por Diferentes Meios:** Possibilite a abertura de chamados por HTTP Endpoint e via chatbot para maior conveniência.
- **Controle de Permissões e Acesso:** Configure permissões específicas para administradores do aplicativo, grupos e chamados.
- **Grupos Privados:** Crie grupos privados para lidar com informações sensíveis e restrinja o acesso apenas aos membros autorizados.

## Contribuição

O Power Track valoriza contribuições da comunidade para aprimorar o projeto. Se você deseja contribuir com melhorias, correções ou novas funcionalidades, siga estas etapas:

1. Faça um fork do repositório.
2. Clone o repositório para o seu ambiente local.
3. Crie uma branch para suas alterações: `git checkout -b feature/nova-funcionalidade`.
4. Faça suas alterações e commit: `git commit -m 'Adiciona nova funcionalidade'`.
5. Faça push para a branch: `git push origin feature/nova-funcionalidade`.
6. Abra um pull request para revisão.

Qualquer necessidade, bug ou sugestão de melhoria também pode ser solicitada como uma issue no projeto. Acompanhe o andamento do desenvolvimento na aba "Projects" do próprio repositório.

## Time do projeto
[Antônio Gabriel Follone Graça](https://www.linkedin.com/in/ant%C3%B4nio-gabriel-follone-gra%C3%A7a-a03515184/) As PM/Dev<br>
[Daniel Damaceno](https://www.linkedin.com/in/daniel-damaceno/) As Tech Writer/Q.A<br>
[Antônio Matheus Follone Graça](https://www.linkedin.com/in/antonio-matheus-follone-gra%C3%A7a-02a940199/) As Dev/Q.A<br>

## Licença

Este projeto é licenciado sob a [MIT License](LICENSE), o que significa que você tem liberdade para usar, modificar e distribuir o código, sujeito às condições da licença.


## Convenções de Nomenclatura

> 🚨 O projeto em questão utiliza Camel Case para nomear soluções, componentes, controles, coleções, variáveis e todos os elementos relacionados ao desenvolvimento do projeto.

> 🚨 Antes de definir sua estratégia de nomenclatura, crie seu Publisher no seu ambiente Power Platform; ele terá um sufixo antes do logical name de todos os componentes criados dentro das soluções.

### Ambientes

> [projeto/departamento][ambiente][região][*instância*] <br>
> itProdUs001 (it = departamento / Prod = ambiente / Us = região / 001 = instância)

Para os administradores de T.I., pode fazer mais sentido adotar a nomenclatura já existente no Azure, o que também é validado pelas melhores práticas da Microsoft em [https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/resource-naming](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/resource-naming). Para aqueles que desenvolvem para terceiros, pode ser interessante adicionar um parâmetro que faça referência ao cliente.

> 🚨 Instância está entre asteriscos porque é um parâmetro opcional

> 🚨 Atente-se a região do seu ambiente, caso não saiba como funciona veja melhor em: [Escolher a região ao configurar um ambiente - Power Platform | Microsoft Learn](https://learn.microsoft.com/pt-br/power-platform/admin/regions-overview)

### Soluções
O exemplo abaixo, sem espaços, será automaticamente aplicado no nome lógico (logical name) da solução. Portanto, ao digitar, pode inserir espaços para que o nome de exibição (display name) fique mais agradável de visualizar, como no exemplo = `Power Track`. 
<br><br>
Sua solução estará dentro do ambiente que já possui uma região definida, então não é necessário adicionar informações como região e departamento no nome da solução, mas se preferir adicione exemplo = `[região][departamento][projeto]`.
<br>
> [projeto] <br>
> PowerTrack (PowerTrack = projeto)

> 🚨 Digite tudo sempre sem caracteres especiais

### Componentes da Solução
Aqui, podemos ser um pouco mais flexíveis, considerando que todo componente já possui um prefixo de publisher e precisa estar dentro de uma solução, o que significa que já estão relacionados. No entanto, é recomendável manter certos padrões, como a abreviação do componente, o projeto do qual ele se origina e seu nome. Outras informações, como região, departamento, etc., podem ser adicionadas, mas isso fica a seu critério.

> [nome][componente] <br>
> Power Track Canvas App (Power Track = nome / Canvas App = componente)

> 🚨 No exemplo, é utilizado um canvas app como componente. Os canvas apps exibem seu nome quando estão sendo abertos e não podem ser alterados durante os pipelines. Portanto, não considero uma boa prática adicionar parâmetros desnecessários, como `[ambiente]/[versão]`, por exemplo, o melhor seria mostrar a versão do app e/ou ambiente em algum lugar de fácil visualização dentro da aplicação. 

Seguindo a lógica do display name e logical name, o nome do aplicativo pode ter espaços e/ou ter seus parâmetros em ordens diferentes ou até de forma descritiva, uma vez que ele possui um display name visível para o usuário final. No entanto, para um Fluxo, não é tão interessante manter dessa forma, como veremos abaixo.

> [componente][projeto][nome] <br>
> ifPowerTrackCreateItem (if = componente / PowerTrack = projeto / CreateItem = nome)

> [componente][projeto][nome] <br>
> srPowerTrackCommonUser (sr = componente / PowerTrack = projeto / CommonUser = nome)

> [nome] <br>
> Users (Users = nome)

| Componente                              | Abreviação                |
|-----------------------------------------|---------------------------|
| Instant flow                            | if                        |
| Automated flow                          | af                        |
| Scheduled flow                          | sf                        |
| Business process flow                   | bpf                       |
| Desktop flow                            | df                        |
| Canvas app                              | capp                      |
| Model Driven app                        | mapp                      |
| Component library                       | cl                        |
| Connection reference                    | cr                        |
| Environment variable decimal number    | evdn                      |
| Environment variable JSON               | evjs                      |
| Environment variable text               | evs                       |
| Environment variable yes/no             | evb                       |
| Environment variable data source        | evd                       |
| Environment variable secret             | evscr                     |
| Security role                           | sr                        |

> 🚨 Note que a tabela não possui parâmetros, pois ela é uma entidade e deve ser usada entre as soluções. Sendo assim, não é necessário adicionar uma tabela de usuários por projeto, mas sim considerar o projeto como uma propriedade da entidade "usuários". No entanto, caso seja necessário, você pode seguir a mesma lógica da nomenclatura dos outros componentes para as tabelas também.

### Variáveis
#### Variáveis globais
> [escopo][tipo][nome] <br>
> vsUser (v = variável global / s = string / User = nome da variável)

#### Variáveis locais
> [escopo][tipo][nome] <br>
> csUser (c = variável local / s = string / User = nome da variável)

| Tipo   | Caractere | Exemplo      |
|--------|-----------|--------------|
| string | s         | vsText       |
| integer| i         | viNumber     |
| boolean| b         | vbFlag       |
| object | o         | voThings     |
| table  | t         | vtCollection |
| string | s         | csText       |
| integer| i         | ciNumber     |
| boolean| b         | cbFlag       |
| object | o         | coThings     |
| table  | t         | ctCollection |

### Coleções
Toda coleção é global e seu tipo é tabela, portanto, podemos seguir o seguinte padrão.
> [escopo][nome] <br>
> colRequests (col = coleção / Requests = nome da coleção)

### Controles de tela
Aqui, aplica-se a lógica da coleção, pois todos os componentes de tela são globais. Portanto, não é necessário seguir o padrão das variáveis.

> [componente][tela][nome][instância]  <br>
> laHomeTitle_1 (la = label / Home = tela / Title = nome / _1 = instância)

| Componente         | Abreviação |
|--------------------|------------|
| Label              | la         |
| Input              | in         |
| Button             | bu         |
| Radio              | ra         |
| Html               | ht         |
| Icon               | ic         |
| Image              | im         |
| Rectangle          | re         |
| DatePicker        | da         |
| DataTable         | dt         |
| Gallery           | ga         |
| Form              | fo         |
| Barcode Scanner   | ba         |
| Camera            | ca         |
| Pen               | pe         |
| Video             | vi         |
| Audio             | au         |
| Add Image         | ad         |

> 🚨 Uma dica para sempre se lembrar da abreviação do componente é começar a digitar o nome dele; a abreviação são os dois primeiros caracteres do nome do componente, por exemplo: label = la, button = bu. Por isso, é recomendável usar a Power Platform em inglês.

### Componentes customizados

> [componente][nome] <br>
> ccHeader (cc = componente / Header = nome)

A regra acima se aplica à criação do componente. Quando ele é importado para a aplicação, ele se torna um componente de tela, sendo necessário aplicar a mesma regra dos componentes comuns. Veja o exemplo abaixo.

> [componente][tela][nome][instância] <br>
> ccHomeHeader_1 (cc = componente / Home = tela / Header = nome / _1 = instância)

> 🚨 A instância é adicionada ao final dos componentes porque, frequentemente, vários componentes do mesmo tipo ou até mesmo com o mesmo nome podem se repetir na aplicação. Dessa forma, ao precisar reutilizar, basta copiar e colar, e automaticamente o item copiado será o próximo na sequência numérica da instância. Por exemplo, ao utilizar "ccHomeHeader_1" duas vezes na mesma tela, ao ser copiado e colado, seu nome será automaticamente alterado para "ccHomeHeader_2".

> 🚨 Créditos a David Wyatt, cujo artigo (https://dev.to/wyattdave/power-apps-naming-conventions-88e - Power Apps Naming Conventions) foi utilizado como base para a elaboração do documento e ao meu amigo [Daniel Damaceno](https://www.linkedin.com/in/daniel-damaceno/) que está auxiliando na revisão deste documento.
