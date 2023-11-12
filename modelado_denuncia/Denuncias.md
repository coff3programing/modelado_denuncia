# Modelado Denuncias

## Listados de Entidades

### denunciante **(ED)**

- denunciante_id **(PK)**
- denunciado_id **(FK)**
- nombres
- apellidos
- documentos_id **(FK)**
- genero_id **(FK)**
- edad
- correo **(UK)**
- parentezco
- estado_civil
- direccion_id **(FK)**
- tipo_telefono **(FK)**
- numero_contacto
- trabajo_id **(FK)**
- evidencia **(UK)**
- descripcion

### denunciado **(ED)**

- denunciando_id **(PK)**
- nombres
- apellidos
- documentos_id **(FK)**
- genero_id **(FK)**
- edad
- correo **(UK)**
- parentezco
- estado civil
- direccion_id **(FK)**
- tipo_telefono **(FK)**
- numero_contacto
- trabajo_id **(FK)**
- descripcion

### genero

- genero_id **(PK)**
- nombre_genero **(UK)**

### tipo_celular **(EC)**

- celular_id **(PK)**
- celular_tipo **(UK)**

### documentos_identidad **(EC)**

- documentos_id **(PK)**
- documento_tipo **(UK)**

### direccion_casa **(ED)**

- direccion_id **(PK)**
- numero_casa **(UK)**
- calle_transversal
- parroquia
- sector
- provincia

### trabajo **(ED)**

- trabajo_id **(PK)**
- trabajo_tipo
- nombre_institucion
- direccion_laboral_id **(FK)**

### direccion_laboral **(ED)**

- direccion_laboral_id **(PK)**
- calle_principal
- calle_transversal
- referencia
- parroquia
- sector

- barrio

## _*Relaciones*_

1. Un **denunciante** denuncia a un **denunciado**
1. Un **denunciante** tiene un **genero**
1. Un **denunciado** tiene un **genero**
1. Un **tipo_celular** pertenece a un **denunciante**
1. Un **tipo_celular** pertenece a un **denunciado**
1. Un **documentos_identidad** pertenece a un **denunciante**
1. Un **documentos_identidad** pertenece a un **denunciado**
1. Un **direccion_casa** tiene un **denunciante**
1. Un **direccion_casa** tiene un **denunciado**
1. Un **trabajo** pertenece a un **denunciante**
1. Un **trabajo** pertenece a un **denunciado**
1. Un **direccion_laboral** pertenece a un **trabajo**
