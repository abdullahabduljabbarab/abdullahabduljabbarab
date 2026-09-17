<img src="https://capsule-render.vercel.app/api?type=waving&height=190&color=0:0d1117,100:134e4a&text=Abdullah%20Abduljabbar&fontColor=e6edf3&fontSize=46&fontAlignY=36&desc=Software%20Engineer%20%C2%B7%20Cardiff%2C%20UK&descAlignY=58&descSize=17" width="100%" alt="Abdullah Abduljabbar, Software Engineer, Cardiff UK">

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=18&pause=1400&color=66D8D2&center=true&vCenter=true&width=640&lines=Payment+systems+built+to+survive+failure;Real-time+simulation+federated+over+DIS%2C+DDS+and+HLA;Correctness+enforced+at+the+boundary" alt="Payment systems built to survive failure. Real-time simulation federated over DIS, DDS and HLA. Correctness enforced at the boundary.">
</p>

<p align="center">
  <a href="https://www.abdullahabduljabbar.com/"><img src="https://img.shields.io/badge/Portfolio-0d1117?style=for-the-badge&logo=googlechrome&logoColor=66D8D2" alt="Portfolio"></a>
  <a href="https://www.linkedin.com/in/aajabbar"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge" alt="LinkedIn"></a>
  <a href="https://www.youtube.com/@AbdullahAmeedAbduljabbar"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube"></a>
</p>

<table>
<tr>
<td width="50%" valign="top">

**About me**

- 3+ years of paid development: multiplayer systems, SQL persistence, client-server architecture
- I build systems where correctness is the point: one owner per piece of state, explicit failure handling, verification against written requirements

</td>
<td width="50%" valign="top">

**Right now**

- Final year, BA (Hons) Computer Games Design, University of South Wales, on track for a First
- Open to full-time Software Engineer roles in Cardiff, Bristol, London or remote

</td>
</tr>
</table>

<a href="https://www.abdullahabduljabbar.com/ABS"><img src="./assets/abs-flow.svg" width="100%" alt="ABS Financial Systems: payments flowing through orchestrator, ledger, risk engine, Pub/Sub, notification and analytics"></a>

<table>
<tr>
<td width="48%" valign="middle"><a href="https://www.abdullahabduljabbar.com/ABS"><img src="https://github.com/abdullahabduljabbarab/abs-financial-systems/raw/main/docs/images/portal-trace.png" alt="ABS Engineering Portal payment trace"></a></td>
<td width="52%" valign="middle">

A distributed payments platform built around one authoritative double-entry ledger. Only the ledger can move money; orchestration, risk, notifications and analytics sit around it behind explicit contracts, live on Google Cloud.

<img src="https://img.shields.io/badge/Live%20failure%20scenarios-13%2F13%20passing-2ea44f?style=flat-square" alt="Live failure scenarios: 13/13 passing"> <img src="https://img.shields.io/badge/Requirements-16%20mapped-2ea44f?style=flat-square" alt="Requirements: 16 mapped"> <img src="https://img.shields.io/badge/Services-5%20on%20Cloud%20Run-4285F4?style=flat-square" alt="Services: 5 on Cloud Run"> <img src="https://img.shields.io/badge/CI%2FCD%20keys-0-7B42BC?style=flat-square" alt="CI/CD keys: 0">

<a href="https://www.abdullahabduljabbar.com/ABS"><b>Case study</b></a> · <a href="https://github.com/abdullahabduljabbarab/abs-financial-systems"><b>Source</b></a>

</td>
</tr>
</table>

<details>
<summary><b>Architecture and all 8 ABS repos</b></summary>

```mermaid
flowchart LR
  O[Payment Orchestrator] -->|decision| R[Risk Engine]
  O -->|reserve / capture / release| L[(Ledger)]
  O --> X[Simulated providers]
  L -->|outbox| Q{{Pub/Sub}}
  O -->|outbox| Q
  R -->|events| Q
  Q --> N[Notification]
  Q --> A[(Analytics / BigQuery)]
```

