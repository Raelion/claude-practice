# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Working with the user

The user is a beginner. After making each change, briefly explain in plain language what it does.

## Overview

A single static page, `index.html`, with all CSS inline in a `<style>` block. There is no build step, package manager, linter, or test suite. To view changes, open `index.html` in a browser (`Start-Process index.html` from PowerShell) and refresh.

## Structure

- Page content: an `h1` followed by a `.cards` grid of `.card` elements (each an `h2` + `p`).
- Theme: dark background (`#121212`) with light text; cards are a slightly lighter dark (`#1e1e1e`). If the body background changes, check heading contrast since cards keep their own colors.
- Font: Inter from Google Fonts, falling back to system fonts.
- Responsive rules live in a `@media (max-width: 600px)` block at the end of the stylesheet; card hover effects are wrapped in `@media (hover: hover)` so they don't stick on touch devices.

## Git

- Remote: `origin` → https://github.com/Raelion/claude-practice (public), branch `main`.
- Commits pushed to GitHub are undone with `git revert`, not by rewriting history.
- The GitHub CLI is installed at `C:\Program Files\GitHub CLI\gh.exe` and may not be on `PATH` in older shells.
