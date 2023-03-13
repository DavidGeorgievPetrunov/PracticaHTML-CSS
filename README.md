# PracticaHTML-CSS

- Almenys 3 arxius HTML i 1 arxiu CSS.
  
  *He creado 4 paginas html y un css.*

- Totes les pagines HTML han de tenir vinculat almenys un arxiu CSS.
  
  *Utilizan el mismo estilo.css.*

- Incloure Viewport a totes les pàgines.
  
  *Incluido.*

- Utilitzar Gridview per ajustar el tamany dels blocs.
  
  *Utilizo divs con display grid.*
  
  div.pagina1 {
    height: 100%;
    width: 100%;
    display: grid;
    grid-template-columns: 35% 50% 15%;
    grid-template-rows: 12% 58% 20% 10%;
  }
  
  div.form {
      height: 100%;
      width: 100%;
      display: grid;
      grid-template-columns: 25% 50% 25% ;
      grid-template-rows: 17% 3% 75% 5%;
  }
  
  div.ContenedorGaleria {
      display: grid;
      height: 100%;
      width: 100%;
      grid-template-rows: 25% 55% 20%;
  }
  
  div.horario {
    height: 100%;
    width: 100%;
    background-color: red;
    display: grid;
    grid-template-columns: 20% 60% 20%;
    grid-template-rows: 30% 60% 10%;
  }
  
- Utilitzar Flex box per maquetar els elements.
  
  *Utilizo display flex en los menus, la galeria y el formulario.*
  
  **Menu lateral, cuando hago hover muestra los contenido uno debajo del otro mediante flex.**
  
  .rightmenu:hover > ul {
    display:flex;
    flex-direction:column;
    padding-top:135px;
    animation-name: displayRightMenu;
    animation-duration: 1.2s;
    bottom: 0px;
  }
  
  **Menu de navegacion utiliza flex para mostrar los contenidos uno al lado del otro.**
  
  nav.top ul li:hover > ul {
    display: flex;
    flex-direction: row;
    height: 70px;
    animation-name: display;
    animation-duration: 0.3s;
  }
  
  **Div que contiene el formulario utilizando flex para que salgan los input, label y legend uno debajo del otro.**
  
  form {
    display: flex;
    flex-direction: column;
    background-color: blueviolet;
    height: 100%;
    width: 60%;
    margin-left: 20%;
    border-bottom: 0px;
  } 
  
  **Div que contiene submit y reset en el formulario utilizando flex para que salgan uno al lado del otro.**
  
  div.subres {
    border:none;
    display: flex;
    flex-direction: row;
  }
  
  **Div de la galeria utiliza flex para que las imagenes salgan una al lado de la otra.**
  
  div.ContenedorGaleria > div {
    grid-row-start: 2;
    grid-row-end: 2;
    background-color: red;
    display: flex;
    flex-direction: row;
    background-image: url(./Galeria1/Foto5.jpeg);
    object-fit: cover;
  }

