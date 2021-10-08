# Sistema informático Jardinería XML
Debemos generar añadir nuestro DTD  de acorde a nuestro XML para el correcto funcionamiento del código, el resultado final seria este.


![2](https://user-images.githubusercontent.com/61906112/136598345-709ce113-1351-4bfc-b846-c586a267deba.PNG)




Para completar nuestro XML, debemos añadir varias  etiquetas que contengan de manera organizada y  de fácil interpretación la siguiente información.
Sistema de un almacén de pedidos de una jardinería, debe haber un elemento raiz que contenga pedidos donde añadimos plantas, flores y utensilios. Cada elemento puede aparecer y repetirse sin orden restrictivo. Puede contener 4 plantas, 2 flores, y 4 utensilios por ejemplo.
    • Toda planta tiene un atributo obligatorio nombre
    • Los elementos flores tienen un atributo optativo color
    • Todo elemento utensilio debe tener dentro un elemento obligatorio número
Para ello vamos a definir nuestro XML creando atributos que ejercerán como padres o raíz, y otros campos como hijos para mantener así de forma ordenada la información relevante entre si. El resultado de nuestro código XML es el siguiente.

![1](https://user-images.githubusercontent.com/61906112/136598350-f7e357ce-914a-442c-952f-0a00144bab5a.PNG)



# Validamos XML  y DTD
Para validad nuestro codigo XML y el DTD disponemos de webs en las cuales realizamos la comprobación.

[Validar XML y DTD](http://xmlvalidator.new-studio.org)

[Validar XML](https://www.w3schools.com/xml/xml_validator.asp)!


![comprobacion dtd](https://user-images.githubusercontent.com/61906112/136598363-617f1866-087a-467f-b712-e3183a8836ca.PNG)
