# Hi, I'm Pablo

<sub><img src="https://api.iconify.design/lucide:terminal.svg?color=%23569cd6" height="16" /></sub> Full Stack Developer &nbsp;·&nbsp; <sub><img src="https://api.iconify.design/lucide:map-pin.svg?color=%23569cd6" height="16" /></sub> Málaga, Spain &nbsp;·&nbsp; <sub><img src="https://api.iconify.design/lucide:compass.svg?color=%23569cd6" height="16" /></sub> Open to new opportunities

## About

Self-taught Full Stack developer, backend-leaning. I care about understanding how things work, not just making them run, and shipping quality code that's easier to maintain and debug.

I run Linux daily, self-host services on Proxmox, and use Coolify for deployment testing. Currently preparing for the AWS Certified Developer – Associate (DVA-C02) to strengthen my cloud and scalability skills.

![Java](https://img.shields.io/badge/Java-1E1E1E?style=flat&logo=openjdk&logoColor=ED8B00) ![TypeScript](https://img.shields.io/badge/TypeScript-1E1E1E?style=flat&logo=typescript&logoColor=3178C6) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-1E1E1E?style=flat&logo=springboot&logoColor=6DB33F) ![React](https://img.shields.io/badge/React-1E1E1E?style=flat&logo=react&logoColor=61DAFB) [![Expo](https://img.shields.io/badge/Expo-1E1E1E?logo=expo&logoColor=fff)](#) ![TailwindCSS](https://img.shields.io/badge/TailwindCSS-1E1E1E?style=flat&logo=tailwindcss&logoColor=06B6D4) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1E1E1E?style=flat&logo=postgresql&logoColor=4169E1) ![Redis](https://img.shields.io/badge/Redis-1E1E1E?style=flat&logo=redis&logoColor=DC382D) ![AWS](https://custom-icon-badges.demolab.com/badge/AWS-1E1E1E.svg?logo=aws&logoColor=FF9900) ![Docker](https://img.shields.io/badge/Docker-1E1E1E?style=flat&logo=docker&logoColor=2496ED) [![Coolify](https://img.shields.io/badge/Coolify-1E1E1E?logo=coolify&logoColor=6B16ED)](#)

## Let's Connect

[![LinkedIn](https://custom-icon-badges.demolab.com/badge/LinkedIn-1E1E1E?logo=linkedin-white)](https://www.linkedin.com/in/vlpablo/) [![Email](https://img.shields.io/badge/Email-1E1E1E?logo=protonmail&logoColor=6D4AFF)](mailto:contact@ivfro.st) [![Website](https://img.shields.io/badge/Portfolio-1E1E1E?logo=firefoxbrowser&logoColor=FF7139)](https://ivfro.st)

## Featured Work

<details>
<summary><strong>Hydrolink</strong>: Full-stack IoT irrigation platform, built solo from ESP32 firmware to React Native app</summary>

<br>

Born from a real need: managing irrigation systems in the countryside without physically checking on them.

**Tech:** Java/Spring Boot · React Native (Expo) · TanStack Query · PostgreSQL · Redis · AWS IoT Core · AWS Cognito · MinIO · Docker · Coolify · ESP32/PlatformIO

**Architecture:**
- Device status flows from the ESP32 to AWS IoT Core over MQTT, is routed by an IoT rule into SQS, and is consumed by the Spring backend
- Commands go the other way: the API publishes to the IoT Data Plane with IAM; the device subscribes to its own command topic
- The app reads live device state directly from IoT Core using temporary Cognito Identity Pool credentials, scoped per device by an IoT policy attached on link

**Features:**
- Device provisioning and linking: an application record created on boot and linked by an ownership secret, separate from the AWS Thing the device provisions itself via fleet provisioning (X.509)
- Authentication fully migrated to AWS Cognito via Amplify; the API verifies tokens as an OAuth2 resource server and derives the user identity server-side, never from the client
- Two-phase secret rotation, gated on a device acknowledgement, so a failed rotation leaves the old secret valid
- Device secrets stored AES-GCM encrypted with a deterministic HMAC-SHA256 fingerprint for lookups
- User profiles with image upload; device images and OTA firmware stored in MinIO
- Area details: image, name, location, description, display ordering
- Stations: configurable, renamable, assignable roles (solenoid, sensor, etc.), manual control with countdown feedback
- Full per-day scheduling system: fixed-time or relative time windows, linked to another station, with conflict detection for overlaps and cycles
- Over-the-air firmware updates: versioned uploads with checksums, announced to matching devices, with a last-dispatched sweep that avoids re-announcing the same update
- Dockerized backend with separate dev/prod builds, Compose orchestration for Postgres, Redis, and MinIO, each with health checks
- Deployed on Coolify with secure environment variable injection

[API Repo](https://github.com/ivfrost/hydrolink-api) · [App Repo](https://github.com/ivfrost/hydrolink-app) (firmware closed source)

</details>

## Featured Certifications

- [Spring Boot 4, Spring Framework 7: Beginner to Guru](https://www.udemy.com/certificate/UC-986f3769-2fde-4e49-bdf7-6cd26d0e65e8/), Udemy, Aug 2026
- [Intermediate React Native, v2](https://static.frontendmasters.com/ud/c/8480cfc763/lXSziQvimH/intermediate-react-native-v2-frontendmasters.pdf), Master.Dev, Jun 2026
- [API Design in Node.js, v5](https://static.frontendmasters.com/ud/c/8480cfc763/xdzGqkzYQB/api-design-nodejs-v5-masterdev.pdf), Master.Dev, Apr 2026
- [Enterprise Java with Spring Boot](https://static.frontendmasters.com/ud/c/8480cfc763/wUbVJunCnV/spring-boot-frontendmasters.pdf), Master.Dev, Jan 2026
- [Java Masterclass 2025: 130+ Hours of Expert Lessons](https://www.udemy.com/certificate/UC-ee9bd34a-8481-4fd4-96b9-dbb6e269c222/), Udemy, Dec 2025
