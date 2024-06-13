
   <h1>deej: Mezclador de Volumen de Hardware</h1>

  <p>deej es un mezclador de volumen de hardware de código abierto para PC con Windows. Te permite usar controles deslizantes físicos (¡como un DJ!) para controlar sin problemas los volúmenes de diferentes aplicaciones (como tu reproductor de música, el juego que estás jugando y tu sesión de chat de voz) sin tener que detener lo que estás haciendo.</p>

   <p>Este proyecto está basado en <a href="https://github.com/omriharel/deej?tab=readme-ov-file">deej</a> y ha sido adaptado con varias modificaciones y mejoras personalizadas.</p>

   <h2>Características</h2>

  <ul>
        <li><strong>Cliente de escritorio liviano</strong>: Escrito en Go y distribuido como un ejecutable portátil (no necesita instalador).</li>
        <li><strong>Vinculación de aplicaciones a diferentes controles deslizantes</strong>: 
            <ul>
                <li>Vincula varias aplicaciones por control deslizante (por ejemplo, un control deslizante para todos tus juegos).</li>
                <li>Vincula el canal maestro.</li>
                <li>Vincula "sonidos del sistema".</li>
                <li>Vincula dispositivos de audio específicos por nombre.</li>
                <li>Vincula la aplicación actualmente activa.</li>
                <li>Vincula todas las demás aplicaciones no asignadas.</li>
            </ul>
        </li>
        <li><strong>Control del nivel de entrada del micrófono</strong>.</li>
        <li><strong>Consumo mínimo de recursos</strong>: El cliente consume alrededor de 10 MB de memoria.</li>
        <li><strong>Ejecución desde la bandeja del sistema</strong>.</li>
        <li><strong>Notificaciones útiles</strong> para avisarte si algo no funciona.</li>
   </ul>

   <h2>Cómo Funciona</h2>

  <h3>Hardware</h3>

  <ul>
        <li><strong>Controles deslizantes</strong>: Originalmente basados en potenciómetros de barra en el proyecto principal, se han adaptado a controles deslizantes tradicionales para mejorar la durabilidad y estabilidad.</li>
        <li><strong>Prototipo 1</strong>: Realizado para verificar el funcionamiento del concepto, sin soldaduras permanentes.
            <ul>
                 <li><strong>Esquema</strong>: 
                    <img src="https://github.com/MagoPato/custom-deej/blob/main/img/Esquema0.png?raw=true" alt="Esquema del Prototipo 2" style="max-width: 400px; height: auto;">
                </li>
                <li><strong>Prototipo Fisico</strong>: 
                    <img src="https://github.com/MagoPato/custom-deej/blob/main/img/prototipo1.png?raw=true" alt="Foto del Prototipo 2 con problemas de cables" style="max-width: 400px; height: auto;">
                </li>
          </ul>
        </li>
       <li><strong>Prototipo 2</strong>: Pensado inicialmente como el diseño final, pero problemas con el movimiento de los cables no soldados afectaron su funcionamiento a largo plazo.
           <ul>
             <li><strong>Esquema</strong>: 
                    <img src="https://github.com/MagoPato/custom-deej/blob/main/img/Esquema1.png?raw=true" alt="Esquema del Prototipo 1" style="max-width: 400px; height: auto;">
                </li>
                <li><strong>Prototipo Fisico</strong>: 
                    <img src="https://github.com/MagoPato/custom-deej/blob/main/img/prototipo2.png?raw=true" alt="Foto del Prototipo 1 sin soldaduras" style="max-width: 400px; height: auto;">
               </li>
            </ul>
        </li>
        <li><strong>Prototipo 3 (Definitivo)</strong>: Diseño finalizado con todas las conexiones soldadas para asegurar estabilidad y durabilidad a largo plazo.
            <ul>
                <li><strong>Esquema</strong>: 
                    <img src="https://github.com/MagoPato/custom-deej/blob/main/img/Esquema2.png?raw=true" style="max-width: 400px; height: auto;">
                </li>
                <li><strong>Prototipo Fisico</strong>: 
                    (Foto pendiente: Prototipo 3 aún no completado)
                </li>
            </ul>
        </li>
    </ul>

  <h3>Software</h3>
    
   <ul>
        <li><strong>Arduino</strong>: El código que se ejecuta en la placa Arduino es un programa en C que escribe constantemente los valores actuales del control deslizante a través de su interfaz serie.</li>
        <li><strong>Cliente en PC</strong>: La PC ejecuta un cliente Go liviano en segundo plano. Este cliente lee la transmisión en serie y ajusta los volúmenes de la aplicación de acuerdo con el archivo de configuración proporcionado.</li>
    </ul>

   <h3>Esquema del Proyecto Base</h3>

   <img src="https://github.com/omriharel/deej/raw/master/assets/schematic.png" alt="Esquema del proyecto deej original" style="max-width: 400px; height: auto;">

   <h2>Requisitos</h2>

   <ul>
        <li><strong>Windows</strong>: No se requieren requisitos adicionales.</li>
    </ul>
  <h2>Descarga e Instalación</h2>

   <ol>
        <li>Dirígete a la página de <a href="https://github.com/MagoPato/custom-deej/releases/tag/deejdeej_v0.9.10">lanzamientos</a> y descarga el archivo ejecutable y de configuración de la última versión (<code>deej.exe</code> y <code>config.yaml</code>).</li>
        <li>Colócalos en el mismo directorio en cualquier lugar de tu máquina.</li>
        <li>(Opcional, en Windows) Crea un acceso directo <code>deej.exe</code> y cópialo a <code>%APPDATA%\Microsoft\Windows\Start Menu\Programs\Startup</code> para que deej se ejecute en el arranque.</li>
    </ol>

  <h2>Agradecimientos</h2>

  <p>Estoy profundamente impresionado por el proyecto <a href="https://github.com/omriharel/deej?tab=readme-ov-file">deej</a> original y he encontrado una gran inspiración en su funcionalidad intuitiva y útil. Agradezco sinceramente a la comunidad y a los desarrolladores por su trabajo y contribución a la comunidad de código abierto.</p>
