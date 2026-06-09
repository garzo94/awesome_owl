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

### Commit 1.4 - t-esc y t-out
- Se agregaron dos variables en el playgorund para desplegar html.
- Dichas variables son utilizadas en el componente "Card"
- t-esc: con una vaialbe se despliega el contgenido html utlilzando t-esc y podemos ver que usando este atributo despleiga el html como string.
- t-out: identiifca el conteniod html y lo despliega como tal. Se usa markup para proteger el codgio de inserciones maliciosas.

### Commit 1.5 - Validactión de Props (componentes hijos)
- Le indicamos explicitamente que variables recibirá el componente y el tipo de de variable (string, float, integer, fuction, etc.)

### Commit 1.6 - Pasar informacion de hijos al Padre
- Componente Hijo recibira una funcion del padre como props que se ejecutará desde otra funcion pero del hijo.
- Componente Padre (Playground) agregamos la funcion y la variable que se actualizará desde el hijo con la funcion que le pasaremos desde el padre
- Le pasamos la funcion Padre al Hijo como props para actualizar la variable en el Padre desde el Hijo.

### Commit 1.7 - Todo List
- Crea el componente todoItem que despliega la información de un todo indiviudal.
- Crea el componente todoList que llama al componente todoItem para hacer un for por cada todo harcodeado y desplegarlo en el todoItem y luego en el playgound.

### Commit 1.8 - Atributos dinamicos
- Con t-att-class podemos agregar expresiones dinamicas para aplicar algun estilo especifico.

### Commit 1.9 - Agregar todo mediante un Input
- Agrega metodo addTodo que será llamado por un evento de teclado (enter)
- Agrega un input en el componente todoList que activará el evento y lo agregará a la lista de todo´s.

### Commit 1.10 - useRef para enfocar input
- t-ref en la vista xml
- desde utils creamos la funcion que recibe al elemento como paramentro para enfocarlo la momento que se monta el objeto.

### Commit 1.11 - Toggle todo cuando esta completado
- Logica en la clase en el xml para marcar el todo como completado (todoItem).
- Al marcar el onchange del checkbox le pasamos el todo al padre mediante la funcion como props para que le cambie el estado a completado!

### Commit 1.12 - Remove TODO
- Otro callback desde todooItem que será llamado cuando le den click en la X
- Funcion como prop que será pasado a todoItem desde todoList que será llamado desde el hijo pasandole el otodo para eliminarlo

### Comit 1.13 - Slots
- En el componente del card se define un t-slot y se setea en props para que reciba este slot como props (submcomponente envuelto por CARD)

### Commit 1.14 - Toggle info card