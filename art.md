---
title: Artistic Resume
layout: page
actions:
  - label: "Download as PDF"
    icon: pdf
    url: "./assets/ManuelRomo_Art_CV_Es.pdf"
permalink: /art/
images:
  - image_path: ../assets/images/Art_Resume/mago1.JPG
    title: Hombre de Hojalata
  - image_path: ../assets/images/Art_Resume/mago2.JPG
    title: Elenco de Buscando al Maravilloso Mago de Oz
  - image_path: ../assets/images/Art_Resume/klaus1.JPG
    title: Klaus Kickenklober
  - image_path: ../assets/images/Art_Resume/klaus2.JPG
    title: Klaus vs Johnny
  - image_path: ../assets/images/Art_Resume/klaus3.JPG
    title: Klaus batalla
---


# Manu Romo

## Resumen
Manu Romo, artista con una sólida formación musical. Ha cultivado su talento en diversas instituciones, incluyendo el Conservatorio de las Rosas, la Facultad de Bellas Artes (UMSNH) y la Casa de la Cultura de Morelia, donde perfeccionó su destreza en guitarra, canto y repertorio. Su incursión en el ámbito vocal lo llevó a participar en el Ensamble Vocal de l'École Polytechnique bajo la dirección de Patrice Holiner, así como a especializarse en la Musique Sacrée à Notre-Dame de Paris, explorando técnicas vocales avanzadas de la mano de Paul Triepels y Rosa Domínguez.

Manu ha destacado también en el ámbito de la composición y producción musical, recalcando su especialización en Film Scoring en Cemucver y su papel como ingeniero de grabación en el estudio de doblaje Koe Dubbing Masters. Su versatilidad se extiende a la actuación, donde ha estudiado con reconocidos profesionales como Rafa Maza y Alfonso Obregón. Ha participado en proyectos teatrales, como "Buscando al Maravilloso Mago de Oz" con la compañía Escenic y "Sing 2" con VAT Company. En doblaje tiene presencia en proyectos como "Curandero", "Familia Ajena", "Soy Fea", "La Venganza" y "La Lista". Actualmente, está bajo la tutela de José Arenas y forma parte de VAT Company.

**********************

## Redes Sociales
{% include icon-youtube.html username='zoobidoobidoo' label='YouTube' %}
{% include icon-instagram.html username='zoobidoobidoobs' label='Instagram' %}
{% include icon-facebook.html username='zoobidoobidoobs' label='Facebook' %}

***********************

## Galeria

<ul class="photo-gallery">
  {% for image in page.images %}
    <img src="{{ image.image_path }}" alt="{{ image.title}}"/>
  {% endfor %}
</ul>