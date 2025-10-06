# Procedimientos-Almacenados
Procedimientos Almacenados (Datacenter)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infografía - Procedimientos Almacenados EPIS</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .header {
            text-align: center;
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            margin-bottom: 30px;
        }

        .university {
            color: #2c3e50;
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .faculty {
            color: #34495e;
            font-size: 18px;
            margin-bottom: 20px;
        }

        .title {
            color: #e74c3c;
            font-size: 32px;
            font-weight: bold;
            margin-bottom: 15px;
        }

        .team-section {
            display: flex;
            justify-content: space-around;
            margin-top: 20px;
        }

        .team {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 10px;
            text-align: center;
        }

        .team-name {
            color: #e74c3c;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .card {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card-title {
            color: #2c3e50;
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 15px;
            border-bottom: 3px solid #3498db;
            padding-bottom: 10px;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin-top: 20px;
        }

        .stat-item {
            text-align: center;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 10px;
        }

        .stat-number {
            font-size: 28px;
            font-weight: bold;
            color: #e74c3c;
        }

        .stat-label {
            font-size: 14px;
            color: #7f8c8d;
            margin-top: 5px;
        }

        .procedure-list {
            list-style: none;
        }

        .procedure-item {
            padding: 10px;
            margin: 8px 0;
            background: #ecf0f1;
            border-radius: 8px;
            border-left: 4px solid #3498db;
        }

        .procedure-category {
            background: #34495e;
            color: white;
            padding: 12px;
            border-radius: 8px;
            margin: 15px 0 10px 0;
            font-weight: bold;
        }

        .database-structure {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 15px;
        }

        .table-card {
            background: #ecf0f1;
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            border: 2px solid #bdc3c7;
        }

        .table-name {
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 8px;
        }

        .table-desc {
            font-size: 12px;
            color: #7f8c8d;
        }

        .highlight {
            background: linear-gradient(120deg, #a8edea 0%, #fed6e3 100%);
            padding: 20px;
            border-radius: 15px;
            margin: 20px 0;
        }

        .footer {
            text-align: center;
            background: white;
            padding: 20px;
            border-radius: 15px;
            margin-top: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        @media (max-width: 768px) {
            .grid-container {
                grid-template-columns: 1fr;
            }
            
            .stats {
                grid-template-columns: 1fr;
            }
            
            .team-section {
                flex-direction: column;
                gap: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="university">UNIVERSIDAD ANDINA DEL CUSCO</div>
            <div class="faculty">FACULTAD DE INGENIERÍA Y ARQUITECTURA</div>
            <div class="title">Sistema de Procedimientos Almacenados</div>
            <div class="team-section">
                <div class="team">
                    <div class="team-name">EQUIPO: LOS DOGS</div>
                    <div>Callo Gastañaga Carlos Eduardo</div>
                    <div>Pancca Tinta Sergio Reynaldo</div>
                </div>
                <div class="team">
                    <div class="team-name">CURSO</div>
                    <div>Modelado de Base de Datos</div>
                    <div>Docente: Hugo Espetia Huamanga</div>
                </div>
            </div>
        </div>

        <!-- Estadísticas Principales -->
        <div class="grid-container">
            <div class="card">
                <div class="card-title">📊 Resumen del Proyecto</div>
                <div class="stats">
                    <div class="stat-item">
                        <div class="stat-number">20</div>
                        <div class="stat-label">Procedimientos Implementados</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">6</div>
                        <div class="stat-label">Tablas de Base de Datos</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">30</div>
                        <div class="stat-label">Alumnos Registrados</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">21</div>
                        <div class="stat-label">Asignaturas Creadas</div>
                    </div>
                </div>
            </div>

            <div class="card">
                <div class="card-title">🏗️ Estructura de Base de Datos</div>
                <div class="database-structure">
                    <div class="table-card">
                        <div class="table-name">TCarrera</div>
                        <div class="table-desc">Programas académicos</div>
                    </div>
                    <div class="table-card">
                        <div class="table-name">TAlumno</div>
                        <div class="table-desc">Información estudiantil</div>
                    </div>
                    <div class="table-card">
                        <div class="table-name">TAsignatura</div>
                        <div class="table-desc">Plan de estudios</div>
                    </div>
                    <div class="table-card">
                        <div class="table-name">TNotas</div>
                        <div class="table-desc">Registro evaluativo</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Categorías de Procedimientos -->
        <div class="grid-container">
            <div class="card">
                <div class="card-title">🔍 Procedimientos de Consulta</div>
                <ul class="procedure-list">
                    <li class="procedure-item">p_ObtenerAlumnosPorCarrera</li>
                    <li class="procedure-item">p_ObtenerNotasAlumnoAsignatura</li>
                    <li class="procedure-item">p_ObtenerPromedioNotasAlumnoSemestre</li>
                    <li class="procedure-item">p_ListarAlumnosConCarrera</li>
                </ul>
            </div>

            <div class="card">
                <div class="card-title">⚙️ Procedimientos de Gestión</div>
                <ul class="procedure-list">
                    <li class="procedure-item">ActualizarNotaFinal</li>
                    <li class="procedure-item">InsertarNuevaCarga</li>
                    <li class="procedure-item">EliminarAlumnoConNotas</li>
                    <li class="procedure-item">ListarDocentesPorNumeroAsignaturas</li>
                </ul>
            </div>

            <div class="card">
                <div class="card-title">📈 Procedimientos Analíticos</div>
                <ul class="procedure-list">
                    <li class="procedure-item">ObtenerAlumnosNotasSuperioresPromedio</li>
                    <li class="procedure-item">CalcularPromedioNotasPorCarrera</li>
                    <li class="procedure-item">ListarAlumnosAsignaturasAprobadasDesaprobadas</li>
                    <li class="procedure-item">ObtenerAlumnosPorRangoNotas</li>
                </ul>
            </div>
        </div>

        <!-- Características Destacadas -->
        <div class="card">
            <div class="card-title">🚀 Características Técnicas</div>
            <div class="highlight">
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px;">
                    <div>
                        <h4>🛡️ Seguridad</h4>
                        <p>Encapsulación de lógica empresarial</p>
                    </div>
                    <div>
                        <h4>⚡ Rendimiento</h4>
                        <p>Consultas optimizadas con JOINs eficientes</p>
                    </div>
                    <div>
                        <h4>🔧 Mantenibilidad</h4>
                        <p>Código modular y reutilizable</p>
                    </div>
                    <div>
                        <h4>🎯 Control de Errores</h4>
                        <p>Manejo de transacciones con TRY-CATCH</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <div style="font-size: 18px; font-weight: bold; color: #2c3e50; margin-bottom: 10px;">
                Sistema de Gestión Académica - Datacenter EPIS
            </div>
            <div style="color: #7f8c8d;">
                Universidad Andina del Cusco • 2025 • Todos los derechos reservados
            </div>
        </div>
    </div>

    <script>
        // Efectos interactivos simples
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.card');
            
            cards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.boxShadow = '0 10px 25px rgba(0,0,0,0.15)';
                });
                
                card.addEventListener('mouseleave', function() {
                    this.style.boxShadow = '0 5px 15px rgba(0,0,0,0.1)';
                });
            });

            // Contador animado para las estadísticas
            const statNumbers = document.querySelectorAll('.stat-number');
            
            statNumbers.forEach(stat => {
                const target = parseInt(stat.textContent);
                let current = 0;
                const increment = target / 50;
                
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        stat.textContent = target;
                        clearInterval(timer);
                    } else {
                        stat.textContent = Math.floor(current);
                    }
                }, 50);
            });
        });
    </script>
</body>
</html>
