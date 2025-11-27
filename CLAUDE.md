# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a LaTeX beamer presentation on FlashAttention, focusing on the mathematical foundations and implementation details of memory-efficient attention mechanisms. The main document `LLM_flashattention.tex` is a comprehensive presentation covering:

- Inefficiencies of standard attention operations
- Memory access patterns in attention computation
- FlashAttention algorithm and optimizations
- Standard attention backward pass implementation
- FlashAttention-2 improvements

## Build Commands

### Building the PDF
```bash
# Using pdflatex (basic build)
pdflatex LLM_flashattention.tex

# Using latexmk (recommended - handles dependencies automatically)
latexmk -pdf LLM_flashattention.tex

# Clean build artifacts
latexmk -C LLM_flashattention.tex
```

### Bibliography
The document uses a bibliography file `references.bib` with citations for FlashAttention papers. To properly build with citations:
```bash
latexmk -pdf LLM_flashattention.tex
```

## Document Structure

The presentation is structured as a beamer document with the following key sections:
- Introduction to attention inefficiencies
- Memory access analysis
- FlashAttention algorithm explanation
- Backward pass derivations
- Implementation considerations

## Development Notes

- The document uses the AnnArbor beamer theme
- Mathematical notation is heavily used with custom commands defined in the preamble
- TikZ is used for diagrams and mathematical illustrations
- Build artifacts are ignored via `.gitignore` (*.aux, *.log, *.pdf, etc.)