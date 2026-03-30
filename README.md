<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Reporte Semanal de Tendencias en Salud Visual — Semana del 24 de Marzo 2026</title>
<style>
:root {
  --primary: #0f4c75;
  --primary-light: #1b6ca8;
  --primary-dark: #0a3655;
  --accent: #3282b8;
  --accent-light: #bbe1fa;
  --bg: #f8fafc;
  --card-bg: #ffffff;
  --text: #1e293b;
  --text-light: #64748b;
  --border: #e2e8f0;
  --success: #059669;
  --warning: #d97706;
  --danger: #dc2626;
  --iit-bg: #fef3c7;
  --iit-border: #f59e0b;
}
* { margin:0; padding:0; box-sizing:border-box; }
body { font-family: 'Segoe UI', system-ui, -apple-system, sans-serif; background: var(--bg); color: var(--text); line-height: 1.6; }
.header { background: linear-gradient(135deg, var(--primary-dark), var(--primary), var(--accent)); color: white; padding: 2.5rem 2rem; text-align: center; position: relative; overflow: hidden; }
.header::before { content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%; background: radial-gradient(ellipse, rgba(255,255,255,0.08) 0%, transparent 60%); }
.header h1 { font-size: 1.9rem; font-weight: 700; margin-bottom: 0.5rem; position: relative; }
.header .subtitle { font-size: 1rem; opacity: 0.9; position: relative; }
.header .date-badge { display: inline-block; background: rgba(255,255,255,0.2); padding: 0.4rem 1.2rem; border-radius: 20px; margin-top: 0.8rem; font-size: 0.9rem; position: relative; }
.container { max-width: 1200px; margin: 0 auto; padding: 1.5rem; }
.tabs { display: flex; flex-wrap: wrap; gap: 0.3rem; background: var(--card-bg); padding: 0.8rem; border-radius: 12px; box-shadow: 0 1px 3px rgba(0,0,0,0.1); margin-bottom: 1.5rem; position: sticky; top: 0; z-index: 100; }
.tab { padding: 0.6rem 1rem; border: none; background: transparent; color: var(--text-light); cursor: pointer; border-radius: 8px; font-size: 0.85rem; font-weight: 500; transition: all 0.2s; white-space: nowrap; }
.tab:hover { background: var(--accent-light); color: var(--primary); }
.tab.active { background: var(--primary); color: white; }
.tab-content { display: none; animation: fadeIn 0.3s ease; }
.tab-content.active { display: block; }
@keyframes fadeIn { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }
.card { background: var(--card-bg); border-radius: 12px; padding: 1.5rem; margin-bottom: 1.2rem; box-shadow: 0 1px 3px rgba(0,0,0,0.08); border-left: 4px solid var(--primary); }
.card h3 { color: var(--primary); margin-bottom: 0.8rem; font-size: 1.15rem; }
.card p, .card li { font-size: 0.95rem; margin-bottom: 0.5rem; }
.card ul { padding-left: 1.2rem; }
.card ul li { margin-bottom: 0.6rem; }
.highlight-box { background: linear-gradient(135deg, #eff6ff, #dbeafe); border: 1px solid #93c5fd; border-radius: 10px; padding: 1.2rem; margin: 1rem 0; }
.iit-card { border-left-color: var(--iit-border); background: linear-gradient(to right, #fffbeb, var(--card-bg)); }
.iit-card h3 { color: #92400e; }
.iit-proposal { background: #fef9ee; border: 1px solid #fbbf24; border-radius: 10px; padding: 1.2rem; margin: 1rem 0; }
.iit-proposal h4 { color: #92400e; margin-bottom: 0.5rem; font-size: 1.05rem; }
.iit-proposal .tag { display: inline-block; background: #fbbf24; color: #78350f; padding: 0.15rem 0.6rem; border-radius: 12px; font-size: 0.75rem; font-weight: 600; margin-right: 0.3rem; margin-bottom: 0.3rem; }
.stat-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1rem; margin: 1.2rem 0; }
.stat-card { background: var(--card-bg); border-radius: 10px; padding: 1.2rem; text-align: center; box-shadow: 0 1px 3px rgba(0,0,0,0.08); border-top: 3px solid var(--accent); }
.stat-card .number { font-size: 2rem; font-weight: 700; color: var(--primary); }
.stat-card .label { font-size: 0.85rem; color: var(--text-light); margin-top: 0.3rem; }
.pdufa-table { width: 100%; border-collapse: collapse; margin: 1rem 0; font-size: 0.9rem; }
.pdufa-table th { background: var(--primary); color: white; padding: 0.8rem; text-align: left; }
.pdufa-table td { padding: 0.7rem 0.8rem; border-bottom: 1px solid var(--border); }
.pdufa-table tr:hover { background: #f1f5f9; }
.congress-table { width: 100%; border-collapse: collapse; margin: 1rem 0; font-size: 0.9rem; }
.congress-table th { background: var(--primary); color: white; padding: 0.8rem; text-align: left; }
.congress-table td { padding: 0.7rem 0.8rem; border-bottom: 1px solid var(--border); }
.congress-table tr:hover { background: #f1f5f9; }
.badge { display: inline-block; padding: 0.2rem 0.6rem; border-radius: 12px; font-size: 0.75rem; font-weight: 600; }
.badge-green { background: #dcfce7; color: #166534; }
.badge-yellow { background: #fef3c7; color: #92400e; }
.badge-red { background: #fee2e2; color: #991b1b; }
.badge-blue { background: #dbeafe; color: #1e40af; }
a.src-link { color: var(--accent); text-decoration: none; font-size: 0.85rem; font-weight: 500; }
a.src-link:hover { text-decoration: underline; color: var(--primary); }
.sources-list { columns: 2; column-gap: 2rem; }
.sources-list li { margin-bottom: 0.5rem; font-size: 0.85rem; break-inside: avoid; }
.executive-kpi { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 0.8rem; margin: 1rem 0; }
.kpi { background: white; border-radius: 8px; padding: 1rem; text-align: center; border: 1px solid var(--border); }
.kpi .icon { font-size: 1.5rem; margin-bottom: 0.3rem; }
.kpi .val { font-size: 1.4rem; font-weight: 700; color: var(--primary); }
.kpi .desc { font-size: 0.78rem; color: var(--text-light); }
.action-item { background: #f0fdf4; border-left: 3px solid var(--success); padding: 0.8rem 1rem; margin: 0.5rem 0; border-radius: 0 8px 8px 0; }
.action-item strong { color: var(--success); }
footer { text-align: center; padding: 2rem; color: var(--text-light); font-size: 0.8rem; border-top: 1px solid var(--border); margin-top: 2rem; }
@media (max-width: 768px) {
  .tabs { flex-direction: column; position: static; }
  .tab { text-align: center; }
  .sources-list { columns: 1; }
  .header h1 { font-size: 1.4rem; }
  .stat-grid { grid-template-columns: 1fr 1fr; }
}
</style>
</head>
<body>

<div class="header">
  <h1>📊 Reporte Semanal de Tendencias en Salud Visual</h1>
  <div class="subtitle">Instituto de Ojos — Puerto Rico | Preparado para el Director Ejecutivo y Director Médico</div>
  <div class="date-badge">Semana del 24 al 30 de marzo de 2026</div>
</div>

<div class="container">

<div class="tabs" id="tabsNav">
  <button class="tab active" onclick="showTab('resumen')">Resumen Ejecutivo</button>
  <button class="tab" onclick="showTab('ia')">IA y Tecnología</button>
  <button class="tab" onclick="showTab('clinica')">Clínica y Cirugía</button>
  <button class="tab" onclick="showTab('pipeline')">Pipeline y Fármacos</button>
  <button class="tab" onclick="showTab('mercado')">Mercado y Negocio</button>
  <button class="tab" onclick="showTab('miopia')">Control de Miopía</button>
  <button class="tab" onclick="showTab('iit')">Oportunidades IIT</button>
  <button class="tab" onclick="showTab('congresos')">Congresos 2026-2027</button>
  <button class="tab" onclick="showTab('fuentes')">Fuentes</button>
</div>

<!-- ============ RESUMEN EJECUTIVO ============ -->
<div class="tab-content active" id="resumen">
  <div class="card">
    <h3>🔑 Resumen Ejecutivo — Semana del 24–30 Marzo 2026</h3>
    <p>Esta semana presenta desarrollos de alto impacto para Instituto de Ojos en múltiples frentes. A continuación los hallazgos más relevantes:</p>
  </div>

  <div class="executive-kpi">
    <div class="kpi"><div class="icon">💊</div><div class="val">4</div><div class="desc">Fechas PDUFA activas en 2026</div></div>
    <div class="kpi"><div class="icon">🧬</div><div class="val">5+</div><div class="desc">Terapias génicas en ensayos clínicos</div></div>
    <div class="kpi"><div class="icon">🤖</div><div class="val">78%</div><div class="desc">Oftalmólogos ven IA como tendencia #1</div></div>
    <div class="kpi"><div class="icon">📈</div><div class="val">$55.5B</div><div class="desc">Mercado global oftalmología 2026</div></div>
    <div class="kpi"><div class="icon">🔬</div><div class="val">3.4%</div><div class="desc">Hispanos en ensayos de glaucoma</div></div>
    <div class="kpi"><div class="icon">👁️</div><div class="val">33.3%</div><div class="desc">Prevalencia RD en Caribe</div></div>
  </div>

  <div class="highlight-box">
    <strong>⚡ Decisiones requeridas esta semana:</strong>
    <ul style="margin-top:0.5rem;">
      <li><strong>FDA/Pipeline:</strong> La FDA emitió una Complete Response Letter (CRL) para reproxalap (Aldeyra) — tercer rechazo para este fármaco de ojo seco. El pipeline de ojo seco sigue activo con OCS-02 (licaminlimab) y ST-100 como alternativas prometedoras. <a class="src-link" href="https://www.hcplive.com/view/fda-issues-third-reproxalap-crl-for-dry-eye-disease" target="_blank">→ HCPLive</a></li>
      <li><strong>IOLs:</strong> Aprobación FDA de Tecnis PureSee EDOF IOL (J&J) — primera EDOF sin advertencia por pérdida de sensibilidad al contraste. Evaluar adopción temprana. <a class="src-link" href="https://eyewire.news/news/johnson-johnson-announces-fda-approval-of-tecni-puresee-iol-for-cataract-surgery" target="_blank">→ Eyewire</a></li>
      <li><strong>IIT Urgente:</strong> Solo el 3.4% de participantes en ensayos de glaucoma son hispanos — Instituto de Ojos con 58K pacientes activos es una plataforma ideal para IITs que cierren esta brecha. Contactar Roche/Genentech para estudio de faricimab en DME en hispanos. <a class="src-link" href="https://pmc.ncbi.nlm.nih.gov/articles/PMC8132140/" target="_blank">→ PMC</a></li>
      <li><strong>MIGS:</strong> MINT (trabeculostomía nasal mínimamente invasiva) reporta 82.5% éxito a 12 meses. Mercado MIGS crece al 29% anual. <a class="src-link" href="https://www.ophthalmologytimes.com/view/migs-continues-innovate-secure-place-glaucoma" target="_blank">→ Ophthalmology Times</a></li>
      <li><strong>Congresos:</strong> ASCRS Washington DC (10–13 abril 2026) en 2 semanas — confirmar asistencia y agenda de reuniones con sponsors potenciales para IITs.</li>
    </ul>
  </div>
</div>

<!-- ============ IA Y TECNOLOGÍA ============ -->
<div class="tab-content" id="ia">
  <div class="card">
    <h3>🤖 IA como Tendencia Transformadora #1 en Oftalmología</h3>
    <p>El 78% de los oftalmólogos encuestados identificaron la IA como la tendencia más transformadora en la especialidad. La integración de IA en diagnósticos se está convirtiendo en parte estándar de la experiencia del paciente en 2026. <a class="src-link" href="https://www.ophthalmologytimes.com/view/how-ai-is-reshaping-ophthalmology-in-2025-and-beyond" target="_blank">→ Ophthalmology Times</a></p>
  </div>

  <div class="card">
    <h3>🔬 Plataforma Altris AI para análisis automatizado de OCT</h3>
    <p>Altris presentó su plataforma de IA capaz de diferenciar entre B-scans patológicos y no patológicos, identificando más de 100 patologías retinianas, incluyendo enfermedades raras. Esta tecnología puede revolucionar el screening de alto volumen. <a class="src-link" href="https://www.ophthalmologytimes.com/view/altris-unveils-artificial-intelligence-platform-for-automated-oct-scans-analysis" target="_blank">→ Ophthalmology Times</a></p>
    <div class="action-item"><strong>Acción:</strong> Evaluar integración de Altris AI con los equipos OCT existentes del Instituto. Con 58K pacientes activos, el ROI de screening automatizado es significativo.</div>
  </div>

  <div class="card">
    <h3>📊 IA Predictiva en Atrofia Geográfica</h3>
    <p>En el congreso Angiogenesis 2026, se presentaron datos emergentes sobre modelos de IA que predicen función retiniana a partir de OCT en pacientes con atrofia geográfica. <a class="src-link" href="https://www.ophthalmologytimes.com/view/ai-predicted-retinal-function-shows-promise-in-geographic-atrophy" target="_blank">→ Ophthalmology Times</a></p>
  </div>

  <div class="card">
    <h3>🧠 deepeye® TPS — Planificación de Tratamiento con IA</h3>
    <p>El algoritmo deepeye® Treatment Planning Support utiliza miles de escaneos 3D de retina combinados con registros médicos para analizar progresión de enfermedad y correlacionarla con regímenes de tratamiento, permitiendo personalización terapéutica. <a class="src-link" href="https://www.ophthalmologytimes.com/view/how-ai-is-reshaping-ophthalmology-in-2025-and-beyond" target="_blank">→ Ophthalmology Times</a></p>
  </div>

  <div class="card">
    <h3>📱 Teleoftalmología y Monitoreo Remoto</h3>
    <p>El OCT domiciliario continúa avanzando — estudios sistemáticos confirman alta concordancia entre escaneos remotos y en consultorio para detección de patologías y medición de grosor retiniano. Los dispositivos portátiles de imagen y el análisis con IA están expandiendo el acceso a poblaciones remotas y desatendidas. <a class="src-link" href="https://pmc.ncbi.nlm.nih.gov/articles/PMC11540653/" target="_blank">→ PMC/Frontiers in Medicine</a></p>
    <div class="action-item"><strong>Acción para PR:</strong> La geografía insular de Puerto Rico hace la teleoftalmología especialmente relevante. Explorar pilotos de screening remoto de RD con cámaras de fondo portátiles + IA en municipios rurales.</div>
  </div>

  <div class="card">
    <h3>🔍 IA en Glaucoma — Individualización Terapéutica</h3>
    <p>La IA está permitiendo identificar la trayectoria individual de pacientes con glaucoma para predecir riesgo de progresión y optimizar el momento de intervención quirúrgica, moviendo el paradigma de tratamiento reactivo a preventivo. <a class="src-link" href="https://www.ophthalmologytimes.com/view/innovations-in-glaucoma-poised-for-breakthrough-in-2026-and-what-might-hold-the-back-" target="_blank">→ Ophthalmology Times</a></p>
  </div>
</div>

<!-- ============ CLÍNICA Y CIRUGÍA ============ -->
<div class="tab-content" id="clinica">
  <div class="card">
    <h3>🏆 FDA Aprueba Tecnis PureSee EDOF IOL (Johnson & Johnson)</h3>
    <p>J&J obtuvo aprobación FDA para Tecnis PureSee, la primera y única EDOF IOL aprobada <strong>sin advertencia por pérdida de sensibilidad al contraste</strong>. Aborda pérdida visual por catarata y presbicia en un solo procedimiento. <a class="src-link" href="https://eyewire.news/news/johnson-johnson-announces-fda-approval-of-tecni-puresee-iol-for-cataract-surgery" target="_blank">→ Eyewire</a></p>
    <div class="action-item"><strong>Acción:</strong> Programar demostración técnica con representante de J&J Vision. Evaluar adopción temprana como diferenciador competitivo.</div>
  </div>

  <div class="card">
    <h3>🔧 Innovaciones en IOLs 2026</h3>
    <p>Las tendencias en IOLs incluyen trifocales mejorados, ópticas guiadas por frente de onda y diseños tóricos EDOF para mejorar contraste y reducir efectos secundarios. Las Light Adjustable Lenses (RxSight) siguen ganando popularidad por su capacidad de ajuste post-quirúrgico con luz UV. <a class="src-link" href="https://www.reviewofophthalmology.com/article/the-2026-iol-preferences-survey" target="_blank">→ Review of Ophthalmology</a></p>
  </div>

  <div class="card">
    <h3>🤖 IA en Cirugía de Catarata</h3>
    <p>Las tecnologías avanzadas de IA proporcionan retroalimentación en tiempo real durante cirugía, asisten en incisiones precisas y optimizan procedimientos. La integración de datos pre, intra y post-operatorios permite análisis refinado de complicaciones y selección personalizada de IOL premium. <a class="src-link" href="https://www.nature.com/articles/s41433-025-03745-x" target="_blank">→ Eye (Nature)</a></p>
  </div>

  <div class="card">
    <h3>💡 MIGS — Nueva Generación</h3>
    <p>El segmento MIGS crece al <strong>29% anual</strong>. Desarrollos clave:</p>
    <ul>
      <li><strong>MINT</strong> (trabeculostomía nasal mínimamente invasiva): Crea múltiples trabeculostomías sin penetrar completamente la esclera. Datos a 12 meses muestran 82.5% de éxito (≥20% reducción PIO). <a class="src-link" href="https://www.ophthalmologytimes.com/view/migs-continues-innovate-secure-place-glaucoma" target="_blank">→ Ophthalmology Times</a></li>
      <li><strong>MINIject</strong> (iStar Medical): Implante MIGS ab interno dirigido al espacio supraciliar.</li>
      <li><strong>Bimatoprost de liberación sostenida:</strong> Datos positivos a 18 meses del ensayo first-in-human presentados en ASCRS 2025. <a class="src-link" href="https://www.reviewofophthalmology.com/article/the-2026-glaucoma-pipeline" target="_blank">→ Review of Ophthalmology</a></li>
    </ul>
  </div>

  <div class="card">
    <h3>🧪 Neuroprotección en Glaucoma — PER-001</h3>
    <p>PER-001 (Perfuse Therapeutics), un antagonista de endotelina como implante intravítreo para glaucoma, mostró en datos Fase I/IIa que una sola administración sobre terapia estándar aumentó flujo sanguíneo ocular y mejoró función visual y estructural. Representa un cambio de paradigma hacia neuroprotección más allá de solo reducir PIO. <a class="src-link" href="https://glaucomatoday.com/resource/glaucoma-pipeline-2026" target="_blank">→ Glaucoma Today</a></p>
  </div>
</div>

<!-- ============ PIPELINE Y FÁRMACOS ============ -->
<div class="tab-content" id="pipeline">
  <div class="card">
    <h3>📋 Fechas PDUFA y Pipeline Oftalmológico 2026</h3>
    <table class="pdufa-table">
      <thead>
        <tr><th>Fármaco</th><th>Compañía</th><th>Indicación</th><th>PDUFA / Estado</th><th>Impacto</th></tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Reproxalap</strong></td>
          <td>Aldeyra Therapeutics</td>
          <td>Ojo seco</td>
          <td><span class="badge badge-red">CRL Marzo 2026</span></td>
          <td>Tercer rechazo FDA. Falta evidencia sustancial de eficacia.</td>
        </tr>
        <tr>
          <td><strong>Idebenone</strong></td>
          <td>Chiesi Global Rare Diseases</td>
          <td>LHON (Neuropatía óptica de Leber)</td>
          <td><span class="badge badge-yellow">PDUFA: 28 Feb 2026</span></td>
          <td>Revisión prioritaria. Primer tratamiento potencial para LHON.</td>
        </tr>
        <tr>
          <td><strong>Veligrotug</strong></td>
          <td>—</td>
          <td>Enfermedad ocular tiroidea (TED)</td>
          <td><span class="badge badge-blue">PDUFA: 30 Jun 2026</span></td>
          <td>Revisión prioritaria.</td>
        </tr>
        <tr>
          <td><strong>MR-141</strong></td>
          <td>Viatris</td>
          <td>Presbicia</td>
          <td><span class="badge badge-blue">PDUFA: 17 Oct 2026</span></td>
          <td>Fentolamina 0.75% solución oftálmica.</td>
        </tr>
        <tr>
          <td><strong>AXPAXLI (OTX-TKI)</strong></td>
          <td>Ocular Therapeutix</td>
          <td>DMAE húmeda</td>
          <td><span class="badge badge-yellow">En revisión</span></td>
          <td>Implante intravítreo bioreabsorbible con axitinib (9-12 meses).</td>
        </tr>
        <tr>
          <td><strong>Tarcocimab (KSI-301)</strong></td>
          <td>Kodiak Sciences</td>
          <td>Retinopatía diabética</td>
          <td><span class="badge badge-blue">Datos GLOW2 Q1 2026</span></td>
          <td>Anti-VEGF de larga duración. Relevante para población DR en PR.</td>
        </tr>
      </tbody>
    </table>
    <p style="font-size:0.85rem; color:var(--text-light);">
      <a class="src-link" href="https://www.ophthalmologytimes.com/view/ophthalmology-pipeline-watch-key-trial-results-and-pdufa-dates-for-q1-2026" target="_blank">→ Ophthalmology Times Pipeline Q1</a> |
      <a class="src-link" href="https://www.ophthalmologytimes.com/view/ophthalmology-pipeline-milestones-for-q2-2026" target="_blank">→ Pipeline Q2</a> |
      <a class="src-link" href="https://www.prnewswire.com/news-releases/fda-accepts-viatris-supplemental-new-drug-application-for-mr-141-phentolamine-ophthalmic-solution-0-75-for-the-treatment-of-presbyopia-302696332.html" target="_blank">→ Viatris PR</a>
    </p>
  </div>

  <div class="card">
    <h3>🧬 Terapias Génicas — Pipeline Avanzado</h3>
    <ul>
      <li><strong>MCO-010 (Nanoscope):</strong> Primera BLA para terapia génica agnóstica para enfermedad retiniana. Sometimiento rolling iniciado julio 2025, envío completo anticipado Q1 2026. Datos del ensayo Fase 2b/3 RESTORE cumplieron endpoints primarios. <a class="src-link" href="https://www.fightingblindness.org/news/retinitis-pigmentosa-research-advances-899" target="_blank">→ Foundation Fighting Blindness</a></li>
      <li><strong>Laru-zova (terapia génica bilateral):</strong> Ensayo LANDSCAPE evaluando dosis bilateral completó reclutamiento en ensayo pivotal Fase 2/3. Resultados esperados 2026. <a class="src-link" href="https://www.ophthalmologyadvisor.com/features/retinal-gene-therapy-options-advance-through-clinical-trial-investigations/" target="_blank">→ Ophthalmology Advisor</a></li>
      <li><strong>SPVN20 (SparingVision):</strong> Terapia génica agnóstica para restaurar visión de conos en RP avanzada. Primer paciente dosificado en ensayo NYRVANA Fase 1/2. Planean solicitar autorización para ensayo en EE.UU. en 2026. <a class="src-link" href="https://www.ophthalmologyadvisor.com/features/retinal-gene-therapy-options-advance-through-clinical-trial-investigations/" target="_blank">→ Ophthalmology Advisor</a></li>
      <li><strong>ATSN-201 (Atsena Therapeutics):</strong> Terapia génica para retinosquisis ligada al X. Dosificación completa enero 2026 en ensayo LIGHTHOUSE Fase 1/2/3, incluyendo cohortes adultas y pediátricas. Sin eventos adversos serios. <a class="src-link" href="https://www.ophthalmologytimes.com/view/ophthalmology-pipeline-milestones-for-q2-2026" target="_blank">→ Ophthalmology Times</a></li>
      <li><strong>OPGx-BEST1 (Opus Genetics):</strong> Terapia génica para distrofia macular viteliforme de Best. Datos preliminares del ensayo BIRD-1 Fase 1/2 esperados Q1 2026. <a class="src-link" href="https://www.ophthalmologytimes.com/view/ophthalmology-pipeline-watch-key-trial-results-and-pdufa-dates-for-q1-2026" target="_blank">→ Ophthalmology Times</a></li>
    </ul>
  </div>

  <div class="card">
    <h3>👁️ Ojo Seco — Pipeline Activo Post-CRL de Reproxalap</h3>
    <ul>
      <li><strong>Tyrptyr (Acoltremon 0.003%):</strong> <span class="badge badge-green">Aprobado FDA Mayo 2025</span> — Primer agonista TRPM8 aprobado para signos y síntomas de ojo seco. <a class="src-link" href="https://www.aao.org/eye-health/tips-prevention/new-dry-eye-treatments-ocular-surface-disease" target="_blank">→ AAO</a></li>
      <li><strong>OCS-02 (Licaminlimab):</strong> Biológico anti-TNFα tópico. Resultados positivos Fase IIb RELIEF — mejoras significativas en tinción con fluoresceína y test de Schirmer. Mejor efecto en pacientes con biomarcador genético TNFR1. <a class="src-link" href="https://www.optometrytimes.com/view/envision-2026-emerging-treatments-pipeline-dry-eye-disease" target="_blank">→ Optometry Times</a></li>
      <li><strong>ST-100:</strong> Repara selectivamente colágeno dañado en ojo seco. Fase III completada, resultados esperados 2026. <a class="src-link" href="https://www.reviewofophthalmology.com/article/the-evolving-landscape-of-dryeye-therapeutics" target="_blank">→ Review of Ophthalmology</a></li>
      <li><strong>Perfluorohexyloctane:</strong> "Escudo de evaporación" que puede combinarse con agentes antiinflamatorios e inmunomoduladores tópicos. <a class="src-link" href="https://www.optometrytimes.com/view/envision-2026-emerging-treatments-pipeline-dry-eye-disease" target="_blank">→ Optometry Times</a></li>
    </ul>
  </div>
</div>

<!-- ============ MERCADO Y NEGOCIO ============ -->
<div class="tab-content" id="mercado">
  <div class="card">
    <h3>📈 Mercado Global de Oftalmología 2026</h3>
    <div class="stat-grid">
      <div class="stat-card"><div class="number">$55.5B</div><div class="label">Valor del mercado 2026</div></div>
      <div class="stat-card"><div class="number">$92.7B</div><div class="label">Proyección 2035</div></div>
      <div class="stat-card"><div class="number">6.76%</div><div class="label">CAGR hasta 2030</div></div>
      <div class="stat-card"><div class="number">29%</div><div class="label">Crecimiento anual MIGS</div></div>
    </div>
    <p>El mercado avanzó de $63.71B (2024) a $67.85B (2025). La adopción de procedimientos mínimamente invasivos, IOLs avanzadas e integración de IA son los principales drivers de crecimiento. <a class="src-link" href="https://market.us/report/ophthalmology-market/" target="_blank">→ Market.us</a></p>
  </div>

  <div class="card">
    <h3>🏢 M&A y Consolidación</h3>
    <p>Las prácticas oftalmológicas representan uno de los segmentos más activos en M&A de consultorios médicos, impulsadas por demografía favorable, ingresos procedimentales sólidos y oportunidades de servicios auxiliares que generan flujos de caja estables. <a class="src-link" href="https://www.healthfmv.com/post/ophthalmology-valuation-guide" target="_blank">→ HealthFMV</a></p>
    <div class="highlight-box">
      <strong>Perspectiva 2026:</strong> El panorama es cautelosamente optimista para prácticas diversificadas que aprovechen capacidades quirúrgicas office-based, upgrades de IOL premium y servicios auxiliares de alto margen para compensar presiones de reembolso. Las prácticas dependientes de cataratas facility-based pueden enfrentar compresión de márgenes.
    </div>
  </div>

  <div class="card">
    <h3>🌐 Tecnología Advanced en Oftalmología</h3>
    <p>El mercado de tecnología avanzada en oftalmología proyecta alcanzar USD 17.43 mil millones para 2034, impulsado por biológicos (terapia génica, células madre), telemedicina e IA diagnóstica. <a class="src-link" href="https://www.precedenceresearch.com/advanced-ophthalmology-technology-market" target="_blank">→ Precedence Research</a></p>
  </div>
</div>

<!-- ============ CONTROL DE MIOPÍA ============ -->
<div class="tab-content" id="miopia">
  <div class="card">
    <h3>👶 Control de Miopía — Estado del Arte 2026</h3>
    <p>Desde la revisión del International Myopia Institute de 2019, las opciones de tratamiento han crecido en cinco categorías: ópticas, farmacológicas, ambientales/conductuales, luz coloreada y quirúrgicas. <a class="src-link" href="https://iovs.arvojournals.org/article.aspx?articleid=2803079" target="_blank">→ IOVS/ARVO</a></p>
  </div>

  <div class="card">
    <h3>💊 Farmacológico: Atropina Baja Dosis</h3>
    <p>La atropina baja dosis sigue siendo el único tratamiento farmacológico considerado efectivo para el manejo de miopía. La concentración de <strong>0.05%</strong> parece óptima, balanceando eficacia clínica con efectos secundarios mínimos (rango efectivo: 0.01%-0.05%). <a class="src-link" href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12448128/" target="_blank">→ PMC/IMI</a></p>
  </div>

  <div class="card">
    <h3>👓 Lentes Espectrales y de Contacto</h3>
    <ul>
      <li><strong>Lentes de defocus simultáneo</strong> (DIMS, HALT, CARE) y lentes de difusión moduladora de contraste (DOT) han demostrado reducciones consistentes y clínicamente significativas en elongación axial.</li>
      <li><strong>SightGlass Vision</strong> presenta nuevos datos en el Netherlands Contact Lens Congress 2026. <a class="src-link" href="https://eyewire.news/news/sightglass-vision-to-present-new-myopia-control-research-at-2026-netherlands-contact-lens-congress" target="_blank">→ Eyewire</a></li>
      <li><strong>Ortoqueratología:</strong> Reducción de elongación axial del 43-63% en estudios controlados.</li>
      <li><strong>Lentes de contacto dual-focus:</strong> Eficacia sustancial demostrada en estudios controlados.</li>
    </ul>
  </div>

  <div class="card">
    <h3>🔴 Terapia de Luz Roja de Baja Intensidad (RLRL)</h3>
    <p>La terapia de luz roja repetida de baja intensidad muestra reducciones prometedoras a corto plazo en elongación axial, aunque la seguridad a largo plazo y efectos rebote siguen siendo inciertos. <a class="src-link" href="https://iovs.arvojournals.org/article.aspx?articleid=2803078" target="_blank">→ IOVS/ARVO</a></p>
  </div>

  <div class="card">
    <h3>🔗 Terapia Combinada — La Frontera</h3>
    <p>La terapia combinada (vías ópticas + farmacológicas) muestra beneficios aditivos, particularmente en niños con control inadecuado con monoterapia. Esto refuerza la necesidad de protocolos personalizados según el perfil de cada paciente. <a class="src-link" href="https://www.mdpi.com/2077-0383/15/4/1545" target="_blank">→ Journal of Clinical Medicine</a></p>
    <div class="action-item"><strong>Acción:</strong> Desarrollar protocolo institucional de control de miopía que incluya terapia combinada escalonada (atropina + lentes de defocus) para población pediátrica del Instituto.</div>
  </div>
</div>

<!-- ============ OPORTUNIDADES IIT ============ -->
<div class="tab-content" id="iit">
  <div class="card iit-card">
    <h3>🎯 VENTAJA ESTRATÉGICA DE INSTITUTO DE OJOS PARA IITs</h3>
    <div class="highlight-box">
      <p><strong>La oportunidad es clara y urgente:</strong></p>
      <ul>
        <li>🏝️ <strong>Jurisdicción FDA</strong> + 100% población hispana = combinación única a nivel mundial</li>
        <li>📊 <strong>58,000+ pacientes activos</strong> = pool de reclutamiento masivo y listo</li>
        <li>🔬 Solo <strong>3.4% de participantes en ensayos de glaucoma son hispanos</strong> — esta brecha es una oportunidad</li>
        <li>⚠️ <strong>Prevalencia elevada:</strong> DM más alta entre hispanos, RD ~33% en Caribe, glaucoma ~5% (15% en >70 años)</li>
        <li>📈 La FDA y la industria están bajo presión creciente para diversificar ensayos clínicos</li>
      </ul>
      <p style="margin-top:0.8rem;"><a class="src-link" href="https://pmc.ncbi.nlm.nih.gov/articles/PMC8132140/" target="_blank">→ PMC: Disparidades raciales en ensayos de glaucoma</a> | <a class="src-link" href="https://pmc.ncbi.nlm.nih.gov/articles/PMC8063130/" target="_blank">→ JAMA Ophthalmology: Disparidades en ensayos FDA</a> | <a class="src-link" href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0296998" target="_blank">→ PLOS ONE: RD en LatAm/Caribe</a></p>
    </div>
  </div>

  <!-- IIT Proposal 1 -->
  <div class="iit-proposal">
    <h4>📌 IIT-1: "CARIBE-DME" — Respuesta a Faricimab en DME en Población Hispana Caribeña</h4>
    <div><span class="tag">RETINA</span><span class="tag">DME</span><span class="tag">ANTI-VEGF</span><span class="tag">DIVERSIDAD</span></div>
    <p style="margin-top:0.8rem;"><strong>Concepto:</strong> Estudio prospectivo de respuesta al tratamiento con faricimab (Vabysmo®) en pacientes hispanos treatment-naïve con DME, evaluando intervalos de retratamiento y respuesta anatómica/funcional en esta población subrepresentada.</p>
    <p><strong>Justificación:</strong> La FDA está exigiendo mayor diversidad en ensayos. Roche/Genentech ya tiene un estudio Fase 4 específico para poblaciones subrepresentadas con DME tratadas con faricimab. PR ofrece el sitio ideal por jurisdicción FDA y pool 100% hispano. La prevalencia de RD en el Caribe (33.3%) garantiza reclutamiento rápido.</p>
    <p><strong>Reclutamiento estimado:</strong> De 58K pacientes, ~15% con DM = ~8,700 → ~33% con RD = ~2,871 → meta: 150-200 pacientes en 6-8 meses.</p>
    <p><strong>Sponsor potencial:</strong> <strong>Roche/Genentech</strong> (fabricante de Vabysmo). También considerar Regeneron (Eylea HD) para estudio comparativo.</p>
    <p><strong>Financiamiento:</strong> Roche Medical Affairs / IISR Program (Investigator-Initiated Study Request). Contactar: <em>genentech-iis@gene.com</em></p>
    <div class="action-item"><strong>Acción inmediata:</strong> Enviar Letter of Intent a Roche/Genentech IISR program referenciando su propio estudio Fase 4 de diversidad en DME y posicionando Instituto de Ojos como sitio complementario con población 100% hispana bajo jurisdicción FDA.</div>
  </div>

  <!-- IIT Proposal 2 -->
  <div class="iit-proposal">
    <h4>📌 IIT-2: "BORICUA-GLAUCOMA" — Neuroprotección con PER-001 en Glaucoma en Hispanos</h4>
    <div><span class="tag">GLAUCOMA</span><span class="tag">NEUROPROTECCIÓN</span><span class="tag">MIGS</span><span class="tag">HISPANO</span></div>
    <p style="margin-top:0.8rem;"><strong>Concepto:</strong> Estudio de eficacia y seguridad del implante intravítreo PER-001 (antagonista de endotelina) en glaucoma de ángulo abierto en pacientes hispanos, evaluando flujo sanguíneo ocular y función visual/estructural.</p>
    <p><strong>Justificación:</strong> Solo el 3.4% de participantes en ensayos de glaucoma son hispanos pese a prevalencia ~5% (15% en >70 años). PER-001 (Perfuse Therapeutics) mostró datos prometedores Fase I/IIa. La neuroprotección es el nuevo paradigma más allá de reducción de PIO.</p>
    <p><strong>Reclutamiento estimado:</strong> De 58K pacientes, ~5% con glaucoma = ~2,900 → meta: 60-80 pacientes.</p>
    <p><strong>Sponsor potencial:</strong> <strong>Perfuse Therapeutics</strong>. También considerar AbbVie (Allergan) para estudios con prostaglandinas de nueva generación.</p>
    <div class="action-item"><strong>Acción inmediata:</strong> Contactar Perfuse Therapeutics vía su portal de clinical affairs. Presentar propuesta en ASCRS 2026 (Washington DC, abril).</div>
  </div>

  <!-- IIT Proposal 3 -->
  <div class="iit-proposal">
    <h4>📌 IIT-3: "PR-SCREEN-AI" — Validación de IA para Screening de RD en Población Hispana</h4>
    <div><span class="tag">IA</span><span class="tag">SCREENING</span><span class="tag">RD</span><span class="tag">VALIDACIÓN</span></div>
    <p style="margin-top:0.8rem;"><strong>Concepto:</strong> Estudio de validación de algoritmos de IA (ej. Altris, IDx-DR) para detección automatizada de retinopatía diabética en población hispana caribeña, comparando rendimiento diagnóstico vs. evaluación estándar por retinólogo.</p>
    <p><strong>Justificación:</strong> Los algoritmos de IA para screening de RD fueron entrenados predominantemente con datos de poblaciones caucásicas y asiáticas. No existen datos robustos de validación en hispanos caribeños. Esto es un gap regulatorio y científico significativo que la FDA reconoce.</p>
    <p><strong>Reclutamiento estimado:</strong> ~2,871 pacientes con RD del pool diabético → meta: 500-1,000 escaneos para validación.</p>
    <p><strong>Sponsor potencial:</strong> <strong>Digital Diagnostics (IDx)</strong>, <strong>Altris</strong>, <strong>Google Health</strong>. También NIH/NEI (R01 grant para disparidades).</p>
    <div class="action-item"><strong>Acción inmediata:</strong> Contactar Digital Diagnostics y Altris para explorar partnership de validación. Preparar abstract para ARVO 2026 (Denver, mayo).</div>
  </div>

  <!-- IIT Proposal 4 -->
  <div class="iit-proposal">
    <h4>📌 IIT-4: "TROPICALE" — Ojo Seco y OCS-02 en Clima Tropical Caribeño</h4>
    <div><span class="tag">OJO SECO</span><span class="tag">BIOLÓGICO</span><span class="tag">CLIMA TROPICAL</span><span class="tag">BIOMARCADOR</span></div>
    <p style="margin-top:0.8rem;"><strong>Concepto:</strong> Estudio de eficacia de OCS-02 (licaminlimab, anti-TNFα tópico) en ojo seco en pacientes hispanos en ambiente tropical caribeño, con estratificación por biomarcador genético TNFR1.</p>
    <p><strong>Justificación:</strong> El clima tropical de PR (humedad, UV) genera un perfil único de ojo seco. OCS-02 mostró resultados positivos en Fase IIb RELIEF, especialmente en pacientes con biomarcador TNFR1. No existen datos en poblaciones tropicales hispanas.</p>
    <p><strong>Reclutamiento estimado:</strong> Prevalencia ojo seco ~15-20% en población general → ~8,700-11,600 pacientes del pool → meta: 100-150.</p>
    <p><strong>Sponsor potencial:</strong> <strong>Oculis SA</strong> (fabricante de OCS-02). También Bausch + Lomb para estudios de perfluorohexyloctane en climas tropicales.</p>
    <div class="action-item"><strong>Acción inmediata:</strong> Contactar Oculis SA clinical development team. El factor diferenciador clave es ambiente tropical + población hispana + biomarcador TNFR1.</div>
  </div>

  <!-- IIT Proposal 5 -->
  <div class="iit-proposal">
    <h4>📌 IIT-5: "MIOPÍA-PR" — Control de Miopía con Terapia Combinada en Niños Hispanos</h4>
    <div><span class="tag">MIOPÍA</span><span class="tag">PEDIÁTRICO</span><span class="tag">COMBINACIÓN</span><span class="tag">HISPANO</span></div>
    <p style="margin-top:0.8rem;"><strong>Concepto:</strong> Ensayo prospectivo de terapia combinada (atropina 0.05% + lentes DOT) vs. monoterapia en progresión de miopía en niños hispanos de 6-14 años en PR.</p>
    <p><strong>Justificación:</strong> La terapia combinada es la nueva frontera en control de miopía pero no hay datos en población hispana caribeña. Los factores ambientales únicos de PR (UV elevado, estilo de vida outdoor) pueden influir en resultados.</p>
    <p><strong>Reclutamiento estimado:</strong> Población pediátrica del Instituto → meta: 100-120 niños (2 brazos).</p>
    <p><strong>Sponsor potencial:</strong> <strong>SightGlass Vision</strong> (lentes DOT), <strong>Hoya</strong> (MiYOSMART/DIMS), <strong>CooperVision</strong> (MiSight). Grant: NIH/NEI K23 o R21.</p>
    <div class="action-item"><strong>Acción inmediata:</strong> Presentar concept paper en Netherlands Contact Lens Congress 2026 donde SightGlass estará presentando datos. Iniciar diálogo con Hoya y CooperVision.</div>
  </div>

  <!-- IIT Proposal 6 -->
  <div class="iit-proposal">
    <h4>📌 IIT-6: "AXPAXLI-CARIBE" — Implante de Liberación Sostenida en DMAE Húmeda en Hispanos</h4>
    <div><span class="tag">RETINA</span><span class="tag">DMAE</span><span class="tag">LIBERACIÓN SOSTENIDA</span><span class="tag">CARGA DE TRATAMIENTO</span></div>
    <p style="margin-top:0.8rem;"><strong>Concepto:</strong> Estudio de vida real (real-world evidence) de AXPAXLI (OTX-TKI, implante intravítreo de axitinib) en DMAE húmeda en pacientes hispanos, evaluando reducción en carga de inyecciones y adherencia.</p>
    <p><strong>Justificación:</strong> La adherencia al tratamiento anti-VEGF mensual es un desafío mayor en PR por barreras geográficas y socioeconómicas. Un implante de 9-12 meses transformaría el manejo. Hispanos subrepresentados en ensayos de DMAE (>92% caucásicos en ensayos anti-VEGF).</p>
    <p><strong>Reclutamiento estimado:</strong> Pool de pacientes con DMAE del Instituto → meta: 50-75 pacientes.</p>
    <p><strong>Sponsor potencial:</strong> <strong>Ocular Therapeutix</strong>. Contactar via medical affairs/IIS portal.</p>
    <div class="action-item"><strong>Acción inmediata:</strong> Monitorear resultado de revisión FDA de AXPAXLI. Preparar LOI para Ocular Therapeutix tan pronto sea aprobado.</div>
  </div>

  <div class="card iit-card">
    <h3>📞 Resumen de Contactos para Acción Inmediata</h3>
    <table class="pdufa-table">
      <thead><tr><th>IIT</th><th>Sponsor</th><th>Canal de Contacto</th><th>Timing</th></tr></thead>
      <tbody>
        <tr><td>CARIBE-DME</td><td>Roche/Genentech</td><td>genentech-iis@gene.com / IISR Portal</td><td>Esta semana</td></tr>
        <tr><td>BORICUA-GLAUCOMA</td><td>Perfuse Therapeutics</td><td>Clinical Affairs Portal / ASCRS abril</td><td>Antes de ASCRS</td></tr>
        <tr><td>PR-SCREEN-AI</td><td>Digital Diagnostics / Altris</td><td>Partnership inquiry / ARVO mayo</td><td>2 semanas</td></tr>
        <tr><td>TROPICALE</td><td>Oculis SA</td><td>Clinical Development Team</td><td>Q2 2026</td></tr>
        <tr><td>MIOPÍA-PR</td><td>SightGlass / Hoya / CooperVision</td><td>R&D partnership</td><td>Q2 2026</td></tr>
        <tr><td>AXPAXLI-CARIBE</td><td>Ocular Therapeutix</td><td>Medical Affairs / IIS Portal</td><td>Post-aprobación FDA</td></tr>
      </tbody>
    </table>
  </div>
</div>

<!-- ============ CONGRESOS 2026-2027 ============ -->
<div class="tab-content" id="congresos">
  <div class="card">
    <h3>🗓️ Congresos de Oftalmología 2026</h3>
    <table class="congress-table">
      <thead><tr><th>Congreso</th><th>Fecha</th><th>Ubicación</th><th>Relevancia para IdO</th></tr></thead>
      <tbody>
        <tr>
          <td><strong>ASCRS 2026</strong></td>
          <td>10–13 Abril 2026</td>
          <td>Washington, DC</td>
          <td><span class="badge badge-green">⭐ Prioridad Alta</span> — Reuniones con sponsors IIT; IOLs; MIGS. <a class="src-link" href="https://annualmeeting.ascrs.org/" target="_blank">→ ASCRS</a></td>
        </tr>
        <tr>
          <td><strong>ARVO 2026</strong></td>
          <td>3–7 Mayo 2026</td>
          <td>Denver, USA</td>
          <td><span class="badge badge-green">⭐ Prioridad Alta</span> — Presentar abstracts IIT; IA; terapia génica. <a class="src-link" href="https://www.aao.org/about/related-organizations/subspecialty-society-meetings" target="_blank">→ AAO Calendar</a></td>
        </tr>
        <tr>
          <td><strong>WOC 2026</strong></td>
          <td>26–29 Junio 2026</td>
          <td>Praga, República Checa</td>
          <td><span class="badge badge-yellow">Networking internacional</span></td>
        </tr>
        <tr>
          <td><strong>AAO 2026</strong></td>
          <td>9–12 Octubre 2026</td>
          <td>New Orleans, LA</td>
          <td><span class="badge badge-green">⭐ Prioridad Alta</span> — Principal congreso anual. <a class="src-link" href="https://www.aao.org/annual-meeting" target="_blank">→ AAO</a></td>
        </tr>
      </tbody>
    </table>
  </div>

  <div class="card">
    <h3>🗓️ Congresos de Oftalmología 2027</h3>
    <table class="congress-table">
      <thead><tr><th>Congreso</th><th>Fecha</th><th>Ubicación</th></tr></thead>
      <tbody>
        <tr><td><strong>ASCRS 2027</strong></td><td>2–5 Abril 2027</td><td>San Diego, CA</td></tr>
        <tr><td><strong>AAO Mid-Year Forum 2027</strong></td><td>7–10 Abril 2027</td><td>Washington, D.C.</td></tr>
        <tr><td><strong>ARVO 2027</strong></td><td>2–6 Mayo 2027</td><td>San Diego, CA</td></tr>
        <tr><td><strong>AAO 2027</strong></td><td>12–15 Noviembre 2027</td><td>Las Vegas, NV</td></tr>
      </tbody>
    </table>
    <p style="margin-top:0.8rem; font-size:0.85rem;"><a class="src-link" href="https://www.market-scope.com/pages/news/7134/2025-ophthalmic-meetings-calendar" target="_blank">→ Market Scope: Calendario Oftalmológico</a> | <a class="src-link" href="https://pr-medicalevents.com/event/aao-2026/" target="_blank">→ PR Medical Events</a></p>
  </div>
</div>

<!-- ============ FUENTES ============ -->
<div class="tab-content" id="fuentes">
  <div class="card">
    <h3>📚 Fuentes Utilizadas en Este Reporte</h3>
    <h4 style="margin:1rem 0 0.5rem; color:var(--primary);">Journals Peer-Reviewed</h4>
    <ul class="sources-list">
      <li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC8132140/" target="_blank">PMC — Disparidades raciales en ensayos de glaucoma</a></li>
      <li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC8063130/" target="_blank">JAMA Ophthalmology — Disparidades en ensayos FDA 2000-2020</a></li>
      <li><a href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0296998" target="_blank">PLOS ONE — RD prevalencia en LatAm/Caribe</a></li>
      <li><a href="https://iovs.arvojournals.org/article.aspx?articleid=2803079" target="_blank">IOVS/ARVO — Miopía infantil: opciones de tratamiento</a></li>
      <li><a href="https://iovs.arvojournals.org/article.aspx?articleid=2803078" target="_blank">IOVS/ARVO — Miopía infantil: mecanismos y opciones emergentes</a></li>
      <li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12448128/" target="_blank">PMC/IMI — Intervenciones para control de miopía 2025</a></li>
      <li><a href="https://www.nature.com/articles/s41433-025-03745-x" target="_blank">Eye (Nature) — Futuro de cirugía de catarata</a></li>
      <li><a href="https://link.springer.com/article/10.1007/s40265-025-02237-2" target="_blank">Drugs (Springer) — Terapia génica en segmento posterior</a></li>
      <li><a href="https://www.frontiersin.org/journals/ophthalmology/articles/10.3389/fopht.2026.1766974/abstract" target="_blank">Frontiers in Ophthalmology — IA: confianza, sesgo y responsabilidad</a></li>
      <li><a href="https://www.nature.com/articles/s41433-025-04145-x" target="_blank">Eye (Nature) — Disparidades raciales en ensayos: barreras y soluciones</a></li>
      <li><a href="https://www.mdpi.com/2077-0383/15/4/1545" target="_blank">J Clinical Medicine — Estrategias de control de miopía</a></li>
      <li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC11540653/" target="_blank">PMC/Frontiers — OCT remoto: revisión sistemática</a></li>
    </ul>

    <h4 style="margin:1rem 0 0.5rem; color:var(--primary);">Industria y Medios Especializados</h4>
    <ul class="sources-list">
      <li><a href="https://www.ophthalmologytimes.com/view/how-ai-is-reshaping-ophthalmology-in-2025-and-beyond" target="_blank">Ophthalmology Times — IA en oftalmología</a></li>
      <li><a href="https://www.ophthalmologytimes.com/view/ophthalmology-pipeline-watch-key-trial-results-and-pdufa-dates-for-q1-2026" target="_blank">Ophthalmology Times — Pipeline Q1 2026</a></li>
      <li><a href="https://www.ophthalmologytimes.com/view/ophthalmology-pipeline-milestones-for-q2-2026" target="_blank">Ophthalmology Times — Pipeline Q2 2026</a></li>
      <li><a href="https://www.ophthalmologytimes.com/view/innovations-in-glaucoma-poised-for-breakthrough-in-2026-and-what-might-hold-the-back-" target="_blank">Ophthalmology Times — Innovaciones en glaucoma 2026</a></li>
      <li><a href="https://www.ophthalmologytimes.com/view/migs-continues-innovate-secure-place-glaucoma" target="_blank">Ophthalmology Times — MIGS innovación</a></li>
      <li><a href="https://www.ophthalmologytimes.com/view/altris-unveils-artificial-intelligence-platform-for-automated-oct-scans-analysis" target="_blank">Ophthalmology Times — Altris AI OCT</a></li>
      <li><a href="https://www.reviewofophthalmology.com/article/the-2026-glaucoma-pipeline" target="_blank">Review of Ophthalmology — Pipeline glaucoma 2026</a></li>
      <li><a href="https://www.reviewofophthalmology.com/article/the-2026-iol-preferences-survey" target="_blank">Review of Ophthalmology — Encuesta IOL 2026</a></li>
      <li><a href="https://glaucomatoday.com/resource/glaucoma-pipeline-2026" target="_blank">Glaucoma Today — Pipeline 2026</a></li>
      <li><a href="https://www.optometrytimes.com/view/envision-2026-emerging-treatments-pipeline-dry-eye-disease" target="_blank">Optometry Times — Pipeline ojo seco 2026</a></li>
      <li><a href="https://glance.eyesoneyecare.com/stories/2026-01-02/what-to-keep-an-eye-on-in-2026/" target="_blank">Eyes on Eyecare — Qué vigilar en 2026</a></li>
      <li><a href="https://eyewire.news/news/johnson-johnson-announces-fda-approval-of-tecni-puresee-iol-for-cataract-surgery" target="_blank">Eyewire — J&J Tecnis PureSee</a></li>
      <li><a href="https://eyewire.news/news/sightglass-vision-to-present-new-myopia-control-research-at-2026-netherlands-contact-lens-congress" target="_blank">Eyewire — SightGlass Vision miopía</a></li>
      <li><a href="https://www.ophthalmologyadvisor.com/features/retinal-gene-therapy-options-advance-through-clinical-trial-investigations/" target="_blank">Ophthalmology Advisor — Terapias génicas retinianas</a></li>
      <li><a href="https://www.fightingblindness.org/news/retinitis-pigmentosa-research-advances-899" target="_blank">Foundation Fighting Blindness — RP avances</a></li>
      <li><a href="https://www.aao.org/eye-health/tips-prevention/new-dry-eye-treatments-ocular-surface-disease" target="_blank">AAO — Nuevos tratamientos ojo seco</a></li>
      <li><a href="https://healthcare.utah.edu/moran/news/2026/01/powering-hope-rise-of-ai-ophthalmology" target="_blank">Moran Eye Center — IA en oftalmología</a></li>
    </ul>

    <h4 style="margin:1rem 0 0.5rem; color:var(--primary);">Comunicados de Prensa y Regulatorios</h4>
    <ul class="sources-list">
      <li><a href="https://ir.aldeyra.com/news-releases/news-release-details/aldeyra-therapeutics-announces-pdufa-extension-new-drug" target="_blank">Aldeyra Therapeutics — PDUFA reproxalap</a></li>
      <li><a href="https://www.hcplive.com/view/fda-issues-third-reproxalap-crl-for-dry-eye-disease" target="_blank">HCPLive — CRL reproxalap</a></li>
      <li><a href="https://www.prnewswire.com/news-releases/fda-accepts-viatris-supplemental-new-drug-application-for-mr-141-phentolamine-ophthalmic-solution-0-75-for-the-treatment-of-presbyopia-302696332.html" target="_blank">PRNewswire — Viatris MR-141</a></li>
    </ul>

    <h4 style="margin:1rem 0 0.5rem; color:var(--primary);">Mercado e Inteligencia de Negocios</h4>
    <ul class="sources-list">
      <li><a href="https://market.us/report/ophthalmology-market/" target="_blank">Market.us — Mercado oftalmología</a></li>
      <li><a href="https://www.precedenceresearch.com/advanced-ophthalmology-technology-market" target="_blank">Precedence Research — Tecnología avanzada</a></li>
      <li><a href="https://www.healthfmv.com/post/ophthalmology-valuation-guide" target="_blank">HealthFMV — Valoración y M&A</a></li>
      <li><a href="https://www.market-scope.com/pages/news/7134/2025-ophthalmic-meetings-calendar" target="_blank">Market Scope — Calendario de congresos</a></li>
    </ul>
  </div>
</div>

</div><!-- /container -->

<footer>
  <p>📊 Reporte generado automáticamente para Instituto de Ojos, Puerto Rico</p>
  <p>Semana del 24 al 30 de marzo de 2026 | Próximo reporte: 6 de abril de 2026</p>
  <p style="margin-top:0.5rem;">Este reporte es para uso interno únicamente. Las propuestas de IIT requieren revisión por el comité de investigación antes de proceder.</p>
</footer>

<script>
function showTab(tabId) {
  document.querySelectorAll('.tab-content').forEach(el => el.classList.remove('active'));
  document.querySelectorAll('.tab').forEach(el => el.classList.remove('active'));
  document.getElementById(tabId).classList.add('active');
  event.target.classList.add('active');
  window.scrollTo({top: document.querySelector('.tabs').offsetTop - 10, behavior: 'smooth'});
}
</script>

</body>
</html>
