---
weight: 5
slug: contacto
title: Contacto
sum: Primer contacto con Juma Legal por correo electrónico.
seo:
  title: Contactar con Manuel Acosta | Despacho Juma Legal
  desc: Escribe a info@jumalegal.com para explicar tu asunto. Primer contacto por correo y citas acordadas; no envíes
    documentación sensible de inicio.
icon: send
tpl:
  sections:
  - file: common-_hero
  - file: contacto-primero

hero:
  sub: Contacto / Primer Paso
  title: Cuéntanos lo esencial. **Nosotros te orientamos.**
  md: |
    El primer contacto permite valorar el asunto.
    Si es necesario estudiar tu caso en una consulta profesional,
    te informaremos de sus condiciones antes de concertarla.
  links:
  - label: Cómo contactar
    url: '#primer-mensaje'
  bi: /u/fotos/manuel-acosta-llamada-primer-plano.webp
  alt: Manuel Acosta, director de Juma Legal atendiendo una llamada
  color: main-light

datos:
  sub: Un primer mensaje es suficiente
  title: Qué conviene **contarnos.**
  md: |
    - Tu nombre y un teléfono de contacto.
    - El área del asunto: militar o administrativo.
    - Un resumen breve de lo ocurrido.
    - Si has recibido una notificación y existe un plazo próximo.

    *No envíes por este primer contacto documentación confidencial, datos de salud ni información de terceros. \
    El envío no suspende plazos ni implica aceptación del encargo.*

    - ::txt:Ámbito:: Atención en toda España
    - ::txt:Presencial:: Murcia · Solo con cita previa
    - ::txt:Lunes - Jueves:: 10:00 - 14:00 y 16:00 - 18:00
    - ::txt:Viernes:: 08:00 - 14:00

    [[info@jumalegal.com ::north_east::]](info@jumalegal.com "{swap ga4:contact}")

formulario:
  sub: Formulario
  title: Una vía de contacto a tu medida.
  inputs:
  - type: text
    name: Nombre y apellidos
    req: true
    # icon: person
  - type: phone
    name: Teléfono
    req: true
    # icon: phone
  - type: mail
    name: Email
    label: Correo electrónico
    req: true
    # icon: mail
  - type: select
    name: Área
    req: true
    x: true
    # icon: balance
    items:
    - label: Militar
    - label: Administrativo
    - label: Otro
  - type: area
    name: Mensaje
    label: Asunto y mensaje breve
    req: true
    # icon: message
---
