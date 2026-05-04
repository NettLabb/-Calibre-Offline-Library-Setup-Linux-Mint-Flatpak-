## System Architecture

### Core Layers

1. Storage Layer
- Local filesystem (/home/op/)
- Separate folders per content type

2. Library Layer (Calibre)
- Independent libraries per category
- Metadata database per library

3. Runtime Layer
- Flatpak sandboxed Calibre
- Qt rendering engine (Fusion theme)

4. Organization Layer
- Tags for classification
- Metadata for search and filtering
