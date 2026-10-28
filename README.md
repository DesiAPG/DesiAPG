<p align="center">
  <a href="https://www.duvanmarin.dev">
    <img src="./assets/banner.svg" alt="Duván Marín — Médico forense de software · Tech Autopsy" width="100%" />
  </a>
</p>

<p align="center">
  <a href="https://www.duvanmarin.dev"><img src="https://img.shields.io/badge/web-duvanmarin.dev-B57BFF?style=for-the-badge&labelColor=0C0A12" alt="Web" /></a>
  <a href="https://www.tiktok.com/@tech.autopsy"><img src="https://img.shields.io/badge/tiktok-@tech.autopsy-B57BFF?style=for-the-badge&logo=tiktok&logoColor=EDE9F5&labelColor=0C0A12" alt="TikTok" /></a>
  <a href="mailto:duvan.marinc10@gmail.com"><img src="https://img.shields.io/badge/mail-contacto-B57BFF?style=for-the-badge&logo=gmail&logoColor=EDE9F5&labelColor=0C0A12" alt="Email" /></a>
</p>

## `>` whoami

```yaml
name:      Duván Marín
role:      Médico forense de software · Backend Engineer
stack:     [Go, Java, AWS, PostgreSQL, Kafka, Docker]
focus:     sistemas de alta concurrencia, microservicios y bases de datos que no se caen
side_ops:  Tech Autopsy — post-mortems de los fallos de software más caros de la historia
status:    disponible para consultoría / freelance
```

## `>` expediente tech autopsy

Cada video disecciona un incidente real de producción. Cada autopsia deja una herramienta open source para que no te pase a ti.

