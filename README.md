# Odoo tutorials

En este repositorio, estudiamos el capitulo 1 de los tutoriales del web framework "OWL" que encontramos en la documentacion oficial de odoo v18:
[official Odoo tutorials](https://www.odoo.com/documentation/18.0/es/developer/tutorials/discover_js_framework/01_owl_components.html).

## Notas

### Primer Commit - Componente
- controllers.py: registramos la ruta /awesome_owl para acceder a nuestro componente playground.
- componente: por cada js hay un xml del componente
- main.js: monta el componente cuando el DOM esta listo.

### Commit 1.1 (varialbe y metodos)
- En la logica del componente agregamos una varialbe en el setup y un metodo increment.
- En la vista llamamos a la variable con "t-esc" y al metodo con un evento "t-on-click"

### Commit 1.2 - Componente reusable
- Guardamos la misma logica anterior pero en un componente por aparte llamado counter para luego importarlo en el playground

### Commit 1.3 - Compartiendo informacion mediante Props
- Creamos un segundo componente llamado Card el cual recibo props como title y content en el xml mediante t-esc="props".
- Luego importamos el compoenente en el playground en el atributo static components para utilizarlo en el xml del playground.



