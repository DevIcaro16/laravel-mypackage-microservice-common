# Microservices Common

Pacote utilitário para microserviços Laravel com traits e serviços comuns.

## Descrição

Este pacote fornece funcionalidades compartilhadas entre microserviços Laravel, incluindo:
- Trait `ConsumeExternalService` para consumo de APIs externas
- Serviços comuns reutilizáveis
- Configurações padronizadas para comunicação entre microserviços

## Instalação

### Instalar o pacote
```bash
composer require devicaro16/microservices-common
```

### Atualizar o pacote
```bash
composer update devicaro16/microservices-common
```

### Regenerar autoload
```bash
composer dump-autoload
```

## Uso

```php
use Devicaro16\MicroservicesCommon\Services\Traits\ConsumeExternalService;

class MyService
{
    use ConsumeExternalService;
    
    public function __construct()
    {
        $this->token = config('services.external.token');
        $this->url = config('services.external.url');
    }
}
```

## Licença

MIT
