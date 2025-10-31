---
title: "Construire un PC avec des pièces de récup (Ryzen 5 5500 / Ryzen 7 3800X + RTX 2070 Super)"
date: 2025-10-31
tags: ["hardware", "PC", "build", "récupération", "upgrade", "budget"]
categories: ["hardware"]
draft: false
description: "Guide pratique pour réutiliser un GPU RTX 2070 Super, 32 Go DDR4 et du stockage existant, en complétant avec une carte mère A520, un ventirad et une alimentation 650 W."
slug: "pc-recuperation-ryzen-2070-super"
summary: "Réemploi malin: base RTX 2070 Super + DDR4 32 Go, avec Ryzen 5 5500 ou Ryzen 7 3800X — quel équilibre perfs/bruit/coût ?"
---

## Objectif

Assembler une machine performante et économique en réemployant des composants en bon état, puis en complétant uniquement le nécessaire neuf. Deux options CPU sont envisagées (Ryzen 5 5500 ou Ryzen 7 3800X) selon votre priorité: silence/efficacité ou multi‑cœurs.

---

## Base réutilisée (pièces de récup)

- GPU: NVIDIA GeForce RTX 2070 Super ZOTAC AMP (8 Go)
- Mémoire: 4×8 Go DDR4 Corsair Vengeance LPX (32 Go)
- Stockage: SSD SATA 480 Go + HDD 3 To

Ces pièces offrent déjà une excellente base pour du 1080p/1440p, bureautique avancée, création légère et jeux compétitifs. Le passage à 32 Go de RAM aide pour le multitâche et certains jeux/éditeurs.

---

## À acheter (neuf)

| Composant | Modèle recommandé | Prix TTC (≈) | Lien |
| :-- | :-- | --: | :-- |
| Carte mère | Gigabyte A520M DS3H V2 (Micro‑ATX, AM4) | 59,99 € | [Lien](https://amzn.to/4oizHUQ) |
| Ventirad CPU | Cooler Master Hyper 212 Halo (AM4) | 28,72 € | [Lien](https://amzn.to/4ojFMjP) |
| Alimentation | Gigabyte P650G — 650 W, 80+ Gold | 58,97 € | [Lien](https://amzn.to/4hB78zf) |

_Prix indicatifs relevés sur Amazon.fr le 31/10/2025 (TTC) — susceptibles de varier selon vendeurs et disponibilités. Certains liens peuvent être affiliés; ils n’affectent pas le prix et contribuent à soutenir le site._

Points de vigilance:

- Vérifier/mettre à jour le BIOS de la carte mère pour une compatibilité optimale (Ryzen 3000/5000). La A520M DS3H V2 supporte Ryzen 3000 (Matisse) et Ryzen 5000 (Vermeer) — un flash BIOS peut être requis selon le lot.
- Le boîtier doit accepter une carte Micro‑ATX et la longueur de la RTX 2070 Super; prévoir 2× 8‑pin PCIe selon le modèle.

### Alternative plus complète (B550, AM4)

- Carte mère: GIGABYTE B550M DS3H AC (Micro‑ATX, AM4, Wi‑Fi AC) | [Lien](https://amzn.to/3WzLFNx)
  - Prix TTC (≈): 88 € — relevé le 31/10/2025 (Amazon.fr), susceptible d’évoluer.

Important: cette carte reste en AM4 et fonctionne avec les Ryzen 3000/5000 et la mémoire DDR4. Intérêt: meilleure connectique (Wi‑Fi AC intégré), un VRM un peu plus robuste que l’A520, et davantage d’options M.2/PCIe (dont PCIe 4.0 via le chipset B550). Vous pouvez donc réutiliser votre CPU et vos barrettes DDR4 tout en gagnant en confort/évolutivité, sans basculer sur l’écosystème AM5/DDR5.

---

## Choix du processeur: quel équilibre ?

Deux profils s’opposent: efficacité/silence (6 cœurs Zen 3) vs polyvalence multi‑cœurs (8 cœurs Zen 2).

### Option A — Ryzen 5 5500 (Zen 3, 6C/12T)

- Atouts:
  - IPC Zen 3 plus élevé que Zen 2: bonne réactivité en usage courant et jeux.
  - Consommation/chauffe modérées: plus simple à refroidir, machine plus silencieuse.
  - PCIe 3.0 uniquement côté CPU — sans impact ici: la RTX 2070 Super est PCIe 3.0 et le SSD principal est en SATA.
- Inconvénients:
  - 6 cœurs/12 threads: limite plus vite en rendu lourd, streaming CPU ou VM multiples.
  - Moins durable sur des workloads massivement multi‑cœurs.

Idéal si votre priorité est le jeu 1080p/1440p, la fluidité générale et le silence, tout en gardant un budget serré.

### Option B — Ryzen 7 3800X (Zen 2, 8C/16T)

- Atouts:
  - 8 cœurs/16 threads: plus de marge pour rendu, encodage CPU, VM et multitâche intensif.
  - Bon compromis si vous faites régulièrement du streaming/record CPU en parallèle des jeux.
- Inconvénients:
  - Chauffe/consommation supérieures: le Hyper 212 suffit mais sera plus sollicité (potentiellement plus audible).
  - IPC inférieur au Zen 3: en pur mono‑cœur, parfois derrière un 5500.

Pertinent si vous faites souvent de la création/encodage/VM, ou si vous cherchez une marge multi‑cœurs à faible coût d’acquisition.

---

## Équilibrage global de la machine

- Goulot attendu en jeu: la RTX 2070 Super reste la limite principale en 1440p; le choix CPU impacte surtout la stabilité des fps en scènes CPU‑bound et la réactivité générale.
- Mémoire 32 Go: confortable pour créa légère, navigateurs gourmands et jeux modernes.
- Stockage: le SSD SATA suffit pour l’OS et 2–3 jeux lourds; placez les bibliothèques massives sur le HDD 3 To.
- Alimentation 650 W Gold: marge suffisante pour la 2070 Super et les deux CPU; câblage propre et ventilation bien gérée = bruit contenu.

---

## Montage et vérifications rapides

- Mettre à jour le BIOS avant installation CPU si besoin (consulter la QVL de la carte mère).
- Monter les 4 barrettes (4×8 Go) en suivant le manuel pour l’ordre des slots.
- Appliquer une pâte thermique de qualité et orienter le Hyper 212 pour un flux avant→arrière.
- Configurer des courbes de ventilateurs souples (silence au repos, discret en charge).
- Installer les derniers pilotes chipset AMD et GPU NVIDIA.

---

## Conclusion rapide

- Vous privilégiez le silence, la réactivité et le jeu: Ryzen 5 5500.
- Vous avez des besoins réguliers en multi‑cœurs (rendu, encodage CPU, VM): Ryzen 7 3800X.

Dans les deux cas, la base RTX 2070 Super + 32 Go DDR4 fait un excellent PC polyvalent, à très bon rapport perfs/prix grâce au réemploi.

---

## Voir aussi

- [Récupérer et upgrader un Dell Precision 3440 SFF](/posts/dell-precision-3440-sff-recuperation-upgrade/)
- [Configuration PC haut de gamme équilibrée pour le rendu 3D (2025)](/posts/pc-haut-de-gamme-rendu-3d/)

---

## Besoin d’un montage ou dépannage à Toulon ?

Basé à Toulon, j’interviens pour le montage, l’upgrade et le dépannage informatique sur Toulon, La Seyne‑sur‑Mer, Hyères, Bandol et plus largement dans le Var (83) et la région PACA.

[Me contacter pour une intervention](/contact/)
