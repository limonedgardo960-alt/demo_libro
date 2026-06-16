<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Historia Una Vida - Autobiografía</title>
    <style>
        /* Importación de tipografías premium para replicar el diseño */
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;700&family=Orbitron:wght@700&display=swap');

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: #000000; /* Fondo negro absoluto */
            color: #ffffff;
            font-family: 'Montserrat', sans-serif;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            overflow-x: hidden;
        }

        /* Contenedor de Contenido */
        .main-container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 60px 24px;
            width: 100%;
        }

        /* Cintillo Superior Naranja */
        .edition-badge {
            font-family: 'Montserrat', sans-serif;
            text-transform: uppercase;
            font-size: 13px;
            letter-spacing: 6px;
            color: #FF5A2B; /* Naranja vibrante de la imagen original */
            font-weight: 500;
            margin-bottom: 35px;
        }

        /* Título Principal con tipografía geométrica estilizada */
        .main-title {
            font-family: 'Orbitron', sans-serif;
            font-size: clamp(38px, 6.5vw, 76px);
            font-weight: 700;
            line-height: 1.1;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 45px;
        }

        .main-title span {
            display: block;
        }

        /* Reseña / Narrativa Central */
        .narrative-text {
            font-size: clamp(16px, 2.2vw, 21px);
            line-height: 1.5;
            font-weight: 400;
            max-width: 780px;
            margin-bottom: 70px;
            color: #FFFFFF;
        }

        /* Zona de Galería / Mockups Visuales */
        .showcase-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            align-items: flex-end;
            margin-bottom: 40px;
        }

        @media (max-width: 768px) {
            .showcase-grid {
                grid-template-columns: 1fr;
                gap: 50px;
                justify-items: center;
            }
        }

        /* Estilización CSS pura de los elementos del libro */
        .showcase-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
        }

        /* 1. Portada del Libro (Izquierda) */
        .book-mockup-closed {
            width: 210px;
            height: 300px;
            background-color: #F4F1EA;
            color: #1A1A1A;
            padding: 30px 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.6), inset -6px 0 12px rgba(0,0,0,0.08);
            border-radius: 2px 6px 6px 2px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            text-align: center;
        }

        .book-mockup-closed .author {
            font-size: 11px;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        .book-mockup-closed .title {
            font-size: 19px;
            letter-spacing: 5px;
            font-weight: 700;
            color: #8B7355;
            margin: 10px 0;
        }

        .book-mockup-closed .subtitle {
            font-size: 8px;
            letter-spacing: 2px;
            text-transform: uppercase;
            opacity: 0.6;
        }

        .book-mockup-closed .badge-chapter {
            font-size: 12px;
            letter-spacing: 1px;
            color: #FFFFFF;
            background-color: #D1C7BD;
            padding: 5px 14px;
            border-radius: 2px;
            text-transform: uppercase;
            margin-top: auto;
        }

        /* 2. Páginas del Libro Abierto (Centro) */
        .book-mockup-open {
            width: 300px;
            height: 240px;
            background: linear-gradient(90deg, #EBE7DF 0%, #F5F2EB 47%, #D0C9BE 50%, #F5F2EB 53%, #EBE7DF 100%);
            box-shadow: 0 20px 40px rgba(0,0,0,0.7);
            border-radius: 4px;
            position: relative;
            padding: 20px;
            display: flex;
            justify-content: space-between;
        }

        .book-mockup-open::before {
            content: "GALERÍA";
            position: absolute;
            top: 45%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-6deg);
            color: rgba(255, 90, 43, 0.85);
            font-size: 18px;
            font-weight: 700;
            letter-spacing: 5px;
            border: 2px solid rgba(255, 90, 43, 0.85);
            padding: 5px 14px;
            z-index: 10;
        }

        .book-mockup-open .page {
            width: 45%;
            font-size: 5px;
            color: #555555;
            line-height: 1.6;
            text-align: justify;
            overflow: hidden;
            opacity: 0.8;
        }

        /* 3. Cuaderno del Autor (Derecha) */
        .book-mockup-author {
            width: 220px;
            height: 280px;
            background-color: #333333;
            color: #ffffff;
            box-shadow: 0 20px 40px rgba(0,0,0,0.6);
            border-radius: 4px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-transform: uppercase;
            font-family: 'Montserrat', sans-serif;
            font-size: 13px;
            letter-spacing: 4px;
            font-weight: 700;
            transform: rotate(6deg);
            border-left: 3px solid #222;
        }

        /* Barra de Datos Inferior (Full-Bleed) */
        .info-footer-banner {
            background-color: #FF5A2B; /* Color naranja exacto */
            color: #000000;
            width: 100%;
            padding: 35px 24px;
        }

        .info-footer-grid {
            max-width: 1100px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        @media (max-width: 600px) {
            .info-footer-grid {
                grid-template-columns: 1fr;
                gap: 25px;
                text-align: center;
            }
        }

        .info-column {
            display: flex;
            flex-direction: column;
        }

        .info-column .accent-title {
            font-size: 19px;
            font-weight: 700;
            line-height: 1.2;
        }

        .info-column .sub-text {
            font-size: 16px;
            font-weight: 400;
            margin-top: 1px;
        }
    </style>
</head>
<body>

    <div class="main-container">
        <div class="edition-badge">Autobiografía · Edición Especial</div>
        
        <h1 class="main-title">
            <span>Mi Historia</span>
            <span>Una Vida</span>
        </h1>
        
        <p class="narrative-text">
            Una narrativa íntima y poderosa sobre los momentos que definen quiénes somos y en quiénes nos convertimos.
        </p>

        <div class="showcase-grid">
            
            <div class="showcase-item">
                <div class="book-mockup-closed">
                    <div class="author">Lerve Oways</div>
                    <div class="title">DIEIGYRE</div>
                    <div class="subtitle">Whein This Voe<br>LCO</div>
                    <div class="badge-chapter">Capítulo I</div>
                </div>
            </div>

            <div class="showcase-item">
                <div class="book-mockup-open">
                    <div class="page">
                        <strong>TREATS</strong><br><br>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin elementum id lectus nec vestibulum. Aliquam nec finibus diam. Vivamus imperdiet, tellus vitae scelerisque elementum.
                    </div>
                    <div class="page">
                        <br><br>
                        Nulla de facilisi. In hac habitasse platea dictumst. Sed ac feugiat sem. Nunc placerat ex sit amet vulputate tempor. Ut sodales purus id erat bibendum, nec feugiat sapien.
                    </div>
                </div>
            </div>

            <div class="showcase-item">
                <div class="book-mockup-author">
                    El Autor
                </div>
            </div>

        </div>
    </div>

    <footer class="info-footer-banner">
        <div class="info-footer-grid">
            <div class="info-column">
                <span class="accent-title">Disponible en</span>
                <span class="sub-text">librería selecta</span>
            </div>
            <div class="info-column">
                <span class="accent-title">Edición limitada</span>
                <span class="sub-text">numerada y firmada</span>
            </div>
            <div class="info-column">
                <span class="accent-title">320 páginas</span>
                <span class="sub-text">Tapa dura</span>
            </div>
        </div>
    </footer>

</body>
</html>
