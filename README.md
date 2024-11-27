# Sistema de Agendamentos

## Estrutura do Projeto

### Pastas Principais
- **/config**: Configurações do projeto, como conexão com o banco de dados e parâmetros globais.
- **/public**: Arquivos acessíveis pelo navegador. Contém o ponto de entrada (`index.php`) e assets públicos.
- **/src**: Lógica principal do sistema, separada em:
  - **controllers**: Classes que controlam as ações e processam as requisições.
  - **models**: Classes que interagem com o banco de dados.
  - **views**: Arquivos HTML/PHP que renderizam a interface visual.
- **/logs**: Logs de eventos e erros do sistema.
- **/migrations**: Scripts SQL para criar e gerenciar tabelas no banco de dados.
- **/tests**: Arquivos para testar as funcionalidades do sistema.

---

### Fluxo do Sistema

1. O **usuário** acessa o sistema via navegador.
2. O **index.php** captura a rota e chama o controlador correspondente.
3. O **controlador** executa a lógica e carrega dados usando os **models**.
4. Os dados são enviados para uma **view**, que é renderizada e exibida ao usuário.

---

### Regras e Padrões
- **Views** nunca devem conter lógica pesada.
- Todas as consultas ao banco devem ser centralizadas nos **models**.
- Logs de eventos importantes devem ser registrados no arquivo `/logs/app.log`.
- Use rotas claras no sistema (ex.: `?url=agendamentos`).

---

### Configuração
1. Configure o banco de dados em `/config/db.php`.
2. Ajuste as configurações globais em `/config/ajustes.php`.

---

### Dependências Futuras
Caso seja necessário, considere o uso de:
- **Composer**: Para gerenciar pacotes externos.
- **Biblioteca de testes**: Para melhorar a cobertura de testes automatizados.