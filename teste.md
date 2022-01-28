# ddf Titulo vídeo

## Requisitos:
##### 1. Integração Tuya ativada no Home Assistent:
https://www.home-assistant.io/integrations/tuya
##### 2. Button Card by @RomRider instalado:
Como instalar: https://github.com/custom-cards/button-card#installation

# Códigos:
### Botão unico:

 ![Led Vermelho](https://raw.githubusercontent.com/kleber0a0m/links-youtube/main/o756cs3o.png)
```
cards:
type: "custom:button-card"
color: rgb(255,0,0)
icon: mdi:lightbulb
name: teste
tap_action:
  action: call-service
  service: scene.turn_on
  service_data:
    entity_id: scene.rgb_ligar
```
