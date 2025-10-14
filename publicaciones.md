---
layout: single
title: "Publicaciones recientes"
permalink: /publicaciones/
classes: wide
author_profile: true
---

Este listado reúne las publicaciones científicas realizadas por miembros de la REC entre los años 2024 y 2025.
Los trabajos aquí presentados reflejan la diversidad de enfoques y colaboraciones dentro de la red, abordando temas relacionados con el paisaje sonoro, la bioacústica y la conservación de los ecosistemas a través del sonido.

<!-- Agrega estos estilos y scripts en tu layout si aún no los tienes -->
<link rel="stylesheet" href="https://cdn.datatables.net/1.13.6/css/jquery.dataTables.min.css">
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://cdn.datatables.net/1.13.6/js/jquery.dataTables.min.js"></script>

<table id="tabla-publicaciones" class="display" style="width:100%">
  <thead>
    <tr>
      <th>Año</th>
      <th>Autores</th>
      <th>Título</th>
      <th>Enlace</th>
    </tr>
  </thead>
  <tbody>
    {% assign publicaciones = site.data.publicaciones %}
    {% for pub in publicaciones %}
    <tr>
      <td>{{ pub["Año de Publicación"] }}</td>
      <td>{{ pub["Autores"] }}</td>
      <td>{{ pub["Título"] }}</td>
      <td><a href="{{ pub["Enlace"] }}" target="_blank">Ver</a></td>
    </tr>
    {% endfor %}
  </tbody>
</table>

<script>
$(document).ready(function() {
  $('#tabla-publicaciones').DataTable({
    order: [[0, 'desc']], // orden inicial por año descendente
    pageLength: 25,
    language: {
      url: 'https://cdn.datatables.net/plug-ins/1.13.6/i18n/es-ES.json'
    }
  });
});
</script>