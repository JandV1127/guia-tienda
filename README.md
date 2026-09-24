{% extends "layout_base.html" %}

{% block title %}NYJ System | Soluciones Corporativas de Gestión{% endblock %}

<nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top shadow">
    <div class="container">

        <a class="navbar-brand fw-bold" href="#">
            NYJ SYSTEM
        </a>

        <button class="navbar-toggler"
                data-bs-toggle="collapse"
                data-bs-target="#menu">
            <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="menu">

            <ul class="navbar-nav ms-auto">

                <li class="nav-item">
                    <a class="nav-link" href="#inicio">Inicio</a>
                </li>

                <li class="nav-item">
                    <a class="nav-link" href="#soluciones">Soluciones</a>
                </li>

                <li class="nav-item">
                    <a class="nav-link" href="#modulos">Módulos</a>
                </li>

                <li class="nav-item">
                    <a class="nav-link" href="#contacto">Contacto</a>
                </li>

            </ul>

            <a href="{{ url_for('login') }}"
               class="btn btn-primary ms-3">
               Iniciar Sesión
            </a>

        </div>
    </div>
</nav>

{% block content %}
<div class="container-fluid p-0">
    
    <div class="bg-dark text-white text-center py-5 position-relative overflow-hidden" style="min-height: 500px; display: flex; align-items: center;">
        <div class="container position-relative z-index-1">
            <span class="badge bg-primary px-3 py-2 mb-3 rounded-pill text-uppercase tracking-wide">Innovación en Gestión</span>
            <h1 class="display-2 fw-bolder mb-4">El cerebro operativo <br><span class="text-primary">de tu empresa</span></h1>
            <p class="lead mb-5 opacity-75 mx-auto" style="max-width: 600px;">Transformamos la complejidad logística en una ventaja competitiva. Control total, datos precisos y escalabilidad real.</p>
            <div class="d-flex justify-content-center gap-3">
                <a href="{{ url_for('login') }}" class="btn btn-primary btn-lg px-5 py-3 rounded-pill shadow-blue">Acceder al Sistema</a>
                <a href="#"
   class="btn btn-outline-light btn-lg px-5 py-3 rounded-pill"
   data-bs-toggle="modal"
   data-bs-target="#demoModal">
    Ver Demo Técnica
</a>
            </div>
        </div>
    </div>

    <div class="container py-5">
        <div class="text-center mb-5">
            <h2 class="fw-bold fs-1">Nuestra Propuesta de Valor</h2>
            <div class="mx-auto bg-primary mt-3" style="width: 80px; height: 4px;"></div>
        </div>

        <div class="row g-4">
            {% for title, icon, desc, color in [
                ('Gestión de Inventarios', 'bi-box-seam', 'Optimización algorítmica de stocks para evitar quiebres y sobrecostos.', 'text-primary'),
                ('Inteligencia de Ventas', 'bi-graph-up-arrow', 'Dashboard ejecutivo con métricas de rendimiento en tiempo real.', 'text-success'),
                ('Arquitectura Segura', 'bi-shield-check', 'Protocolos de cifrado avanzado para proteger tus activos digitales.', 'text-warning'),
                ('Soporte 360°', 'bi-headset', 'Asistencia técnica dedicada para garantizar la continuidad operativa.', 'text-info')
            ] %}
            <div class="col-md-3">
                <div class="card h-100 border-0 shadow-sm p-4 rounded-4 hover-lift">
                    <i class="bi {{ icon }} {{ color }} fs-1 mb-3"></i>
                    <h5 class="fw-bold">{{ title }}</h5>
                    <p class="text-muted small lh-base">{{ desc }}</p>
                </div>
            </div>
            {% endfor %}
        </div>
    </div>

    <div class="py-5 bg-primary text-white text-center">
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <h2 class="display-4 fw-bold">+500</h2>
                    <p class="text-uppercase tracking-wide">Comercios Digitalizados</p>
                </div>
                <div class="col-md-4">
                    <h2 class="display-4 fw-bold">99.9%</h2>
                    <p class="text-uppercase tracking-wide">Tiempo de Disponibilidad</p>
                </div>
                <div class="col-md-4">
                    <h2 class="display-4 fw-bold">+1M</h2>
                    <p class="text-uppercase tracking-wide">Transacciones Seguras</p>
                </div>
            </div>
        </div>
    </div>

    <!-- BANNER CORPORATIVO -->
