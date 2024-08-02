[Duck DNS]: https://www.duckdns.org/

[wg-easy]: https://github.com/wg-easy/wg-easy

[docker-compose.yml]: docker-compose.yml

[WireGuard]: http://ip_raspberry:51821

[Repositorio Duck DNS]: https://github.com/miguel-shadow/docker-duckdns


**Contenidos**
- [1. Docker WireGuard](#1-docker-wireguard)
- [2. DNS dinámico](#2-dns-dinámico)
- [3. Instalación](#3-instalación)
- [4. Ejecutar](#4-ejecutar)
- [5. Portal WEB](#5-portal-web)
- [6. Actualizar DNS Dinámico automáticamente](#6-actualizar-dns-dinámico-automáticamente)


# 1. Docker WireGuard
- Permite crear una **VPN WireGuard** mediante **Docker** en una **Raspberry Pi**


# 2. DNS dinámico
- Mediante [Duck DNS], crear un **dominio** para nuestra IP dinámica


# 3. Instalación
> [!NOTE]
> Esta guía está basada en la **documentación** en Github de [wg-easy]

- Modificar las variables (señaladas con `<>`) en el archivo [docker-compose.yml]
    - `<dominio_dns_dinamico>`: Nombre del dominio DNS Dinámico (**\*Creado en Duck DNS anteriormente**)
    - `<password_wg>`: Contraseña del portal WEB de WireGuard


# 4. Ejecutar
- `docker compose up -d --build`


# 5. Portal WEB
- **Acceder** mediante un **navegador**: `http://<ip>:51821` ([WireGuard])


# 6. Actualizar DNS Dinámico automáticamente
Al disponer de una **IP dinámica**, la IP puede cambiar y estropear todo lo anterior, dejando de funcionar la VPN.

En este repositorio explico cómo **actualizar el DNS Dinámico de manera automática**: [Repositorio Duck DNS]