| caso | incidente | causa de muerte | antídoto |
| :--: | :-- | :-- | :-- |
| `#001` | **GitLab · 2017** | `rm -rf` en la base de datos de producción equivocada: ~6 h de datos perdidos | [**go-guard**](https://github.com/DesiAPG/tech-autopsy-gitlab-2017) · Go |
| `#002` | **Cloudflare · 2019** | una regex con backtracking catastrófico en el WAF: CPU casi al 100 % en todo el mundo, 27 min caídos | [**regex-guard**](https://github.com/DesiAPG/tech-autopsy/tree/main/autopsia/002-cloudflare-2019-regex) · Go |
| `#003` | **Cloudflare · LavaRand** | una pared de lámparas de lava como fuente extra de entropía: basta con que una fuente siga secreta | [**entropy-mix**](https://github.com/DesiAPG/tech-autopsy/tree/main/anatomia/003-cloudflare-lavarand) · Go |
| `#004` | **Cloudflare · Pingora** | tiraron NGINX y escribieron su propio proxy en Rust: −70 % CPU y −67 % memoria con el mismo tráfico | [**pool-bench**](https://github.com/DesiAPG/tech-autopsy/tree/main/diagnostico/004-cloudflare-pingora) · Go |
| `#005` | **Cloudflare · Quicksilver** | un log con secuencia lleva cada cambio a todo el planeta en ~2 s, y un hueco se detecta | [**qs-mini**](https://github.com/DesiAPG/tech-autopsy/tree/main/anatomia/005-cloudflare-quicksilver) · Go |
| `#006` | **Cloudflare · 2025** | un archivo de features duplicado y un `unwrap()`: la peor caída desde 2019 | [**config-gate**](https://github.com/DesiAPG/tech-autopsy/tree/main/autopsia/006-cloudflare-2025-feature-file) · Go |
| `#007` | **AWS · 2017** | un input mal escrito en un comando del playbook retiró los servidores que sostenían S3 en us-east-1: ≈ 4 h caído | [**capacity-guard**](https://github.com/DesiAPG/tech-autopsy/tree/main/autopsia/007-aws-2017-s3) · Go |
| `#008` | **Figma · multijugador** | sin Operational Transformation: last-writer-wins por propiedad con un servidor central que decide el orden | [**multiplayer**](https://github.com/DesiAPG/tech-autopsy/tree/main/anatomia/008-figma-multiplayer) · Go |
| `#009` | **Discord · 2023** | particiones calientes en 177 nodos de Cassandra; con ScyllaDB y request coalescing en Rust, 72 nodos y p99 de 15 ms | [**coalesce-bench**](https://github.com/DesiAPG/tech-autopsy/tree/main/diagnostico/009-discord-coalescing) · Go |
| `#010` | **Stack Overflow · 2016** | 11 servidores web cuando les bastaba 1: caché L1 en memoria + L2 en Redis, y SQL solo si nadie lo tiene | [**cache-bench**](https://github.com/DesiAPG/tech-autopsy/tree/main/anatomia/010-stackoverflow-cache) · Go |
| `#011` | **Knight Capital · 2012** | un servidor de 8 sin deploy despertó código muerto de 2003 con una bandera reciclada: más de $460 M en ~45 min | [**deploy-verify**](https://github.com/DesiAPG/tech-autopsy/tree/main/autopsia/011-knight-capital-2012) · Go |
| `B01` | **PHP · 2026** *(boletín)* | PHP2Shell: dos RCE en el núcleo de PHP, CVSS 9.2; actualizar es la única mitigación confiable | [**php-patch-check**](https://github.com/DesiAPG/tech-autopsy/tree/main/boletin/b01-php-patch-check) · Go |
| `L01` | **CrowdStrike · 2024** *(video largo)* | un campo 21 que el sensor nunca entregaba, en un driver del kernel: 8,5 millones de equipos Windows caídos | [**content-gate**](https://github.com/DesiAPG/tech-autopsy/tree/main/autopsia/L01-crowdstrike-2024) · Go |
| `B02` | **Anthropic · Scion** *(boletín)* | por qué reemplazó Git en su monorepo: un almacén direccionado por contenido | [**content-addressed**](https://github.com/DesiAPG/tech-autopsy/tree/main/boletin/b02-content-addressed) · Go |
| `B03` | **GitLab · 2026** *(boletín)* | una regex con gravedad 10 de 10: desbordamiento de entero al compilarla, sin autenticación | [**gitlab-patch-check**](https://github.com/DesiAPG/tech-autopsy/tree/main/boletin/b03-gitlab-patch-check) · Go |
| `B04` | **Anthropic · S-1** *(boletín)* | sale a bolsa: limitada por cómputo, cuatro familias de chips y una capa de orquestación | [**chip-router**](https://github.com/DesiAPG/tech-autopsy/tree/main/boletin/b04-chip-router) · Go |

```diff
- [ERROR] db1.cluster · rm -rf /var/opt/gitlab/postgresql/data
+ [ OK  ] go-guard · comando destructivo bloqueado: requiere aprobación de un segundo ingeniero
- [ERROR] waf.edge · regla .*(?:.*=.*) → CPU ≈100 % en todo el planeta
+ [ OK  ] regex-guard · ✖ comodines-seguidos: la regla no pasa el CI
```

## `>` procedimientos

| | procedimiento | qué hago | entrega |
| :--: | :-- | :-- | :-- |
| `01` | **Autopsia de arquitectura** | Reviso tu sistema como si ya se hubiera caído: puntos únicos de falla, cuellos de botella, permisos peligrosos y backups sin probar. | Informe + plan de acción |
| `02` | **Cirugía de base de datos** | Índices, planes de ejecución, particionado y caché. Queries de segundos a milisegundos bajo carga real. | Cambios + métricas antes/después |
| `03` | **Guardarraíles cloud · AWS** | Infraestructura como código, autoescalado, observabilidad y controles para que un error humano no tumbe producción. | IaC + runbooks |

→ **[Solicitar una autopsia](mailto:duvan.marinc10@gmail.com)**

## `>` stack

<p>
  <img src="https://img.shields.io/badge/Go-14111D?style=flat-square&logo=go&logoColor=00ADD8" alt="Go" />
  <img src="https://img.shields.io/badge/Java-14111D?style=flat-square&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Spring_Boot-14111D?style=flat-square&logo=springboot&logoColor=6DB33F" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/AWS-14111D?style=flat-square&logo=amazonwebservices&logoColor=FF9900" alt="AWS" />
  <img src="https://img.shields.io/badge/PostgreSQL-14111D?style=flat-square&logo=postgresql&logoColor=4169E1" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/MySQL-14111D?style=flat-square&logo=mysql&logoColor=4479A1" alt="MySQL" />
  <img src="https://img.shields.io/badge/Redis-14111D?style=flat-square&logo=redis&logoColor=FF4438" alt="Redis" />
  <img src="https://img.shields.io/badge/Kafka-14111D?style=flat-square&logo=apachekafka&logoColor=white" alt="Kafka" />
  <img src="https://img.shields.io/badge/Docker-14111D?style=flat-square&logo=docker&logoColor=2496ED" alt="Docker" />
  <img src="https://img.shields.io/badge/Kubernetes-14111D?style=flat-square&logo=kubernetes&logoColor=326CE5" alt="Kubernetes" />
  <img src="https://img.shields.io/badge/Terraform-14111D?style=flat-square&logo=terraform&logoColor=844FBA" alt="Terraform" />
  <img src="https://img.shields.io/badge/Linux-14111D?style=flat-square&logo=linux&logoColor=FCC624" alt="Linux" />
</p>

---

<p align="center">
  <code>$ echo "¿tu sistema necesita una autopsia antes de morir?"</code><br />
  <a href="mailto:duvan.marinc10@gmail.com"><b>duvan.marinc10@gmail.com</b></a> · <a href="https://www.duvanmarin.dev"><b>www.duvanmarin.dev</b></a>
</p>