<div class="container my-5">

    <div class="card border-0 shadow-lg overflow-hidden rounded-4">

        <div class="row g-0 align-items-center">

            <div class="col-lg-7 p-5">

                <span class="badge bg-primary px-3 py-2 mb-3">
                    SOFTWARE EMPRESARIAL
                </span>

                <h2 class="fw-bold display-5">
                    Administra tu negocio
                    <span class="text-primary">
                        de forma inteligente
                    </span>
                </h2>

                <p class="lead text-muted mt-3">
                    NYJ System integra ventas, inventario,
                    clientes, proveedores, reportes financieros,
                    promociones y soporte técnico en una sola plataforma.
                </p>

                <div class="row mt-4">

                    <div class="col-md-6 mb-3">
                        <div class="d-flex align-items-center">
                            <i class="bi bi-check-circle-fill text-success fs-4 me-2"></i>
                            Gestión de Ventas
                        </div>
                    </div>

                    <div class="col-md-6 mb-3">
                        <div class="d-flex align-items-center">
                            <i class="bi bi-check-circle-fill text-success fs-4 me-2"></i>
                            Inventario Inteligente
                        </div>
                    </div>

                    <div class="col-md-6 mb-3">
                        <div class="d-flex align-items-center">
                            <i class="bi bi-check-circle-fill text-success fs-4 me-2"></i>
                            Clientes y Proveedores
                        </div>
                    </div>

                    <div class="col-md-6 mb-3">
                        <div class="d-flex align-items-center">
                            <i class="bi bi-check-circle-fill text-success fs-4 me-2"></i>
                            Reportes en Tiempo Real
                        </div>
                    </div>

                </div>

                <a href="{{ url_for('login') }}"
                   class="btn btn-primary btn-lg rounded-pill px-5 mt-3">

                    <i class="bi bi-rocket-takeoff-fill"></i>
                    Probar NYJ System

                </a>

            </div>

            <div class="col-lg-5 text-center bg-light p-4">

                <img src="{{ url_for('static', filename='img/publicidad_nyj.png') }}"
                     class="img-fluid rounded-4 shadow"
                     alt="NYJ System">

            </div>

        </div>

    </div>

</div>

    <div class="py-5 text-center">
        <div class="container py-5">
            <h2 class="display-4 fw-bold mb-3">¿Listo para llevar tu gestión al siguiente nivel?</h2>
            <p class="lead text-muted mb-5">Nuestra infraestructura está lista para escalar contigo.</p>
            <a href="#"
   class="btn btn-dark btn-lg px-5 py-3 rounded-pill shadow-lg"
   data-bs-toggle="modal"
   data-bs-target="#consultoriaModal">
    Solicitar consultoría
</a>
    </div>
</div>

<!-- Modal Demo Técnica -->
<div class="modal fade" id="demoModal" tabindex="-1" aria-labelledby="demoModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-xl modal-dialog-centered">
        <div class="modal-content border-0 shadow-lg rounded-4">

            <div class="modal-header bg-primary text-white">
                <h4 class="modal-title fw-bold" id="demoModalLabel">
                    🚀 Demo Técnica - NYJ System
                </h4>

                <button type="button"
                        class="btn-close btn-close-white"
                        data-bs-dismiss="modal"
                        aria-label="Cerrar">
                </button>
            </div>

            <div class="modal-body p-4">

                <div class="row g-4">

                    <div class="col-md-6">
                        <div class="card border-0 shadow-sm h-100">
                            <div class="card-body">
                                <h5 class="fw-bold text-primary">📦 Gestión de Inventario</h5>
                                <p class="text-muted">
                                    Control inteligente de stock con actualización automática después de cada venta.
                                </p>
                            </div>
                        </div>
                    </div>

                    <div class="col-md-6">
                        <div class="card border-0 shadow-sm h-100">
                            <div class="card-body">
                                <h5 class="fw-bold text-success">💰 Ventas y Facturación</h5>
                                <p class="text-muted">
                                    Registro rápido de ventas, cálculo de descuentos y generación automática de comprobantes.
                                </p>
                            </div>
                        </div>
                    </div>

                    <div class="col-md-6">
                        <div class="card border-0 shadow-sm h-100">
                            <div class="card-body">
                                <h5 class="fw-bold text-warning">👥 Gestión de Clientes</h5>
                                <p class="text-muted">
                                    Historial de compras, datos de contacto y seguimiento de clientes.
                                </p>
                            </div>
                        </div>
                    </div>

                    <div class="col-md-6">
                        <div class="card border-0 shadow-sm h-100">
                            <div class="card-body">
                                <h5 class="fw-bold text-info">📊 Panel Ejecutivo</h5>
                                <p class="text-muted">
                                    Métricas empresariales en tiempo real, reportes y análisis de rendimiento.
                                </p>
                            </div>
                        </div>
                    </div>

                </div>

                <hr class="my-4">

                <div class="text-center">
                    <h4 class="fw-bold mb-3">🔐 Tecnología Implementada</h4>

                    <div class="d-flex flex-wrap justify-content-center gap-2">
                        <span class="badge bg-primary p-2">Python</span>
                        <span class="badge bg-success p-2">Flask</span>
                        <span class="badge bg-warning text-dark p-2">MySQL</span>
                        <span class="badge bg-info text-dark p-2">Bootstrap 5</span>
                        <span class="badge bg-danger p-2">Flask-Login</span>
                        <span class="badge bg-dark p-2">Bcrypt</span>
                    </div>
                </div>

                <div class="alert alert-primary mt-4 text-center">
                    <strong>NYJ System</strong> integra inventarios, ventas,
                    clientes, promociones, reportes financieros y seguridad
                    empresarial en una sola plataforma.
                </div>

            </div>

            <div class="modal-footer">
                <button type="button"
                        class="btn btn-secondary"
                        data-bs-dismiss="modal">
                    Cerrar
                </button>

                <a href="{{ url_for('login') }}"
                   class="btn btn-primary">
                    Acceder al Sistema
                </a>
            </div>

        </div>
    </div>
