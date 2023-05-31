# Endpoint com parâmetro
```csharp

        [HttpGet("Apresentar/{nome}")]
        public IActionResult Apresentar(string nome){
            var mensagem = $"Olá {nome} seja bem vindo"; //criando mensagem
            return Ok(new {mensagem}); // retornando um objeto anônimo
        }

```