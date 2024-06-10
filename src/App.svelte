<script>
  import * as d3 from "d3";
  import { writable, derived } from "svelte/store";
  import { LayerCake, Svg } from "layercake";
  import Line from "./_components/Line.svelte";
  import Area from "./_components/Area.svelte";
  import AxisX from "./_components/AxisX.svelte";
  import AxisY from "./_components/AxisY.svelte";
  import data from "./_data/MilitaryExpenditureRussia.csv";
  import data2 from "./_data/RussiaGPD.csv";

  const xKey = "myX"; // Asegúrate de que "myX" es la columna correcta en tu CSV
  const yKey = "myY"; // Asegúrate de que "myY" es la columna correcta en tu CSV
  let year = writable(2022);

  const filteredData = derived(year, $year => {
    return data.filter(d => +d[xKey] <= $year); // Asegúrate de convertir a número
  });

  const filteredData2 = derived(year, $year => {
    return data2.filter(d => +d[xKey] <= $year); // Asegúrate de convertir a número
  });
</script>

<main>
  <div class="header">Una guía visual a</div>
  <h2 class="headline">
    <b>La Guerra y la prosperidad económica.</b>
  </h2>
  <p class="bajada">Por Lucas Brea y Nazaret Seranusoglu</p>
  <div class="Texto">
    <h3>
      <p>
      Durante décadas, ha habido un debate sobre la relación entre guerra y economía. Algunos creen que los conflictos llevan a
      la ruina económica, mientras que otros sugieren que la guerra puede impulsar el crecimiento. Exploraremos cómo las economías de los países han fluctuado a lo largo de los años.
      </p>
      <p>
        Los conflictos bélicos históricamente han actuado como catalizadores de transformaciones económicas significativas. 
        Durante períodos de guerra, la necesidad de desarrollar nuevas tecnologías y capacidades industriales para apoyar los 
        esfuerzos militares ha llevado a avances notables en diversos campos, desde la aviación hasta la informática. 
        Estas innovaciones no solo han sido cruciales para la estrategia militar, sino que también han tenido un impacto duradero 
        en la economía civil, impulsando el crecimiento industrial y la creación de empleo. 
      </p>
      <p>
        Sin embargo, es importante reconocer que estos beneficios vienen acompañados de enormes costos humanos y materiales. 
        La guerra causa destrucción masiva de infraestructura, desplazamiento de poblaciones y pérdida de vidas, 
        lo que tiene repercusiones económicas y sociales a largo plazo. Además, la redistribución de recursos durante 
        los períodos de conflicto puede agravar las desigualdades económicas y sociales, ya que ciertos sectores reciben más atención 
        y financiamiento que otros. Aunque la guerra puede impulsar la innovación y el crecimiento económico en el corto plazo, 
        sus efectos negativos a largo plazo son difíciles de ignorar, lo que subraya la importancia de buscar soluciones pacíficas para
        los conflictos globales.
      </p>
    </h3>
  </div>
  <h2 class="headline2">
    <b> Conflictos actuales - <span class="Rusia"> Rusia</span> y <span class="Ucrania">Ucrania</span></b>
  </h2>
  <div class="ImagenesContainer">
    <img src="images/Putin.png" alt="Putin" class="ImagenesLideres1">
    <img src="images/Zelenskyy.png" alt="Zelenskyy" class="ImagenesLideres2">
  </div>
  <div class="Texto">
    <h3>
      El conflicto sorprendió al mundo y tuvo múltiples impactos económicos. Se observó un aumento en los precios de la energía 
      y alimentos, cambios en la cadena de suministros y en los tratados de comercio. 
      Enfoquémonos en lo sucedido a los principales beligerantes del conflicto:
    </h3>
  </div>
  <h2 class="headline3">
    <b> <span class="Rusia">Rusia</span></b>
  </h2>
  <div class="Texto2">
    <h3>
      El país, en el ultimo tiempo ha cambiado el tipo de economía, pasando de ser una de una fuertemente dependiente del petroleo 
      y o de los gases naturales, a ser una de tipo militar. 
      Además, su gasto militar ha aumentado significativamente, como podemos verlo aquí:
    </h3>
  </div>
  <!-- Slider para seleccionar el año -->
  <div class="input-container">
    <input
      type="range"
      min="1993"
      max="2022"
      step="1"
      bind:value={$year}
    />
    <span class="counter-container"><h8>Cantidad de Dinero utilizado para el gasto militar durante el año:</h8> <b>{$year}</b></span>
  </div>
  <!-- Gráfico inicial -->
  <div class="chart-container">
    <LayerCake
      padding={{ top: 8, right: 10, bottom: 20, left: 25 }}
      x={xKey}
      y={yKey}
      yDomain={[0, null]}
      data={$filteredData}
    >
      <Svg>
        <AxisX ticks={4} />
        <AxisY ticks={4} />
        <Line stroke="#38538A" />
        <Area fill="#38538A20" />
      </Svg>
    </LayerCake>
  </div>
  <div class="Texto">
    <h3>
      El gasto militar ha crecido exponencialmente desde el inicio de la guerra, llegando a cerca de 90 mil millones de dólares, 
      representando incluso el 4% del PIB del país, un porcentaje que muy pocas economías alcanzan. Esto indica que el complejo 
      industrial militar ruso ha crecido significativamente en el último tiempo.
    </h3>
  </div>
  <div class= "Texto">
    <h3>
      Algo a tener en cuenta, es que Rusia ha sufrido múltiples congelamientos de activos, fue desplazado del sistema Swift, sin embargo, parece
      haber tenido un impacto nulo, ya que su economía ha crecido, alcanzado maximos historicos. Esto lo podemos ver gracias al siguiente
      gráfico:
    </h3>
  </div>
   <!-- Slider para seleccionar el año -->
   <div class="input-container">
    <input
      type="range"
      min="1993"
      max="2022"
      step="1"
      bind:value={$year}
    />
    <span class="counter-container"><h8>Crecimiento del PBI ruso año tras año: </h8> <b>{$year}</b></span>
  </div>
  <div class="chart-container">
    <LayerCake
      padding={{ top: 8, right: 10, bottom: 20, left: 25 }}
      x={xKey}
      y={yKey}
      yDomain={[0, null]}
      data={$filteredData2}
    >
      <Svg>
        <AxisX ticks={4} />
        <AxisY ticks={4} />
        <Line stroke="#38538A" />
        <Area fill="#38538A20" />
      </Svg>
    </LayerCake>
  </div>
  <div class="Texto">
    <h3>
      Además, en el ultimo año y en el actual, esta economía llego a superar al de las principales potencias europeas, a continuación, el gráfico 
      que muestra esto:
    </h3>
  </div>
  <!-- Slider para seleccionar el año -->
  <div class="input-container">
    <input
      type="range"
      min="1993"
      max="2022"
      step="1"
      bind:value={$year}
    />
    <span class="counter-container"><h8>Crecimiento del PBI ruso año tras año: </h8> <b>{$year}</b></span>
  </div>
  <div class="chart-container">
    <LayerCake
      padding={{ top: 8, right: 10, bottom: 20, left: 25 }}
      x={xKey}
      y={yKey}
      yDomain={[0, null]}
      data={$filteredData2}
    >
      <Svg>
        <AxisX ticks={4} />
        <AxisY ticks={4} />
        <Line stroke="#38538A" />
        <Area fill="#38538A20" />
      </Svg>
    </LayerCake>
  </div>
  <h2 class = "headline">
    <b><span class="Ucrania"> Ucrania</span></b>
  </h2>
  <div class="Texto">
    <h3>
      En cuanto a la economía y el gasto militar de Ucrania, la situación es completamente diferente. A diferencia de Rusia, 
      este país no tiene una industria militar asentada, con lo cual, es difícil realizar una economía de guerra y gran parte de su gasto 
      militar depende fuertemente de los países que le donan equipamiento, dinero, etc. 
    </h3>
  </div>
   <!-- Slider para seleccionar el año -->
   <div class="input-container">
    <input
      type="range"
      min="1993"
      max="2022"
      step="1"
      bind:value={$year}
    />
    <span class="counter-container"><h8>Crecimiento del PBI ruso año tras año: </h8> <b>{$year}</b></span>
  </div>
  <div class="chart-container">
    <LayerCake
      padding={{ top: 8, right: 10, bottom: 20, left: 25 }}
      x={xKey}
      y={yKey}
      yDomain={[0, null]}
      data={$filteredData2}
    >
      <Svg>
        <AxisX ticks={4} />
        <AxisY ticks={4} />
        <Line stroke="#38538A" />
        <Area fill="#38538A20" />
      </Svg>
    </LayerCake>
  </div>
  <div class="Texto">
    <h3>
      A pesar de ello, la economía ucraniana, en el 2023, sorprendentemente ha crecido, en comparación al año 2022, en el que había caído 
      un 30% (aproximadamente)
    </h3>
  </div>
     <!-- Slider para seleccionar el año -->
     <div class="input-container">
      <input
        type="range"
        min="1993"
        max="2022"
        step="1"
        bind:value={$year}
      />
      <span class="counter-container"><h8>Crecimiento del PBI ruso año tras año: </h8> <b>{$year}</b></span>
    </div>
    <div class="chart-container">
      <LayerCake
        padding={{ top: 8, right: 10, bottom: 20, left: 25 }}
        x={xKey}
        y={yKey}
        yDomain={[0, null]}
        data={$filteredData2}
      >
          <Svg>
            <AxisX ticks={4} />
            <AxisY ticks={4} />
            <Line stroke="#38538A" />
            <Area fill="#38538A20" />
          </Svg>
        </LayerCake>
      </div>
      <h2 class="headline2">
        <b> Conflictos históricos - <span class="GuerraMundial"> Segunda Guerra Mundial.</span></b>
      </h2>
      <h2 class="headline3">
        <b>Introducción.</b>
      </h2>
      <div class="Texto">
      <h3>
      <p>La Segunda Guerra Mundial tuvo profundos impactos económicos. La destrucción masiva de infraestructuras en Europa y Asia interrumpió la economía y el comercio, y requirió una inversión significativa para la reconstrucción, como el Plan Marshall de Estados Unidos.
      Estados Unidos emergió como la principal potencia económica, mientras que las economías europeas quedaron debilitadas, desplazando 
      el poder económico hacia Estados Unidos y la Unión Soviética. La guerra aceleró la innovación tecnológica y las técnicas de
      producción en masa, beneficiando posteriormente al sector civil. 
      </p>
      <p>El comercio internacional se redujo inicialmente, pero se reconfiguró con un mayor papel para Estados Unidos y un 
      crecimiento del comercio intraeuropeo. Muchos países adoptaron políticas keynesianas para fomentar el crecimiento y establecieron 
      sistemas de bienestar social.</p>
      </h3></div>
      <h2 class="headline3">
        Durante la guerra.
      </h2>
      <div class="Texto">
        <h3>
          Durante la Segunda Guerra Mundial, muchos países experimentaron un aumento temporal en su PIB debido a la producción bélica y 
          el aumento del gasto gubernamental en el esfuerzo de guerra. Sin embargo, este crecimiento no fue sostenible y estuvo acompañado
          por la destrucción de infraestructura.
        </h3>
      </div>
      <div class="input-container">
        <input
          type="range"
          min="1993"
          max="2022"
          step="1"
          bind:value={$year}
        />
        <span class="counter-container"><h8>Crecimiento del PBI ruso año tras año: </h8> <b>{$year}</b></span>
      </div>
      <div class="chart-container">
        <LayerCake
          padding={{ top: 8, right: 10, bottom: 20, left: 25 }}
          x={xKey}
          y={yKey}
          yDomain={[0, null]}
          data={$filteredData2}
        >
          <Svg>
            <AxisX ticks={4} />
            <AxisY ticks={4} />
            <Line stroke="#38538A" />
            <Area fill="#38538A20" />
          </Svg>
        </LayerCake>
      </div>
      <h2 class="headline3">
        Luego de la guerra.
      </h2>
      <div class="Texto">
        <h3>
          Al finalizar la guerra, las economías de Europa y Asia sufrieron debido a la destrucción masiva, resultando en una caída inicial
          del PIB. La ayuda del Plan Marshall de Estados Unidos fue crucial para la reconstrucción, lo que permitió una rápida 
          recuperación y crecimiento del PIB en Europa Occidental.
        </h3>
      </div>
      <div class="Texto">
        <h3>
          <p>
          En las décadas siguientes, muchos países, especialmente Alemania y Japón, experimentaron un rápido crecimiento económico conocido como "milagro económico". 
          Estados Unidos emergió como una superpotencia con un PIB en crecimiento sostenido. La Guerra Fría impulsó el gasto militar y 
          tecnológico, afectando el PIB de ambos bloques. La reestructuración económica global y la aceleración de la globalización 
          promovieron un crecimiento económico sostenido a nivel mundial.
        </p><p>
          En resumen, la Segunda Guerra Mundial tuvo un impacto profundo y complejo en el PIB de los países, con un crecimiento temporal
          durante el conflicto, una caída inmediata posguerra seguida por una rápida recuperación, y efectos a largo plazo que han 
          influido en la economía global hasta hoy.
        </p>
        </h3>
      </div>
      <h2 class = "headline3">
        Conclusión.
      </h2>
      <div class="Texto">
        <h3>
          <p>
            La prosperidad económica en tiempos de guerra es un fenómeno complejo y a menudo contradictorio. Si bien es cierto que algunos
            sectores de la economía pueden experimentar un crecimiento durante períodos de conflicto, como la industria de defensa y 
            ciertas ramas de la producción, este crecimiento generalmente está acompañado de costos humanos y económicos significativos.
          </p>
          <p>
            La prosperidad económica durante la guerra suele ser impulsada por la demanda de productos y servicios relacionados con el 
            esfuerzo bélico, como armas, municiones, equipo militar y suministros. Esto puede generar empleo y aumentar la actividad
            económica en estas áreas específicas. Además, la movilización de recursos y la expansión del gasto público pueden estimular 
            la economía en el corto plazo.
          </p>
          <p>
            Sin embargo, este crecimiento está vinculado a la destrucción y el sufrimiento humanos causados por el conflicto. Los recursos
            que se destinan a la guerra podrían haberse utilizado para inversiones en infraestructura, educación, salud u otras áreas que
            promueven el desarrollo a largo plazo y el bienestar general de la sociedad. Además, la incertidumbre y la inestabilidad 
            asociadas con la guerra pueden desalentar la inversión privada y afectar negativamente otros sectores de la economía.
          </p>
          <p>
            En resumen, si bien la prosperidad económica durante la guerra puede ser evidente en algunos aspectos, es importante considerar
            los costos humanos y económicos más amplios del conflicto. La verdadera prosperidad económica se basa en el desarrollo 
            sostenible, la estabilidad y el bienestar general de la sociedad, que a menudo se ven amenazados por la guerra y sus 
            consecuencias.
          </p>
        </h3>
      </div>
      <hr class = "hr-style">
      <footer class = "footer">
        <p class  = "Text-footer"> Esta página fue creada por Lucas Brea y Nazaret Seranusoglu.</p>
        <p class = "Text-footer"> Para poder contactarnos, cuenta con los siguientes medios de comunicación:</p>
        <ul>
          <li class = "Text-footer2">Gmail de Nazaret: Nazaretseranusoglu@gmail.com</li>
          <li class = "Text-footer2">Gmail de Lucas: Lucasjbrea@gmail.com</li>
        </ul>
      </footer>
