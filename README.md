# Epic Storytelling: The Complete PsychToonsHQ Pipeline

`epic-storytelling` is an end-to-end content creation engine designed to write, format, visualize, and vocalize viral psychological storytelling videos in the signature style of **PsychToonsHQ**.

Unlike informational channels that recite dry bullet points, or teleprompter tools that mechanically chop sentences at `and`, `or`, and `but`, this skill orchestrates the complete workflow across **three interdependent output tiers**:
1. **Tier 1: Original Master Script (`Original`)**: Written to the user's preferred line count (e.g., 400 lines, 800 lines) with rich narrative plot arcs, relatable micro-simulations, continuous curiosity loops, and conversational cadence.
2. **Tier 2: Split Script (`Split`)**: Derived from the Original script via the **4-Word Comma-Splitting Doctrine**. Saved as a **pure line-by-line script with zero headers, zero descriptions, and zero line tags**, formatted with clean markdown paragraph spacing (`\n\n`), companion numbered markdown (`.md`), and raw text (`.txt`).
3. **Tier 3: Visual Prompt CSV (`CSV`)**: Formatted strictly as `SN, SCRIPT, PROMPT`, generated **1-to-1 directly from the Split Script lines** so every visual scene cuts with each comma-split spoken beat.
4. **Autonomous Kaggle T4 Audio Engine**: Zero-shot F5-TTS voice synthesis, modern Kaggle metadata settings (`machine_shape: "NvidiaTeslaT4"`), 10-line batching to prevent cross-attention drift, volume normalization, and pitch-preserved tempo acceleration (1.25x).

---

## 1. The Core Golden Rule: Anti-Staccato Cadence

Never break sentences mechanically at conjunctions like `and`, `or`, `but`, or `because`:
> ❌ *Robotic Staccato:*
> You walk into the room  
> and you look at your boss  
> but you notice his expression  
> or maybe it was just a shadow.

**In Epic Storytelling, thoughts are spoken as cohesive, natural narrative units:**
> ✅ *Natural PsychToonsHQ Flow:*
> You walk into the room and look at your boss, but within two seconds, your brain has already registered the slight tightening in his jaw.  
> Everyone else in the room thinks it is just another normal Monday morning meeting.  
> You, on the other hand, already know the budget was rejected before he even opens his mouth.

- Conjunctions belong to their clauses to maintain spoken momentum.
- Sentences breathe with natural human conversational cadence, emotional pauses, and rhythmic rise and fall.

---

## 2. The 6 Pillars of PsychToonsHQ Storytelling

### Pillar I: Narrative Plot Arcs (Every Point Is a Micro-Simulation)
Never explain a concept in the abstract. Wrap every point, sign, or rule inside a relatable micro-simulation:
1. **The Scene**: Ground the listener in a tangible, physical environment (e.g., office meeting, dinner table, airport gate, midnight kitchen).
2. **The Micro-Conflict**: Introduce a sudden friction, awkward tension, or unspoken dynamic.
3. **The Divergence**: Contrast ordinary reactions (freezing, panicking) vs. the subject's reaction (quiet assessment, calculated action).
4. **The Science/Psychology**: Cite credible scientific frameworks (e.g., Dr. Bruce Ellis, Dr. Seth Pollak, Dr. Ann Masten, Dr. Chiraag Mittal) translated into everyday clarity.
5. **The Emotional Landing**: Close with a validating truth that makes the listener feel deeply seen.

### Pillar II: Continuous Retention & Curiosity Loops (The 60-Second Re-Hook)
Viral retention requires constant psychological tension:
- **The "Wait for It" Loop**: Hint at an unexpected twist revealed later (*"Most people assume this makes you invincible, but in about three minutes, you are going to see why this exact skill keeps you awake on Sunday night."*).
- **Perceptual Contrast**: Juxtapose opposing realities (*"A brain built in luxury learns to plan ten years ahead; a brain built in chaos learns to calculate the trajectory of an airborne plate before it hits the floor."*).
- **Direct Reality Checks**: Speak directly to the listener (*"Be honest with yourself: how many times have you quietly run that exact calculation this week?"*).

