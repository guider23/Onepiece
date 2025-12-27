# OnePiece - The Brutal Coder

> This tool is not related to the Japanese anime One Piece in any way; the name was chosen purely as a fan-inspired reference.

<img width="1584" height="396" alt="OP" src="https://github.com/user-attachments/assets/7a8bfe19-0c5f-442a-9946-4084af01d812" />


## What is this?

OnePiece is your invisible coding assistant that helps you tackle tough online coding exams. Press a hotkey, it captures your screen, reads the question with AI-powered OCR, asks Llama AI for the answer, and either shows it to you or types it automatically. All completely stealth - no tab switching, no windows popping up.

## Features

**Five Power Moves:**

1. **Ctrl+Alt+F8 - Code Mode**
   - Captures screen, reads question, AI generates Java code, stores in memory
   - Perfect for "write a program to..." questions
   - Returns clean, copy-paste-ready code
   - Uses current selected model (default: Llama 8B - Fast)

2. **Ctrl+Alt+F10 - MCQ Mode**
   - Captures screen, reads question, AI picks the right answer, shows it instantly
   - Works with A/B/C/D, 1/2/3/4, or clickable button answers
   - Answer appears in a tiny overlay at the bottom
   - Always uses Llama 70B (Smart model for better accuracy)

3. **Ctrl+Alt+F9 - Auto-Type Mode**
   - Types the answer from memory character by character
   - Press again to cancel if needed
   - Looks like manual typing

4. **Ctrl+Alt+F11 - Model Switcher**
   - Cycles through 4 different AI models for code mode
   - Available models: 8B (Fast), 11B (Balanced), 70B (Smart), 90B (Most Powerful)
   - Shows current model in overlay
   - MCQ mode always uses 70B regardless of selection

5. **Ctrl+Alt+F12 - Error Debugger**
   - Got a compilation error? Press this!
   - Captures error screen, reads error message
   - Combines with previous code from memory
   - AI analyzes and fixes the bug logically
   - Shows "Fixed! Press Ctrl+Alt+F9 to type"
   - Corrected code ready to paste

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
5. If code has errors:
   - Submit code and see error
   - Press Ctrl+Alt+F12 to capture error
   - Wait for "Fixed!" message
   - Clear old code, click in editor
   - Press Ctrl+Alt+F9 to type corrected code

## Technical Details

- OCR: Tesseract 5.2.0
- AI Models: AWS Bedrock Meta Llama
  - Code Mode: 8B / 11B / 70B / 90B (switchable)
  - MCQ Mode: 70B (fixed for accuracy)
- Auto-typing: WindowsInput simulator
- Framework: .NET 8.0 WPF + Windows Forms
- Authentication: Hardcoded Bearer token
- Region: us-east-1

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
- MCQ mode uses Llama 70B for better accuracy (80-85% correct)
- Ensure full question with all options is visible on screen
- Try to minimize screen clutter and noise

**"Want faster/smarter code generation"**
- Press Ctrl+Alt+F11 to cycle through models
- 8B = Fastest but basic
- 11B = Good balance
- 70B = Smarter but slower
- 90B = Most powerful but slowest

## Hotkeys Reference

| Hotkey | Function |
|--------|----------|
| Ctrl+Alt+F8 | Capture & analyze (Code mode) |
| Ctrl+Alt+F10 | Capture & analyze (MCQ mode - uses 70B) |
| Ctrl+Alt+F9 | Type answer / Cancel typing |
| Ctrl+Alt+F11 | Cycle AI model (8B → 11B → 70B → 90B) |
| Ctrl+Alt+F12 | Debug error (captures error + fixes code) |

## Disclaimers

- Use at your own risk - not responsible for academic integrity violations
- AI answers aren't always correct - double-check when possible
- Requires internet connection
- English text only
- Not a guarantee of success

---

> "The rise of worst generation ?"


Built with C#, AWS Bedrock, Tesseract, and questionable exam ethics.

"The sea of code is vast. Navigate it with OnePiece!"

