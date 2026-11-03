CheckEarth — Defectos en puestas a tierra (CD/CT)
--------------------------------------------------
Archivo único: index.html (HTML + CSS + JS). Súbelo al repositorio para GitHub Pages.

Uso:
- Elige la provincia: se cargan su Id y su límite de herrajes, y se aplican sus criterios.
- Rellena línea, nº CD y fecha; Rm de herrajes, límite del proyecto (opcional) e Id.
- Añade hasta 6 transformadores con Rn (neutro) y Rmn (herrajes–neutro).
- El resultado se calcula al momento. Guardar lo pasa al historial; Compartir lo envía por WhatsApp.
- Historial → Exportar Excel (CSV).
- Engranaje (⚙) → valores por provincia (Id, límite herrajes, Vmáx, Rn máx), valores generales
  y provincia predeterminada. "Exportar tabla" genera un .json que otro usuario puede importar.

Valores de fábrica por provincia:
- Están en index.html, en la constante TABLA_BASE. Lo que pongas ahí lo tendrá cualquiera que abra la app.
  Ejemplo:  'Cáceres':{Id:300,Lim:400},

Comprobaciones (Guía FED029):
- T51D  No existe PAT de protección / sin registro
- T53D  Rm > límite del proyecto o tabla territorial
- T55D  Vd = Rc × Id > Vmáx (1000 V), con Rc = (Rm + Rn − Rmn) / 2
- T62D  Rn neutro > 37 Ω
- T65D  No existe PAT de neutro
- Aviso de medidas incoherentes si Rc sale fuera de 0…min(Rm, Rn)

Herramienta orientativa: no sustituye el criterio en campo ni los procedimientos NEZ004/NMZ002.
