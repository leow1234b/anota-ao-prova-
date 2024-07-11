Guia de estudos para a prova de C#
----------------------------------


   ----------------------------------
   link do git do trabalho

   https://gitlab.com/AndreMarcassi/biblioteca-react
   ----------------------------------
   link do git do professor 

   https://github.com/dideconto/2024-topicos-especiais-em-sistemas-sexta
   ----------------------------------


GIT
----------------------------------

1. Criar o repositori no git com o ReadMe
	( se criar pelo GitHub colocar o .gitignore "VisualStudio").

2. baixar o repositoria na maquina
	git clone nomeDoRepositorio


para adicionar novas pastar e arquivos no git

1. git add.

2. git commit -m "alguma coisa"

3. git push



API
----------------------------------

1. baixar a API que for disponibilizada dentro da pasta que foi clonada

2. primeiramente arruma a configuração padrão da API


   Program.cs
   ----------------------------------

   1.  Configurar a política de CORS

	builder.Services.AddCors(options =>
    	   options.AddPolicy("Acesso Total",
              configs => configs
                 .AllowAnyOrigin()
                 .AllowAnyHeader()
                 .AllowAnyMethod())
	);



   2. Colocar o código acima antes do "var app = builder.Build();"

   3. app.UseCors("Acesso Total");

   4. Colocar o código acima antes do "app.Run();"

   ----------------------------------



   AppDataContext.cs
   ----------------------------------

   1. em optionsBuilder.UseSqlite("Data Source=App.db");
	alterar o "App" para o seu nome caso seja necessária.


   2. Criar o "banco"
	dotnet ef migrations add NomeMigracao

	alterar "NomeMigracao" para outro nome

   3. "aplicar o banco"
	dotnet ef database update


   4. Recomendo ja enviar as informações para o git

	1. git add.

	2. git commit -m "alguma coisa"

	3. git push

----------------------------------



React
----------------------------------

1. Criar o Front dentro da pasta que foi baixado do git

	npx create-react-app my-app --template typescript

	    alterar o "my-app" para outro nome


2. apos cria o arquivo deletar a .git que vem dentro do arquivo


3. fazer a limpeza do arquivo

	Delete os seguintes arquivos do diretório `src`:
    	
	   `App.css`
    	   `App.test.tsx`
    	   `logo.svg`
    	   `reportWebVitals.ts`
    	   `setupTests.ts`

      
4. Apos a limpeza recomendo ja enviar as informações para o git

	1. git add.

	2. git commit -m "alguma coisa"

	3. git push

----------------------------------

----------------------------------
   código para rodara a API

   dotnet run
----------------------------------
   código para rodara o Front
  ss
   npm start
----------------------------------
