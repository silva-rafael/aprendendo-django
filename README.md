# Aprendendo-django
Um repositório para aprendizado de Django. Com as principais configurações e comandos necessários para o aprendizado deste framework.

**1- Comando iniciais**
```bash
python -m venv venv
venv/scripts/activate
pip install django
django-admin startproject core .
python manage.py startapp blog
mkdir static
mkdir media
mkdir partials
```

**2- No arquivo settings.py**
```python
INSTALLED_APPS = [
    '...',
    'blog', # registro do app aqui
]

# REGISTRA OS PARTIALS
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [
            BASE_DIR / 'partials/'
        ],
        '...'
    },
]

# MUDAR AS CONFIGURAÇÕES DE TIMEZONE
LANGUAGE_CODE = 'pt-br'
TIME_ZONE = 'America/Sao_Paulo'

# CONFIGURAÇÕES DE DOS ARQUIVOS ESTÁTICOS
STATIC_URL = 'static/'
STATICFILES_DIRS = [
    BASE_DIR / 'static/'
]

MEDIA_URL = 'media/'
MEDIA_ROOT = BASE_DIR / 'media/'

```
