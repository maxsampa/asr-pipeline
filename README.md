# Speech Processing Lab

Comparative evaluation of automatic speech recognition (ASR) models on Portuguese audio, covering preprocessing, feature extraction and transcription.

## Why this exists

Whisper and Wav2Vec2 are the two default choices for Portuguese ASR, and the trade-off between them is rarely stated in concrete terms. This repository runs both over the same audio set under the same preprocessing, and reports where each one wins — by error rate, by processing time and by failure mode.

## Scope

- Audio preprocessing: resampling, normalization, silence handling
- Feature extraction with Librosa
- Transcription with Wav2Vec2 and Whisper
- Side-by-side comparison on the same inputs

## Results

<!-- PREENCHER — sem esta tabela o repositório continua sendo "experimentos", não estudo.

| Model | WER | CER | s per audio minute | Notes |
| --- | --- | --- | --- | --- |
| Wav2Vec2 (<checkpoint>) | | | | |
| Whisper <size> | | | | |

Condições do teste: <nº de arquivos>, <duração total>, <qualidade do áudio>, hardware: <CPU/GPU>.
Referência de transcrição: <como o ground truth foi produzido>.

Inclua pelo menos um caso em que o modelo pior no agregado ganhou — ruído,
sotaque, termo técnico. É o que mostra que você olhou os dados. -->

## What I learned

<!-- PREENCHER — 3 a 5 bullets. O que quebrou, o que surpreendeu, o que você
     faria diferente. Esta seção é a que mais eleva percepção de senioridade,
     e é a que praticamente nenhum portfólio tem. -->

## Stack

Python · Hugging Face Transformers · Whisper · Wav2Vec2 · Librosa · PyTorch

## Running locally

```bash
git clone https://github.com/maxsampa/asr-pipeline.git
cd asr-pipeline

python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate

pip install -r requirements.txt

python <!-- PREENCHER: nome final do script --> --input samples/<arquivo>.mp3
```

<!-- PREENCHER: se o script exige ffmpeg ou outra dependência de sistema,
     declare aqui. É a causa nº 1 de "não roda na máquina do avaliador". -->

**Sample audio:** `samples/` <!-- PREENCHER: commitar 1 ou 2 áudios curtos e
livres de direitos, para o avaliador conseguir rodar sem arrumar dado próprio. -->

## Limitations

<!-- PREENCHER. Candidatos honestos aqui: tamanho da amostra, ausência de
     dataset padronizado (Common Voice PT seria o passo seguinte), ground
     truth produzido manualmente, ausência de teste em áudio ruidoso real. -->

## License

MIT — see [LICENSE](LICENSE).
