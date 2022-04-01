<h1>Etapa 1: Adicionar Repositório PostgreSQL</h1>
<span>
# Crie a configuração do repositório de arquivos:
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $ (lsb_release -cs) -pgdg main"> /etc/apt/sources.list.d/pgdg.list'

# Importe a chave de assinatura do repositório:
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
</span>
