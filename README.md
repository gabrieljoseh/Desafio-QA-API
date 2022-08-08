# Desafio-QA-API

Este projeto tem como finalidade testar os seguintes cenários de teste **Criar um novo usuário, Ler usuário já cadastrado,Listar todos os usuários cadastrados, Listar usuário por ID e Deletar o mesmo também através do ID**, utilizando a API pública https://serverest.dev/.

### Download da pasta com os arquivos para teste

É possível fazer o download da pasta .zip através do link https://github.com/gabrieljoseh/Desafio-QA-API/archive/refs/heads/main.zip ou também a pasta pode ser clonada através do comando abaixo, basta digitar esse comando no terminal da sua máquina:
```
git clone https://github.com/gabrieljoseh/Desafio-QA-API.git
```

# Instalação das ferramentas necessárias para o teste

### Postman

- Baixar o instalador do Postman para de acordo com o sistema operacional que está sendo usado, o Postman pode ser baixado através do link https://www.postman.com/downloads/;
- Executar a instalação do Postman;
- Após a instalação do Postman abra o programa e crie uma conta para começar a usar a ferramenta.

### Importando a Collection e configurando o Environment

- Após abrir o Postman clique em **Import** depois em **Upload Files**, conforme imagem abaixo.

![image](https://user-images.githubusercontent.com/110433514/183310196-5aadd55c-e768-4b05-9f34-ed6f1a3eec40.png)

- Selecione a Collection e o Environment que está na pasta que foi baixada/clonada inicialmente (selecione os 2 arquivos juntos como mostrado na imagem abaixo).

![image](https://user-images.githubusercontent.com/110433514/183310313-cd2d0cdc-e773-47bc-930d-dfa78ed949f0.png)

- Ao selecionar os arquivos clique em **Import** para importar os arquivos no Postman.

![image](https://user-images.githubusercontent.com/110433514/183310407-c88037b3-642d-4d79-8060-811ce86a9636.png)

### Configurando o Environment

- Como não foi configurado nenhum ambiente de teste ainda será necessário mudar a opção de **No Environment** para **Desafio QA API**, conforme mostrado na imagem abaixo.

![image](https://user-images.githubusercontent.com/110433514/183310547-ec69915e-891b-4f0e-af44-e19edd522ff6.png)

### Realizando teste através da Request

- Para realizar o teste testando Request por Request, selecione uma Request e clique no botão **Send**, porém para cada Request é necessário verificar o que será testado, por exemplo para **Criar um usuário com email diferente**, verifique em **Body** se os dados estão preenchidos e se o email ainda não foi usado, caso todos os dados estejam corretos após executar o teste clicando em **Send** teremos o seguinte:

![image](https://user-images.githubusercontent.com/110433514/183310897-951de492-94bc-497d-95a5-ec03bab9d983.png)

- E o código que o Postman irá entregar será o seguinte(Os códigos podem ser verificados na aba Test Results):

![image](https://user-images.githubusercontent.com/110433514/183310939-441ef9f0-311c-4e4c-aa66-6f899e27ac6c.png)

- Para testar as demais Request o procedimento é basicamente o mesmo porém deve-se atentar para as Request que utilizam o **GET** e o **DELETE**, pois essas Requests não usam o **Body** para entrada de dados, pois no **GET** é conferido a mensagem de resposta depois de uma requisição.

- Para os testes que precisam listar um usuário e excluir um usuário, é necessário buscar o **ID** do usuário desejado, (esse **ID** pode ser encontrado na Request **Listar todos os usuários cadastrados**) e colar o **ID** junto com a URL, segue exemplo abaixo.

- Listando os usuários para pegar o **ID** do usuário criado.

![image](https://user-images.githubusercontent.com/110433514/183312290-036cf69d-b876-4249-8d7e-269417c6159a.png)

- Colando o **ID** na URL e listando o usuário criado através do **ID**.

![image](https://user-images.githubusercontent.com/110433514/183312396-0e3eb8b0-94cb-4d0c-bb96-2cd21462e80b.png)

- Excluindo o usuário criado através do **ID**.

![image](https://user-images.githubusercontent.com/110433514/183312476-0d30b78e-4072-4064-b8b8-db7728b688d7.png)

### Realizar testes de forma automatizada com o Postman

- Na aba Collections em frente ao nome da pasta **Teste API Desafio QA** clique nos (3 pontos) **...** e depois clique em **Run Collection**

![image](https://user-images.githubusercontent.com/110433514/183312700-883e1873-df77-4c0d-80e6-a4fa28f482cf.png)

- Podemos alterar o número de iterações e o tempo de atraso, porém para esse caso de teste será mantido da forma que está.

![image](https://user-images.githubusercontent.com/110433514/183312846-5005ef50-1f8a-423b-a177-e2ed24c65253.png)

- Do lado esquerdo da tela irá aparecer as Request que serão testadas, é necessário checar se todas as que desejam ser testadas estão marcadas, se caso todas estiverem marcadas clique em **Run Testes Desafio QA API**

![image](https://user-images.githubusercontent.com/110433514/183312979-b0675bb6-029a-41c1-895c-96f3cf760d27.png)

- Depois de clicar em **Run Testes Desafio QA API** veremos os resultados dos testes que foram feitos onde o Postman irá retornar com **Pass** os testes que estão Ok e com **Fail** os testes que não passaram, como foi ajustado tudo de forma correta para que não houvesse falha vemos que todos os testes passaram.

![image](https://user-images.githubusercontent.com/110433514/183313167-8ac06376-ce6b-45d6-8c9f-4f106fa4cff3.png)
![image](https://user-images.githubusercontent.com/110433514/183313193-9f3c77d7-3874-44cd-a9d1-eca839de1d73.png)

#### Dessa forma temos a validação dos testes de forma automatizada utilizando o Postman.