- Utilitzar Media Queries per a que almenys totes les pàgines puguin ser visualitzades a pantalles d'escriptori i telèfons mòbils amb disposicions diferents.
  
  *Hay media queries para cuando la pagina disminuye a 900px o menos que se realizen ciertos cambios*
  
  **Cambios en los menus,el header, el body y el html.**
  
  @media only screen and (max-width: 900px) {
    header{
        height: 3%;
        font-size:0.6em;
    }
    nav.top {
        font-size: 0.2em;
        margin-top: -40px;
        height: 23px;
    }
    nav.top:hover {
        height: 40px;
    }
    nav.top > ul{
        height: 23px;
    }
    nav.top ul li ul li {
        height: 15px;
    }
    .rightmenu {
        background-size: 30px;
        height: 7%;
    }
    .rightmenu:hover{
        font-size: 0.2em;
        background-size: 90px 30px;
        height: 90px;
        width: 130px;
        margin-left: 83%;
    }
    .rightmenu:hover ul {
        padding-top: 30px;
    }
    body,html {
        height: 200%;
    background-color: blue;
    }
  }

  **Cambios pagina 1.**

  @media only screen and (max-width: 900px) {
    .HtmlPag1 {
        height:max-content;
    }
    .BodyPag1 {
        height:max-content
    }
    section, article {
        overflow: scroll;
    }
    p {
        font-size: 0.2em;
    }
    footer {
        font-size: 1em;
        height:27px;
        margin-top: 0px;
    }
    footer:hover {
        font-size: 1.1em;
    }
  }

  **Cambios formulario.**
  
  @media only screen and (max-width: 900px) {
    div.form {
        margin-top: -160px
    }´
    input.submit, input.reset  {
        margin-left: 55px;
        margin-right: 0px;
        font-size: 0.1em;
        padding-left: 3px;
    }
    input.submit {
        margin-left:10px;
        font-size: 0.1em;
    }
  }

  **Cambios galeria.** 
  
    @media only screen and (max-width: 900px) {
    html.galeria,body.galeria {
        height: 100%;
    }
    div.ContenedorGaleria {
        height: 1100px;
        background-color: blue;
        margin-top:-220px;
    }
    .ContenedorGaleria > div{
        flex-wrap: wrap;
        flex-direction: column;
        width: 100%;
        height:100%
    }
    .ContenedorGaleria div.b{
        flex-direction: column;
        width: 100%;
        height:180%;
        text-align: center;
    }
    div.ContenedorGaleria div > div {
        margin-left: 150px;
        background-repeat: repeat;
        height:20%;
        width: max-content;
    }
    div div div p {
        margin-top: -40px;
        color: red;
        font-size: 2em;
        padding-left: 23px;
    }
  }
  **Cambios horario.** 
  
  @media only screen and (max-width: 900px) {
    html.horario {
        height: 320px;
    }
    body.horario {
        height: 320px;
    }
    div.horario {
        height: 300px;
    }
    td,th,tr,table {
        font-size: 0.1em;
    }
    td:hover,th:hover,tr:hover {
        background-color: white;
    }
  }


- Tamany de lletres amb unitats em.
  
  *Si.*

- Utilitzar els Layout de HTML (<header>, <article>, <section>...)
  
  *En la primera pagina se utilizan header, section, article y footer, en el resto solo utilizo el header.*
  
  **Pagina1, sin los contenidos en los layout.**
  
  <section class="left">
        </section>
        <article>
        </article>
        <section class="topright"> 
        </section>
        <section class=right>
        </section>
        <footer> FIN</footer>
    </div>
    <section class="rightmenu">
    </section>

- Incloure un menú superior fixe amb desplegables.
  
  *Incluido en todas las paginas.*

- Incloure un menú lateral ocultable.

  *Incluido un menu lateral en la parte superior derecha con un icono, este menu incrementa de tamaño cuando pasas el raton encima.*

- Incloure un formulari:

- Almenys 4 inputs de diferents types.
  
  *Input tel, email, text, radi y dos date.*
  
  - Botó de submit. 
  
  *Incluido.*

- Botó de reset.
  
  *Incluido.*

- Totes els inputs amb atribut name.
  
  *Incluido.*

   <form method="post">
                <label for="Nombre">Nombre</label>
                <input type="text" id="Nombre" name="Nombre" placeholder="Inserte Nombre" required>
                <label for="Telefono">Telefono</label>
                <input type="tel" id="Telefono" name="Telefono" placeholder="Inserte Telefono" required>
                <label for="email">Email</label>
                <input type="email" id="email" name="email" placeholder="Inserte Email">
                <legend>Elige tu bicicleta a reservar! </legend>
                <ul class="form">
                    <li>
                        <label for="Montaña">Montaña</label>
                        <input type="radio" id="Montaña" name="bicicleta">
                    </li>
                    <li>
                        <label for="Hibrida">Hibrida</label>
                        <input type="radio" id="Hibrida" name="bicicleta">
                    </li>
                    <li>
                        <label for="Electrica">Electrica</label>
                        <input type="radio" id="Electrica" name="bicicleta">
                    </li>
                    <li>
                        <label for="Urbana">Urbana</label>
                        <input type="radio" id="Urbana" name="bicicleta">
                    </li>
                </ul>
                <label for="Ireserva">Inserte la fecha de inicio reserva</label>
                <input type="date" id="Ireserva" name="Ireserva" required>
                <label for="Freserva">Inserte la fecha de fin reserva</label>
                <input type="date" id="Freserva" name="Freserva" required>
                <div class="subres">
                    <input type="submit" id="submit" name="submit" class="submit">
                    <input type="reset" id="reset" name="reset" class="reset">
                </div>
  
