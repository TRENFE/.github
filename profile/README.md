
# TRENFE

Este workspace agrupa tres proyectos que forman la plataforma Trenfe:

- `Trenfe_BackEnd`: BackEnd API. [Here](https://github.com/TRENFE/Trenfe_BackEnd)
- `Trenfe_FrontEnd`: Web pública para usuarios. [Here](https://github.com/TRENFE/Trenfe_FrontEnd)
- `Trenfe_Intranet`: Panel interno de administración. [Here](https://github.com/TRENFE/Trenfe_Intranet)

## Arquitectura

1. `Trenfe_FrontEnd` consume endpoints locales `/api/*`.
2. Esos endpoints hacen proxy hacia `Trenfe_BackEnd`.
3. `Trenfe_Intranet` también consume `Trenfe_BackEnd` para operaciones admin.
4. `Trenfe_BackEnd` persiste en MongoDB.

## Estructura del repositorio

```text
TRENFE/
├── Trenfe_BackEnd/
├── Trenfe_FrontEnd/
├── Trenfe_Intranet/
```

## Variables de entorno

### BackEnd

- `MONGO_URI`
- `PORT`
- `ADMIN_TOKEN`
- `JWT_SECRET`
- `API_NINJAS_API_KEY`
- `GOOGLE_API_KEY`

### FrontEnd

- `GEMINI_API_KEY`

### Intranet

- `EMAIL`
- `PASSWORD`

## Orden de arranque (local)

1. Arranca backend.
2. Arranca frontend.
3. Arranca intranet.

### Comandos

#### BackEnd

```bash
deno task start
```

#### FrontEnd

```bash
deno task start
```

#### Intranet

```bash
deno task start
```


## Documentación por proyecto

- [BackEnd README](https://github.com/TRENFE/Trenfe_BackEnd/blob/main/README.md)
- [FrontEnd README](https://github.com/TRENFE/Trenfe_FrontEnd/blob/main/README.md)
- [Intranet README](https://github.com/TRENFE/Trenfe_Intranet/blob/main/README.md)
