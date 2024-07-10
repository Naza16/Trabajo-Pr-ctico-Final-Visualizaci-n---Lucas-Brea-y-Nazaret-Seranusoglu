<main>
  <div class="centerContainer">
    <div class="header">Una guía visual a</div>
      <h2 class="headline">
        <b>La Guerra y la prosperidad económica.</b>
      </h2>
    <p class="bajada">Por Lucas Brea y Nazaret Seranusoglu</p>
  </div>
  <div id="year-container">
    <div id="year">1939</div>
    <div id="year-text">Evento Historico</div>
    <script>
      window.addEventListener('scroll', function() {
        var posicionDesplazamiento = window.scrollY;
        var añoInicial = 1933;
        var añoFinal = 2024;
        var alturaDocumento = document.body.scrollHeight - window.innerHeight;
        var posicionDesplazamientoFinal = alturaDocumento * 0.9;
        var porcentajeDesplazamiento = posicionDesplazamiento / posicionDesplazamientoFinal;
        if (porcentajeDesplazamiento > 1) porcentajeDesplazamiento = 1;

        var añoActual = Math.floor(añoInicial + (añoFinal - añoInicial) * porcentajeDesplazamiento);

        if (añoActual > añoFinal) añoActual = añoFinal;
        if (añoActual < añoInicial) añoActual = añoInicial;

        document.getElementById('year').innerText = añoActual;

        var textoAño = {
          1939: "Inicio de la Segunda Guerra Mundial",
          1940: "Segunda Guerra Mundial",
          1945: "Fin de la Segunda Guerra Mundial",
          1947: "Inicio de la Guerra Fría",
          1953: "Guerra de Corea",
          1954: "Guerra Fría",
          1960: "Guerra de Vietnam y la Carrera Espacial",
          1961: "EEUU invade Cuba",
          1962: "Crisis de los misiles",
          1963: "John F. Kennedy es asesinado",
          1965: "Invasión de EEUU a Vietnam",
          1969: "Estados Unidos gana la carrera espacial",
          1973: "Invasión de EEUU a Vietnam",
          1979: "Invasión soviética a Afganistán",
          1985: "Asume Gorbachov",
          1989: "Caída del muro de Berlín",
          1991: "Caída de la URSS",
          2001: "Atentados del 11 de septiembre",
          2002: " ",
          2003: "Guerra de Irak",
          2008: "Invasión de Rusia a Georgia",
          2014: "Rusia anexa Crimea",
          2020: "Pandemia COVID-19",
          2022: "Rusia invade Ucrania",
          2024: "Año Actual"
        };

        var texto = "Eventos Históricos";

        for (var año in textoAño) {
          if (añoActual >= año) {
            texto = textoAño[año];
          }
        }

        if (añoActual < 1939) {
          document.getElementById('year-container').style.color = 'black';
        } else {
          document.getElementById('year-container').style.color = 'white';
        }

        document.getElementById('year-text').innerText = texto;
      });
    </script>
  </div>
  <body>
  <div class="Texto">
      <p>
        Durante décadas, ha habido un debate sobre la relación entre guerra y economía. Algunos creen que los conflictos llevan a la ruina
        económica, mientras que otros sugieren que pueden impulsar el crecimiento.
      </p>
      <p>
        Los conflictos bélicos han catalizado transformaciones económicas significativas, impulsando el desarrollo de tecnologías y
        capacidades industriales. Estas innovaciones, cruciales para la estrategia militar, también han tenido un impacto duradero en la
        economía civil.
      </p>
      <p>
        Sin embargo, la guerra trae beneficios económicos a corto plazo, pero conlleva altos costos. La
        destrucción de infraestructura y el desplazamiento de poblaciones tienen efectos duraderos, resaltando la necesidad de soluciones
        pacíficas para los conflictos globales.
      </p>
  </div>
  <h2 class="headline2">
    <b> Conflictos históricos - <span class="GuerraMundial"> Segunda Guerra Mundial</span></b>
  </h2>
  <div class = "ImagenesContainer2">
    <img src="images/WorldWar.jpg" alt="WW2">
  </div>
  <h3 class="headline3">
    <b><span class="GuerraMundial"> Introducción </span></b>
  </h3>
  <div class="Texto">
    <p>La Segunda Guerra Mundial tuvo profundos impactos económicos. La devastación de infraestructuras interrumpió el
    comercio y la economía, impulsando grandes inversiones como el Plan Marshall. Se aceleró la innovación tecnológica y las técnicas de producción en masa.
    </p>
  </div>
  <h3 class="headline3">
    <b><span class="GuerraMundial"> Durante la Guerra </span></b>
  </h3>
  <div class="Texto">
    <p>
      Durante la Segunda Guerra Mundial, muchos países experimentaron un aumento temporal en su PIB debido a la producción bélica y
      el aumento del gasto gubernamental en el esfuerzo de guerra. Sin embargo, este crecimiento no fue sostenible y estuvo acompañado
      por la destrucción de infraestructura. Como bien, se muestra acá:
    </p>
  </div>
  <div class="chart-container2">
    <iframe title="PBI de los paises involucrados en la Segunda Guerra Mundial (en U$D y en millones)" aria-label="Stacked Bars" id="datawrapper-chart-EyeIj" src="https://datawrapper.dwcdn.net/EyeIj/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe>
      <script type="text/javascript">!function(){
        "use strict";window.addEventListener("message",(function(a){
          if(void 0!==a.data["datawrapper-height"]){
            var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){
              var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}
            }
          }))
        }();
    </script>
  </div>
  <h3 class="headline3">
    <b><span class="GuerraMundial"> Luego de la Guerra </span></b>
  </h3>
  <div class="Texto">
    <p>
      Al finalizar la guerra, las economías de Europa y Asia sufrieron debido a la destrucción masiva, resultando en una caída inicial
      del PIB. La ayuda del Plan Marshall de Estados Unidos fue crucial para la reconstrucción, lo que permitió una rápida
      recuperación y crecimiento del PIB en Europa Occidental.
    </p>
  </div>
  <div class="chart-container2">
    <iframe title="Crecimiento Económico Post-Guerra" aria-label="Stacked Bars" id="datawrapper-chart-qhxgM" src="https://datawrapper.dwcdn.net/qhxgM/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe>
      <script type="text/javascript">!function () {
        "use strict";
        window.addEventListener("message", (function (a) {
          if (void 0 !== a.data["datawrapper-height"]) {
            var e = document.querySelectorAll("iframe");
            for (var t in a.data["datawrapper-height"]) for (var r = 0; r < e.length; r++) if (e[r].contentWindow === a.source) {
              var i = a.data["datawrapper-height"][t] + "px";
              e[r].style.height = i
            }
          }
        }))
      }
      ();
    </script>
  </div>
  <div class="Texto">
    <p>
      Tras la Segunda Guerra Mundial, Alemania y Japón experimentaron un rápido crecimiento económico conocido como
      'milagro
      económico', mientras que Estados Unidos se consolidaba como superpotencia. Durante la Guerra Fría, el gasto
      militar y
      tecnológico impactó en el PIB de ambos bloques.
    </p>
    <p>
      La Segunda Guerra Mundial impactó el PIB: crecimiento durante el conflicto, caída posguerra, rápida recuperación y
      efectos duraderos en la economía global.
    </p>
  </div>
  <h2 class="headline2">
    <b> Conflictos históricos - <span class="GuerraFria"> Guerra Fría</span> </b>
  </h2>
  <div class="ImagenesContainer2">
    <img src="images/coldWar.jpg" alt="coldWar">
  </div>
  <h3 class="headline3">
    <b><span class="GuerraFria"> Introducción </span></b>
  </h3>
  <div class="Texto">
    <p>
      La Guerra Fría fue un enfrentamiento global entre Estados Unidos y la Unión Soviética tras la Segunda Guerra Mundial. Se
      caracterizó por una intensa rivalidad política, ideológica y tecnológica.
    </p>
    <p>
    Dividió al mundo en dos bloques: el occidental, liderado por Estados Unidos, y el oriental, por la Unión Soviética. Aunque no hubo
    combates directos entre ellos, compitieron por influencia global y apoyaron regímenes afines.
    </p>
  </div>
  <h3 class="headline3">
    <b><span class="GuerraFria"> Conflictos y la carrera de armas </span></b>
  </h3>
  <div class="Texto">
    <p>El gasto militar durante la Guerra Fría fue colosal, reflejando la intensa competencia entre las superpotencias.</p>
    <ul>
      <li class="Items">
        Estados Unidos en 1980, el gasto militar estadounidense fue de aproximadamente $135 mil millones.
      </li>
      <li class="Items">
        Unión Soviética, aunque las cifras exactas son difíciles de determinar debido a la falta de transparencia, se estima que el
        gasto militar soviético en 1980 fue alrededor de $250 mil millones, ajustado por el poder adquisitivo.
      </li>
    </ul>
  </div>
    <div class="Texto">
    <p>En cuanto a conflictos, nunca hubo, de forma directa, entre los Estados Unidos y la URSS.
      Sin Embargo, hubieron multiples conflictos indirectos o proxy wars. En este periodo, la economía fue afectada por estos enfrentamientos, y veremos como es que se relacionan. </p>
    <p>A continuación, enumeraremos algunos de los más emblemáticos:</p>
    </div>
    <h2 class="headline2">
      <b>Década de 1950 - <span class="GuerraFria"> Guerra de Corea </span></b>
    </h2>
    <div class="Texto">
      Durante la Guerra de Corea (1950-1953), el gasto militar de Estados Unidos se incrementó significativamente, con estimaciones
      que rondan los $50-60 mil millones anuales ajustados a dólares de 1980. Este aumento en el gasto representó aproximadamente el
      10-15% del PIB al comienzo del conflicto, disminuyendo a cerca del 10% hacia el final de la década de 1950.
    </div>
    <div class="chart-container2">
      <iframe title="Presupuesto del gasto militar de EE.UU en la guerra de Corea (en U$D)" aria-label="Interactive line chart" id="datawrapper-chart-Pg1ja" src="https://datawrapper.dwcdn.net/Pg1ja/8/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"]){var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}}}))}();
      </script>
    </div>
    <h2 class="headline2">
      <b> Decada de 1960 - <span class="GuerraFria"> Guerra de Vietnam y Carrera Espacial </span></b>
    </h2>
    <div class="Texto">
    <p>En los años 60, el gasto militar de Estados Unidos creció considerablemente debido a la Guerra de Vietnam y la carrera armamentista.
      En 1960, el gasto militar se estimaba en alrededor de $47 mil millones (ajustados a dólares de 1980). Con la escalada del conflicto en
      Vietnam, los gastos aumentaron drásticamente, las estimaciones oscilan entre $60 y $90 mil millones, ajustados a dólares de 1980.
    </p>
    <p>La Unión Soviética, por su parte, incrementó su gasto militar durante este período, aunque las cifras exactas son difíciles
      de precisar, se estima que el gasto militar soviético representaba
      entre el 12% y el 14% de su PIB durante la década de 1960.
    </p>
    </div>
    <div class="chart-container2">
      <iframe title="Gasto militar de EE.UU y la URSS como parte de su PBI (durante la década del 60) " aria-label="Interactive line chart" id="datawrapper-chart-CYN3N" src="https://datawrapper.dwcdn.net/CYN3N/3/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"]){var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}}}))}();
      </script>
    </div>
    <div class="headline2">
      <b><span class="GuerraFria"> La década de los 70 </span> </b>
    </div>
    <div class="Texto">
      <p>
      Durante la década de 1970, tanto Estados Unidos como la Unión Soviética realizaron inversiones significativas en sus fuerzas
      militares, reflejando la intensa competencia de la Guerra Fría. El gasto militar de Estados Unidos oscilaba entre 90 y 120 mil
      millones de dólares anuales (ajustados a dólares de 1980).
      </p>
      <p>
      Por otro lado, el gasto militar de la Unión Soviética se estimaba en aproximadamente 200 mil millones de rublos anuales
      (ajustados a dólares de 1980), representando entre el 12 y el 14% de su PIB. La URSS se centró en la expansión y
      modernización de su capacidad militar.
      </p>
    </div>
    <div class="chart-container2">
      <iframe title="Gasto militar de la URSS y EEUU en los 70s (medido en U$D)" aria-label="Interactive line chart" id="datawrapper-chart-5vOpc" src="https://datawrapper.dwcdn.net/5vOpc/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe>
        <script type="text/javascript">!function(){
          "use strict";window.addEventListener("message",(function(a){
            if(void 0!==a.data["datawrapper-height"]){
              var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){
                var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}
              }
            }))
          }();
        </script>
    </div>
  <div class="headline2">
    <b><span class="GuerraFria"> La década de los 80s </span></b>
  </div>
  <div class = "Texto">
    <p>
      Durante la década de 1980, bajo la administración Reagan, se produjo un aumento significativo en el gasto militar de los
      Estados Unidos, un componente clave de la política conocida como "Reaganomics" y la intensificación de la Guerra Fría.
    </p>
    <p>
      En 1980, el gasto militar aumentó drásticamente, situándose en estimaciones de entre 150 y 200 mil millones de dólares anuales
      ajustados a los valores de 1980. Este aumento reflejaba una estrategia de defensa intensiva en respuesta a la percepción
      de amenazas estratégicas de la Unión Soviética.
    </p>
    <div class="chart-container2">
      <iframe title="Presupuesto militar de los Estados Unidos en la decada del 80 (en U$D)" aria-label="Interactive line chart" id="datawrapper-chart-sLBiU" src="https://datawrapper.dwcdn.net/sLBiU/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 80% !important; border: none;" height="400" data-external="1"></iframe>
      <script type="text/javascript">!function(){
        "use strict";window.addEventListener("message",(function(a){
          if(void 0!==a.data["datawrapper-height"]){
            var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){
              var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}
          }
        }))
      }();
      </script>
    </div>
  </div>

  <h2 class="headline2">
    <b> Conflictos actuales - <span class="Rusia"> Rusia</span> y <span class="Ucrania">Ucrania</span></b>
  </h2>
  <div class="ImagenesContainer2">
    <img src="images/Putin.jpg" alt="Putin">
  </div>
  <div class="Texto">
      <p>El conflicto sorprendió al mundo y tuvo múltiples impactos económicos. Se observó un aumento en los precios de la energía
      y alimentos, cambios en la cadena de suministros y en los tratados de comercio. Enfoquémonos en lo sucedido a los principales beligerantes del conflicto:</p>
  </div>
  <h2 class="headline2">
    <b><span class="Rusia">Rusia</span></b>
  </h2>
  <div class="Texto">
      <p>El país, en el ultimo tiempo ha cambiado el tipo de economía, pasando de ser una de una fuertemente dependiente del petroleo
      y o de los gases naturales, a ser una de tipo militar.
      Además, su gasto militar ha aumentado significativamente, como podemos verlo aquí:
      </p>
  </div>
      <div class = "chart-container2">
        <iframe title="Presupuesto Militar Ruso (en U$D)" aria-label="Interactive line chart" id="datawrapper-chart-VowJU" src="https://datawrapper.dwcdn.net/VowJU/7/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe>
          <script type="text/javascript">!function(){
            "use strict";window.addEventListener("message",(function(a){
              if(void 0!==a.data["datawrapper-height"]){
                var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){
                  var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}
                }
              }))
            }();
        </script>
      </div>
  <div class="Texto">
    <p>
      El gasto militar ha crecido exponencialmente desde el inicio de la guerra, llegando a cerca de 90 mil millones de dólares,
      representando incluso el 4% del PIB del país, un porcentaje que muy pocas economías alcanzan. Esto indica que el complejo
      industrial militar ruso ha crecido significativamente en el último tiempo.
    </p>
  </div>
  <div class= "Texto">
    <p>
      Algo a tener en cuenta, es que Rusia ha sufrido múltiples congelamientos de activos, fue desplazado del sistema Swift, sin embargo,
      parece haber tenido un impacto nulo, ya que su economía ha crecido, alcanzado maximos historicos. Esto lo podemos ver gracias al
      siguiente gráfico:
    </p>
  </div>
  <div class="chart-container2">
    <iframe title="PBI de Rusia a lo largo de los años (en U$D)" aria-label="Interactive line chart" id="datawrapper-chart-6TIHu" src="https://datawrapper.dwcdn.net/6TIHu/3/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"]){var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}}}))}();
    </script>
  </div>
  <div class="Texto">
    <p>
      Además, en el ultimo año y en el actual, esta economía llego a superar al de las principales potencias europeas, a continuación, el gráfico
      que muestra esto:
    </p>
  </div>
    <div class="chart-container2">
      <iframe title="Crecimiento de potencias europeas" aria-label="Bar Chart" id="datawrapper-chart-p65y2" src="https://datawrapper.dwcdn.net/p65y2/3/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe>
        <script type="text/javascript">!function(){
          "use strict";window.addEventListener("message",(function(a){
            if(void 0!==a.data["datawrapper-height"]){
              var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}
            }
          }))
        }();
      </script>
  </div>
  <h2 class = "headline2">
    <b><span class="Ucrania"> Ucrania</span></b>
  </h2>
  <div class="Texto">
    <p>
      En cuanto a la economía y el gasto militar de Ucrania, la situación es completamente diferente. A diferencia de Rusia,
      este país no tiene una industria militar asentada, con lo cual, es difícil realizar una economía de guerra y gran parte de su gasto
      militar depende fuertemente de los países que le donan equipamiento, dinero, etc. A continuación, mostraremos los mayores donantes:
    </p>
    </div>
  <div class="chart-container2">
    <iframe title="Mayores donantes a Ucrania (en U$D)" aria-label="Donut Chart" id="datawrapper-chart-8s7QS" src="https://datawrapper.dwcdn.net/8s7QS/12/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe>
      <script type="text/javascript">!function(){
        "use strict";window.addEventListener("message",(function(a){
          if(void 0!==a.data["datawrapper-height"]){
            var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){
              var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}
            }
          }))
        }();
    </script>
  </div>
  <div class="Texto">
    No obstante, su presupuesto militar ha crecido exponencialmente:
  </div>
  <div class="chart-container2">
    <iframe title="Presupuesto Militar en Ucrania (en U$D)" aria-label="Interactive line chart" id="datawrapper-chart-DFu8R" src="https://datawrapper.dwcdn.net/DFu8R/3/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe>
      <script type="text/javascript">!function(){
        "use strict";window.addEventListener("message",(function(a){
          if(void 0!==a.data["datawrapper-height"]){
            var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){
              var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}}
            }))
          }();
    </script>
  </div>
    <div class="Texto">
      <p>
      Esto, tiene sus impactos en su economía a futuro, ya que a pesar de haber caído fuertemente por la guerra, se espera que vaya
      creciendo a punto tal de que en un momento vuelva a niveles previos de la guerra. A continuación, podemos verlo en el siguiente
      grafico:
      </p>
    </div>
    <div class="chart-container2">
      <iframe title="Crecimiento del PBI Ucraniano en el futuro (Estimación en U$D)" aria-label="Interactive line chart" id="datawrapper-chart-LfaBF" src="https://datawrapper.dwcdn.net/LfaBF/3/" scrolling="no" frameborder="0" style="width: 0; min-width: 70% !important; border: none;" height="200" data-external="1"></iframe>
        <script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){
          if(void 0!==a.data["datawrapper-height"]){
            var e=document.querySelectorAll("iframe");for(var t in a.data["datawrapper-height"])for(var r=0;r<e.length;r++)if(e[r].contentWindow===a.source){
              var i=a.data["datawrapper-height"][t]+"px";e[r].style.height=i}
            }
          }))
        }();
      </script>
    </div>
    <h3 class="headline3">
    <b><span class="Ucrania"> Conclu</span><span class="Rusia">sión</span></b>
     </h3>
  <div class="Texto">
    <p>
      Como pudimos ver de este conflicto, los beligerantes han, al principio, sufrido una leve caída en su actividad económica. Sin
      embargo, al pasar a tener una economía de guerra, uno de los participantes, ha llegado a volver a tener maximos historicos en
      niveles económicos.
    </p>
  </div>
  <h2 class = "headline2">
    <b><span class="fuego">Cierre Final</span></b>
  </h2>
      <div class="Texto">
          <p>
            La prosperidad económica en tiempos de guerra es compleja y contradictoria. Aunque algunos sectores crecen, como la
            industria de defensa, esto viene con grandes costos humanos y económicos.
          </p>
          <p>
            La prosperidad económica durante la guerra es impulsada por la demanda de productos bélicos, generando empleo y actividad
            económica. La movilización de recursos y el aumento del gasto público también estimulan la economía a corto plazo.
          </p>
          <p>
            Sin embargo, este crecimiento conlleva destrucción y sufrimiento. Los recursos destinados a la guerra podrían haberse usado
            en infraestructura, educación y salud. Además, la incertidumbre de la guerra desalienta la inversión privada y afecta
            negativamente otros sectores económicos.
          </p>
      </div>
  </body>
    <hr class = "hr-style">
    <footer class = "footer">
      <h2 class="headline_footer"> Referencias y créditos </h2>
      <p class = "Text-footer"> A continuación, listaremos links y/o libros en donde hemos podido hallar la informacion necesaria para poder realizar este trabajo: </p>
      <ul>
        <li class = "Text-footer2"> https://www.europarl.europa.eu/RegData/etudes/BRIE/2024/747858/IPOL_BRI(2024)747858_EN.pdf </li>
        <li class = "Text-footer2"> https://data.worldbank.org/indicator/NY.GDP.MKTP.CD?end=2023&locations=RU&start=1988 </li>
        <li class = "Text-footer2"> https://data.worldbank.org/indicator/MS.MIL.XPND.CD?locations=RU </li>
        <li class = "Text-footer2"> https://www.statista.com/statistics/263604/gross-domestic-product-gdp-growth-rate-in-france/#:~:text=It%20is%20an%20important%20indicator,compared%20to%20the%20previous%20year.</li>
        <li class = "Text-footer2"> https://www.voanews.com/a/russia-economy-grew-in-2023-despite-war-and-sanctions/7478952.html </li>
        <li class = "Text-footer2"> https://www.ons.gov.uk/economy/grossdomesticproductgdp/bulletins/gdpfirstquarterlyestimateuk/octobertodecember2023#:~:text=UK%20GDP%20is%20estimated%20to,(COVID%2D19)%20pandemic.</li>
        <li class = "Text-footer2"> https://www.euronews.com/business/2024/02/23/germany-sees-declining-economic-growth-in-last-quarter-of-2023#:~:text=Public%20spending%20also%20inched%20up,%2C%20Germany's%20GDP%20shrank%200.3%25.</li>
        <li class = "Text-footer2"> https://www.statista.com/statistics/263606/gross-domestic-product-gdp-growth-rate-in-italy/#:~:text=In%202023%2C%20Italy's%20real%20GDP,compared%20to%20the%20previous%20year.&text=Italy's%20economy%20is%20a%20developed,well%20as%20the%20European%20Union.</li>
        <li class = "Text-footer2"> https://www.afhistory.af.mil/FAQs/Fact-Sheets/Article/458992/1965-operation-rolling-thunder/</li>
        <li class = "Text-footer2"> https://www.cndh.org.mx/noticia/fin-de-la-invasion-y-guerra-de-vietnam-retiro-del-ejercito-de-eua-despues-de-10-anos-de#:~:text=Tras%20diez%20a%C3%B1os%20de%20permanencia,norteamericanos%20que%20combatieron%20en%20Vietnam.</li>
        <li class= "Text-footer2">  https://www.britannica.com/event/Soviet-invasion-of-Afghanistan</li>
        <li class= "Text-footer2">  https://es.euronews.com/2018/08/08/el-conflicto-entre-georgia-y-rusia-analizado-diez-anos-despues </li>
        <li class= "Text-footer2">  https://www.bbc.com/mundo/noticias-internacional-60500020</li>
        <li class= "Text-footer2">  https://www.britannica.com/event/2022-Russian-invasion-of-Ukraine</li>
        <li class= "Text-footer2">  https://data.worldbank.org/indicator/MS.MIL.XPND.CD?end=2022&locations=UA&skipRedirection=true&start=1960&view=chart</li>
        <li class= "Text-footer">   https://www.bbc.com/mundo/noticias-internacional-62982023</li>
        <li class= "Text-footer2">  https://www.bbc.com/mundo/resources/idt-b3e123dd-b5ae-4c62-8d43-9fd15bfef127</li>
        <li class = "Text-footer2"> https://airandspace.si.edu/about/acerca-del-museo-nacional-del-aire-y-el-espacio/apolo-11</li>
        <p class = "Text-footer"> Durante la guerra fría y la Segunda Guerra Mundial, es más dificil estimar los gastos miltares, dado el secretismo y la falta de trasparencia por parte de ciertas administraciones, sin embargo, gran parte de la informacion proviene de las siguietnes fuentes: </p>
        <li class = "Text-footer2"> Stockholm International Peace Research Institute </li>
        <li class = "Text-footer2"> Historical Statistics of the United States, Colonial Times to 1970</li>
        <li class = "Text-footer2"> "The Rise and Fall of the Great Powers" de Paul Kennedy</li>
        <li class = "Text-footer2"> https://www.statista.com/statistics/1334676/wwii-annual-war-gdp-largest-economies/ </li>
        <li class = "Text-footer2"> Maddison, Angus. "The World Economy: Historical Statistics." OECD, 2003 </li>
        <li class = "Text-footer2"> Crafts, N. F. R., and Toniolo, Gianni (eds). "Economic Growth in Europe Since 1945." Cambridge University Press, 1996. </li>
        <li class = "Text-footer2"> Ohkawa, Kazushi, and Rosovsky, Henry. "Japanese Economic Growth: Trend Acceleration in the Twentieth Century." Stanford University Press, 1973.</li>
        <li class = "Text-footer2"> Bureau of Economic Analysis (BEA), U.S. Department of Commerce </li>
        <li class = "Text-footer2"> https://ourworldindata.org/grapher/military-expenditure-total?tab=chart&time=1950..1959&country=~USA </li>
        <li class = "Text-footer2"> https://ourworldindata.org/grapher/military-expenditure-total?tab=chart&time=1970..1979&country=~USA</li>
      </ul>
      <p class  = "Text-footer"> Esta página fue creada por Lucas Brea y Nazaret Seranusoglu. Para poder contactarnos, cuenta con los siguientes medios de comunicación:</p>
      <ul>
        <li class = "Text-footer3">Mail de Nazaret: Nazaretseranusoglu@gmail.com</li>
        <li class = "Text-footer3">Mail de Lucas: Lucasjbrea@gmail.com</li>
      </ul>
      <p class = "Text-footer"> Todos los gráficos han sido creados gracias a Datawrapper.</p>
    </footer>
