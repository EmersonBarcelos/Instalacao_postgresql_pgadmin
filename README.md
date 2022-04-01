<h1>Etapa 1: Adicionar Repositório PostgreSQL</h1>

Crie a configuração do repositório de arquivos:
<pre>
 <span style="font-weight: 400">sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $ (lsb_release -cs) -pgdg main"> /etc/apt/sources.list.d/pgdg.list'</span>
</pre>
  
Importe a chave de assinatura do repositório:
<pre>
 <span style="font-weight: 400">wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -</span>
</pre>

<h1>Etapa 2: atualize e instale o PostgreSQL</h1>

Atualize a lista de pacotes e instale:
<pre>
<span style="font-weight: 400">sudo apt-get update
sudo apt-get -y install postgresql</span>
</pre>

<h1>Etapa 3: Acessando PostgreSQL</h1>

Os comandos abaixo podem ser utilizados para parar, iniciar, habilitar e verificar seu status.
<pre>
<span style="font-weight: 400">Shell sudo systemctl stop postgresql.service
sudo systemctl start postgresql.service
sudo systemctl enable postgresql.service
sudo systemctl status postgresql.service</span>
</pre>


Depois de instalado seu SGBD postgre, vamos acessa-lo:

<pre>
<span style="font-weight: 400">sudo su
su postgres
psql</span>
</pre>

Agora que está logado com o postgre vamos criar um primeiro usuário.

<pre>
<span style="font-weight: 400">CREATE USER nomedousuario SUPERUSER INHERIT CREATEDB CREATEROLE;</span>
</pre>

depois entre com o comando:

<pre>
<span style="font-weight: 400">ALTER USER nomedousuario PASSWORD 'senha';</span>
</pre>

<h1>Etapa 4: Instalação pgAdmin 4 (APT)</h1>

Instale a chave pública para o repositório:
<pre>
<span style="font-weight: 400">sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add</span>
</pre>

Crie o arquivo de configuração do repositório:
<pre>
<span style="font-weight: 400">sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main"> /etc/apt/sources.list.d/pgadmin4.list && apt update '</span>
</pre>

Instale para os modos desktop e web:
<pre>
<span style="font-weight: 400">sudo apt install pgadmin4</span>
</pre>

Caso não tenha sucesso entre na pagina oficial do <a href="https://www.postgresql.org/download/linux/ubuntu/">PostgreSQL</a> e <a href="https://www.pgadmin.org/download/pgadmin-4-apt/">pgadmin</a>.