### Pillar III: Simple Grammar & 5th-Grade Clarity
- Speak like a brilliant, street-smart friend across a kitchen table.
- Never use academic jargon when a concrete metaphor hits harder:
  - *Academic*: "Hypervigilance induces elevated autonomic arousal during baseline conditions."
  - *PsychToonsHQ*: "Your nervous system is basically a smoke detector with the sensitivity cranked so high it screams every time someone makes toast."

### Pillar IV: Relatable Everyday Micro-Simulations
Ground abstract ideas in visceral, universal experiences:
- Burned toast on a stressful morning.
- The dreaded Slack ping: *"Hey, do you have five minutes to chat?"*
- Making an emergency midnight meal out of half an onion, leftover rice, and mustard.
- Scanning the restaurant for the seat facing the front entrance.

### Pillar V: Emotional Resonance & Cathartic Validation
- Acknowledge the cost of survival without romanticizing trauma or indulging in pity.
- Give dignity to the past: *"You didn't turn out this way because you were flawed; you turned out this way because your brain did its job so well that you are still standing here today."*

### Pillar VI: Observational Humor & Self-Aware Wit
- Add comedic relief to balance heavy psychological themes: *"Congratulations, your brain just treated a slightly delayed text message like an incoming tactical airstrike."*
- Dry, deadpan commentary that releases tension before diving into deeper revelations.

---

## 3. The 3-Tier Output Architecture & Deliverables Hierarchy

The Epic Storytelling pipeline produces content through **three interdependent deliverables**. Agents must understand and maintain the strict relationship between these three tiers:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. ORIGINAL MASTER SCRIPT                                              │
│    • Written strictly to user's preferred line count (e.g. 400 lines) │
│    • Full, unbroken narrative sentences with natural spoken flow       │
│    • Formatted with double newlines (\n\n) between spoken lines        │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │
                     [Apply 4-Word Comma Split Rule]
                                    │
                                    ▼
┌────────────────────────────────────────────────────────────────────────┐
│ 2. SPLIT SCRIPT (Derived from Original)                                │
│    • Split at commas ONLY if (pre_words >= 4) AND (post_words >= 4)    │
│    • Naturally expands line count (e.g. 400 master lines -> 585 lines) │
│    • Pure line-by-line script: ZERO descriptions, ZERO headers/tags   │
│    • Clear \n\n spacing in .md, Numbered (.md), and Raw Plain Text (.txt)│
└───────────────────────────────────┬────────────────────────────────────┘
                                    │
                     [1-to-1 Row-by-Line Generation]
                                    │
                                    ▼
┌────────────────────────────────────────────────────────────────────────┐
│ 3. VISUAL IMAGE PROMPTS CSV (Derived from Split)                       │
│    • Generated strictly and directly from the Split Script lines       │
│    • Columns: SN, SCRIPT, PROMPT                                       │
│    • Row 1 = Split Line 1, Row N = Split Line N (e.g. 585 rows)        │
│    • Scene cuts precisely match each comma-split spoken breath beat    │
└────────────────────────────────────────────────────────────────────────┘
```

### Tier Specifications:

| Tier | Name | Derived From | Line Count | Output Format & Doctrine |
| :--- | :--- | :--- | :--- | :--- |
| **Tier 1** | **Original Master Script** | User's topic & line count request | Exactly matches user request (e.g. 400 or 800 lines) | Full conversational narrative units with `\n\n` paragraph spacing. Embodies full PsychToonsHQ storytelling style. |
| **Tier 2** | **Split Script** | Gotten from **Tier 1 (Original)** via Comma Split Rule | Expands based on valid commas (e.g. 400 lines → 585 lines) | **Pure line-by-line script**. Absolutely NO scene descriptions, NO section headings (`### Script Line X`), and NO bracketed tags (`[Line 1.1]`). Formatted with `\n\n` in Markdown, plus Numbered (`.md`) and Raw (`.txt`). |
| **Tier 3** | **Image Prompts CSV** | Gotten directly from **Tier 2 (Split Script)** | Exactly matches Tier 2 line count (e.g. 585 rows) | Standard CSV (`SN, SCRIPT, PROMPT`). 1-to-1 mapping with split lines. Prompts follow the PsychToons minimalist 2D vector style. |

