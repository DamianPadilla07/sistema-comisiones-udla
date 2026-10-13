# 📊 Sistema de Cálculo de Comisiones RBA

**Autor:** Damian Padilla  
**Institución:** Universidad de Las Américas (UDLA)  

Este proyecto permite calcular las comisiones generadas por vendedores en función del monto total vendido durante un rango de fechas específico, basado en reglas configurables.

## 🛠️ Tecnologías Utilizadas
- **Frontend:** Angular 16 (Diseño moderno personalizado)
- **Backend:** ASP.NET Core Web API (.NET 9)
- **Base de Datos:** Microsoft SQL Server (Local)

## ⚙️ Funcionalidad Principal
1. El usuario ingresa un **rango de fechas** en la interfaz.
2. El sistema consulta y calcula el total vendido por cada vendedor en ese periodo.
3. Se aplica automáticamente una **regla de comisión** (porcentaje) según el total acumulado.
4. El resultado muestra en una tabla moderna el nombre del vendedor, total vendido y la comisión ganada.

---

## 🗄️ Estructura de la Base de Datos

### Tabla `Regla`
| Id | Porcentaje | MontoMinimo |
| :--- | :--- | :--- |
| 1 | 0.06 | 0.00 |
| 2 | 0.08 | 500.00 |
| 3 | 0.10 | 800.00 |
| 4 | 0.15 | 1000.00 |

### Tabla `Vendedor`
- **Id** (PK)
- **Nombre**

### Tabla `Venta`
- **Id** (PK)
- **VendedorId** (FK)
- **FechaVenta**
- **Monto**

---

## 💻 Ejecución Local

### 1. Backend (.NET)
```bash
dotnet run

### Frontend (Angular)
Bash
cd frontend-clasico
npm install
ng serve