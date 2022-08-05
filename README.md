# PXE-Cliente

## Pré-requisitos

### Instalar plugin de controle de discos do vagrant
```bash
vagrant plugin install vagrant-disksize
```

### Configuracoes minimas do cliente:
- 2048 vRAM
- 1 vCPU

## Etapas

### Subir o cliente:
`vagrant up`

Ao subir dará erro na tela pois ainda não encontrou o server

Desligar a maquina cliente com `Power OFF`

### Executar comando para modificar ordem de boot

```bash
vboxmanage modifyvm <NOME_VM_CLIENT> --boot1 net --boot2 disk --boot3 none --boot4 none 
```

### Mudar rede para mesma rede do SERVER
Trocar a rede do cliente para a mesma rede do SERVER_PXE em Settings > Network > Host-only adapter <vboxnetXX>

Ao terminar subir o cliente com o botão `Power ON` e ver tela azul do PXE :)

## Screenshots

Expected results
![Expected](https://github.com/hansnewton/pxe-client-lab/raw/master/resultado.png)