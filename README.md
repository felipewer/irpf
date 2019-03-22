  # IRPF - Programa de Declaração do Imposto sobre a Renda de Pessoa Física

Container Docker do programa que os brasileiros mais gostam de instalar todo ano.

## Instruções:

**Opção 1:** Rode manualmente:

```
docker run -it --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME:/home/irpf felipewer/irpf
```

**Opção 2:** Utilize o compose:

```YAML
version: '3'

services:
  irpf:
    image: felipewer/irpf
    environment:
      - DISPLAY=$DISPLAY
    volumes:
      - /tmp/.X11-unix:/tmp/.X11-unix
      - $HOME:/home/irpf
```
