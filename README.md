<p align="center">
  <a href="https://www.duvanmarin.dev">
    <img src="./assets/banner.svg" alt="Duván Marín — Backend & Systems Architecture" width="100%" />
  </a>
</p>

<p align="center">
  <a href="https://www.duvanmarin.dev"><img src="https://img.shields.io/badge/web-duvanmarin.dev-00FF66?style=for-the-badge&labelColor=0B0E14" alt="Web" /></a>
  <a href="https://www.tiktok.com/@tech.autopsy"><img src="https://img.shields.io/badge/tiktok-@tech.autopsy-FF3366?style=for-the-badge&logo=tiktok&logoColor=FF3366&labelColor=0B0E14" alt="TikTok" /></a>
  <a href="mailto:duvan.marinc10@gmail.com"><img src="https://img.shields.io/badge/mail-contacto-00E5FF?style=for-the-badge&logo=gmail&logoColor=00E5FF&labelColor=0B0E14" alt="Email" /></a>
</p>

## `>` whoami

```yaml
name:      Duván Marín
role:      Backend Engineer · Systems Architecture
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

```diff
- [ERROR] db1.cluster · rm -rf /var/opt/gitlab/postgresql/data
+ [ OK  ] go-guard · comando destructivo bloqueado: requiere aprobación de un segundo ingeniero
```

## `>` servicios

| | servicio | qué hago |
| :--: | :-- | :-- |
| 🟥 | **Diseño de microservicios** | Descomposición de monolitos, contratos entre servicios, colas y resiliencia (circuit breaker, retries, idempotencia). |
| 🟦 | **Optimización de bases de datos** | Índices, planes de ejecución, particionado y caché. Queries de segundos a milisegundos bajo carga real. |
| 🟩 | **Cloud & AWS** | Infraestructura como código, autoescalado, observabilidad y guardarraíles para que nadie borre producción un viernes. |

## `>` stack

<p>
  <img src="https://img.shields.io/badge/Go-0B0E14?style=flat-square&logo=go&logoColor=00ADD8" alt="Go" />
  <img src="https://img.shields.io/badge/Java-0B0E14?style=flat-square&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Spring_Boot-0B0E14?style=flat-square&logo=springboot&logoColor=6DB33F" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/AWS-0B0E14?style=flat-square&logo=amazonwebservices&logoColor=FF9900" alt="AWS" />
  <img src="https://img.shields.io/badge/PostgreSQL-0B0E14?style=flat-square&logo=postgresql&logoColor=4169E1" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/MySQL-0B0E14?style=flat-square&logo=mysql&logoColor=4479A1" alt="MySQL" />
  <img src="https://img.shields.io/badge/Redis-0B0E14?style=flat-square&logo=redis&logoColor=FF4438" alt="Redis" />
  <img src="https://img.shields.io/badge/Kafka-0B0E14?style=flat-square&logo=apachekafka&logoColor=white" alt="Kafka" />
  <img src="https://img.shields.io/badge/Docker-0B0E14?style=flat-square&logo=docker&logoColor=2496ED" alt="Docker" />
  <img src="https://img.shields.io/badge/Kubernetes-0B0E14?style=flat-square&logo=kubernetes&logoColor=326CE5" alt="Kubernetes" />
  <img src="https://img.shields.io/badge/Terraform-0B0E14?style=flat-square&logo=terraform&logoColor=844FBA" alt="Terraform" />
  <img src="https://img.shields.io/badge/Linux-0B0E14?style=flat-square&logo=linux&logoColor=FCC624" alt="Linux" />
</p>

---

<p align="center">
  <code>$ echo "¿tu sistema necesita una autopsia antes de morir?"</code><br />
  <a href="mailto:duvan.marinc10@gmail.com"><b>duvan.marinc10@gmail.com</b></a> · <a href="https://www.duvanmarin.dev"><b>www.duvanmarin.dev</b></a>
</p>
