# django_bootstrap_template
基于 coreUI 的前端模板 整合到 django 应用中

## 开发语言与框架

- 编辑语言：Python3.6 + HTML +　JavaScript
- 前端框架：coreUI
- 后端框架：Django 2.1.3

## 安装环境配置 
拉取代码 

    git clone https://github.com/holen/django_bootstrap_template.git
    
安装模块

    pip install -r requirements.txt
    
配置文件设置    
可以直接把 devops/settings_template.py 重命名为 devops/setttings.py 就可以    
也可以自己新建设置，如下

    INSTALLED_APPS = [
        ...
        'dashboard.apps.AppConfig',
    ]
    
配置数据库信息

    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.mysql',
            'NAME': 'dbname',
            'USER': 'username',
            'PASSWORD': 'password',
            'HOST': 'host_ip',
            'PORT': 'port',
        }
    }
        
生成数据表与管理员账户

    python manage.py migrate
    python manage.py createsuperuser
    
    
启动部署平台

    python manage.py runserver 0.0.0.0:8000