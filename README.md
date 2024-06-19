# Check-the-Smart-Contract
Tareas de vottun
Modificaciones
1.	Declaración incorrecta de owner:
    -	El contrato ya hereda de Ownable, lo que proporciona una funcionalidad adecuada para manejar el propietario del contrato. La declaración de private address owner; es redundante e incorrecta. La variable owner definida manualmente se eliminó porque Ownable ya proporciona esta funcionalidad.
2.	Uso incorrecto de owner() en withdrawTips:
    -	La función owner() devuelve la dirección del propietario. No es necesario llamar a owner().send. En su lugar, se debe usar payable(owner()).transfer.
    -	Se utilizó payable(owner()).transfer(address(this).balance); para enviar el saldo al propietario de manera segura.
3.	Nombres de funciones y eventos:
    -	Por convención, las variables de estado deben tener nombres en minúsculas y camello (camelCase), y los eventos también pueden seguir esta convención para mayor claridad.
4.	Visibilidad y seguridad:
    -	Es una buena práctica marcar explícitamente las funciones del constructor y los modificadores de visibilidad, incluso si son public por defecto.
5.	Renombrado de Tips a tips:
    -	Se renombró la variable de estado Tips a tips para seguir las convenciones de nombres.

