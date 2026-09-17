# Fernando Prestes Godinho

**Analista de TI · Desenvolvimento e Infraestrutura** — São Roque, SP

Construo os sistemas que a operação usa e mantenho eles de pé. Trabalho do
incidente até o deploy: suporte, rede, banco, backend e a tela do operador.

---

### Em produção agora

**Central de monitoramento de alarmes** — recebe os eventos das centrais dos
clientes, abre o atendimento na tela do operador e registra a ocorrência.
Rodando 24/7 para **135 clientes**, com **mais de 112 mil eventos** processados.
Substituiu o software de terceiros que a empresa licenciava.
`Python` `FastAPI` `PostgreSQL` `WebSocket`

**Arena AMP** — produto de gestão para arenas esportivas, instalado em cliente
real. App desktop compilado com Nuitka e distribuído por instalador próprio,
licença assinada em **Ed25519**, assinatura recorrente e atualização automática.
Um serviço de nuvem multi-tenant espelha os dados para a equipe usar pelo
celular, com sincronização offline-first nos dois sentidos.
`Flask` `SQLAlchemy` `Nuitka` `Render` `Supabase`

**ERP** — clientes, contratos, ordens de serviço, financeiro, estoque e seis
relatórios gerenciais. Segurança tratada como contrato do projeto: Argon2id,
segundo fator TOTP, exclusão lógica no financeiro, log de auditoria e checklist
revisado a cada módulo entregue.
`Python` `FastAPI` `PostgreSQL`

---

### Coisas que aprendi fazendo

**Quando não tem API, automatize a interface.** O AMT Remoto da Intelbras não
expõe nada, então o sistema pilota a janela dele — lê a tela por pixel e manda
clique e tecla. As posições são guardadas como *fração da janela*, não como
pixel, e por isso sobrevivem a mudança de escala e de monitor.

**Legado se isola, não se reescreve.** O mesmo sistema lê PostgreSQL, Firebird e
SQL Server ao mesmo tempo. O SQL Server entra por PowerShell porque o driver não
estava disponível e instalar em produção não valia o risco — com cache, porque
cada chamada custa meio segundo.

**Uma consulta lenta derruba a operação.** A supervisão levava 3,7 s e travava o
popup do próximo alarme. Foi para 79 ms.

---

### Ferramentas

`Python` · `FastAPI` · `Flask` · `SQL` · `JavaScript` · `PostgreSQL` ·
`SQLite` · `SQL Server` · `Firebird` · `WebSocket` · `Playwright` ·
`Nuitka` · `Render` · `Tailscale` · `TOTVS Protheus`

---

📫 [fehgodinho98@gmail.com](mailto:fehgodinho98@gmail.com) ·
[LinkedIn](https://linkedin.com/in/fernando-p-362785220)

> A maior parte dos repositórios aqui é privada — são sistemas em produção, com
> dado de cliente dentro.
