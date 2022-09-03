# <PersonalCheff>
<!---Esses são exemplos. Veja https://shields.io para outras pessoas ou para personalizar este conjunto de escudos. Você pode querer incluir dependências, status do projeto e informações de licença aqui--->
![Python](https://img.shields.io/badge/Python-14354C?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
<img src="exemplo.webp" alt="exemplo imagem">
> Uma aplicação web de receitas chamada PersonalCheff desenvolvida durante o curso de Python no Senac Americana. A aplicação listará receitas e clicando em cada nome de receita você pode ver a receita completa.
### Lista de tarefas
Segue a lista de tarefas a serem desenvolvidas no projeto:
- [X] Pré-requisitos
    - [X] Instalar o Python
    - [X] Instalar Visual Studio Code
- [X] Criar e ativar o ambiente virtual

```
python -m venv .\venv\
venv\Scripts\activate
```

- [X] Instalar o Django

```
python -m pip install django==3.2
```

- [X] Criar o projeto PersonalCheff

```
django-admin.py help ou django-admin help
django-admin.py startproject PersonalCheffProj
```

- [X] Subir o servidor e testar o projeto

```
Entrar na pasta do projeto (Código abaixo)
cd PersonalCheffProj
python manage.py runserver
```

- [X] Alterar o idioma do projeto para `pt-br`
    -Abrir o arquivo `settings.py` na pasta PersonalCheffProj e mudar a linguagem para `pt-br` na linha 106

- [X] Alterar o timezone do projeto para `America/Sao_Paulo`
    -Abrir o arquivo `settings.py` na pasta PersonalCheffProj e mudar o timezone para `America/Sao_Paulo` na linha 108

- [X] Criar o app receitas
```
 Caso preciso executar o projeto no servidor (cd PersonalCheffProj)
python manage.py startapp receitas
```

- [X] Registrar o app receitas
    -Abrir o arquivo `settings.py` na pasta PersonalCheffProj adicionar `'receitas',` em INSTALLED_APPS[ na linha 40

- [ ] Configurar a rota inicial(index)
    -Na pasta `receitas` criar um arquivo `urls.py`
```
Adicionar este código:

from django.urls import Path
from . import views

urlpatterns = [
    path('', views.index, name='index')
]

Entrar na pasta `views.py` e adicionar este código:

from django.shortcuts import render
from django.http import HttpResponse

def index(request):
    return HttpResponse("Seja bem vindo")

Após isso ir na pasta `PersonalCheffProj` no arquivo `urls.py` e adicionar include nos códigos:

from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('receitas.urls'))
]
```

- [ ] Criar a view para a rota inicial
- [ ] Registrar a rota inicial
- [ ] Criar o arquivo index

## 📝 Licença
Esse projeto está sob licença. Veja o arquivo [LICENÇA](LICENSE.md) para mais detalhes.
[⬆ Voltar ao topo](#nome-do-projeto)<br>
