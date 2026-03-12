# Bit Squash – Huffman Compression Tool

A GUI-based file compression and decompression tool built with Python and Tkinter, implementing Huffman Encoding from scratch using a min-heap (priority queue).

This project demonstrates core data structures, tree construction, binary encoding, and file handling — all wrapped in an interactive desktop interface.

## Features

### Core Algorithm

- Huffman Encoding implemented from scratch
- Min-Heap based tree construction (heapq)
- Prefix-free binary code generation

### Compression System

- Custom `.huff` file format
- Optional compressed header using zlib
- Binary-safe file handling

### Visualization & Analysis

- Encoded bitstream preview (first 1000 chars)
- ASCII Huffman code view
- Compression ratio & space savings calculation

### User Interface

- Built fully with Tkinter
- Progress bar + live status updates
- Supports TXT, CSV, and binary files

## How It Works

### Compression

- Read file in binary mode
- Calculate byte frequency
- Build Huffman Tree using Min-Heap
- Generate binary codes via DFS
- Convert data → bitstring → padded bytes
- Store header + payload in `.huff` format

### Decompression

- Read header & rebuild Huffman tree
- Convert bytes → bitstring
- Decode bitstream back to original bytes
- Write reconstructed file

## Requirements

- Python 3.8+
- No external libraries required

Built-in modules used:

- tkinter
- heapq
- json
- zlib
- os

## How to Run

```bash
python main.py
