## Architeq-Lab Odoo_v11

#### Procedimiento de instalacion y levantamiento Odoo_v11, Postgresql_v10, Python3.


1. Instalacion de Repositorio Odoo_v11

  - git clone https://github.com/architeq/odoo.git
  - git clone (Version enterprices) git clone https://github.com/odoo/enterprise.git

-------------------------

2. Instalacion Postgresql_v10

  - apt-get install postgresql -y
  - sudo su - postgres -c "createuser -s $USER"

  - sudo su - postgres
  - CREATE USER odoo11 PASSWORD 'odoo11';
  - ALTER ROLE odoo11 WITH SUPERUSER;
  - CREATE DATABASE odoo11_db WITH OWNER odoo11;
  - GRANT ALL PRIVILEGES ON DATABASE odoo11_db TO odoo11;

-------------------------

3. Instalar ambiente virtual virtualenvwrapper 4.8.5.dev9

  - sudo apt install virtualenvwrapper
  - source /usr/share/virtualenvwrapper/virtualenvwrapper.sh
  - sudo apt install build-essential python3-dev libxslt-dev libzip-dev libldap2-dev libsasl2-dev
  - mkvirtualenv -p /usr/bin/python3 odoo-venv
  - which python3
  * workon odoo-venv
      *    **pip3 install -r requirements.txt**

  * desactivar ambiente virtual
      *    deactivate

-------------------------      

4. Instalar dependencias Nodejs y less  

  - wget -qO- https://deb.nodesource.com/setup | bash -
  - sudo apt-get install -y nodejs
  - sudo apt-get install node-less

-------------------------

5. Levantar Odoo_v11

  - python3 odoo-bin -w odoo11 -r odoo11

-------------------------
Apoyo Tecnico sitio oficial Documentacion Odoo <a href="https://www.odoo.com/documentation/master/setup/install.html">Instrucciones</a>
Tutoriales oficial Odoo  <a href="https://www.odoo.com/documentation/master/tutorials.html">Tutoriales para Desarrolladores</a>
