# O que é uma controller
* Classe para agrupar requisições http
* Agrupamento de classes em comum
* Criando um usuario controller
* Primerio criar uma classe chamada `UsuarioController` 
* É bom colocar `Controller` no final para identifacar que a classe é um controller

```csharp

using Microsoft.AspNetCore.Mvc; // fazer using

namespace DotNet_Introducao_API.Controllers
{
    
    [ApiController] // após criar a classe colocar os atrubitos
    [Route("[Controller]")] // atributo da rota
    public class UsuarioController:ControllerBase //acrescentar ControllerBase
    {
        
    }
}

```
* criando um método get
```csharp

    [ApiController]
    [Route("[Controller]")]
    public class UsuarioController:ControllerBase
    {
        [HttpGet("ObterDataHoraAtual")] //atributo para o método get
        public IActionResult ObterDataHora()
        {

            //criando um objeto para retornar data e hora
            var obj = new {
                Data = DateTime.Now.ToLongDateString(),
                Hora = DateTime.Now.ToShortTimeString()
            };

            return Ok(obj); //retorando os valores
        }
    }

```