---

## 4. Structural Blueprint for Master Scripts

| Section | 400-Line Target | 800-Line Target | Focus |
| :--- | :--- | :--- | :--- |
| **Cold Open & Anomaly Hook** | Lines 1 – 25 | Lines 1 – 50 | Relatable scenario, crowd vs. subject contrast, psychological thesis naming. |
| **Origin Science & Hidden Talents** | Integrated | Integrated | Bruce Ellis, neurobiology of adaptation, living in storm vs. simulator. |
| **The 10 Dramatized Episodes (Signs 1–10)**| Lines 26 – 375 (35 lines/sign) | Lines 51 – 750 (70 lines/sign) | Each sign is an immersive micro-story with scene, conflict, divergence, science, and humor. |
| **The Peacetime Crisis & Final Truth** | Lines 376 – 390 | Lines 751 – 780 | The trap of waiting for the ceiling to collapse; shifting from survival to thriving. |
| **Cathartic Outro & Call to Action** | Lines 391 – 400 | Lines 781 – 802 | Honoring the warrior within, validation, like/subscribe/comment prompts. |

---

## 5. The 4-Word Comma-Splitting Engine (Pure Line-by-Line Doctrine)

When preparing a script for visual production, video editing, subtitle generation, or image prompt mapping, apply the **4-Word Comma-Splitting Rule** to the **Original Master Script**:

### The Splitting Logic
Split a sentence at a comma into a new line **ONLY if both the preceding text has at least 4 words AND the succeeding text has at least 4 words**:

```
IF (words_before_comma >= 4) AND (words_after_comma >= 4):
    SPLIT to new line at comma
ELSE:
    KEEP intact on the same line
```

### Output Format Doctrine: Pure Line-by-Line Script
The output of the split must be saved as a **clean, pure line-by-line script without descriptions, headers, or line numbers**:
- ❌ **Do NOT include descriptions or markdown headings** like `### Script Line 1` or `# Act 1`.
- ❌ **Do NOT include bracketed tags** like `- [Line 1.1]` or bullet points.
- ✅ **DO write exactly one spoken/visual fragment per line**, separated by double newlines (`\n\n`):
  ```
  There is a very rare kind of intelligence that no classroom ever tested you for,

  and school never had a grade for it.

  Psychologists have spent decades trying to give it a clinical name,

  but most people who carry it simply call it survival.

  Today, we are calling it what it genuinely is: Survivor's Intelligence.
  ```

### Why This Rule Exists
1. **Prevents Orphaned Micro-Fragments**: Words like `"Yes,"`, `"However,"`, `"In fact,"`, or `", you know,"` are never chopped onto their own isolated lines.
2. **Creates Natural Visual Beats**: Compound clauses representing distinct visual thoughts are split cleanly, allowing the video scene or caption to cut rhythmically with the narrator's breath pause.
3. **Direct Foundation for 1-to-1 Visual Prompts**: This clean line-by-line split file becomes the exact direct input for the Image Prompt CSV engine.

### Reference Python Implementation
```python
import re

def count_words(text):
    return len(re.findall(r'\b\w+\b', text))

def split_sentence_at_commas(sentence, min_words=4):
    sentence = sentence.strip()
    if not sentence or ',' not in sentence:
        return [sentence]
    
    parts = sentence.split(',')
    fragments = []
    current_chunk = parts[0]
    
    for i in range(1, len(parts)):
        next_part = parts[i]
        left_words = count_words(current_chunk)
        remaining_tail = ','.join(parts[i:])
        tail_words = count_words(remaining_tail)
        next_part_words = count_words(next_part)
        
        if left_words >= min_words and tail_words >= min_words and next_part_words >= min_words:
            fragments.append(current_chunk.strip() + ',')
            current_chunk = next_part.strip()
        else:
            current_chunk = current_chunk + ',' + next_part
            
    if current_chunk.strip():
        if fragments and count_words(current_chunk) < min_words:
            prev = fragments.pop()
            current_chunk = prev + ' ' + current_chunk
        fragments.append(current_chunk.strip())
        
    return fragments
```

