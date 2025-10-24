🏦 Power Apps - Gestión de Movimientos Bancarios


📄 Descripción
Aplicación de Power Apps Canvas para gestionar movimientos bancarios de manera visual y eficiente.

Permite:
Registrar ingresos y egresos por banco.
Consultar saldos actualizados con formato monetario (€).
Visualizar movimientos generales o filtrados por banco.
Crear, editar y eliminar movimientos de forma sencilla.
Colorear automáticamente los saldos: 🔴 negativo, 🔵 positivo.

La app utiliza tres listas de SharePoint como fuente de datos:
Moves → movimientos de cada banco.
Banks → información de los bancos.
Concepts → tipos de conceptos (IN / EG, etc.).


⚙️ Funcionalidades principales

Pantalla Bancos:
Listado de bancos con saldo calculado automáticamente.
Selección rápida para ver movimientos de cada banco.
Pantalla Movimientos por Banco:
Filtrado automático según el banco seleccionado.
Orden descendente por fecha y, en caso de empate, por ID.
Visualización de saldo con formato monetario.

Pantalla Movimientos Generales:
Listado completo de movimientos.
Filtros por concepto o fecha.

Formulario Movimiento:
Crear o editar registros, detectando automáticamente si es nuevo o existente.
Manejo de variables para seleccionar el registro correcto desde distintas pantallas (Movimientos Generales y Movimientos por Banco).

Variables y lógica:
RegistroSeleccionadoMovimiento → registro actual en edición.
varSaldoBanco → saldo calculado del banco seleccionado.
varConfirmDelete → confirmación de eliminación.
Manejo de delegación y errores de tipo (Blank(), Defaults(Moves)).

🛠 Tecnologías utilizadas
Microsoft Power Apps (Canvas App)
SharePoint (listas Moves, Banks, Concepts)
Funciones clave: ClearCollect, AddColumns, LookUp, Filter, SortByColumns, Set, Blank(), Defaults().

🚀 Instalación y uso
Abrir el archivo de la app en Power Apps Studio.
Configurar conexiones a las listas de SharePoint: Moves, Banks, Concepts.

Ejecutar la app:
Seleccionar un banco para ver sus movimientos.
Crear, editar o eliminar movimientos.
Consultar el saldo actualizado automáticamente.

💡 Buenas prácticas
Usar variables separadas o parámetros de navegación para registros seleccionados en distintas pantallas.
Mantener nombres consistentes en columnas y colecciones para evitar errores de delegación.
Usar Defaults(Moves) al crear un registro nuevo para evitar problemas de tipo.
Considerar la delegación al filtrar u ordenar listas de SharePoint grandes.

👤 Autor
Ignacio Febles Rivas