</main>

<style>
  main {
  position: relative;
  z-index: 1;
  width: 100%;
  scroll-behavior: smooth;
}
p{
  margin:5px;
  padding: 20px;
  max-width: 100%;
}
.header, .bajada, .footer {
  padding:10px;
  position:relative;
  width: 100%;
}
.header, .bajada {
  font-size: 30px;
  text-align: center;
  margin-bottom: 20px;
  width: 100%;
  font-family:'Roboto Mono', monospace;
  font-optical-sizing: auto;
  font-style: normal;
}
.headline2{
  font-size: 55px;
  -webkit-background-clip: text;
  background-clip: text;
  color: white;
  border-radius: 8px;
  text-align: center;
  position: relative;
  width: 100%;
  padding-top: 10px;
  padding-bottom: 5px;
  font-family: "Roboto Mono", monospace;
  font-optical-sizing: auto;
  font-style: normal;
  view-timeline-name: --Titulo2;
  view-timeline-axis: block;
  animation-timeline: --Titulo2;
  animation-name:show;
  animation-range: entry 25% cover 50%;
  animation-fill-mode: both;
}

.headline3 {
  font-size: 45px;
  -webkit-background-clip: text;
  background-clip: text;
  color: white;
  border-radius: 8px;
  text-align: center;
  position: relative;
  width: 100%;
  font-family: "Roboto Mono", monospace;
  font-optical-sizing: auto;
  font-style: normal;
  view-timeline-name: --Titulo3;
  view-timeline-axis: block;
  animation-timeline: --Titulo3;
  animation-name:show;
  animation-range: entry 25% cover 50%;
  animation-fill-mode: both;
}
.headline_footer {
  font-size: 35px;
  -webkit-background-clip: text;
  color: white;
  background-clip: text;
  border-radius: 8px;
  text-align: center;
  position: relative;
  background-size: 200% 200%;
  width: 100%;
  font-family: "Roboto Mono", monospace;
  font-optical-sizing: auto;
  font-style: normal;
}

