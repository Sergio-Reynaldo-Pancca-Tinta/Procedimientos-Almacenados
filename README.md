<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infografía - Procedimientos Almacenados</title>
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #2ecc71;
            --warning: #f39c12;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a3a, #2c3e50);
            color: var(--light);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 30px 0;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: var(--light);
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }
        
        .authors {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 15px;
        }
        
        .author {
            background: rgba(52, 152, 219, 0.2);
            padding: 10px 20px;
            border-radius: 30px;
            font-size: 0.9rem;
        }
        
        .section {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .section-title {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--secondary);
            border-bottom: 2px solid var(--secondary);
            padding-bottom: 10px;
        }
        
        .highlight {
            color: var(--accent);
            font-weight: bold;
        }
        
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            transition: transform 0.3s, box-shadow 0.3s;
            border-left: 4px solid var(--secondary);
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .card-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .stats {
            display: flex;
            justify-content: space-around;
            margin: 30px 0;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .stat {
            text-align: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            min-width: 150px;
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--success);
            margin-bottom: 10px;
        }
        
        .stat-label {
            font-size: 0.9rem;
            color: var(--light);
        }
        
        .architecture {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin-top: 20px;
        }
        
        .table {
            background: rgba(255, 255, 255, 0.1);
            padding: 15px;
            border-radius: 10px;
            min-width: 200px;
            text-align: center;
        }
        
        .table-name {
            font-weight: bold;
            margin-bottom: 10px;
            color: var(--warning);
        }
        
        .procedure-list {
            columns: 2;
            column-gap: 20px;
        }
        
        .procedure-item {
            margin-bottom: 10px;
            padding-left: 20px;
            position: relative;
            break-inside: avoid;
        }
        
        .procedure-item:before {
            content: "▶";
            position: absolute;
            left: 0;
            color: var(--secondary);
        }
        
        .conclusion {
            background: rgba(46, 204, 113, 0.2);
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            border-left: 4px solid var(--success);
        }
        
        .recommendation {
            background: rgba(243, 156, 18, 0.2);
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            border-left: 4px solid var(--warning);
        }
        
        footer {
            text-align: center;
            padding: 30px 0;
            margin-top: 50px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .link {
            color: var(--secondary);
            text-decoration: none;
            font-weight: bold;
            margin-top: 10px;
            display: inline-block;
        }
        
        .link:hover {
            text-decoration: underline;
        }
        
        @media (max-width: 768px) {
            .cards, .procedure-list {
                grid-template-columns: 1fr;
                columns: 1;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Procedimientos Almacenados (Datacenter)</h1>
            <p class="subtitle">Implementación de 20 procedimientos almacenados en SQL Server para gestión académica</p>
            <div class="authors">
                <div class="author">C. Callo</div>
                <div class="author">S. Pancca</div>
            </div>
            <p>Universidad Andina del Cusco, Av. La Arapa, Cusco, Perú</p>
        </header>
        
        <div class="section">
            <h2 class="section-title">Resumen</h2>
            <p>Se implementaron <span class="highlight">20 procedimientos almacenados</span> sobre la base de datos Académico en SQL Server. Mediante <span class="highlight">CREATE PROCEDURE</span> y consultas <span class="highlight">JOIN, AVG y BETWEEN</span> se automatizaron operaciones de consulta, inserción, actualización y eliminación de alumnos, docentes, asignaturas y notas.</p>
            <p>Se lograron reportes clave: alumnos por carrera, docentes por carga, promedios, rangos de notas y estado de aprobación. La solución reduce código repetido, centraliza la lógica en el motor y sirve como capa de datos reusable para aplicaciones académicas.</p>
            
            <div class="stats">
                <div class="stat">
                    <div class="stat-number">20</div>
                    <div class="stat-label">Procedimientos Implementados</div>
                </div>
                <div class="stat">
                    <div class="stat-number">6</div>
                    <div class="stat-label">Tablas Principales</div>
                </div>
                <div class="stat">
                    <div class="stat-number">4</div>
                    <div class="stat-label">Tipos de Operaciones</div>
                </div>
                <div class="stat">
                    <div class="stat-number">100%</div>
                    <div class="stat-label">Objetivos Cumplidos</div>
                </div>
            </div>
        </div>
        
        <div class="section">
            <h2 class="section-title">Arquitectura de la Base de Datos</h2>
            <p>Se diseñó un esquema de base de datos relacional que comprende seis tablas principales interconectadas mediante relaciones de integridad referencial.</p>
            
            <div class="architecture">
                <div class="table">
                    <div class="table-name">TCarrera</div>
                    <div>Gestión de programas académicos</div>
                </div>
                <div class="table">
                    <div class="table-name">TUsuario</div>
                    <div>Control de acceso y autenticación</div>
                </div>
                <div class="table">
                    <div class="table-name">TAlumno</div>
                    <div>Información estudiantil con vinculación curricular</div>
                </div>
                <div class="table">
                    <div class="table-name">TAsignatura</div>
                    <div>Plan de estudios con prerrequisitos</div>
                </div>
                <div class="table">
                    <div class="table-name">TDocente</div>
                    <div>Recursos humanos académicos</div>
                </div>
                <div class="table">
                    <div class="table-name">TCarga</div>
                    <div>Asignación docente-asignatura</div>
                </div>
                <div class="table">
                    <div class="table-name">TNotas</div>
                    <div>Registro evaluativo estudiantil</div>
                </div>
            </div>
        </div>
        
        <div class="section">
            <h2 class="section-title">Procedimientos Implementados</h2>
            
            <div class="cards">
                <div class="card">
                    <h3 class="card-title">Consultas Básicas</h3>
                    <ul class="procedure-list">
                        <li class="procedure-item">p_ObtenerAlumnosPorCarrera</li>
                        <li class="procedure-item">p_ObtenerAsignaturasPorDocenteSemestre</li>
                        <li class="procedure-item">p_ObtenerNotasAlumnoAsignatura</li>
                        <li class="procedure-item">p_ObtenerNombreCompletoAlumno</li>
                        <li class="procedure-item">p_ListarAlumnosConCarrera</li>
                    </ul>
                </div>
                
                <div class="card">
                    <h3 class="card-title">Gestión Académica</h3>
                    <ul class="procedure-list">
                        <li class="procedure-item">ActualizarNotaFinal</li>
                        <li class="procedure-item">InsertarNuevaCarga</li>
                        <li class="procedure-item">EliminarAlumnoConNotas</li>
                        <li class="procedure-item">p_ObtenerPromedioNotasAlumnoSemestre</li>
                        <li class="procedure-item">p_ObtenerAlumnosPorAsignaturaSemestre</li>
                    </ul>
                </div>
                
                <div class="card">
                    <h3 class="card-title">Análisis Avanzados</h3>
                    <ul class="procedure-list">
                        <li class="procedure-item">ObtenerAlumnosNotasSuperioresPromedio</li>
                        <li class="procedure-item">ListarAlumnosAsignaturasAprobadasDesaprobadas</li>
                        <li class="procedure-item">ObtenerAlumnosPorRangoNotas</li>
                        <li class="procedure-item">CalcularPromedioNotasPorCarrera</li>
                        <li class="procedure-item">ListarDocentesPorNumeroAsignaturas</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <div class="section">
            <h2 class="section-title">Resultados y Conclusiones</h2>
            
            <div class="conclusion">
                <h3>Logros Principales</h3>
                <p>La implementación de procedimientos almacenados en el Datacenter de la EPIS ha demostrado ser altamente efectiva, logrando automatizar veinte procesos críticos de gestión académica que mejoran significativamente la eficiencia operativa y consistencia de datos.</p>
                <p>El proyecto cumplió integralmente con todos los objetivos establecidos, destacándose la correcta implementación de parámetros de entrada/salida, lógica de control de flujo y manejo robusto de errores, estableciendo así las bases para un sistema académico escalable y mantenible que optimiza los recursos institucionales.</p>
            </div>
            
            <div class="recommendation">
                <h3>Recomendaciones Futuras</h3>
                <p>Para futuras mejoras, se recomienda expandir la suite con:</p>
                <ul>
                    <li>Triggers de auditoría automática</li>
                    <li>Procedimientos de reportes estadísticos avanzados</li>
                    <li>Sistema de permisos granular basado en roles</li>
                    <li>APIs REST para integración web</li>
                    <li>Mecanismos de logging para monitoreo</li>
                    <li>Procedimientos de mantenimiento automatizado</li>
                    <li>Optimización de índices estratégicos</li>
                </ul>
            </div>
        </div>
        
        <footer>
            <p>Universidad Andina del Cusco - EPIS</p>
            <p>Base de Datos Académica BDacademicoLosDog1</p>
            <a href="https://sergio-reynaldo-pancca-tinta.github.io/Procedimientos-Almacenados/" class="link">Ver Infografía Completa</a>
        </footer>
    </div>
</body>
</html>
