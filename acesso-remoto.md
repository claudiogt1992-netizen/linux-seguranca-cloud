
## Comando de ligação
```bash
ssh seu_usuario@endereco_ip
```

Exemplo:
```bash
ssh ubuntu@192.168.1.100
```

## Resultado obtido
- SSH está instalado e ativo/no serviço está inativo (escolha conforme seu output)
- Endereço IP identificado: [SEU_IP]
- Para testar acesso remoto, seria necessário conectar de outra máquina usando o comando acima

## Limitações encontradas
- Ambiente é uma VM local, sem acesso remoto externo configurado
- Para testar SSH real, seria necessário:
  1. Ter outra máquina na mesma rede
  2. Configurar firewall para permitir porta 22
  3. Verificar configurações de rede do VMware (NAT/Bridged)
- O serviço SSH está disponível mas não foi testado de máquina remota por ser ambiente isolado de laboratório