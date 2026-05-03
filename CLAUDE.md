# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-file static web app — a French-language replica of the **Service Hub** Jotform app. Everything lives in `index.html` (HTML + CSS + vanilla JS, no build step, no dependencies).

## Running the App

Open `index.html` directly in a browser. No server needed.

## Architecture

The entire app is one file with three logical sections:

1. **Navbar** — logo + navigation links + Login/Sign Up buttons.
2. **Pages** — five `<div class="page">` sections (`home`, `auto`, `maintenance`, `pets`, `earn`). Only the one with class `active` is visible at a time. `showPage(name)` handles switching.
3. **Modals** — two overlay divs (`overlay-login`, `overlay-signup`) positioned absolutely under the navbar. `openModal`, `bgClose`, and `switchModal` control them.

## Design Tokens

| Token | Value |
|---|---|
| Background | `#1e2f8e` (deep blue) |
| Primary / buttons | `#1565c0` |
| Service-item cards | `#dde3f5` / hover `#c5cde8` |
| Sub-page item cards | `#d0d8f0` / hover `#b3c0e8` |
| White cards | `border-radius: 10px`, `padding: 22-24px` |

## Content Language

All UI text is in **French**. Key translations used:
- Home → Accueil, Auto → Auto, Maintenance → Entretien, Pets → Animaux, Earn → Gagner
- Login → Connexion, Sign Up → S'inscrire
- Automotive Services → Services Automobiles
- Home Improvement → Rénovation et Entretien de Maison
- Pet and Animal Services → Services pour Animaux
- Earn With Us → Gagnez Avec Nous
- Share This App → Partager Cette Application
- Contact Us → Contactez-Nous
