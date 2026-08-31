# Myshor GS XG SoundFont

[![Latest Release](https://img.shields.io/github/v/release/Myshor/Myshor-GS-XG?include_prereleases&label=Latest%20Release&color=brightgreen)](https://github.com/Myshor/Myshor-GS-XG/releases)
[![Total Downloads](https://img.shields.io/github/downloads/Myshor/Myshor-GS-XG/total?label=Total%20Downloads&color=blue)](https://github.com/Myshor/Myshor-GS-XG/releases)
[![SoundFont Format](https://img.shields.io/badge/Format-SF2-orange.svg)](https://github.com/Myshor/Myshor-GS-XG)
[![MIDI Standards](https://img.shields.io/badge/Compatibility-GM%20%7C%20GS%20%7C%20XG-informational.svg)](https://github.com/Myshor/Myshor-GS-XG)
[![License](https://img.shields.io/badge/License-Fair--Use%20%2F%20Non--Commercial-lightgrey.svg)](LICENSE.md)

**Myshor GS XG** is a balanced SoundFont (`.sf2`) bank engineered for high-quality PC MIDI playback, karaoke tracking (`.kar` / `.mid`), and retro gaming synthesis. It combines General MIDI (GM), Roland GS, and Yamaha XG compatibility with a selective, hand-tuned balance.

---

## Editions & Branch Architecture

| Edition | Version | Target Environment | Memory Profile | Status |
| :--- | :--- | :--- | :--- | :--- |
| **No Limits PC Edition** | **v3.4** | Modern PCs (Software synthesis) | ~67.4 MB (RAM Uncapped) | **Active / Main** |
| **Legacy 64MB Edition** | **v2.12** | Retro hardware (AWE64), mobile MIDI synths | ≤ 64.0 MB (Hardware Cap) | Archived / Frozen |

---

## Download

Pre-packaged binary archives (`.7z`) containing the `.sf2` bank and TiMidity configuration files (`timidity.cfg`, patch mapping lists) are available on the **[Releases Page](https://github.com/Myshor/Myshor-GS-XG/releases)**.

---

## Changelog & Sound Set Evolution

Base SoundFont: **GeneralUser GS v2.0.1** by S. Christian Collins.

### Baseline Changes (Myshor GS XG 2.12 Legacy Edition)
1. Added XG SFX banks 64 and 126.
2. Increased default Chorus and Reverb to emulate Yamaha S-YXG50 spatial response.
3. Changed Overdrive Guitar (preset 0:29) to ColomboGMGS2 (attenuation reduced from 5 to 3 for higher volume).
4. Changed Choir Aaah and Ooooh (presets 0:52 and 0:53) to presets from SGM-2.01-HQ-3.0.
5. Added SFX banks (presets 126:56, 126:57, 126:58) from ColomboGMGS2.
6. Reduced Piano (preset 0:0) volume to 80%.
7. Replaced Bagpipe (preset 0:109) with quieter and smoother version from SGM 2.01 by Shan.
8. Replaced Atmosphere (preset 0:99) with clearer version from SGM 2.01 by Shan.
9. Replaced Trumpet (preset 0:56) with SGM 2.01 version (improves playback in karaoke files like *Chumbawamba - Tubthumping*).
10. Replaced Fret Noise (preset 0:120) with short transient sample (improves thunder effect in *V-Rally mobile "Speed Spirit"* MIDI; original instrument preserved for SFX presets).
11. Removed Chorus and Reverb modulators from Tine Electric Piano (preset 0:004) to avoid excessive processing on midis with global CC values.
12. Added 127 drum banks from `XG_Sound_Set__from_SoundMAX_DLSbyXG_.sf2` for extended Yamaha XG MIDI compatibility.
13. Duplicated preset 127:40 to 127:41 for improved XG drum compatibility.
14. Set preset 0:0 Reverb to 33% (previously set to 7%).
15. Replaced Crystal (preset 0:98) with SGM 2.01 version.
16. Reduced attenuation for preset 0:2 Electric Grand Piano and preset 0:16 Tonewheel Organ for better volume balance.
17. Adjusted attenuation to 3 for preset 0:120 Fret Noise to balance loud playback occurrences.
18. Added preset 26:30 Rythm Distortion from `SGM-V2.01-XG-2.05.sf2` (balances playback in *Disturbed - Shout 2000* demo sequences).
19. Removed key range limit for Vocal Oooh (preset 0:53).
20. Adjusted key ranges for instruments associated with Vocal Oooh (preset 0:53) and Vocal Aaah (preset 0:52).
21. Changed Gun Shot (preset 0:127) to SGM-XG preset.
22. Changed Shakuhachi (preset 0:77) to the sample set from Creative 8MBGSFX E-mu Rev B.
23. Balanced Chorus and Reverb sends across updated instruments.

---

### Update 3.0 (No Limits PC Edition)
1. Removed the 64MB memory limit to optimize playback fidelity for PC MIDI synthesizers (VirtualMIDISynth, Falcosoft, TiMidity++).
2. Implemented Yamaha XG spatial emulation on all updated presets (Preset Chorus set to 25%, Reverb set to 33%).
3. Upgraded Clean Guitar (preset 0:27) to an isolated "Clean Guitar SGM 12L" instrument (12-velocity-layer, SGM 2.01 by Shan) with dynamic LPF and +3dB boost.
4. Replaced Muted Guitar (preset 0:28) with ColomboGMGS2 version for realistic string pluck attack and decay choke.
5. Replaced Viola (preset 0:41) with ColomboGMGS2 version for natural bow transients and body resonance.
6. Replaced String Ensemble 1 (preset 0:48) with ColomboGMGS2 version, reducing harsh high frequencies.
7. Replaced Slow Strings (preset 0:49) with ColomboGMGS2 version (optimized footprint by sharing String Ens 1 samples with extended loop envelopes).
8. Replaced Tenor Sax (preset 0:66) with ColomboGMGS2 version to eliminate lower-midrange muddiness.
9. Replaced Flute (preset 0:73) with ColomboGMGS2 version with +3dB attenuation padding against high-velocity clipping.
10. Replaced Pan Flute (preset 0:75) with ColomboGMGS2 version and balanced global attenuation (+4dB).
11. Replaced Synth Calliope (preset 0:82) with modified ColomboGMGS2 version, enriching lower-mids and softening high sibilance.
12. Replaced Solo Vox (preset 0:85) with ColomboGMGS2 version for smooth vocal formants.
13. Replaced Fiddle (preset 0:110) with ColomboGMGS2 version.
14. Added Pure Pan Lead (preset 2:82) from ColomboGMGS2 for expanded stereo XG compatibility.
15. Renamed legacy GeneralUser "Clean Guitar" instrument to "Clean Guitar GU" to preserve mapping for shared presets (*Chorused Clean Gt.*, *Clean Guitar 2*, *Funk Guitar*, *Star Theme*).
16. Cleaned and purged orphaned, unused samples from replaced instruments.

---

### Update 3.1
1. Reverted Clean Guitar (preset 0:27) to original GeneralUser GS instrument to preserve standard sequence mix balance.
2. Renamed legacy "Clean Guitar GU" instrument back to "Clean Guitar".

---

### Update 3.2
1. Replaced Guitar Harmonics (preset 0:31) with ColomboGMGS2 version for natural resonance and sustain loops.
2. Implemented Yamaha XG spatial sends on Guitar Harmonics (Chorus: 25%, Reverb: 33%).
3. Adjusted Guitar Harmonics attenuation from 6.40 to 4.40 (+2dB gain boost).
4. Purged orphaned samples from the replaced GeneralUser Gt. Harmonics instrument.

---

### Update 3.3
1. Replaced Melodic Woodblock (preset 0:115) with ColomboGMGS2 version.
2. Implemented Yamaha XG spatial sends on Woodblock (Chorus: 25%, Reverb: 33%).
3. Preserved original GeneralUser Wood Block instruments to maintain structural integrity for drum kits.

---

### Update 3.4
1. Replaced Charang (preset 0:84 / GM 85 Lead 5) with dual-layer Clavinet + Distortion Guitar from SGM 2.01 by Shan for improved clarity and punch in pop/rock mixes.
2. Implemented Yamaha XG spatial sends on Charang (Chorus: 25%, Reverb: 33%).
3. Purged orphaned samples and sub-instruments from the replaced GeneralUser Charang to maintain clean database structure.

---

## Issue Reporting & MIDI Playback Testing

If you encounter acoustic anomalies, unbalanced levels, or missing bank variations during MIDI playback:

1. Open a new ticket in the **[Issues Tab](https://github.com/Myshor/Myshor-GS-XG/issues)**.
2. Include:
   * MIDI / Karaoke file details (title, artist, or file link).
   * Playback timestamp (`MM:SS`) where the anomaly occurs.
   * MIDI Channel, Program Change (Preset ID), and Bank Select (`CC0` / `CC32`) values if known.
   * Playback software used (e.g., Falcosoft Soundfont MIDI Player, VirtualMIDISynth, TiMidity++, DOSBox).

---

## Legal Notice & Attribution

This SoundFont is distributed strictly for **non-commercial, educational, and preservation purposes**. It incorporates edited and rebalanced samples originating from community projects and legacy wavetable hardware:

* **GeneralUser GS:** S. Christian Collins
* **SGM 2.01:** Shan
* **ColomboGMGS2:** Duwindu Tharinda Perera
* **SoundFonts4U (SGM-2.01-HQ):** J.N.
* **Original Wavetable Heritage:** Creative Labs / E-mu Systems, Roland Corporation, Yamaha Corporation.
