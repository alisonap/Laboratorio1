# Laboratorio1
Crea un codigo para un biblioteca
<html>
  <head>
    <title>Tablas con Bootstrap</title>

    <link
      href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css"
      rel="stylesheet"
    />
  </head>
  <body>
    <div class="container mt-4">
      <h2>Libros por Tipo</h2>

      <script>
        function eliminarFila(button) {
          var row = button.parentNode.parentNode;
          var table = row.parentNode;
          table.deleteRow(row.rowIndex);
        }
        function agregarFila(tipo) {
        var tablaId = 'tabla' + tipo;
        var tabla = document.getElementById(tablaId).getElementsByTagName('tbody')[0];

        var newRow = tabla.insertRow(tabla.rows.length);
        var cell1 = newRow.insertCell(0);
        var cell2 = newRow.insertCell(1);
        var cell3 = newRow.insertCell(2);

        cell1.innerHTML = tabla.rows.length; 
        cell2.innerHTML = '<input type="text" class="form-control" placeholder="Nombre del libro" disabled />';
        cell3.innerHTML = '<button class="btn btn-primary" onclick="editarFila(this)">Editar</button> ' +
                        '<button class="btn btn-danger" onclick="eliminarFila(this)">Eliminar</button>';
         }
         function editarFila(button) {
         var row = button.parentNode.parentNode;
         var cells = row.getElementsByTagName('td');
         var inputField = cells[1].getElementsByTagName('input')[0];
         var editButton = cells[2].getElementsByTagName('button')[0];

         if (inputField.disabled) {
         inputField.disabled = false;
         editButton.innerHTML = 'Guardar';
         } else {
       
          var nuevoNombre = inputField.value;
         
          inputField.disabled = true;
          editButton.innerHTML = 'Editar';
          }
           } 
</script>

      </script>

      <h3>
        Drama
        <button class="btn btn-success" onclick="agregarFila('Drama')">
          Agregar
        </button>
      </h3>
      <table id="tablaDrama" class="table table-striped">
        <thead>
          <tr>
            <th>ID</th>
            <th>Nombre</th>
            <th>Acciones</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Los miserables"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>2</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Crimen y castigo"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>3</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Hamlet"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>4</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Matar a un ruiseñor"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
        </tbody>
      </table>

      <h3>
        Ficción
        <button class="btn btn-success" onclick="agregarFila('Ficción')">
          Agregar
        </button>
      </h3>
      <table id="tablaFicción" class="table table-striped">
        <thead>
          <tr>
            <th>ID</th>
            <th>Nombre</th>
            <th>Acciones</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Harry Potter y la piedra filosofal"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>2</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="1984"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>3</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="El Gran Gatsby"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>4</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Don Quijote de la Mancha"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
        </tbody>
      </table>

      <h3>
        Suspenso
        <button class="btn btn-success" onclick="agregarFila('Suspenso')">
          Agregar
        </button>
      </h3>
      <table id="tablaSuspenso" class="table table-striped">
        <thead>
          <tr>
            <th>ID</th>
            <th>Nombre</th>
            <th>Acciones</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="El Silencio de los Corderos"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>2</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Misery"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>3</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="El Resplandor"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>4</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="La Chica del Tren"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
        </tbody>
      </table>

      <h3>
        Romance
        <button class="btn btn-success" onclick="agregarFila('Romance')">
          Agregar
        </button>
      </h3>
      <table id="tablaRomance" class="table table-striped">
        <thead>
          <tr>
            <th>ID</th>
            <th>Nombre</th>
            <th>Acciones</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Orgullo y Prejuicio"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>2</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Cumbres Borrascosas"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>3</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Romeo y Julieta"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
          <tr>
            <td>4</td>
            <td>
              <input
                type="text"
                class="form-control"
                placeholder="Nombre del libro"
                value="Bajo el Sol de Medianoche"
              />
            </td>
            <td>
              <button class="btn btn-primary" onclick="editarFila(this)">Editar</button>
              <button class="btn btn-danger" onclick="eliminarFila(this)">
                Eliminar
              </button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>

    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
  </body>
</html>
