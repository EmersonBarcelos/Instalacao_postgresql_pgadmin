<h1>Etapa 1: Adicionar Repositório PostgreSQL</h1>

<h2>Crie a configuração do repositório de arquivos:</h2>
<pre>
 <span style="font-weight: 400">sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $ (lsb_release -cs) -pgdg main"> /etc/apt/sources.list.d/pgdg.list'</span>
</pre>
  
<h2>Importe a chave de assinatura do repositório:</h2>
<pre>
 <span style="font-weight: 400">wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -</span>
</pre>

<pre>
 <span style="font-weight: 400"></span>
</pre>
