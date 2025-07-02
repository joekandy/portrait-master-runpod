#  Portrait Master FLUX - Automazione Completa per RunPod

Installazione automatica e completa di **Portrait Master FLUX** su RunPod con tutti i modelli, nodi personalizzati e configurazioni necessarie.

##  **Installazione Rapida (1 Comando)**

Copia e incolla questo comando nel terminale di RunPod:

`ash
wget -O - https://raw.githubusercontent.com/joekandy/portrait-master-runpod/main/install.sh | bash
`

##  **Cosa Include Questa Automazione**

###  **Modelli AI Inclusi:**
- **FLUX1-dev.safetensors** (23GB) - Modello base principale
- **FLUX1-dev-fp8.safetensors** (17GB) - Versione ottimizzata
- **FLUX1-Redux-dev** (123MB) - Style model adapter
- **VAE FLUX** (ae.safetensors, 335MB)
- **CLIP Text Encoders** (clip_l + t5xxl_fp16, ~9.4GB totali)
- **CLIP Vision** (sigclip_vision_patch14_384, 817MB)
- **Stable Diffusion 1.5** (4GB)
- **SD2 Inpainting** (4.9GB)
- **LoRA Premium** (MoXin, BlindBox, Photorealistic Skin)
- **Modelli SAM** per segmentazione
- **Upscalers 4K** specializzati per volti

###  **Custom Nodes (39+ Nodi Installati):**
- **ComfyUI-Manager** (gestione senza restrizioni)
- **ComfyUI_LayerStyle** (essenziale per Portrait Master)
- **ComfyUI-Easy-Use** (interfaccia semplificata)
- **Detail-Daemon** (miglioramento dettagli volti)
- **Impact-Pack** (face enhancement)
- **WAS Node Suite** (nodi matematici e utility)
- **rgthree-comfy** (workflow management)
- **Custom-Scripts** (automazioni)
- **E molti altri...**

###  **Workflow Pronti all'Uso:**
- **PortraitMaster_Flux1_Core** - Workflow completo professionale
- **PortraitMaster_Flux1_Lite** - Versione leggera e veloce
- **PortraitMaster_Flux1_Expression** - Specializzato per espressioni
- **PortraitMaster_BatchGen** - Generazione in batch
- **PortraitMaster_Lite_GGuF** - Versione ottimizzata GGUF

###  **Configurazioni Ottimizzate:**
- **Fix CUBLAS** automatico per RTX 4090
- **Parametri VRAM** ottimizzati (24GB)
- **Compatibilità FP8/FP16** gestita automaticamente
- **Tunnel Cloudflare** per accesso pubblico
- **Gestione errori** automatica

##  **Requisiti RunPod**

- **GPU:** RTX 4090 (24GB VRAM) - **Raccomandato**
- **Spazio Disco:** Minimo 100GB liberi
- **Template:** unpod/pytorch:2.1.0-py3.10-cuda11.8.0-devel-ubuntu22.04
- **Connessione:** Stabile per download (~80GB totali)

##  **Installazione Manuale (Opzionale)**

Se preferisci installare manualmente:

### 1. Clona il Repository
`ash
git clone https://github.com/joekandy/portrait-master-runpod.git
cd portrait-master-runpod
`

### 2. Configura i Token (Opzionale)
`ash
# Modifica install.sh e inserisci i tuoi token se necessario
nano install.sh
`

### 3. Esegui l'Installazione
`ash
chmod +x install.sh
./install.sh
`

### 4. Avvia ComfyUI
`ash
./start_comfyui.sh
`

### 5. Accedi Tramite Tunnel
`ash
./start_tunnel.sh
`

##  **Risoluzione Problemi Comuni**

###  Errore CUBLAS_STATUS_NOT_SUPPORTED
`ash
# Risolto automaticamente dallo script, ma se persiste:
./fix_cublas.sh
`

###  Modelli Non Trovati
`ash
# Verifica e riscarica modelli mancanti:
./verify_models.sh
`

###  Nodi Mancanti
`ash
# Reinstalla nodi custom:
./scripts/install_additional_nodes.sh
`

###  Errori di VRAM
`ash
# Avvia con parametri ridotti:
# Modifica start_comfyui.sh e aggiungi --cpu-vram
`

##  **Come Usare Portrait Master**

1. **Avvia ComfyUI** con il tunnel
2. **Carica un workflow** da /workspace/ComfyUI/workflows/
3. **Carica la tua foto** in input
4. **Configura i parametri** (prompt, stile, ecc.)
5. **Genera** il tuo ritratto professionale!

##  **Changelog**

### v2.0.0 (Dicembre 2024)
-  Automazione completa dell'installazione
-  Fix definitivo errori CUBLAS con FLUX FP8
-  39+ custom nodes preinstallati
-  5 workflow Portrait Master inclusi
-  Gestione automatica dipendenze Python
-  Tunnel Cloudflare integrato
-  Sistema di verifica modelli

##  **Supporto**

- **Issues:** [GitHub Issues](https://github.com/joekandy/portrait-master-runpod/issues)
- **Discussioni:** [GitHub Discussions](https://github.com/joekandy/portrait-master-runpod/discussions)

##  **Licenza**

MIT License - Sentiti libero di modificare e distribuire.

##  **Ringraziamenti**

- **Portrait Master Team** per i workflow originali
- **ComfyUI Community** per i nodi personalizzati
- **RunPod** per la piattaforma GPU cloud
- **FLUX Team** per i modelli AI avanzati

---

 **Se questo progetto ti è stato utile, lascia una stella su GitHub!**
