<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>GestiónTiendas</title>

<style>
body { font-family: Arial; margin: 0; display: flex; }

.sidebar {
    width: 250px;
    background: #0a1f44;
    color: white;
    height: 100vh;
    padding: 20px;
}

.sidebar p {
    cursor: pointer;
    padding: 10px;
}

.sidebar p:hover {
    background: #1c3a6b;
}

.content {
    flex: 1;
    padding: 30px;
}

.section {
    display: none;
}

.active {
    display: block;
}

.card {
    background: #eee;
    padding: 10px;
    margin: 5px;
    display: inline-block;
    border-radius: 8px;
}
</style>

<script>
function mostrar(seccion) {
    let secciones = document.querySelectorAll('.section');
    secciones.forEach(s => s.classList.remove('active'));

    document.getElementById(seccion).classList.add('active');
}
</script>

</head>

<body>

<div class="sidebar">
    <p onclick="mostrar('inicio')">🏠 Inicio</p>
    <p onclick="mostrar('uso')">📘 Cómo usar</p>
    <p onclick="mostrar('mision')">🎯 Misión</p>
    <p onclick="mostrar('vision')">👁 Visión</p>
</div>

<div class="content">

<div id="inicio" class="section active">
    <h1>Bienvenido</h1>
    <p>Guía del sistema de gestión de tiendas</p>
</div>

<div id="uso" class="section">
    <h2>Cómo usar el software</h2>
    <div class="card">1. Inicia sesión</div>
    <div class="card">2. Gestiona productos</div>
    <div class="card">3. Realiza ventas</div>
    <div class="card">4. Controla inventario</div>
    <div class="card">5. Reportes</div>
</div>

<div id="mision" class="section">
    <h2>Misión</h2>
    <p>Brindar una solución integral para tiendas.</p>
</div>

<div id="vision" class="section">
    <h2>Visión</h2>
    <p>Ser líder en software de gestión de tiendas.</p>
</div>

</div>

</body>
</html>
