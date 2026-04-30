DESIGN.md – Plomería Campos
1. Introducción

Este documento define las reglas de diseño para la implementación digital de la marca Plomería Campos. Está basado en el manual de identidad visual y adaptado para desarrollo web moderno.

El objetivo es garantizar consistencia visual, escalabilidad y correcta implementación en interfaces digitales.

2. Concepto de Marca

La marca representa:

Servicios de fontanería e hidrosanitaria
Soluciones técnicas confiables
Profesionalismo y durabilidad
Elementos conceptuales:
Llave / grifo → funcionalidad técnica
Letra "C" → identidad del fundador
Agua → fluidez, limpieza, confianza
3. Colores (Design Tokens)
🎨 Paleta principal
:root {
  --color-primary: #274e86;
  --color-secondary: #80cce2;
  --color-tertiary: #ceddef;
  --color-background: #eef0f4;
}
Uso recomendado
Color	Uso
#274e86	Primario (botones, headers, CTA)
#80cce2	Secundario (hover, highlights)
#ceddef	Fondos suaves, cards
#eef0f4	Background general
Significado
Azul oscuro → confianza, profesionalismo
Celeste → calma, limpieza, accesibilidad
4. Tipografía
Principal
Helvetica Neue LT Std 95 Black
Uso: títulos, branding, encabezados
Secundaria
Poppins SemiBold
Uso: UI, botones, textos digitales
Fallback web
font-family: "Poppins", "Helvetica Neue", Arial, sans-serif;
5. Sistema Tipográfico
Elemento	Tamaño	Peso
H1	32–40px	Bold
H2	24–32px	SemiBold
H3	20–24px	Medium
Body	14–16px	Regular
Small	12–14px	Regular
6. Logo
Variantes
Horizontal (preferido para web)
Vertical
Isotipo (solo ícono)
Reglas
Mantener área de seguridad (padding equivalente al alto de la "C")
No deformar ni rotar
No cambiar colores
No aplicar sombras ni contornos
Uso en web
Navbar → versión horizontal
Favicon → isotipo
Footer → versión completa
7. Espaciado y Layout
Escala de spacing
--space-xs: 4px;
--space-sm: 8px;
--space-md: 16px;
--space-lg: 24px;
--space-xl: 32px;
--space-2xl: 48px;
Grid
Base: 8px
Contenedor: max-width 1200px
Padding lateral: 16–24px
8. Componentes UI
Botones
.btn-primary {
  background-color: var(--color-primary);
  color: white;
  border-radius: 8px;
  padding: 10px 16px;
}

.btn-primary:hover {
  background-color: var(--color-secondary);
}
Cards
.card {
  background: white;
  border-radius: 12px;
  padding: 16px;
  border: 1px solid var(--color-tertiary);
}
Inputs
.input {
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 10px;
}

.input:focus {
  border-color: var(--color-primary);
}
9. Iconografía
Estilo: lineal o minimalista
Inspiración: herramientas de plomería
Evitar iconos complejos o caricaturescos
10. Imágenes
Estilo
Fotografía real (no stock genérico si es posible)
Contexto: obras, instalaciones, técnicos trabajando
Colores fríos y neutros
11. Patrones de Marca
Uso de formas fluidas (simulando agua)
Líneas curvas suaves
Fondos con degradados azul → celeste
12. UX / UI Guidelines
Principios
Claridad (servicio técnico directo)
Confianza (interfaces limpias)
Accesibilidad (contraste adecuado)
Botones clave
"Solicitar servicio"
"Cotizar ahora"
"Contacto"
13. Aplicaciones Web
Navbar
Logo izquierda
CTA a la derecha
Home
Hero con mensaje claro
Servicios destacados
CTA visible
Dashboard (si SaaS)
UI limpia
Uso fuerte de azul primario
Cards informativas
14. Usos Incorrectos (Digital)

❌ Cambiar colores
❌ Usar sombras en el logo
❌ Estirar o deformar
❌ Usar fondos no corporativos
❌ Mezclar tipografías fuera del sistema

15. Recomendaciones para Desarrollo
Usar variables CSS o Tailwind config
Crear un sistema de design tokens reutilizable
Mantener consistencia en todos los módulos (multi-tenant si aplica)
Centralizar estilos en theme global
16. Tailwind Config (Opcional)
theme: {
  extend: {
    colors: {
      primary: "#274e86",
      secondary: "#80cce2",
      tertiary: "#ceddef",
      background: "#eef0f4",
    }
  }
}
17. Conclusión

Este sistema de diseño garantiza:

Consistencia visual
Escalabilidad en productos digitales
Fidelidad al manual de marca

Debe aplicarse en todas las interfaces web, apps y material digital.