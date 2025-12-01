# OnePiece - The Brutal Coder

> This tool is not related to the Japanese anime One Piece in any way; the name was chosen purely as a fan-inspired reference.

<img width="1584" height="396" alt="OP" src="https://github.com/user-attachments/assets/7a8bfe19-0c5f-442a-9946-4084af01d812" />


## What is this?

OnePiece is your invisible coding assistant that helps you tackle tough online coding exams. Press a hotkey, it captures your screen, reads the question with AI-powered OCR, asks Llama 3.1 for the answer, and either shows it to you or types it automatically. All completely stealth - no tab switching, no windows popping up.

## Features

**Three Power Moves:**

1. **Ctrl+Alt+F8 - Code Mode**
   - Captures screen, reads question, AI generates Java code, stores in memory
   - Perfect for "write a program to..." questions
   - Returns clean, copy-paste-ready code

2. **Ctrl+Alt+F10 - MCQ Mode**
   - Captures screen, reads question, AI picks the right answer, shows it instantly
   - Works with A/B/C/D, 1/2/3/4, or clickable button answers
   - Answer appears in a tiny overlay at the bottom

3. **Ctrl+Alt+F9 - Auto-Type Mode**
   - Types the answer from memory character by character
   - Press again to cancel if needed
   - Looks like manual typing

**Stealth Operation:**

- No window activation - browser stays focused
- No clipboard interference - everything in memory
- Tiny bottom overlay - barely noticeable
- Silent operation - no sounds or popups
- Zero detection by exam sites

## How to Use

1. Launch OnePiece.exe (ensure logo.png and tessdata folder are present)
2. Navigate to your exam in fullscreen browser
3. For coding questions:
   - Press Ctrl+Alt+F8
   - Wait for "Ready!" message
   - Click in code editor
   - Press Ctrl+Alt+F9 to auto-type
4. For MCQ questions:
   - Press Ctrl+Alt+F10
   - Read answer in overlay
   - Click the correct option

## Technical Details

- OCR: Tesseract 5.2.0
- AI: AWS Bedrock Llama 3.1 8B
- Auto-typing: WindowsInput simulator
- Framework: .NET 8.0 WPF + Windows Forms
- Authentication: Hardcoded Bearer token

## Requirements

- Windows 10/11
- Internet connection
- tessdata folder with eng.traineddata
- Exam questions visible on screen

## Troubleshooting

**"Failed to initialize Tesseract"**
- Ensure tessdata folder is next to OnePiece.exe
- Check eng.traineddata file exists inside tessdata

**"Bedrock API error"**
- Verify internet connection
- Bearer token might be expired

**"No text found"**
- Screenshot may be blurry
- Try capturing again
- OCR doesn't work on handwritten text

**"Wrong MCQ answer"**
- AI can make mistakes
- Ensure full question with all options is visible
- Sometimes it guesses wrong

## Hotkeys Reference

| Hotkey | Function |
|--------|----------|
| Ctrl+Alt+F8 | Capture & analyze (Code mode) |
| Ctrl+Alt+F10 | Capture & analyze (MCQ mode) |
| Ctrl+Alt+F9 | Type answer / Cancel typing |

## Disclaimers

- Use at your own risk - not responsible for academic integrity violations
- AI answers aren't always correct - double-check when possible
- Requires internet connection
- English text only
- Not a guarantee of success

---

Built with C#, AWS Bedrock, Tesseract, and questionable exam ethics lol.

> "The rise of worst generation ?"
