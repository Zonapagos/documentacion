
# 7.1 CONSULTA

El método cumplirá la función de consultar el estado de la cartera dependiendo de un número de factura o identificación del cliente.

## Endpoint

```http
POST http://dominio_comercio/ApiPagosN3/Consulta
```

## Método de mensajería

```json
JSON
```

# 7.1.1 Request

| Nombre | Tipo y Tamaño | Descripción |
|---|---|---|
| IdComercio | Integer Obligatorio | Identificador comercio |
| Password | String(15) Obligatorio | Credencial comercio |
| IdFactura | String(15) Opcional | Número factura |
| IdCliente | String(20) Opcional | Documento cliente |
| ClaveConsulta | String(20) Opcional | Clave consulta |
| ForzarParamConsulta | String(5) Opcional | Parámetro configuración |

## Ejemplo Request

```json
{
  "IdComercio": 2652,
  "Password": "PagosN3",
  "IdCliente": "A123456789",
  "ClaveConsulta": "2701",
  "ForzarParamConsulta": ""
}
```

# 7.1.2 Response

| Nombre | Tipo | Descripción |
|---|---|---|
| CodRespuesta | Integer | Código respuesta |
| Descripcion | String | Descripción |
| Facturas | Array | Facturas |
| CodServicioPse | String | Código PSE |
| CambiarClave | Integer | Cambio clave |

## Arreglo Facturas

| Campo | Tipo | Descripción |
|---|---|---|
| IdFactura | String | Factura |
| Concepto | String | Concepto |
| TotalFactura | Double | Total |
| TotalIVA | Double | IVA |
| Saldo | Double | Saldo |
| FechaVencimiento | Date | Fecha |
| Orden | Integer | Orden |
| TipoIdCliente | String | Tipo documento |
| IdCliente | String | Documento |
| Nombre | String | Nombre |
| Apellido | String | Apellido |
| Email | String | Correo |
| Telefono | String | Teléfono |
| CampoAdicional1 | String | Campo 1 |
| CampoAdicional2 | String | Campo 2 |
| CampoAdicional3 | String | Campo 3 |

## Ejemplo Response

```json
{
  "CodRespuesta": 0,
  "Descripcion": "Consulta Exitosa",
  "Facturas": [
    {
      "IdFactura": "123456789",
      "Concepto": "Concepto1",
      "TotalFactura": 9999.00,
      "TotalIVA": 1899.81,
      "Saldo": 11898.81
    }
  ]
}
```