.headline {
  font-size: 60px;
  background: radial-gradient(circle, red, rgb(255, 175, 90), rgb(255, 244, 33));
  -webkit-background-clip: text;
  background-clip: text;
  border-radius: 8px;
  text-align: center;
  position: relative;
  color: transparent;
  animation: fuego 5s alternate-reverse infinite;
  background-size: 200% 200%;
  width: 100%;
  font-family: "Roboto Mono", monospace;
  font-optical-sizing: auto;
  font-style: normal;
}
@keyframes fuego {
  0% {
    background-position: 100% 100%;
  }
  100% {
    background-position: 0% 0%;
  }
}
@keyframes show{
  from{
    opacity: 0;
    scale: 0%;
  }
  to{
    opacity: 1;
    scale: 100%
  }
}
.chart-container2{
  padding-bottom: 2%;
  padding-top: 4%;
  text-align: center;
  margin: 20px 0;
  view-timeline-name: --container;
  view-timeline-axis: block;
  animation-timeline: --container;
  animation-name:show;
  animation-range: entry 25% cover 50%;
  animation-fill-mode: both;
}
.chart-container2 iframe{
  max-width: 100%;
  border:none;
}
.ImagenesContainer2 {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  view-timeline-name: --image;
  view-timeline-axis: block;
  animation-timeline: --image;
  animation-name:show;
  animation-range: entry 55% cover 50%;
  animation-fill-mode: both;
}
.ImagenesContainer2 img {
  padding-bottom: -5%;
  max-width: 80%; /* Ajusta el tamaño de la imagen según tus preferencias */
  height: auto;
  display: block;
  margin: 0 auto; /* Centra la imagen horizontalmente */
}