</main>

<style>
  main {
  position: relative;
  z-index: 1;
  color: white;
  text-shadow: 0 0 10px black;
  margin: 0;
  padding: 0;
}

.header, .bajada, .headline, .headline2, .headline3, .Texto, .Texto2, .footer {
  margin-left: 0;
  margin-right: 0;
  padding-left: 0;
  padding-right: 0;
}

.header, .bajada {
  font-size: 35px;
  text-align: center;
  margin-bottom: 20px;
}

.headline2, .headline3 {
  font-size: 55px;
  -webkit-background-clip: text;
  background-clip: text;
  border-radius: 8px;
  text-align: center;
  position: relative;
}

.headline {
  font-size: 65px;
  background: radial-gradient(circle, red, rgb(255, 175, 90), rgb(255, 244, 33));
  -webkit-background-clip: text;
  background-clip: text;
  border-radius: 8px;
  text-align: center;
  position: relative;
  color: transparent;
  animation: fuego 8s alternate-reverse infinite; 
  background-size: 200% 200%;
}

@keyframes fuego {
  0% {
    background-position: 100% 100%;
  }
  100% {
    background-position: 0% 0%;
  }
}

.ImagenesContainer {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: -200px;
  padding-bottom: 5%;
}

.ImagenesLideres1, .ImagenesLideres2 {
  display: block;
  height: auto;
  max-width: 100%;
}

