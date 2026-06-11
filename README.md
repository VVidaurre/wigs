# Marcador WIG 4DX — GBM

Scoreboard 4DX: Excel compartido (datos) + marcador HTML para TV (visual) +
PGX (Samba + nginx) como servidor. Ver **CLAUDE.md** para la arquitectura,
el contrato Excel↔parser y los flujos de trabajo.

## Inicio rápido
```
pip install openpyxl            # y LibreOffice para recalc
make build                      # construye el tablero
make demo && open dist/demo.html  # ver el marcador con datos dummy
make test                       # validar el contrato
```

## Producción
1. `deploy/setup-wig.sh` en el PGX (Samba + nginx + timer).
2. `make deploy PGX=usuario@ip` para publicar marcador.html.
3. El tablero compartido vive en `\\PGX\WIG`; los dueños digitan cada lunes.
