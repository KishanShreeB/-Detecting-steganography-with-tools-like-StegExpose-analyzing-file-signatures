# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
List of Images with Steganography Detection Scores and File Signature Details
<img width="872" height="185" alt="Screenshot 2025-09-27 140756" src="https://github.com/user-attachments/assets/7c0fefe2-cf22-4f20-b3fe-fc22ad36a5e0" />
<img width="872" height="185" alt="Screenshot 2025-09-27 140756" src="https://github.com/user-attachments/assets/ee1fa404-004a-40d6-b6e1-0dd2d008a059" />

<img width="929" height="179" alt="Screenshot 2025-09-27 144016" src="https://github.com/user-attachments/assets/46ee5572-b4b1-41a8-8416-de0a78e55db5" />
<img width="945" height="78" alt="Screenshot 2025-09-27 144025" src="https://github.com/user-attachments/assets/6491bd00-8a16-47d3-b654-2b5f16055060" />


## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
