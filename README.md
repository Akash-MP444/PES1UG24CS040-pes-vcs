# PES-VCS

A lightweight Git-inspired Version Control System implemented in C to understand low-level filesystem operations, object storage, staging areas, commits, and repository management.

---

## Overview

PES-VCS is a miniature local version control system that mimics core Git internals.  
The project demonstrates how version control tools manage:

- Object storage
- File tracking
- Commit history
- Trees and snapshots
- References and HEAD management
- Filesystem-level persistence

The system was developed as part of an Operating Systems / Systems Programming learning project.

---

## Features

### Core Version Control Operations
- Initialize repositories
- Stage files
- Create commits
- View commit logs
- Track repository status

### Object Storage System
- Blob object creation
- Tree object generation
- Commit object management
- SHA-based object storage
- Object sharding structure

### Internal Git Concepts
- Index / staging area
- Branch references
- HEAD pointer management
- Tree snapshots
- Commit chaining

### Testing & Validation
- Object storage testing
- Tree structure validation
- Integration test scripts

---

## Tech Stack

- **Language:** C
- **Build System:** Makefile
- **Platform:** Linux / POSIX systems
- **Concepts Used:** Filesystems, hashing, object stores, persistence

---

## Repository Structure

```text
PES1UG24CS040-pes-vcs/
│
├── commit.c              # Commit object handling
├── tree.c                # Tree object management
├── object.c              # Object storage logic
├── index.c               # Staging/index management
├── pes.c                 # Main CLI implementation
│
├── include/              # Header files
├── screenshots/          # Project screenshots
│
├── test_objects.c        # Object tests
├── test_tree.c           # Tree tests
├── test_sequence.sh      # Integration tests
│
├── Makefile
└── README.md
```

---

## Build Instructions

Compile the project using:

```bash
make
```

Or manually:

```bash
gcc *.c -o pes
```

---

## Running the Project

### Initialize Repository

```bash
./pes init
```

### Add Files

```bash
./pes add <filename>
```

### Check Status

```bash
./pes status
```

### Create Commit

```bash
./pes commit "Initial commit"
```

### View Commit Log

```bash
./pes log
```

---

## Internal Architecture

### Object Store
Objects are stored inside:

```text
.pes/objects/
```

Each object is hashed and stored similarly to Git's object database.

### Index
The staging area tracks files before commits.

### Trees
Tree objects represent directory snapshots.

### Commits
Commit objects store:
- Parent commit reference
- Tree reference
- Commit metadata

---

## Implemented Concepts

| Concept | Description |
|---|---|
| Blob Objects | File content storage |
| Tree Objects | Directory snapshots |
| Commit Objects | Repository history |
| SHA Hashing | Object identification |
| Staging Area | File tracking before commits |
| HEAD References | Current branch tracking |

---

## Testing

Run object tests:

```bash
./test_objects
```

Run tree tests:

```bash
./test_tree
```

Run integration tests:

```bash
make test-integration
```

---

## Learning Outcomes

This project helped in understanding:

- Git internals
- POSIX filesystem operations
- Persistent storage systems
- Hash-based object management
- Branch and commit architecture
- Garbage collection concepts
- Working directory synchronization

---

## Future Improvements

- Branch checkout support
- Merge functionality
- Detached HEAD handling
- Garbage collection
- Conflict detection
- Remote repository support

---

## Author

**Akash MP**
