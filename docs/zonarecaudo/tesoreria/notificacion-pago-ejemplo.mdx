---
title: "Ejemplos de la integración "
---

# Endpoint: Notificación de Pago

## URL

```http
POST http://dominio_comercio/ApiPagosN3/api/NotificarPagos
```

## Descripción

Registra la notificación de un pago exitoso realizado por un cliente.

---

# Código Fuente

```csharp
public class NotificarPagoController : ApiController
{
    [HttpPost]
    [Route("ApiPagosN3/api/NotificarPago")]
    public IHttpActionResult Notificar(NotificarPagoRequest request)
    {
        if (request == null ||
            request.IdComercio <= 0 ||
            string.IsNullOrWhiteSpace(request.Password) ||
            string.IsNullOrWhiteSpace(request.IdTransaccion))
        {
            return Ok(new NotificarPagoResponse
            {
                CodEstado = 1,
                DescripcionEstado = "No se pudo realizar la actualización del pago. Faltan parámetros."
            });
        }

        if (request.IdComercio != @IdComercio || request.Password != "@Clave")
        {
            return Ok(new NotificarPagoResponse
            {
                CodEstado = 2,
                DescripcionEstado = "Error en autenticación de seguridad."
            });
        }

        try
        {
            // proceso necesario para el comercio

            return Ok(new NotificarPagoResponse
            {
                CodEstado = 0,
                DescripcionEstado = "Se realizó exitosamente la actualización del pago."
            });
        }
        catch (Exception)
        {
            return Ok(new NotificarPagoResponse
            {
                CodEstado = 99,
                DescripcionEstado = "Error técnico o inesperado en la operación."
            });
        }
    }
}
```