.GuerraMundial {
  background: radial-gradient(circle, red, white);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  animation: guerraMundial 5s alternate-reverse infinite;
  background-size: 200% 200%;
  text-align: center;
}

.GuerraFria{
  background: radial-gradient(circle, red,blue);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  animation: guerraFria 10s alternate-reverse infinite;
  background-size: 200% 200%;
  text-align: center;
}
@keyframes guerraFria{
  0%{
    background-position: 0% 0%;
  }
  25%{
    background-position: 100% 100%;
  }
  50%{
    background-position: 0% 0%;
  }
  75%{
    background-position: 100% 100%;
  }
  100%{
    background-position: 0% 0%;
  }
}
@keyframes guerraMundial {
  0% {
    background-position: 0% 0%;
  }
  50% {
    background-position: 100% 100%;
  }
  75% {
    background-position: 0% 0%;
  }
  100% {
    background-position: 100% 100%;
  }
}

.Ucrania {
  background: radial-gradient(circle, rgb(0, 191, 255), rgb(255, 255, 0));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  animation: ucrania 5s alternate-reverse infinite;
  background-size: 200% 200%;
  text-align: center;
}
@keyframes ucrania {
  0% {
    background-position: 0% 0%;
  }
  50% {
    background-position: 100% 100%;
  }
  75% {
    background-position: 0% 0%;
  }
}
.Rusia {
  background: radial-gradient(circle, rgb(255, 255, 255), rgb(0, 0, 255), rgb(255, 0, 0));
  background-clip: text;
  color: transparent;
  animation: rusia 5s alternate-reverse infinite;
  background-size: 200% 200%;
  width: 100%;
  text-align: center;
}
@keyframes rusia {
  0% {
    background-position: 0% 0%;
  }
  50% {
    background-position: 100% 100%;
  }
  75% {
    background-position: 0% 0%;
  }
  100%{
    background-position: 0% 0%;
  }
}
.Texto{
  font-size: 20px;
  justify-content: center;
  text-align: left;
  width: 80%;
  margin: auto;
  font-family: "Roboto Mono", monospace;
  font-optical-sizing: auto;
  font-style: normal;
  color: #BCBCBC;
  view-timeline-name: --texto;
  view-timeline-axis: block;
  animation-timeline: --texto;
  animation-name:show;
  animation-range: entry 25% cover 50%;
  animation-fill-mode: both;
}

