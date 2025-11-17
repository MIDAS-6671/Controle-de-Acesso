# Controle de Acesso ao Estoque - Projeto Wokwi

Projeto acadêmico desenvolvido para simular um sistema de controle de acesso usando Arduino, teclado matricial e display LCD, com o objetivo de aumentar a segurança no estoque da empresa Martinstec.

##  Componentes utilizados
- Arduino Uno  
- Teclado matricial 4x4  
- Display LCD 16x2 (I2C)  
- Servo motor (tranca da porta)  
- Buzzer  
- LED  

## Funcionamento 

## Inicialização

Ao ligar o Arduino, o LCD exibirá “Iniciando…” por 1,5 segundos.

Se ainda não houver senha definida, o LCD mostrará “Defina a senha:”.

Caso já exista uma senha, o LCD mostrará “Digite a senha:”.

## Definindo a Senha Inicial

Digite pelo teclado pelo menos 4 dígitos.

Pressione # para confirmar.

O LCD exibirá “Senha salva!” e mudará para o modo de autenticação.

As entradas são mascaradas com * no LCD.

## Autenticação (Acesso ao Estoque)

Digite sua senha definida.

Pressione # para confirmar.

Se correta: LCD mostra “ACESSO LIBERADO” e o relé é acionado por 3 segundos.

Se incorreta: LCD mostra “Senha incorreta” e solicita a senha novamente.

Dica: Para alterar a senha, pressione * antes de digitar a senha atual.

## Alterando a Senha

Pressione * no modo autenticação.

O LCD exibirá “Senha atual:”.

Digite a senha atual e pressione #.

Se correta: LCD pede “Nova senha:”.

Se incorreta: LCD mostra “Senha incorreta” e retorna à solicitação da senha atual.

Digite a nova senha (mínimo 4 dígitos) e pressione #.

O LCD exibirá “Senha salva!” e voltará ao modo de autenticação.

## Funcionamento do Relé

O relé é acionado (HIGH) quando a senha correta é digitada.

Após 3 segundos, o relé desliga (LOW), simulando o fechamento da porta.

## Log de Eventos

Todo evento é registrado via Serial Monitor:

Acesso liberado

Acesso negado

Senha inicial definida

Senha alterada

Abra o Serial Monitor (115200 bps) para acompanhar os logs.

## Boas Práticas

Sempre teste a senha antes de instalar o sistema em produção.

Use senhas com pelo menos 4 dígitos.

Não pressione várias teclas ao mesmo tempo, isso pode confundir o teclado matricial.

Garanta que o relé e o dispositivo que ele controla estejam isolados eletricamente para evitar danos.
##  Link do simulador Wokwi
 [Acesse o projeto no Wokwi](https://wokwi.com/projects/443281111710977025)

##  Integrantes
Adrielle Vieira  
Douglas Henrique  
Felipe da Silva  
Hugo Leandro  
Matheus Alves  

##  Licença
Este projeto está licenciado sob a licença MIT — veja o arquivo LICENSE para mais detalhes.
