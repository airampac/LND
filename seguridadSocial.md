# Seguridad Social XML

Para completar nuestro XML, debemos añadir varias listados que contengan de manera organizada y entendible la siguiente información.

    • DNI o NIE
    
    • Nombre
    
    • Apellidos
    
    • Situación laboral
    
    • Fecha de nacimiento
    
    • Listado de bajas
    
    • Listado de prestaciones.
    
Para ello vamos a definir nuestro XML creando atributos que ejercerán como padres o raíz, y otros campos como hijos para mantener así de forma ordenada la información relevante entre si. El resultado de nuestro código XML es el siguiente.

![xml](https://user-images.githubusercontent.com/61906112/136469069-039c7dc8-2082-4f32-9651-0ddade34b074.PNG)

Ahora debemos generar añadir nuestro DTD  de acorde a nuestro XML para el correcto funcionamiento del código, el resultado final seria este.

![dtd](https://user-images.githubusercontent.com/61906112/136469077-b7483898-d20a-43c7-a248-6ec9c960c479.PNG)

# Validamos XML  y DTD

Para validad nuestro codigo XML y el DTD disponemos de webs en las cuales realizamos la comprobación.

[Validar XML y DTD](http://xmlvalidator.new-studio.org)

[Validar XML](https://www.w3schools.com/xml/xml_validator.asp)!


![no error DTD](https://user-images.githubusercontent.com/61906112/136469275-3b1e58df-9b2f-4a08-9621-42521554335a.PNG)

![no error xml](https://user-images.githubusercontent.com/61906112/136469228-d930938a-9596-4cf7-b4bd-a0e31dd09784.png)