.Items{
  font-size:18px;
  justify-content: center;
  margin-left: 50px;
  width: 100%;
  font-family: 'Roboto Mono', monospace;
  font-optical-sizing: auto;
  font-style: normal;
  color: #BCBCBC;
  view-timeline-name: --items;
  view-timeline-axis: block;
  animation-timeline: --items;
  animation-name:show;
  animation-range: entry 25% cover 50%;
  animation-fill-mode: both;
}
  .footer {
    width: 100%;
    text-align: center;
    view-timeline-name: --footer;
    view-timeline-axis: block;
    animation-timeline: --footer;
    animation-name:show;
    animation-range: entry 25% cover 50%;
    animation-fill-mode: both;
  }
  .Text-footer {
    font-size: 18px;
    text-align: center;
    width: 100%;
    font-family: "Roboto Mono", monospace;
    font-optical-sizing: auto;
    font-style: normal;
    padding-top: -20%;
  }
  .Text-footer2 {
    font-size: 15px;
    content: '•';
    text-align: left;
    color:white;
    width: 100%;
    font-family: "Roboto Mono", monospace;
    font-optical-sizing: auto;
    font-style: normal;
  }

  .Text-footer3 {
    font-size: 15px;
    content: '•';
    text-align: center;
    color:white;
    width: 100%;
    font-family: "Roboto Mono", monospace;
    font-optical-sizing: auto;
    font-style: normal;
  }

.hr-style {
  max-width: 100%;
  background-color: #FFFFFF;
  margin-top:20px;
  view-timeline-name: --barra;
  view-timeline-axis: block;
  animation-timeline: --barra;
  animation-name:show;
  animation-range: entry 25% cover 50%;
  animation-fill-mode: both;
}
.centerContainer{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin-top: 120px;
}

  #year-container {
    position: fixed;
    top: 20px;
    left: 20px;
    background: rgba(0, 0, 0, 0.7);
    color: white;
    padding: 10px;
    border-radius: 5px;
    text-align: left;
  }

  #year {
    font-size: 24px;
    font-weight: bold;
  }

  #year-text {
    font-size: 18px;
    width: 60%;
  }
  .fuego{
    background: radial-gradient(circle, red, rgb(255, 175, 90), rgb(255, 244, 33));
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    animation: fuego 10s alternate-reverse infinite;
    background-size: 200% 200%;
    text-align: center;

  }
</style>
