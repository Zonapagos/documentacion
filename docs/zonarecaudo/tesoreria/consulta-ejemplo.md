---
title: "Ejemplos de la integración"
---

# Endpoint: Consulta

## URL

```http
POST http://dominio_comercio/ApiPagosN3/api/Consulta
```

## Descripción

Permite consultar el estado de una transacción con base en una clave de consulta proporcionada.

---

# Código Fuente

```csharp
public class ConsultaController : ApiController
{
    [HttpPost]
    [Route("ApiPagosN3/api/Consulta")]
    public IHttpActionResult ConsultarEstado(ConsultaRequest request)
    {
        if (request == null ||
            request.IdComercio <= 0 ||
            string.IsNullOrWhiteSpace(request.Password) ||
            string.IsNullOrWhiteSpace(request.ClaveConsulta))
        {
            return Ok(new ConsultaResponse
            {
                Codrespuesta = "99",
                Descripcion = "Parametros invalidos.",
                Factura = null,
                CodServicioPpal = null,
                CambiarClave = 0
            });
        }

        if (request.IdComercio != @idComercio || request.Password != "@Clave")
        {
            return Ok(new ConsultaResponse
            {
                Codrespuesta = "99",
                Descripcion = "Credenciales incorrectas.",
                Factura = null,
                CodServicioPpal = null,
                CambiarClave = 0
            });
        }

        return Ok(response);
    }
}
```
