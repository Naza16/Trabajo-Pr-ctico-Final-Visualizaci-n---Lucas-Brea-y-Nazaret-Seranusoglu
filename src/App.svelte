<script>
  import * as d3 from "d3";
  import { writable, derived } from "svelte/store";
  import { LayerCake, Svg } from "layercake";

  import Line from "./_components/Line.svelte";
  import Area from "./_components/Area.svelte";
  import AxisX from "./_components/AxisX.svelte";
  import AxisY from "./_components/AxisY.svelte";


  import data from "./_data/points.csv";

  const xKey = "myX";
  const yKey = "myY";

  let year = writable(2015);

  const filteredData = derived(year, $year => {
    return data.filter(d => d[xKey] <= $year);
  });
/*
  document.addEventListener("DOMContentLoaded", () => {
    const mainContent = document.getElementById("mainContent");
    const backgroundImages = [
      "url('images/F35.jpg')",
      "url('images/F22.jpg.wepp')",
      "url('images/F15.jpg.wepp')",
      // Agrega más imágenes según sea necesario
    ];

    window.addEventListener("scroll", () => {
      const scrollPosition = window.scrollY;
      const windowHeight = window.innerHeight;
      const docHeight = document.documentElement.scrollHeight;
      const scrollFraction = scrollPosition / (docHeight - windowHeight);
      const imageIndex = Math.floor(scrollFraction * backgroundImages.length);

      mainContent.style.backgroundImage = backgroundImages[imageIndex];
    });
  });
*/
</script>
<main id>
  <div class="header">
    Una guía visual a
  </div>
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
      min="1992"
      max="2022"
      step="1"
      bind:value={$year}
    />
    <span class="counter-container"><i>Cantidad de Dinero utilizado para el gasto militar durante el año: </i> <b>{$year}</b></span>
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
</main>

<style>
  main {
    position: relative;
    z-index: 1;
    color: white;
    text-shadow: 0 0 5px black;
  }

  .header {
    font-size: 35px;
    font-family: Helvetica;
    text-align: center;
    margin-bottom: 20px; 
  }

  .bajada {
    font-size: 35px;
    font-weight: normal;
    text-align: center;
    font-family: Helvetica;
    margin-bottom: 20px; 
  }

  .headline2{
    font-size: 55px;
    -webkit-background-clip: text;
    background-clip: text;
    border-radius: 8px;
    text-align: center;
    position: relative;
    font-family:Helvetica;
    padding-bottom: 10%;
  }

  .headline3{
    font-size: 55px;
    -webkit-background-clip: text;
    background-clip: text;
    border-radius: 8px;
    text-align: center;
    position: relative;
    font-family:Helvetica;
  }

  .headline {
    font-size: 65px;
    background: radial-gradient(circle, red, rgb(255, 175, 90));
    -webkit-background-clip: text;
    background-clip: text;
    border-radius: 8px;
    text-align: center;
    position: relative;
    color: transparent;
    animation: fuego 5s alternate-reverse infinite; 
    font-family:Helvetica;
    background-size: 200% 200%;
  }
  @keyframes fuego {
    0% {
      background-position:  100% 100%;
    }
    100% {
      background-position: 0% 0%;
    }
  }

  .ImagenesContainer{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
    margin-right: -200px;
    padding-bottom: 5%;
  }

  .ImagenesLideres1, .ImagenesLideres2{
    display: block;
    height: auto;
    max-width: 100%;
  }

  .Ucrania{
    background: radial-gradient(circle, rgb(0, 191, 255), rgb(255, 255, 0));
    background-clip: text;
    color: transparent;
    animation: ucrania 2s alternate-reverse infinite;
    background-size: 200% 200%;
  }

  @keyframes ucrania {
    0% {
      background-position: 100% 100%;
    }
    100% {
      background-position: 0% 0%;
    }
  }

  .Rusia{
    background: radial-gradient(circle, red, rgb(0, 0, 255), rgb(255, 255, 255));
    background-clip: text;
    color: transparent;
    animation: rusia 8s alternate-reverse infinite;
    background-size: 200% 200%;
  }

  @keyframes rusia {
    0% {
      background-position: 0% 0%;
    }
    50%{
      background-position: 100% 100%;
    }
    75% {
      background-position: 0% 0%;
    }
  }

  .Texto {
    font-size: 25px;
    font-weight: normal;
    font-family: Helvetica;
    justify-content: center;
    text-align:start;
  }

  .Texto2 {
    font-size: 25px;
    font-weight: normal;
    font-family: Helvetica;
    padding-bottom: 5%;
    justify-content: center;
    text-align: start;
  }
  
  .headline b {
    display: block;
  }

  .chart-container {
    width: 100%;
    height: 500px;
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
</style>
