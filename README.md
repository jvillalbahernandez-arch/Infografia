<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Infografía Matrícula - Santa Rosa de Lima</title>
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&family=Poppins:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --azul-oscuro: #0a2a6e;
    --azul-medio: #1a4db8;
    --azul-claro: #3b82f6;
    --azul-cielo: #60a5fa;
    --azul-palido: #bfdbfe;
    --cyan: #06b6d4;
    --turquesa: #0891b2;
    --amarillo: #fbbf24;
    --naranja: #f97316;
    --verde: #10b981;
    --rosa: #ec4899;
    --blanco: #ffffff;
    --gris-claro: #f0f7ff;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Nunito', sans-serif;
    background: linear-gradient(135deg, #0a1628 0%, #0d2252 40%, #0a3a6b 70%, #062a52 100%);
    min-height: 100vh;
    padding: 0;
    overflow-x: hidden;
  }

  /* Floating background shapes */
  body::before {
    content: '';
    position: fixed;
    top: -200px; right: -200px;
    width: 600px; height: 600px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(59,130,246,0.15) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }
  body::after {
    content: '';
    position: fixed;
    bottom: -200px; left: -200px;
    width: 700px; height: 700px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(6,182,212,0.12) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  .wrapper {
    max-width: 750px;
    margin: 0 auto;
    padding: 30px 20px 60px;
    position: relative;
    z-index: 1;
  }

  /* ===== HEADER ===== */
  .header {
    background: linear-gradient(135deg, #1e3a8a 0%, #1d4ed8 50%, #0ea5e9 100%);
    border-radius: 24px;
    padding: 32px 28px 28px;
    text-align: center;
    margin-bottom: 36px;
    position: relative;
    overflow: hidden;
    box-shadow: 0 20px 60px rgba(0,0,0,0.5), inset 0 1px 0 rgba(255,255,255,0.2);
  }
  .header::before {
    content: '';
    position: absolute; top: -60px; right: -60px;
    width: 200px; height: 200px;
    border-radius: 50%;
    background: rgba(255,255,255,0.07);
  }
  .header::after {
    content: '';
    position: absolute; bottom: -40px; left: -40px;
    width: 150px; height: 150px;
    border-radius: 50%;
    background: rgba(6,182,212,0.15);
  }
  .header-badge {
    display: inline-block;
    background: rgba(251,191,36,0.2);
    border: 2px solid var(--amarillo);
    color: var(--amarillo);
    font-family: 'Poppins', sans-serif;
    font-weight: 700;
    font-size: 0.7rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    padding: 5px 16px;
    border-radius: 20px;
    margin-bottom: 14px;
  }
  .header h1 {
    font-family: 'Poppins', sans-serif;
    font-weight: 800;
    font-size: 1.6rem;
    color: var(--blanco);
    line-height: 1.3;
    margin-bottom: 10px;
    position: relative;
    z-index: 1;
  }
  .header h1 span { color: var(--azul-cielo); }
  .header p {
    color: rgba(255,255,255,0.8);
    font-size: 0.95rem;
    font-weight: 600;
    position: relative;
    z-index: 1;
  }
  .school-name {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    margin-top: 16px;
    padding-top: 16px;
    border-top: 1px solid rgba(255,255,255,0.2);
  }
  .school-name span {
    color: var(--blanco);
    font-weight: 800;
    font-size: 1rem;
    letter-spacing: 0.5px;
  }
  .school-icon {
    font-size: 1.5rem;
  }

  /* ===== STEP CARD ===== */
  .step-card {
    background: rgba(255,255,255,0.05);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 20px;
    margin-bottom: 20px;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;
  }
  .step-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 16px 40px rgba(0,0,0,0.4);
  }
  .step-card.active {
    border-color: rgba(255,255,255,0.25);
    background: rgba(255,255,255,0.08);
  }

  .step-header {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 20px 22px;
    position: relative;
    overflow: hidden;
  }
  .step-header::after {
    content: '';
    position: absolute;
    right: -30px; top: -30px;
    width: 100px; height: 100px;
    border-radius: 50%;
    background: rgba(255,255,255,0.04);
  }

  /* Color accents per step */
  .step-1 .step-header { background: linear-gradient(135deg, rgba(29,78,216,0.6), rgba(6,182,212,0.3)); border-left: 4px solid var(--cyan); }
  .step-2 .step-header { background: linear-gradient(135deg, rgba(16,185,129,0.4), rgba(59,130,246,0.4)); border-left: 4px solid var(--verde); }
  .step-3 .step-header { background: linear-gradient(135deg, rgba(249,115,22,0.4), rgba(251,191,36,0.3)); border-left: 4px solid var(--naranja); }
  .step-4 .step-header { background: linear-gradient(135deg, rgba(236,72,153,0.4), rgba(167,139,250,0.3)); border-left: 4px solid var(--rosa); }
  .step-5 .step-header { background: linear-gradient(135deg, rgba(16,185,129,0.5), rgba(6,182,212,0.3)); border-left: 4px solid var(--verde); }
  .step-6 .step-header { background: linear-gradient(135deg, rgba(139,92,246,0.4), rgba(59,130,246,0.4)); border-left: 4px solid #8b5cf6; }
  .step-7 .step-header { background: linear-gradient(135deg, rgba(251,191,36,0.4), rgba(249,115,22,0.3)); border-left: 4px solid var(--amarillo); }

  .step-number {
    width: 52px; height: 52px;
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-family: 'Poppins', sans-serif;
    font-weight: 900;
    font-size: 1.4rem;
    color: var(--blanco);
    flex-shrink: 0;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
  }
  .step-1 .step-number { background: linear-gradient(135deg, var(--azul-medio), var(--cyan)); }
  .step-2 .step-number { background: linear-gradient(135deg, var(--verde), #0d9488); }
  .step-3 .step-number { background: linear-gradient(135deg, var(--naranja), var(--amarillo)); }
  .step-4 .step-number { background: linear-gradient(135deg, var(--rosa), #a855f7); }
  .step-5 .step-number { background: linear-gradient(135deg, var(--turquesa), var(--verde)); }
  .step-6 .step-number { background: linear-gradient(135deg, #7c3aed, var(--azul-claro)); }
  .step-7 .step-number { background: linear-gradient(135deg, var(--amarillo), var(--naranja)); }

  .step-title-area { flex: 1; }
  .step-label {
    font-size: 0.68rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1.5px;
    opacity: 0.7;
    color: var(--blanco);
    margin-bottom: 3px;
  }
  .step-title {
    font-family: 'Poppins', sans-serif;
    font-weight: 700;
    font-size: 0.98rem;
    color: var(--blanco);
    line-height: 1.3;
  }
  .step-emoji { font-size: 1.8rem; flex-shrink: 0; }
  .toggle-icon {
    color: rgba(255,255,255,0.6);
    font-size: 1.2rem;
    transition: transform 0.3s ease;
    flex-shrink: 0;
  }
  .step-card.active .toggle-icon { transform: rotate(180deg); }

  /* ===== COLLAPSIBLE BODY ===== */
  .step-body {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  }
  .step-body.open { max-height: 1000px; }

  .step-content {
    padding: 20px 22px 22px;
    border-top: 1px solid rgba(255,255,255,0.08);
  }
  .step-desc {
    color: rgba(255,255,255,0.85);
    font-size: 0.9rem;
    line-height: 1.7;
    margin-bottom: 14px;
  }

  /* ===== DOCS GRID (Paso 2) ===== */
  .docs-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
    margin-top: 14px;
  }
  .doc-item {
    background: rgba(16,185,129,0.12);
    border: 1px solid rgba(16,185,129,0.3);
    border-radius: 12px;
    padding: 14px;
    display: flex;
    align-items: flex-start;
    gap: 10px;
    transition: background 0.2s;
  }
  .doc-item:hover { background: rgba(16,185,129,0.2); }
  .doc-letter {
    width: 28px; height: 28px;
    border-radius: 8px;
    background: linear-gradient(135deg, var(--verde), #0d9488);
    display: flex; align-items: center; justify-content: center;
    font-weight: 900;
    font-size: 0.8rem;
    color: var(--blanco);
    flex-shrink: 0;
    font-family: 'Poppins', sans-serif;
  }
  .doc-text {
    color: rgba(255,255,255,0.9);
    font-size: 0.82rem;
    line-height: 1.4;
    font-weight: 600;
  }

  /* ===== BITACORA NOTE (Paso 3) ===== */
  .alert-box {
    background: rgba(249,115,22,0.12);
    border: 1px solid rgba(249,115,22,0.4);
    border-radius: 12px;
    padding: 14px 16px;
    display: flex;
    align-items: center;
    gap: 12px;
    margin-top: 10px;
  }
  .alert-icon { font-size: 1.5rem; }
  .alert-text {
    color: rgba(255,255,255,0.85);
    font-size: 0.85rem;
    line-height: 1.5;
    font-weight: 600;
  }
  .alert-text strong { color: var(--naranja); }

  /* ===== FLUJO (Paso 4) ===== */
  .flow-steps {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    margin-top: 12px;
  }
  .flow-chip {
    background: rgba(236,72,153,0.15);
    border: 1px solid rgba(236,72,153,0.35);
    border-radius: 20px;
    padding: 6px 14px;
    color: rgba(255,255,255,0.9);
    font-size: 0.8rem;
    font-weight: 700;
  }

  /* ===== SIMAT highlight (Paso 5) ===== */
  .simat-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: linear-gradient(135deg, rgba(6,182,212,0.3), rgba(16,185,129,0.3));
    border: 1px solid rgba(6,182,212,0.5);
    border-radius: 12px;
    padding: 10px 18px;
    margin-top: 12px;
    color: var(--blanco);
    font-weight: 800;
    font-size: 0.95rem;
  }

  /* ===== DB (Paso 6) ===== */
  .db-row {
    display: flex;
    align-items: center;
    gap: 10px;
    background: rgba(139,92,246,0.1);
    border: 1px solid rgba(139,92,246,0.25);
    border-radius: 10px;
    padding: 10px 14px;
    margin-top: 10px;
    color: rgba(255,255,255,0.85);
    font-size: 0.85rem;
    font-weight: 600;
  }

  /* ===== ARCHIVO (Paso 7) ===== */
  .file-tags {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    margin-top: 12px;
  }
  .file-tag {
    background: rgba(251,191,36,0.15);
    border: 1px solid rgba(251,191,36,0.4);
    border-radius: 20px;
    padding: 6px 14px;
    color: var(--amarillo);
    font-size: 0.8rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 5px;
  }

  /* ===== PROGRESS ===== */
  .progress-bar-outer {
    background: rgba(255,255,255,0.08);
    border-radius: 20px;
    height: 6px;
    margin: 8px 0 0;
    overflow: hidden;
  }
  .progress-bar-inner {
    height: 100%;
    border-radius: 20px;
    width: 0%;
    transition: width 0.6s ease;
  }

  /* ===== CONNECTOR LINE ===== */
  .connector {
    display: flex;
    justify-content: center;
    margin: -8px 0;
    opacity: 0.4;
  }
  .connector::before {
    content: '';
    width: 2px;
    height: 20px;
    background: linear-gradient(to bottom, var(--azul-claro), transparent);
  }

  /* ===== FOOTER ===== */
  .footer {
    background: linear-gradient(135deg, rgba(6,182,212,0.2), rgba(29,78,216,0.3));
    border: 1px solid rgba(6,182,212,0.3);
    border-radius: 18px;
    padding: 20px 24px;
    text-align: center;
    margin-top: 30px;
  }
  .footer p {
    color: rgba(255,255,255,0.7);
    font-size: 0.85rem;
    line-height: 1.6;
  }
  .footer strong { color: var(--azul-cielo); }

  /* ===== EXPAND ALL BUTTON ===== */
  .btn-expand {
    background: linear-gradient(135deg, var(--azul-medio), var(--cyan));
    color: white;
    border: none;
    border-radius: 30px;
    padding: 12px 28px;
    font-family: 'Nunito', sans-serif;
    font-weight: 800;
    font-size: 0.9rem;
    cursor: pointer;
    display: block;
    margin: 0 auto 28px;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: 0 6px 20px rgba(0,0,0,0.3);
  }
  .btn-expand:hover {
    transform: translateY(-2px);
    box-shadow: 0 10px 30px rgba(0,0,0,0.4);
  }

  /* Animations */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .step-card {
    animation: fadeUp 0.5s ease both;
  }
  .step-card:nth-child(1) { animation-delay: 0.1s; }
  .step-card:nth-child(3) { animation-delay: 0.15s; }
  .step-card:nth-child(5) { animation-delay: 0.2s; }
  .step-card:nth-child(7) { animation-delay: 0.25s; }
  .step-card:nth-child(9) { animation-delay: 0.3s; }
  .step-card:nth-child(11) { animation-delay: 0.35s; }
  .step-card:nth-child(13) { animation-delay: 0.4s; }

  .tip-box {
    background: rgba(96,165,250,0.1);
    border-left: 3px solid var(--azul-cielo);
    border-radius: 0 10px 10px 0;
    padding: 10px 14px;
    margin-top: 10px;
    color: rgba(255,255,255,0.8);
    font-size: 0.83rem;
    font-style: italic;
  }
</style>
</head>
<body>
<div class="wrapper">

  <!-- HEADER -->
  <div class="header">
    <div class="header-badge">📋 Guía Oficial 2026</div>
    <h1>Revisión y Organización de<br><span>Carpetas de Matrícula</span></h1>
    <p>Protocolo paso a paso para secretaría académica</p>
    <div class="school-name">
      <span>I.E. Santa Rosa de Lima</span>
    </div>
  </div>

  <!-- BOTÓN EXPANDIR TODO -->
  <button class="btn-expand" onclick="toggleAll()">📂 Expandir / Colapsar todos</button>

  <!-- PASO 1 -->
  <div class="step-card step-1" onclick="toggleStep(this)">
    <div class="step-header">
      <div class="step-number">1</div>
      <div class="step-title-area">
        <div class="step-label">Paso 1 · Recepción</div>
        <div class="step-title">Reciba la carpeta física en secretaría</div>
      </div>
      <div class="step-emoji">📁</div>
      <div class="toggle-icon">▼</div>
    </div>
    <div class="step-body">
      <div class="step-content">
        <div class="progress-bar-outer"><div class="progress-bar-inner" style="background: linear-gradient(90deg, var(--azul-medio), var(--cyan)); width: 14%;"></div></div>
        <p class="step-desc" style="margin-top:14px;">Reciba la carpeta de matrícula física entregada por el acudiente en la secretaría y ubíquela de inmediato en la <strong style="color:var(--azul-cielo)">bandeja de revisión</strong> para evitar la acumulación de papeles y mantener el espacio despejado.</p>
        <div class="tip-box">💡 Mantener el escritorio organizado desde el inicio agiliza todo el proceso.</div>
      </div>
    </div>
  </div>

  <div class="connector"></div>

  <!-- PASO 2 -->
  <div class="step-card step-2" onclick="toggleStep(this)">
    <div class="step-header">
      <div class="step-number">2</div>
      <div class="step-title-area">
        <div class="step-label">Paso 2 · Auditoría</div>
        <div class="step-title">Audite la carpeta y verifique documentos requeridos</div>
      </div>
      <div class="step-emoji">🔍</div>
      <div class="toggle-icon">▼</div>
    </div>
    <div class="step-body">
      <div class="step-content">
        <div class="progress-bar-outer"><div class="progress-bar-inner" style="background: linear-gradient(90deg, var(--verde), #0d9488); width: 28%;"></div></div>
        <p class="step-desc" style="margin-top:14px;">Audite la carpeta <strong style="color:#6ee7b7">hoja por hoja</strong> y verifique que contenga los documentos requeridos obligatorios para el trámite:</p>
        <div class="docs-grid">
          <div class="doc-item">
            <div class="doc-letter">A</div>
            <div class="doc-text">Copia del documento de identificación del estudiante</div>
          </div>
          <div class="doc-item">
            <div class="doc-letter">B</div>
            <div class="doc-text">Certificados de notas de los años anteriores</div>
          </div>
          <div class="doc-item">
            <div class="doc-letter">C</div>
            <div class="doc-text">Certificado del SISBÉN</div>
          </div>
          <div class="doc-item">
            <div class="doc-letter">D</div>
            <div class="doc-text">Certificado de salud (ADRES)</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="connector"></div>

  <!-- PASO 3 -->
  <div class="step-card step-3" onclick="toggleStep(this)">
    <div class="step-header">
      <div class="step-number">3</div>
      <div class="step-title-area">
        <div class="step-label">Paso 3 · Control</div>
        <div class="step-title">Registre novedades en la bitácora</div>
      </div>
      <div class="step-emoji">📝</div>
      <div class="toggle-icon">▼</div>
    </div>
    <div class="step-body">
      <div class="step-content">
        <div class="progress-bar-outer"><div class="progress-bar-inner" style="background: linear-gradient(90deg, var(--naranja), var(--amarillo)); width: 42%;"></div></div>
        <p class="step-desc" style="margin-top:14px;">En caso de identificar que la carpeta está incompleta, registre <strong style="color:var(--amarillo)">de inmediato</strong> la novedad en la bitácora de inconsistencias de la secretaría para mantener un control riguroso.</p>
        <div class="alert-box">
          <div class="alert-icon">⚠️</div>
          <div class="alert-text"><strong>¡Importante!</strong> Ninguna inconsistencia debe quedar sin registrar. El control riguroso garantiza el seguimiento efectivo de cada caso.</div>
        </div>
      </div>
    </div>
  </div>

  <div class="connector"></div>

  <!-- PASO 4 -->
  <div class="step-card step-4" onclick="toggleStep(this)">
    <div class="step-header">
      <div class="step-number">4</div>
      <div class="step-title-area">
        <div class="step-label">Paso 4 · Gestión</div>
        <div class="step-title">Gestione las inconsistencias sin detener el flujo</div>
      </div>
      <div class="step-emoji">🔄</div>
      <div class="toggle-icon">▼</div>
    </div>
    <div class="step-body">
      <div class="step-content">
        <div class="progress-bar-outer"><div class="progress-bar-inner" style="background: linear-gradient(90deg, var(--rosa), #a855f7); width: 57%;"></div></div>
        <p class="step-desc" style="margin-top:14px;">Solicite de inmediato los documentos faltantes al acudiente, <strong style="color:#f9a8d4">evitando archivar carpetas incompletas</strong> y sin detener el flujo de revisión de los demás casos.</p>
        <div class="flow-steps">
          <div class="flow-chip">📞 Contactar acudiente</div>
          <div class="flow-chip">📋 Indicar faltantes</div>
          <div class="flow-chip">⏳ Establecer plazo</div>
          <div class="flow-chip">🔄 Continuar revisando</div>
        </div>
      </div>
    </div>
  </div>

  <div class="connector"></div>

  <!-- PASO 5 -->
  <div class="step-card step-5" onclick="toggleStep(this)">
    <div class="step-header">
      <div class="step-number">5</div>
      <div class="step-title-area">
        <div class="step-label">Paso 5 · Sistema</div>
        <div class="step-title">Verifique y actualice en SIMAT</div>
      </div>
      <div class="step-emoji">💻</div>
      <div class="toggle-icon">▼</div>
    </div>
    <div class="step-body">
      <div class="step-content">
        <div class="progress-bar-outer"><div class="progress-bar-inner" style="background: linear-gradient(90deg, var(--turquesa), var(--verde)); width: 71%;"></div></div>
        <p class="step-desc" style="margin-top:14px;">Una vez completa la carpeta, verifique que el trámite quedó realizado y que la información del estudiante sea actualizada en el sistema nacional.</p>
        <div class="simat-badge">
          🖥️ Sistema Integrado de Matrículas — <span style="color:var(--azul-cielo)">SIMAT</span>
        </div>
      </div>
    </div>
  </div>

  <div class="connector"></div>

  <!-- PASO 6 -->
  <div class="step-card step-6" onclick="toggleStep(this)">
    <div class="step-header">
      <div class="step-number">6</div>
      <div class="step-title-area">
        <div class="step-label">Paso 6 · Base de Datos</div>
        <div class="step-title">Sistematice en la base de datos interna</div>
      </div>
      <div class="step-emoji">🗄️</div>
      <div class="toggle-icon">▼</div>
    </div>
    <div class="step-body">
      <div class="step-content">
        <div class="progress-bar-outer"><div class="progress-bar-inner" style="background: linear-gradient(90deg, #7c3aed, var(--azul-claro)); width: 85%;"></div></div>
        <p class="step-desc" style="margin-top:14px;">Proceda a sistematizar los datos verificados en la base de datos interna de la institución, asegurando que la información local coincida plenamente con la plataforma nacional.</p>
        <div class="db-row">🗂️ <strong style="color:#c4b5fd">Microsoft Access</strong> — Registro institucional local sincronizado con SIMAT</div>
      </div>
    </div>
  </div>

  <div class="connector"></div>

  <!-- PASO 7 -->
  <div class="step-card step-7" onclick="toggleStep(this)">
    <div class="step-header">
      <div class="step-number">7</div>
      <div class="step-title-area">
        <div class="step-label">Paso 7 · Archivo</div>
        <div class="step-title">Archive y realice copia de seguridad</div>
      </div>
      <div class="step-emoji">💾</div>
      <div class="toggle-icon">▼</div>
    </div>
    <div class="step-body">
      <div class="step-content">
        <div class="progress-bar-outer"><div class="progress-bar-inner" style="background: linear-gradient(90deg, var(--amarillo), var(--naranja)); width: 100%;"></div></div>
        <p class="step-desc" style="margin-top:14px;">Al finalizar, quienes se encarguen del archivo deben guardar la carpeta física <strong style="color:var(--amarillo)">organizada alfabéticamente y por grados</strong> en los estantes, y realizar una copia de seguridad local.</p>
        <div class="file-tags">
          <div class="file-tag">📂 Orden alfabético</div>
          <div class="file-tag">🎓 Por grados</div>
          <div class="file-tag">💾 Backup local</div>
          <div class="file-tag">✅ Proceso completado</div>
        </div>
      </div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <p>📌 Este protocolo garantiza la <strong>integridad, trazabilidad y seguridad</strong> de la información de cada estudiante matriculado en la <strong>I.E. Santa Rosa de Lima</strong>.<br>Secretaría Académica · 2026</p>
  </div>

</div>

<script>
  function toggleStep(card) {
    const body = card.querySelector('.step-body');
    const isOpen = body.classList.contains('open');
    body.classList.toggle('open', !isOpen);
    card.classList.toggle('active', !isOpen);
  }

  let allExpanded = false;
  function toggleAll() {
    allExpanded = !allExpanded;
    document.querySelectorAll('.step-card').forEach(card => {
      const body = card.querySelector('.step-body');
      body.classList.toggle('open', allExpanded);
      card.classList.toggle('active', allExpanded);
    });
  }

  // Open step 2 by default to show documents
  window.addEventListener('load', () => {
    const step2 = document.querySelectorAll('.step-card')[1];
    if (step2) {
      step2.querySelector('.step-body').classList.add('open');
      step2.classList.add('active');
    }
  });
</script>
</body>
</html>
