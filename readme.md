el compontente Buscador.jsx es el Home
coloque en el app.js en la siguiente ruta para hacer las pruebas
          <Route path="/buscar" element={<Buscador />}/>

todas las busquedas funcionaron y no dieron ningun errror

el componente Filtro.jsx esta importado tambien en Buscador.jsx
cualquier duda con los componentes y las funciones, me avisan 




el metodo que use para agregar el whatsapp es el siguiente

 <li className="liNav">
            <a
              className="enlancesDeNav"
              href="https://wa.me/+595985317367?text=Hola,%20estoy%20interesado%20en%20un%20asesoramiento%20en%20un%20proyecto%20inmobiliario!"
              target="_blank"
              rel="noopener noreferrer"
            >
              Whatsapp aquí
            </a>
   </li>
 

 por ejemplo si se quiere enviar lo siguiente:
    MENSAJE: estoy interesado en el articulo que publicacaste con "titulo" de id "_id"
    SE ENVIARA EL MENSAJE AL: +595 985 317 367  
 Se vera de la siguiente manera:
siendo "titulo" y "_id" unas variables
al  numero alojado en publicacion.numero


<li className="liNav">
  <a
    className="enlancesDeNav"
    href={`https://wa.me/${publicacion.numero}?text=Hola,%20estoy%20interesado%20en%20el%20articulo%20que%20publicaste%20con%20"${titulo}"%20de%20id%20"${_id}"`}
    target="_blank"
    rel="noopener noreferrer"
  >
    Whatsapp aquí
  </a>
</li>




o si es un boton viendose de estta forma 


<button
  className="botonWhatsapp"
  onClick={() => {
    window.open(
      `https://wa.me/${publicacion.numero}?text=Hola,%20estoy%20interesado%20en%20el%20articulo%20que%20publicaste%20con%20"${titulo}"%20de%20id%20"${_id}"`,
      "_blank"
    );
  }}
>
  Whatsapp aquí
</button>

para probar puedes usar el siguiente CSS

.botonWhatsapp {
  display: inline-block;
  padding: 10px 20px;
  background-color: #25D366;
  color: #FFFFFF;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
}

.botonWhatsapp:hover {
  background-color: #128C7E;
}





