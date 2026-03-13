# Feed NuGet Privado (BaGet)

Feed NuGet privado para crear, publicar y consultar paquetes. Configurado para Hostinger VPS con Traefik/Dokploy.

## Requisitos

- Red `dokploy-network` (Traefik)
- Subdominio: `nuget.ingeovisualservices.cloud`

## Despliegue

```bash
cp nuget.env.example nuget.env
# Edita nuget.env y configura NUGET_API_KEY

docker compose up -d
```

## Uso

- **Publicar:** `dotnet nuget push -s https://nuget.ingeovisualservices.cloud/v3/index.json -k TU_API_KEY paquete.nupkg`
- **Restaurar:** `dotnet restore --source https://nuget.ingeovisualservices.cloud/v3/index.json`