- Incloure una taula amb estils alterns per línia i estil diferenciat a la primera línea.
  
  *Incluido.*
  
  th:nth-child(odd) {
    background-color: yellow;
    color: red;
  }
  
  th:nth-child(even) {   
    background-color: orange;
    color: blue;
  }
  
  td:nth-child(odd) {
    background-color: blueviolet;
    color: black;
  }
  
  td:nth-child(1) {
    background-color:aqua;
    color: brown;
  }
  
  td:nth-child(even) {
    background-color: blue;
    color: black;
  }
  
  td:hover,th:hover,tr:hover {
    font-size: 1.3em;
  }


- Incloure una galeria amb imatges d’un mateix tamany amb text a sota (Object-fit).
  
  *Incluido.*

- Incloure una galeria amb imatges d’un mateix tamany més petites que a l’anterior punt (Object-fit).	
  
  *Incluido.*

  **Div general**
  div.ContenedorGaleria {
    display: grid;
    height: 100%;
    width: 100%;
    grid-template-rows: 25% 55% 20%;
  }

  **Div que contiene la primera galeria**
  div.ContenedorGaleria > div {
    grid-row-start: 2;
    grid-row-end: 2;
    display: flex;
    flex-direction: row;
    background-image: url(./Galeria1/Foto5.jpeg);
  }

  **Div que contiene la segunda galeria**
  div.ContenedorGaleria div.b {
    grid-row-start: 3;
    grid-row-end: 4;
    display: flex;
    flex-direction: row;
    background-image: url(./Galeria1/Foto5.jpeg);
    margin-top: 20px;
}
  
  **Div con las imagenes y las palabras**
  div.ContenedorGaleria div div {
    width: 25%;
    height:90%;
    margin-top: 20px;
    margin-left: 10px;
    border: none;
  }

  **imagenes galeria 1**
  div.ContenedorGaleria div img {
    width: 100%;
    height:100%;
    object-fit:fill;
  }

  **imagenes galeria 2**
  div.ContenedorGaleria div.b img {
    object-fit: scale-down;
  }

  **Modificado los p**
  div div div p {
    margin-top: -40px;
    color: red;
    font-size: 2em;
    padding-left: 100px;
  }



- Tots els elements HTML han de tenir estils (border, shadow, font, margin, padding, tamany…) adequats per donar un estil homogeni i modern.
  
  *Incluido.*

- Resaltar la majoria d’elements amb estils hover.
  
  *Incluido.*

- Almenys dues animacions/transicions per HTML.
  
  *Los menus son un total de 3 animaciones y estan presentes en cada pagina, adicionalmente en la pagina formulario tengo una animacion que cambia el background.* 
  
  **Animacion formulario, cambia el fondo entre las siguentes imagenes.**
  
  @keyframes galeria1 {
    25% {background-image: url(./Galeria1/Foto1.jpeg); background-size: cover;}
    50% {background-image: url(./Galeria1/Foto2.jpeg); background-size: cover;}
    75% {background-image: url(./Galeria1/Foto3.jpeg); background-size: cover;}
    100% {background-image: url(./Galeria1/Foto4.jpeg); background-size: cover;}
  }

  **Animacion menu navegacion, muestra el menu expandirse.**

  @keyframes display {
    0% {overflow: hidden; height: 0px;}
    25% { height: 20px;}
    50% { height: 40px;}
    75% { height: 60px;}
    100% {  height: 70px;}
  }

  **Animacion menu lateral, muestra el menu extenderse.**

  @keyframes displayRightMenu {
    0% {overflow: hidden; height: 0%;}
    25% { height: 50%;}
    50% { height: 100%;}
    75% { height: 150%;}
    100% {  height: 200%;}
  }

  **Aumenta el tamaño del icono en el menu lateral, utilizo otra animacion ya que queria usar distintos tiempos para cada           animacion.**

  @keyframes increase {
    0% {overflow: hidden; background-size: 140px 70px;}
    25% {  background-size: 180px 80px;}
    50% {  background-size: 240px 90px;}
    75% {  background-size: 280px 100px;}
    100% {  background-size: 300px 110px;}
  }
