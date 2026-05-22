
# 7.2 NOTIFICAR PAGOS

El método cumplirá la función de registrar pagos dependiendo del número de facturas involucradas en la transacción.

## Endpoint

```http
POST http://dominio_comercio/ApiPagosN3/NotificarPago
```

# 7.2.1 Request

| Nombre | Tipo | Descripción |
|---|---|---|
| IdComercio | Integer | Comercio |
| Password | String | Credencial |
| IdCliente | String | Cliente |
| Facturas | Array | Facturas |
| EstadoPago | Integer | Estado |
| FormaPago | Double | Medio pago |
| ValorTotalPagado | Integer | Total |
| FechaPago | String | Fecha |
| IdPago | Integer | Id pago |

## Ejemplo Request

```json
{
  "IdComercio": 2652,
  "Password": "PagosN3",
  "IdCliente": "A123456789",
  "EstadoPago": 1,
  "ValorTotalPagado": 23797.62
}
```

# 7.2.2 Response

| Nombre | Tipo | Descripción |
|---|---|---|
| CodEstado | Integer | Estado |
| DescripcionEstado | String | Resultado |

## Ejemplo Response

```json
{
  "CodEstado": 0,
  "DescripcionEstado": "Se realizó exitosamente la actualización del pago."
}
```