---

## 6. Visual Storytelling & Image Prompt CSV Engine (`SN, SCRIPT, PROMPT`)

The Image Prompt CSV is generated **directly from the clean line-by-line Split Script (Tier 2)**, NOT from the un-split master script.

### 1-to-1 Mapping Rule
- **Every single line of the Split Script becomes exactly one row in the CSV.**
- For example, if a 400-line master script splits into 585 lines, the Image CSV has **exactly 585 rows** (`SN 1` to `SN 585`).
- This guarantees that every visual scene corresponds 1-to-1 with every spoken breath beat.

### CSV Schema
Standard CSV format with exact headers:
`SN,SCRIPT,PROMPT`

- **`SN`**: Serial number counting sequentially from 1 downwards (`1, 2, 3... N`).
- **`SCRIPT`**: Exact line text from the Split Script.
- **`PROMPT`**: A descriptive, interesting image scene capturing the mental picture of that sentence.

### Mental Picture Translation Rules
1. **Externalize the Mind**: Translate internal thoughts, feelings, or brain mechanics into tangible, symbolic cartoon imagery (e.g. *a character with an illuminated brain showing spinning golden clockwork gears*).
2. **Action & Interaction**: Depict expressive character gestures, physical props, and environmental settings.
3. **No Words or Text in Prompts**: Images must communicate through visual storytelling—never written words, banners, or speech bubbles.
4. **The PsychToons Aesthetic Anchor**: Append to every prompt:
   > `style of minimalist hand-drawn 2D animation, simple stick-figure cartoon, clean white background, black line art, limited muted color palette, vector illustration, no text.`

---

## 7. Autonomous Kaggle Audio Generation Engine (F5-TTS & T4 GPU)

To generate human-quality narration audio for large scripts without rate limits, use the autonomous Kaggle F5-TTS pipeline.

### 1. Kaggle Kernel Metadata (`kernel-metadata.json`)
Modern Kaggle GPU scheduling requires explicit machine shaping. Setting `"enable_gpu": true` alone is insufficient and often defaults to older P100 hardware. You **must** include `"machine_shape": "NvidiaTeslaT4"`:

```json
{
  "id": "<kaggle_username>/audio-generation-f5tts-full",
  "title": "Audio Generation F5TTS Full",
  "code_file": "generate_full.py",
  "language": "python",
  "kernel_type": "script",
  "is_private": "true",
  "enable_gpu": "true",
  "enable_internet": "true",
  "dataset_sources": [],
  "competition_sources": [],
  "kernel_sources": [],
  "model_sources": [],
  "machine_shape": "NvidiaTeslaT4"
}
```

### 2. Voice Reference Selection
- **Timbre**: Authoritative, calm, warm male storytelling voice (e.g. `en-US-ChristopherNeural`).
- **Phonetic Sample**: Clean, 8–10 second sample at 24,000 Hz mono PCM WAV, matched with exact reference text:
  > *"Once upon a time, in a world full of endless possibilities, there lived a storyteller who understood the profound power of silence."*
- **Embedding**: Base64-encoded into the runner script.