| Repo | What it does |
| --- | --- |
| [**abs-financial-systems**](https://github.com/abdullahabduljabbarab/abs-financial-systems) | System-of-systems architecture, requirements traceability, black-box verification harness and the Engineering Portal |
| [**ledger-api**](https://github.com/abdullahabduljabbarab/ledger-api) | Python / FastAPI double-entry ledger: idempotency, reconciliation, tamper-evident history |
| [**abs-ledger-spring**](https://github.com/abdullahabduljabbarab/abs-ledger-spring) | The ledger core rebuilt on Java 21 and Spring Boot, every invariant enforced in PostgreSQL, 15 Testcontainers tests |
| [**payment-orchestrator**](https://github.com/abdullahabduljabbarab/payment-orchestrator) | Reserve / capture / release lifecycle, provider routing, timeout reconciliation and compensation |
| [**risk-engine**](https://github.com/abdullahabduljabbarab/risk-engine) | Deterministic, versioned ALLOW / REVIEW / BLOCK decisions with explainable reasons |
| [**notification-service**](https://github.com/abdullahabduljabbarab/notification-service) | Downstream email and SMS simulation with per-channel idempotency and bounded retry |
| [**analytics-service**](https://github.com/abdullahabduljabbarab/analytics-service) | BigQuery event history and CQRS projections that rebuild deterministically |
| [**platform-infrastructure**](https://github.com/abdullahabduljabbarab/platform-infrastructure) | Terraform, Workload Identity Federation and least-privilege runtime identities |

</details>

<br>

<a href="https://www.abdullahabduljabbar.com/CLEARANCE"><img src="./assets/clearance-radar.svg" width="100%" alt="CLEARANCE: animated radar scope with a rotating sweep revealing aircraft contacts"></a>

<table>
<tr>
<td width="48%" valign="middle"><a href="https://www.abdullahabduljabbar.com/CLEARANCE"><img src="https://github.com/abdullahabduljabbarab/CLEARANCE/raw/main/Docs/Images/heroshot.png" alt="CLEARANCE main menu at Warton ACC"></a></td>
<td width="52%" valign="middle">

A C++ / Unreal Engine 5 ATC and air-defence synthetic training simulator built around one authoritative simulation state, with networked instructor and operator stations, radar and EW, replay and after-action review, and geospatial VR.

<img src="https://img.shields.io/badge/Automated%20tests-52-2ea44f?style=flat-square" alt="Automated tests: 52"> <img src="https://img.shields.io/badge/Requirements-69-2ea44f?style=flat-square" alt="Requirements: 69"> <img src="https://img.shields.io/badge/Federation%20paths-4-1f6feb?style=flat-square" alt="Federation paths: 4"> <img src="https://img.shields.io/badge/MBD%20workflows-3-E16737?style=flat-square" alt="MBD workflows: 3">

<a href="https://www.abdullahabduljabbar.com/CLEARANCE"><b>Case study</b></a> · <a href="https://github.com/abdullahabduljabbarab/CLEARANCE"><b>Source</b></a>

</td>
</tr>
</table>

<table>
<tr>
<td width="33%" align="center" valign="top"><a href="https://youtu.be/kii0oPH0a2I"><img src="https://img.youtube.com/vi/kii0oPH0a2I/maxresdefault.jpg" alt="Final showcase"></a><br><sub><b>Final showcase</b> · 5 min</sub></td>
<td width="33%" align="center" valign="top"><a href="https://youtu.be/trnNMP-3RLs"><img src="https://img.youtube.com/vi/trnNMP-3RLs/maxresdefault.jpg" alt="Full two-role playthrough"></a><br><sub><b>Full two-role playthrough</b> · 48 min</sub></td>
<td width="33%" align="center" valign="top"><a href="https://youtu.be/25d2I24uIs4"><img src="https://img.youtube.com/vi/25d2I24uIs4/maxresdefault.jpg" alt="Every C++ system explained"></a><br><sub><b>Every C++ system explained</b> · 58 min</sub></td>
</tr>
</table>

<p align="center"><sub>Deep dives: <a href="https://youtu.be/u7qeIkqkt4s">DIS + DDS + RTI Connext + HLA</a> · <a href="https://youtu.be/nqjFOimsYHw">Simulink subsystems live in UE5</a></sub></p>

<details>
<summary><b>Architecture and all 5 CLEARANCE repos</b></summary>

```mermaid
flowchart LR
  M[Simulink models] -->|Embedded Coder C| S((Authoritative<br/>sim tick))
  S --> D[IEEE 1278 DIS]
  S --> F[Fast DDS]
  S --> C[RTI Connext]
  S --> H[HLA-Evolved / OpenRTI]
```

| Repo | What it does |
| --- | --- |
| [**CLEARANCE**](https://github.com/abdullahabduljabbarab/CLEARANCE) | UE5 C++ simulator core: aircraft behaviour, radar / GCI, instructor tooling, replay / AAR, tests and documentation |
| [**clearance-federation**](https://github.com/abdullahabduljabbarab/clearance-federation) | DIS, Fast DDS, RTI Connext and HLA-Evolved federation stack with standalone consumers |
| [**autopilot-mbd**](https://github.com/abdullahabduljabbarab/autopilot-mbd) | Simulink cascade autopilot generated to portable C with Embedded Coder |
| [**radar-mbd**](https://github.com/abdullahabduljabbarab/radar-mbd) | Pulsed-radar DSP: LFM, MVDR beamforming, matched filter, range-Doppler, CA-CFAR |
| [**missile-mbd**](https://github.com/abdullahabduljabbarab/missile-mbd) | 3-DOF proportional-navigation guidance model with generated C and documented limitations |

</details>

<br>

<h2 align="center">Tech stack</h2>

<div align="center">
<table>
<tr>
<td align="right" valign="middle"><b>Languages</b></td>
<td align="left" valign="middle"><img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++"> <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java"> <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge" alt="SQL"></td>
</tr>
<tr>
<td align="right" valign="middle"><b>Backend</b></td>
<td align="left" valign="middle"><img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot"> <img src="https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white" alt="Hibernate"> <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI"></td>
</tr>
<tr>
<td align="right" valign="middle"><b>Data and messaging</b></td>
<td align="left" valign="middle"><img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/Flyway-CC0200?style=for-the-badge&logo=flyway&logoColor=white" alt="Flyway"> <img src="https://img.shields.io/badge/BigQuery-669DF6?style=for-the-badge&logo=googlebigquery&logoColor=white" alt="BigQuery"> <img src="https://img.shields.io/badge/Pub%2FSub-4285F4?style=for-the-badge&logo=googlepubsub&logoColor=white" alt="Pub/Sub"></td>
</tr>
<tr>
<td align="right" valign="middle"><b>Cloud and DevOps</b></td>
<td align="left" valign="middle"><img src="https://img.shields.io/badge/Google%20Cloud-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white" alt="Google Cloud"> <img src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" alt="Terraform"> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"> <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions"></td>
</tr>
<tr>
<td align="right" valign="middle"><b>Testing</b></td>
<td align="left" valign="middle"><img src="https://img.shields.io/badge/JUnit%205-25A162?style=for-the-badge&logo=junit5&logoColor=white" alt="JUnit 5"> <img src="https://img.shields.io/badge/Testcontainers-17A6B2?style=for-the-badge" alt="Testcontainers"></td>
</tr>
<tr>
<td align="right" valign="middle"><b>Simulation</b></td>
<td align="left" valign="middle"><img src="https://img.shields.io/badge/Unreal%20Engine%205-313131?style=for-the-badge&logo=unrealengine&logoColor=white" alt="Unreal Engine 5"> <img src="https://img.shields.io/badge/MATLAB%20%2F%20Simulink-E16737?style=for-the-badge" alt="MATLAB / Simulink"> <img src="https://img.shields.io/badge/DIS%20%2F%20DDS%20%2F%20HLA-1f6feb?style=for-the-badge" alt="DIS / DDS / HLA"> <img src="https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white" alt="Wireshark"></td>
</tr>
</table>
</div>

<img src="https://capsule-render.vercel.app/api?type=waving&height=110&section=footer&color=0:134e4a,100:0d1117" width="100%" alt="">