</div>

<!-- Modal Solicitud de Consultoría -->
<div class="modal fade" id="consultoriaModal" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog modal-lg modal-dialog-centered">
        <div class="modal-content border-0 shadow-lg rounded-4">

            <div class="modal-header bg-dark text-white">
                <h4 class="modal-title">
                    📋 Solicitud de Consultoría
                </h4>

                <button type="button"
                        class="btn-close btn-close-white"
                        data-bs-dismiss="modal">
                </button>
            </div>

            <div class="modal-body">

                <form id="formConsultoria">

                    <div class="row">

                        <div class="col-md-6 mb-3">
                            <label class="form-label">Nombre Completo</label>
                            <input type="text"
                                   class="form-control"
                                   id="nombreConsultoria"
                                   required>
                        </div>

                        <div class="col-md-6 mb-3">
                            <label class="form-label">Empresa</label>
                            <input type="text"
                                   class="form-control"
                                   id="empresaConsultoria">
                        </div>

                    </div>

                    <div class="row">

                        <div class="col-md-6 mb-3">
                            <label class="form-label">Correo Electrónico</label>
                            <input type="email"
                                   class="form-control"
                                   id="correoConsultoria"
                                   required>
                        </div>

                        <div class="col-md-6 mb-3">
                            <label class="form-label">Teléfono</label>
                            <input type="text"
                                   class="form-control"
                                   id="telefonoConsultoria"
                                   required>
                        </div>

                    </div>

                    <div class="mb-3">
                        <label class="form-label">Mensaje</label>
                        <textarea class="form-control"
                                  id="mensajeConsultoria"
                                  rows="4"
                                  placeholder="Describa brevemente su necesidad o proyecto..."
                                  required></textarea>
                    </div>

                </form>

                <div class="alert alert-info">
                    Un asesor de NYJ System se pondrá en contacto con usted para analizar sus necesidades y proponer la mejor solución tecnológica.
                </div>

            </div>

            <div class="modal-footer">

                <button type="button"
                        class="btn btn-secondary"
                        data-bs-dismiss="modal">
                    Cancelar
                </button>

                <button type="button"
                        class="btn btn-success"
                        onclick="enviarConsultoria()">
                    <i class="bi bi-send-fill"></i>
                    Enviar Solicitud
                </button>

            </div>

        </div>
    </div>
</div>

<script>
function enviarConsultoria() {

    let nombre = document.getElementById("nombreConsultoria").value;
    let empresa = document.getElementById("empresaConsultoria").value;
    let correo = document.getElementById("correoConsultoria").value;
    let telefono = document.getElementById("telefonoConsultoria").value;
    let mensaje = document.getElementById("mensajeConsultoria").value;

    if (!nombre || !correo || !telefono || !mensaje) {
        alert("Por favor complete todos los campos obligatorios.");
        return;
    }

    let texto =
`📋 NUEVA SOLICITUD DE CONSULTORÍA

👤 Nombre: ${nombre}
🏢 Empresa: ${empresa}
📧 Correo: ${correo}
📱 Teléfono: ${telefono}

📝 Mensaje:
${mensaje}`;

    let numero = "573015651473"; // CAMBIAR POR TU NÚMERO

    window.open(
        `https://wa.me/${numero}?text=${encodeURIComponent(texto)}`,
        "_blank"
    );
}
</script>

<style>
    /* Estilos Premium */
    .hover-lift { transition: transform 0.4s ease, box-shadow 0.4s ease; cursor: pointer; }
    .hover-lift:hover { transform: translateY(-15px); box-shadow: 0 20px 40px rgba(0,0,0,0.1) !important; }
    .shadow-blue { box-shadow: 0 10px 20px rgba(13, 110, 253, 0.3); }
    .tracking-wide { letter-spacing: 2px; }
    .rounded-4 { border-radius: 1.5rem !important; }
    .z-index-1 { position: relative; z-index: 1; }
</style>
{% endblock %}
