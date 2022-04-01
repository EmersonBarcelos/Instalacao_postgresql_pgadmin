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