### 3. Kaggle Execution Script (`generate_full.py`)
```python
import os
import sys
import json
import base64
import numpy as np
import scipy.io.wavfile

print("Installing dependencies...")
os.system("pip install -q f5-tts torch torchaudio soundfile")

import torch
import torchaudio
from f5_tts.api import F5TTS

# 1. Decode reference voice
with open("reference_voice.mp3", "wb") as f:
    f.write(base64.b64decode("<BASE64_AUDIO_STRING>"))

wav_tensor, sr = torchaudio.load("reference_voice.mp3")
if sr != 24000:
    wav_tensor = torchaudio.transforms.Resample(sr, 24000)(wav_tensor)
if wav_tensor.shape[0] > 1:
    wav_tensor = wav_tensor.mean(dim=0, keepdim=True)
torchaudio.save("reference_voice.wav", wav_tensor, 24000)

# 2. Load Model on T4 GPU
model = F5TTS(device="cuda:0")
ref_audio_path = "reference_voice.wav"
ref_text = "Once upon a time, in a world full of endless possibilities, there lived a storyteller who understood the profound power of silence."

# 3. Load Pure Script Lines (No commentary, no headers)
lines = json.loads('''<JSON_ENCODED_LINES_ARRAY>''')

# 4. Chunk into 10-line blocks (~150-190 words) to prevent cross-attention drift
chunks = [lines[i:i+10] for i in range(0, len(lines), 10)]
all_audio = []

for i, chunk_lines in enumerate(chunks):
    chunk_text = " ".join(chunk_lines)
    print(f"Generating chunk {i+1} / {len(chunks)}...")
    try:
        wav, sr, _ = model.infer(ref_file=ref_audio_path, ref_text=ref_text, gen_text=chunk_text)
        all_audio.append(wav)
    except Exception as e:
        print(f"Error on chunk {i+1}: {e}")

# 5. Concatenate & Volume Boost (1.5x)
final_audio = np.concatenate(all_audio) * 1.5
final_audio = np.clip(final_audio, -1.0, 1.0)
final_int16 = np.int16(final_audio * 32767)

scipy.io.wavfile.write("final_output.wav", 24000, final_int16)
print("Done writing final_output.wav!")
```

### 4. Background Monitoring & Download (`poll_f5tts_full.py`)
```python
import os, time, subprocess, shutil

slug = "<kaggle_username>/audio-generation-f5tts-full"
download_dir = r"C:\Users\DELL\Downloads\f5tts_output"

while True:
    res = subprocess.run(f"kaggle kernels status {slug}", shell=True, capture_output=True, text=True)
    status = res.stdout.strip()
    print(f"[{time.strftime('%H:%M:%S')}] {status}")
    if "complete" in status.lower():
        break
    elif "error" in status.lower() or "fail" in status.lower():
        sys.exit(1)
    time.sleep(30)

subprocess.run(f'set PYTHONUTF8=1 && kaggle kernels output {slug} -p "{download_dir}"', shell=True)
```

### 5. Pitch-Preserved Speedup (1.25x Tempo Filter)
To create an accelerated, punchy version without altering vocal pitch or causing distortion, use FFmpeg's `atempo` filter:

```bash
ffmpeg -y -i final_output.wav -filter:a "atempo=1.25" -c:a pcm_s16le -ar 24000 final_output_1.25x.wav
```
- **Filter**: `atempo=1.25` scales playback speed by 125% while preserving formants and vocal timbre.
- **Encoding**: `-c:a pcm_s16le -ar 24000` maintains uncompressed 16-bit PCM WAV at 24kHz.

---

## 8. Execution Checklist for Agents

When running the **epic-storytelling** pipeline:
- [ ] **Tier 1 (Original Script)**: Is the master script written strictly to the user's requested line count, with conversational rise and fall and double-newline (`\n\n`) separation?
- [ ] **Tier 2 (Split Script)**: Has the 4-word comma-splitting rule been strictly executed (`preceding_words >= 4` AND `succeeding_words >= 4`)?
- [ ] **Split Output Cleanliness**: Is the Split Script saved as a **pure line-by-line script with zero descriptions, zero headers, and zero bracketed line tags**?
- [ ] **Split Deliverable Formats**: Are both clean Markdown (`.md` with `\n\n`), Numbered Markdown (`.md`), and Raw Plain Text (`.txt`) provided?
- [ ] **Tier 3 (Image Prompts CSV)**: Is the CSV generated **1-to-1 directly from the Split Script lines**, having strictly `SN,SCRIPT,PROMPT` with the PsychToons 2D minimalist aesthetic anchor?
- [ ] **Kaggle Audio**: Is `machine_shape: "NvidiaTeslaT4"` set in `kernel-metadata.json`?
- [ ] **Voice Selection**: Is a warm, authoritative male voice reference used with 100% matched phonetic text?
- [ ] **Pure Script Guarantee**: Has all commentary, metadata, and bracketed content been removed before audio synthesis?
- [ ] **Speedup Option**: If 1.25x is requested, is it processed via FFmpeg's `atempo=1.25` filter to preserve pitch?\n