.Ucrania {
  background: radial-gradient(circle, rgb(0, 191, 255), rgb(255, 255, 0));
  background-clip: text;
  color: transparent;
  animation: ucrania 8s alternate-reverse infinite;
  background-size: 200% 200%;
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
  animation: rusia 8s alternate-reverse infinite;
  background-size: 200% 200%;
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
}

.Texto, .Texto2 {
  font-size: 25px;
  font-weight: normal;
  justify-content: center;
  text-align: start;
  margin-left: 0;
  margin-right: 0;
  padding-left: 0;
  padding-right: 0;
}

.headline b {
  display: block;
}

.chart-container {
  width: 100%;
  height: 500px;
  padding-bottom: 5%;
}

.input-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 10px;
  width: 100%;
}

.input-container input {
  margin: 0 10px;
  -webkit-appearance: none;
  appearance: none;
  width: 200px;
  height: 5px;
  background: #ddd;
  outline: none;
  opacity: 0.7;
}

.input-container input::-webkit-slider-runnable-track {
  width: 100%;
  height: 5px;
  cursor: pointer;
  background: #38538A50;
}

.input-container input::-webkit-slider-thumb {
  border: 1px solid #000000;
  height: 15px;
  width: 15px;
  border-radius: 50%;
  background: #38538A;
  cursor: pointer;
  -webkit-appearance: none;
  margin-top: -5px;
}

.footer {
  width: 100%;
  text-align: center;
  padding: 20px;
  margin-top: 50px;
}

.Text-footer {
  font-size: 22px;
  font-weight: bold;
  text-align: center;
}

.Text-footer2 {
  font-size: 20px;
  padding-right: 10px;
  content: '•';
  color: white;
}

.hr-style {
  max-width: 100%;
  height: 2px;
  background-color: #FFFFFF;
  margin-top: 180px;;
}
</style>
