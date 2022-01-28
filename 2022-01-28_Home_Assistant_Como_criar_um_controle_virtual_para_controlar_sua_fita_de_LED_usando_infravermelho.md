# Home Assistant: Como criar um controle virtual para controlar sua fita de LED usando infravermelho

Link de compra para os aparelhos usados no védeo:
- Infravermelho Avatto: https://bit.ly/3INl6eD
- Fita led com controle infravermelho:
  - Fita com entrada USB: https://bit.ly/3IJxAE7
  - Controlador 12V com controle: https://bit.ly/3Glfffj

#### Vídeo:
  [![Foo](https://raw.githubusercontent.com/kleber0a0m/links-youtube/main/imagens/m97xmi49.png)](https://youtu.be/yE3Z0WE3MTE)
  
## Requisitos:
##### 1. Integração Tuya ativada no Home Assistent:
https://www.home-assistant.io/integrations/tuya
##### 2. Button Card by @RomRider instalado:
Como instalar: https://github.com/custom-cards/button-card#installation

## Códigos:
Ícones: https://materialdesignicons.com/
### Botão unico:

 ![Botão unico](https://raw.githubusercontent.com/kleber0a0m/links-youtube/main/imagens/o756cs3o.png)
```
cards:
type: "custom:button-card"
color: rgb(255,0,0)
icon: mdi:led-on
tap_action:
  action: call-service
  service: scene.turn_on
  service_data:
    entity_id: scene.rgb_ligar
```

### Controle RGB:

 ![Controle RGB](https://raw.githubusercontent.com/kleber0a0m/links-youtube/main/imagens/q2qr2xug.png)
```
type: vertical-stack
cards:
  - type: horizontal-stack
    cards:
      - type: horizontal-stack
        cards:
          - type: custom:button-card
            color: rgb(0,130,0)
            icon: mdi:led-on
            tap_action:
              action: call-service
              service: scene.turn_on
              service_data:
                entity_id: scene.rgb_ligar
          - type: custom:button-card
            color: rgb(130,0,0)
            icon: mdi:led-variant-off
            tap_action:
              action: call-service
              service: scene.turn_on
              service_data:
                entity_id: scene.rgb_desligar
          - type: custom:button-card
            color: rgb(255,255,255)
            icon: mdi:checkbox-blank-circle
            tap_action:
              action: call-service
              service: scene.turn_on
              service_data:
                entity_id: scene.rgb_w
          - type: custom:button-card
            color: rgb(255,255,255)
            icon: mdi:transfer-up
            tap_action:
              action: call-service
              service: scene.turn_on
              service_data:
                entity_id: scene.rgb_up
          - type: custom:button-card
            color: rgb(255,255,255)
            icon: mdi:transfer-down
            tap_action:
              action: call-service
              service: scene.turn_on
              service_data:
                entity_id: scene.rgb_down
  - type: horizontal-stack
    cards:
      - type: custom:button-card
        color: rgb(255,0,0)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_r0
      - type: custom:button-card
        color: rgb(0,255,0)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_g0
      - type: custom:button-card
        color: rgb(0,0,255)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_b0
  - type: horizontal-stack
    cards:
      - type: custom:button-card
        color: rgba(220,73,41)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_r1
      - type: custom:button-card
        color: rgba(15,139,35)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_g1
      - type: custom:button-card
        color: rgba(20,99,174)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_b1
  - type: horizontal-stack
    cards:
      - type: custom:button-card
        color: rgb(225,95,45)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_r2
      - type: custom:button-card
        color: rgba(1,159,165,255)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_g2
      - type: custom:button-card
        color: rgba(81,48,93,255)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_b2
  - type: horizontal-stack
    cards:
      - type: custom:button-card
        color: rgba(229,135,48,255)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_r3
      - type: custom:button-card
        color: rgba(9,111,139,255)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_g3
      - type: custom:button-card
        color: rgba(125,70,123,255)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_b3
  - type: horizontal-stack
    cards:
      - type: custom:button-card
        color: rgba(220,196,9,255)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_r4
      - type: custom:button-card
        color: rgba(26,88,102,255)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_g4
      - type: custom:button-card
        color: rgba(187,71,136,255)
        icon: mdi:checkbox-blank-circle
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_b4
  - type: horizontal-stack
    cards:
      - type: custom:button-card
        color: rgba(255,255,255,255)
        icon: mdi:alpha-s-box
        name: FLASH
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_flash
      - type: custom:button-card
        color: rgba(255,255,255,255)
        icon: mdi:alpha-s-circle
        name: STROBE
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_strobe
      - type: custom:button-card
        color: rgba(255,255,255,255)
        icon: mdi:alpha-f-circle
        name: FADE
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_fade
      - type: custom:button-card
        color: rgba(255,255,255,255)
        icon: mdi:alpha-s-box
        name: SMOOTH
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.rgb_smooth
```

### Controle TV:

 ![Controle TV](https://github.com/kleber0a0m/links-youtube/blob/main/imagens/yb4rda9b.png)
```
type: vertical-stack
cards:
  - type: horizontal-stack
    cards:
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:power-standby
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.tv_power
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:video-input-hdmi
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.tv_menu
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:volume-off
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.tv_mudo
  - type: horizontal-stack
    cards:
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:volume-minus
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.tv_volume_down
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:dots-horizontal
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.tv_home
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:volume-plus
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.tv_volume_up
  - type: horizontal-stack
    cards:
      - cards: null
        type: custom:button-card
        icon: mdi:-
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
      - cards: null
        type: custom:button-card
        icon: mdi:-
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
      - cards: null
        type: custom:button-card
        icon: mdi:-
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
  - type: horizontal-stack
    cards:
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:v
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:arrow-up-thick
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.tv_up
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:v
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
  - type: horizontal-stack
    cards:
      - type: horizontal-stack
        cards:
          - type: custom:button-card
            color: rgb(255,255,255)
            icon: mdi:arrow-left-thick
            tap_action:
              action: call-service
              service: scene.turn_on
              service_data:
                entity_id: scene.tv_left
          - type: custom:button-card
            color: rgb(255,255,255)
            icon: mdi:circle-outline
            tap_action:
              action: call-service
              service: scene.turn_on
              service_data:
                entity_id: scene.tv_ok
          - type: custom:button-card
            color: rgb(255,255,255)
            icon: mdi:arrow-right-thick
            tap_action:
              action: call-service
              service: scene.turn_on
              service_data:
                entity_id: scene.tv_right
  - type: horizontal-stack
    cards:
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:-
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:arrow-down-thick
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.tv_down
      - type: custom:button-card
        color: rgb(255,255,255)
        icon: mdi:-
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
  - type: horizontal-stack
    cards:
      - cards: null
        type: custom:button-card
        icon: mdi:-
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
      - cards: null
        type: custom:button-card
        icon: mdi:-
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
      - cards: null
        type: custom:button-card
        icon: mdi:-
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
  - type: horizontal-stack
    cards:
      - cards: null
        type: custom:button-card
        icon: mdi:keyboard-return
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
      - cards: null
        type: custom:button-card
        icon: mdi:-
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: scene.tv_down
      - cards: null
        type: custom:button-card
        icon: mdi:-
        tap_action:
          action: call-service
          service: scene.turn_on
          service_data:
            entity_id: null
```
##### Fim =)
