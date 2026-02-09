---
title: "Aretaslab"
date: 2026-02-09T23:00:00Z
draft: false
---

{{ define "main" }}

<!-- Hero Section -->
<section class="hero">
    <div class="container">
        <div class="hero-content">
            <div class="hero-text">
                <h1>{{ .Title }}</h1>
                <p class="hero-subtitle">{{ .Site.Params.description }}</p>
                <a href="/contacto" class="btn">Hablemos de tu proyecto</a>
                <a href="/productos" class="btn btn-ghost" style="margin-left: 1rem;">Ver productos</a>
            </div>
            <div class="hero-image">
                <svg viewBox="0 0 400 400" fill="none">
                    <circle cx="200" cy="200" r="180" fill="#E6E1DD" opacity="0.5"/>
                    <circle cx="200" cy="200" r="120" fill="#D4A373" opacity="0.3"/>
                    <rect x="120" y="100" width="160" height="180" rx="16" fill="#FFFFFF" stroke="#D4A373" stroke-width="3"/>
                    <rect x="140" y="130" width="120" height="8" rx="4" fill="#E6E1DD"/>
                    <rect x="140" y="150" width="80" height="8" rx="4" fill="#E6E1DD"/>
                    <rect x="140" y="180" width="120" height="60" rx="8" fill="#B7B7A4" opacity="0.5"/>
                    <circle cx="280" cy="120" r="30" fill="#D4A373"/>
                    <path d="M280 105V135M265 120H295" stroke="#4A443F" stroke-width="4" stroke-linecap="round"/>
                    <circle cx="100" cy="280" r="20" fill="#A98467"/>
                    <path d="M95 275L105 285M105 275L95 285" stroke="#4A443F" stroke-width="2"/>
                    <circle cx="320" cy="300" r="25" fill="#B7B7A4"/>
                    <path d="M310 300H330M320 290V310" stroke="#4A443F" stroke-width="2" stroke-linecap="round"/>
                </svg>
            </div>
        </div>
    </div>
</section>

<!-- Services Grid -->
<section id="productos">
    <div class="container">
        <h2 class="section-title">Nuestros Productos</h2>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">
                    <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <rect x="2" y="5" width="20" height="14" rx="2"/>
                        <line x1="2" y1="10" x2="22" y2="10"/>
                    </svg>
                </div>
                <h3>Gastos Familia</h3>
                <p style="color: var(--text-muted); margin-bottom: 1.5rem;">Gestión inteligente de gastos familiares con reconocimiento automático de tickets de compra.</p>
                <a href="#" class="btn btn-ghost">Saber más</a>
            </div>
            <div class="service-card">
                <div class="service-icon">
                    <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"/>
                    </svg>
                </div>
                <h3>Mcpone</h3>
                <p style="color: var(--text-muted); margin-bottom: 1.5rem;">Próximamente - Solución de gestión MCP para desarrolladores.</p>
                <span style="color: var(--text-muted); font-size: 0.9rem;">En desarrollo</span>
            </div>
            <div class="service-card">
                <div class="service-icon">
                    <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <circle cx="12" cy="12" r="10"/>
                        <polygon points="10 8 16 12 10 16 10 8"/>
                    </svg>
                </div>
                <h3>Solorol</h3>
                <p style="color: var(--text-muted); margin-bottom: 1.5rem;">Próximamente - Plataforma de gestión de juegos de rol.</p>
                <span style="color: var(--text-muted); font-size: 0.9rem;">En desarrollo</span>
            </div>
        </div>
    </div>
</section>

<!-- Values Zig-Zag -->
<section class="values-section">
    <div class="container">
        <h2 class="section-title">Nuestros Valores</h2>

        <div class="value-item">
            <div class="value-text">
                <h3>Cooperativismo</h3>
                <p style="color: var(--text-muted);">Somos una cooperativa de trabajo. Las decisiones se toman entre todos, compartiendo responsabilidades y beneficios.</p>
            </div>
            <div class="value-image">
                <svg viewBox="0 0 300 200" fill="none">
                    <circle cx="150" cy="80" r="40" fill="#D4A373" opacity="0.3"/>
                    <circle cx="80" cy="140" r="30" fill="#A98467" opacity="0.3"/>
                    <circle cx="220" cy="140" r="30" fill="#B7B7A4" opacity="0.3"/>
                    <line x1="150" y1="80" x2="80" y2="140" stroke="#D4A373" stroke-width="2"/>
                    <line x1="150" y1="80" x2="220" y2="140" stroke="#D4A373" stroke-width="2"/>
                    <line x1="80" y1="140" x2="220" y2="140" stroke="#D4A373" stroke-width="2"/>
                </svg>
            </div>
        </div>

        <div class="value-item">
            <div class="value-text">
                <h3>Transparencia</h3>
                <p style="color: var(--text-muted);">Todo lo que hacemos es abierto. Código fuente accesible, procesos claros y comunicación honesta con clientes y comunidad.</p>
            </div>
            <div class="value-image">
                <svg viewBox="0 0 300 200" fill="none">
                    <rect x="100" y="50" width="100" height="120" rx="8" fill="#FFFFFF" stroke="#D4A373" stroke-width="2"/>
                    <rect x="115" y="70" width="70" height="8" rx="4" fill="#E6E1DD"/>
                    <rect x="115" y="90" width="50" height="8" rx="4" fill="#E6E1DD"/>
                    <rect x="115" y="110" width="70" height="6" rx="3" fill="#B7B7A4" opacity="0.5"/>
                    <rect x="115" y="125" width="60" height="6" rx="3" fill="#B7B7A4" opacity="0.5"/>
                    <rect x="115" y="140" width="40" height="6" rx="3" fill="#B7B7A4" opacity="0.5"/>
                </svg>
            </div>
        </div>

        <div class="value-item">
            <div class="value-text">
                <h3>Software Libre</h3>
                <p style="color: var(--text-muted);">Utilizamos y contribuimos al software libre. Creemos que la tecnología debe ser accesible y mejorable por todos.</p>
            </div>
            <div class="value-image">
                <svg viewBox="0 0 300 200" fill="none">
                    <path d="M150 40 L100 160 L200 160 Z" fill="#D4A373" opacity="0.3" stroke="#D4A373" stroke-width="2"/>
                    <circle cx="150" cy="40" r="20" fill="#A98467"/>
                    <circle cx="100" cy="160" r="15" fill="#B7B7A4"/>
                    <circle cx="200" cy="160" r="15" fill="#B7B7A4"/>
                    <circle cx="150" cy="100" r="8" fill="#FFFFFF" stroke="#D4A373" stroke-width="2"/>
                </svg>
            </div>
        </div>
    </div>
</section>

<!-- Social Proof -->
<section class="social-proof">
    <div class="container">
        <h2 style="text-align: center; margin-bottom: 3rem; font-size: 1.5rem; color: var(--text-muted);">Formamos parte de la economía social</h2>
        <div class="partners-grid">
            <span class="partner-logo">Coopdevs</span>
            <span class="partner-logo">Galicloud</span>
            <span class="partner-logo">Som Energia</span>
            <span class="partner-logo">La Comunal</span>
        </div>
    </div>
</section>

{{ end }}
