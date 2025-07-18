
# Offensive Scan Tool

Este proyecto automatiza el reconocimiento y escaneo ofensivo de un objetivo, aplicando técnicas básicas de evasión usando Nmap.

## Características
- Escaneo SYN (`-sS`) con fragmentación y relleno
- Spoofing de MAC address
- Scripts de detección de vulnerabilidades (`--script vuln`)
- Generación automática de reportes HTML

## Uso
1. Asegúrate de tener Nmap instalado.
2. Lista tus objetivos en `targets.txt` (una IP por línea).
3. Ejecuta:

```bash
python main.py
```

## Requisitos
- Python 3
- Nmap
