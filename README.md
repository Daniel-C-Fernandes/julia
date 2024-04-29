# Linguagem JULIA

Tutorial de instalação:

1. Instalação do Anaconda pelo windows powershell
2. Instalação do Julia pelo windows powershell
3. Instalação do Anaconda pelo modo gráfico
4. Instalação do Julia pelo modo gráfico
5. Julia "Hello World"
6. Integração da linguagem Julia no jupyter-notebook
7. Exemplo de otimização

# Jupyter Notebook + Julia

<hr>

## Instalação pelo prompt de comando:

Abra o Windows PowerShell:

![1](https://github.com/Daniel-C-Fernandes/julia/blob/img/1.powershell.png)

![1](https://github.com/Daniel-C-Fernandes/julia/blob/img/2.powershell.png)

## 1. Anaconda (Jupyter Notebook)

Inclua o comando de instalação winget no prompt do PowerShell (se necessário execute como administrador):

```
winget install --id=Anaconda.Anaconda3  -e
```



![Winget Anaconda](https://github.com/Daniel-C-Fernandes/julia/blob/img/3.wingetAnaconda.png)



No prompt de comando digite o seguinte para inicializar:

```

jupyter-notebook

```

ou

```
jupyter-lab
```

## 2. Julia

Inclua o comando de instalação winget no prompt do PowerShell (se necessário execute como administrador):

```
winget install julia -s msstore
```



![Winget julia](https://github.com/Daniel-C-Fernandes/julia/blob/img/4.julia.png)



No prompt de comando digite o seguinte para inicializar:

```
julia
```

### 3. Integrando Anaconda + Julia

<a href="#Config"> Seguir para o tutorial de inicialização e integração.</a>

<hr>

## Tutorial de Instalação - Aplicativos Gráficos

## 1. Anaconda (Jupyter Notebook)

Primeiramente, deveremos baixar o instalador de *Jupyter Notebook*.

Para isso, podemos pesquisar as palavras **anaconda download* ou acessar o link abaixo:

[Free Download | Anaconda](https://www.anaconda.com/download)

![f019c11f-a764-4fcd-a687-7e687cb5be8b](
https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/f019c11f-a764-4fcd-a687-7e687cb5be8b.png)

Faça o download do instalador para Windows.

Agora instale o software *Anaconda*.

![06e53882-f2f3-44aa-99a9-ad54187ef290](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/06e53882-f2f3-44aa-99a9-ad54187ef290.png)

![bbd726fa-b04b-46b8-854f-be01a27da7af](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/bbd726fa-b04b-46b8-854f-be01a27da7af.png)

Pronto, agora o *Jupyter Notebook* está instalado.

Após a instalação, procure por *Anaconda Navigator* e o execute.

Clique no botão *Launch* do ícone *Jupyter Notebook* e se abrirá no navegador de internet o ambiente do *Jupyter Notebook*:

![a12ee999-138f-4e34-a8bc-321d53292c01](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/a12ee999-138f-4e34-a8bc-321d53292c01.png)

Veja que, ao clicar em *novo*, não há a opção *julia*. Dessa forma, iremos instalar a linguagem julia e integrá-la ao notebook.

![6f2b8a12-a0c0-46db-948d-f8ff60cce45c](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/6f2b8a12-a0c0-46db-948d-f8ff60cce45c.png)

Feche o Jupyter Notebook e o Anaconda.

## 2. Julia

Agora, deveremos baixar o instalador da linguagem *Julia*.

Para isso, podemos pesquisar as palavras *julia lang* ou acessar o link abaixo:

[Download Julia (julialang.org)](https://julialang.org/downloads/)

![8e151a4af1ba47a5a9ed80e150382ba7](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/8e151a4a-f1ba-47a5-a9ed-80e150382ba7.png?msec=1692916450047)

Faça o download do instalador para Windows e execute-o.

![10b13a86-0858-457f-871a-b66a68aeb158](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/10b13a86-0858-457f-871a-b66a68aeb158.png)

A linguagem *julia* foi instalada.

<div id="config"></div>

Acesse o prompt pelo link.

![1b16b625-2e42-40b2-a76b-8bfbe58eeee2](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/1b16b625-2e42-40b2-a76b-8bfbe58eeee2.png)

Irá abrir o seguinte prompt:

![c0572250-66af-4f46-8f45-9fc3de832030](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/c0572250-66af-4f46-8f45-9fc3de832030.png)

Vamos testar nossa primeira linha de código em *julia*:

```
println("Olá Mundo!")
```

![823072ea-f1a0-4d72-9d06-883612ff6a0b](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/823072ea-f1a0-4d72-9d06-883612ff6a0b.png)

Pronto, temos o *Jupyter Notebook* e a linguagem *julia* instalados.


## 4. Configurando tudo - Dentro do ambiente julia

Agora integraremos tudo.

Acesse o console julia e vamos utilizar o comando *Pkg*:

```
using Pkg
Pkg.update()
```

Inicialmente vamos verificar a versão instalada:

```
versioninfo()
```

Apenas para termos certeza que estamos com a última versão instalada em nosso computador, vamos atualizá-la. Para isso, utilize o comando a seguir:

```
Pkg.update()
```

Verifique a atualização:

```
versioninfo()
```

Alternativamente, podemos utilizar o pacote UpdateJulia:

```
Pkg.add("UpdateJulia")
using UpdateJulia
update_julia()
```

### Pacotes de Otimização

Vamos agora, instalar os Pacotes de Otimização:

```
Pkg.add("JuMP")
```

```
Pkg.add("HiGHS")
```

## 5. Testando

Vamos agora testar os comandos a seguir para verificar se tudo está funcionando adequadamente. 

Incluiremos os comandos para verificar se a integração entre *Julia* e o *Gurobi* está funcionando adequadamente:

```
using JuMP, HiGHS
```

```
model = direct_model(HiGHS.Optimizer())
```

Deveremos obter as seguintes mensagens:

![d530b07c-6b7a-4ec5-8649-2422c8e71982](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/d530b07c-6b7a-4ec5-8649-2422c8e71982.png)

### Integrando tudo ao *Jupyter Notebook*

Vamos integrar a linguagem Julia e o Gurobi para usar o Jupyter Notebook

```
using Pkg
Pkg.add("IJulia")
Pkg.add("Homebrew")
Pkg.build("Homebrew")
Pkg.build("IJulia")
```

## Teste de uso para otimização

Vamos agora acessar o *Jupyter Notebook* e otimizar nosso primeiro modelo. Verifique que agora há a opção *julia* para criação de um novo notebook:

![0d13d18a-11da-476d-b4e8-bea9d37b8b51](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/0d13d18a-11da-476d-b4e8-bea9d37b8b51.png)

Crie um novo notebook, onde modelaremos o nosso primeiro modelo de otimização para solução usando o Gurobi:



max $x_1+2x_2$

$5x_1+6x_2\leq 30$

$3x_1+2x_2\leq 12$

$10x_1+3x_2\leq 30$



![cbe1ff25-d5e6-448c-9045-c23c09ec66c7](https://raw.githubusercontent.com/Daniel-C-Fernandes/Tutorial-Jupyter-Notebook-Julia-Gurobi/img/cbe1ff25-d5e6-448c-9045-c23c09ec66c7.png)



### Código

```
## Importar pacotes necessários
using JuMP, HiGHS

## Estabelecer o modelo para otimização
model = Model(HiGHS.Optimizer)

## Configurar as variáveis
@variable(model, x_1 >= 0)
@variable(model, x_2 >= 0)

## Configurar a função objetivo
@objective(model, Max, 2*x_1+x_2)

## Configurar as restrições
@constraint(model, c1, 5*x_1+6*x_2 <= 30)
@constraint(model, c2, 3*x_1+2*x_2 <= 12)
@constraint(model, c3, 10*x_1+3*x_2 <= 30)

# Otimizar o modelo
optimize!(model)

#---------------------------
# Modelo:
print(model)

# Relatório
solution_summary(model; verbose = true)

# Valor dos variáveis ótimas
println(value(x_1))
println(value(x_2))

# Valor ótimo
objective_value(model)
```

```

```


