# MSSQL Staging Database

Entorno de base de datos SQL Server 2019 para staging local.

## 🚀 Inicio Rápido

1. **Clonar y configurar:**
```bash
   cp .env.example .env
   # Editar .env con tu password
```

2. **Levantar la base de datos:**
```bash
   docker-compose up -d
```

3. **Verificar estado:**
```bash
   docker-compose ps
   docker-compose logs -f mssql-2019
```

## 🔌 Conexión

- **Host:** `localhost`
- **Puerto:** `1433`
- **Usuario:** `sa`
- **Password:** (definido en `.env`)

### Conexión desde línea de comandos:
```bash
docker exec -it mssql-2019 /opt/mssql-tools/bin/sqlcmd -S localhost -U sa -P 'TuPassword'
```

### Connection String:
```
Server=localhost,1433;Database=master;User Id=sa;Password=TuPassword;TrustServerCertificate=True;
```

## 🛠️ Comandos Útiles
```bash
# Iniciar
docker-compose up -d

# Detener
docker-compose down

# Ver logs
docker-compose logs -f

# Reiniciar
docker-compose restart

# Eliminar TODO (incluyendo datos)
docker-compose down -v
```

## 📊 Recursos

- **Memoria asignada:** 4GB
- **Edición:** Developer (full features, gratis)
- **Persistencia:** `./data` (no versionar)

## ⚠️ Notas

- Este entorno es **solo para desarrollo/staging local**
- Los datos persisten en `./data`
- No exponer el puerto 1433 públicamente