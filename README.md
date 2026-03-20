# aClip

A VST3 hard clipper / limiter plugin built with [JUCE](https://juce.com/).

## What it does

aClip applies hard clipping to an audio signal: samples that exceed the threshold are clamped to ±1.0. A makeup gain control lets you compensate for the resulting level reduction.

**Parameters:**

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Threshold | −∞ to 0 dB | 0 dB | Clipping boundary |
| Makeup Gain | −30 to +30 dB | 0 dB | Post-clip gain compensation |

## Building

**Requirements:**
- CMake 3.30+
- C++23 compiler
- Internet access (CMake fetches JUCE 8.0.8 automatically)

**Linux dependencies:**
```bash
sudo apt install libxext-dev libxrandr-dev libxinerama-dev libxcursor-dev \
                 libxi-dev libgtk-3-dev libasound2-dev
```

**Build:**
```bash
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --config Release
```

The compiled VST3 plugin will be in the `build/` directory.

## Installation

Copy the `.vst3` bundle to your DAW's VST3 plugin folder:

- **Linux:** `~/.vst3/` or `/usr/lib/vst3/`
- **macOS:** `~/Library/Audio/Plug-Ins/VST3/`
- **Windows:** `C:\Program Files\Common Files\VST3\`

## Plugin info

| | |
|---|---|
| Format | VST3 |
| Channels | Stereo |
| MIDI | None |
| Version | 0.0.1 |
| Manufacturer | anotherSimpleCoder |
