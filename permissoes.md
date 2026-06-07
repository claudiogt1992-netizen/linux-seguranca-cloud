
## Ficheiros criados
- **publico.txt**: Ficheiro de acesso público para leitura
- **restrito.txt**: Ficheiro com acesso restrito ao proprietário e grupo
- **script.sh**: Script shell com permissão de execução para o proprietário

## Permissões aplicadas

| Ficheiro | Permissão | Justificação |
|---|---:|---|
| publico.txt | 644 | Leitura para todos, escrita apenas pelo proprietário - adequado para conteúdo público |
| restrito.txt | 640 | Leitura para proprietário e grupo, nenhum acesso para outros - protege informação sensível |
| script.sh | u+x | Apenas o proprietário pode executar - previne execução não autorizada |

## Relação com o princípio do menor privilégio

As permissões aplicadas seguem o princípio do menor privilégio porque:

1. **publico.txt (644)**: Em vez de 777 (permissões totais para todos), usa 644 que permite leitura pública mas mantém o controlo de escrita apenas para o proprietário. Isso evita que qualquer usuário modifique o ficheiro.

2. **restrito.txt (640)**: Em vez de 666 ou 777, restringe o acesso a apenas proprietário (leitura/escrita) e grupo (leitura), bloqueando completamente outros usuários. Isso protege informação sensível de acessos não autorizados.

3. **script.sh (u+x)**: Em vez de adicionar x para todos (755), only o proprietário pode executar. Isso previne que usuários maliciosos executem código potencialmente perigoso.

**Conclusão**: Permissões totais (777) seriam um risco de segurança porque qualquer usuário poderia ler, escrever ou executar ficheiros sem necessidade. O princípio do menor privilégio garante que cada usuário tenha apenas as permissões essenciais para sua função.