# manga-ocr-video-generator
This is first code 
# AI Manga Recap Generator

An advanced Python script that automatically converts manga PDFs into engaging Hindi vidLooks like something went wrong!
eo recaps for YouTube. Perfect for content creators who want to produce high-quality manga recap videos with minimal manual effort.

## Features

- **High-Quality PDF Extraction**: Extracts crisp pages from manga PDFs with advanced image processing
- **Advanced OCR**: Uses EasyOCR with enhanced preprocessing for accurate text extraction
- **AI-Powered Script Generation**: Creates engaging Hindi narratives using state-of-the-art language models
- **Professional Text-to-Speech**: High-quality Hindi voice synthesis using Microsoft Edge TTS
- **Smart Video Creation**: Automatically formats manga pages for optimal YouTube viewing
- **GPU Optimized**: Designed specifically for Google Colab T4 GPUs
- **YouTube Ready**: Outputs 1920x1080 HD videos with perfect formatting

## Tech Stack

- **Computer Vision**: OpenCV, PIL, PyMuPDF
- **OCR**: EasyOCR with multi-language support
- **AI Models**: Transformers (BART, Helsinki NLP translation models)
- **Audio**: Microsoft Edge TTS
- **Video**: MoviePy with advanced effects
- **GPU**: CUDA support for faster processing

## Quick Start

### 1. Setup in Google Colab

```python
# Install dependencies
!pip install -q moviepy pillow easyocr PyMuPDF transformers torch accelerate
!pip install -q edge-tts asyncio nest-asyncio
!pip install -q opencv-python numpy scikit-image
!pip install -q sentence-transformers
```

### 2. Upload Your PDF
Upload your manga PDF to `/content/Ch_199_Side_Story_20.pdf` in Colab

### 3. Run the Script
```python
# Simply run the main script
asyncio.run(main())
```

### 4. Customize Settings
```python
# Change voice (choose from 3 Hindi voices)
SELECTED_VOICE = VOICE_OPTIONS[1]  # Female voice

# Adjust video quality
BITRATE = "8000k"  # Higher quality
FPS = 30          # Smooth playback

# Process more pages
max_pages = 6     # Longer videos
```

## Configuration Options

### Voice Options
- `hi-IN-MadhurNeural` - Male, clear and professional
- `hi-IN-SwaraNeural` - Female, expressive and engaging
- `hi-IN-AnanyaNeural` - Female, warm and friendly

### Video Settings
- **Resolution**: 1920x1080 (Full HD)
- **Frame Rate**: 30 FPS
- **Bitrate**: 5000k-8000k (adjustable)
- **Format**: MP4 with H.264 encoding

### AI Models
- **Summarization**: facebook/bart-large-cnn
- **Translation**: Helsinki-NLP/opus-mt-en-hi
- **OCR**: EasyOCR with English + Japanese support

## How It Works

1. **PDF Processing**: Extracts high-resolution pages with smart resizing
2. **Image Enhancement**: Applies noise reduction, contrast enhancement, and sharpening
3. **OCR Extraction**: Uses advanced preprocessing to extract clean text
4. **Content Generation**: Creates engaging narratives using AI models
5. **Translation**: Converts content to natural Hindi using neural translation
6. **Audio Synthesis**: Generates professional-quality Hindi narration
7. **Video Creation**: Combines images with smart scaling and smooth transitions

## Output Files

After processing, you'll get:
- `manga_recap_chapter_X.mp4` - Final YouTube-ready video
- `narration.wav` - High-quality audio file
- `generated_script.txt` - AI-generated script with translations
- `raw_ocr_text.txt` - Extracted text for debugging

## Advanced Features

### Smart Image Processing
- Automatic manga page detection
- Panning effects for tall pages
- Optimal scaling for readability
- Professional transitions and effects

### Robust OCR
- Multi-pass text extraction
- Confidence-based filtering
- Common error correction
- Noise reduction preprocessing

### Intelligent Fallbacks
- Generic script generation when OCR fails
- Multiple narrative templates
- Error handling and recovery
- Cached processing for faster reruns

## System Requirements

- **GPU**: T4 or better (Google Colab free tier works)
- **RAM**: 12GB+ recommended
- **Storage**: 2GB+ for dependencies and output
- **Python**: 3.7+

## Limitations

- Optimized for manga/comic content
- Best results with clear, high-contrast text
- Processing time: 5-15 minutes depending on content
- Requires stable internet for AI model downloads

## Troubleshooting

### Common Issues

**OCR returns garbled text:**
```python
# The script includes enhanced preprocessing
# Check raw_ocr_text.txt for debugging
# Fallback scripts are automatically generated
```

**Video quality issues:**
```python
# Increase bitrate for better quality
BITRATE = "8000k"

# Adjust FPS if needed
FPS = 30
```

**Memory errors:**
```python
# Reduce max_pages
max_pages = 3

# Use CPU if GPU memory insufficient
device = "cpu"
```

## Contributing

Pull requests welcome! Areas for improvement:
- Additional language support
- More voice options
- Enhanced video effects
- Better OCR preprocessing
- Alternative AI models

## License

MIT License - feel free to use for commercial projects

## Credits

- **OCR**: EasyOCR by JaidedAI
- **AI Models**: Hugging Face Transformers
- **TTS**: Microsoft Edge Text-to-Speech
- **Video**: MoviePy library
- **PDF Processing**: PyMuPDF

## Support

If you find this useful:
- Star the repository
- Share with other content creators
- Report issues or suggest features

---

**Note**: This tool is designed for educational and creative purposes. Please respect copyright laws and manga creators' rights when using this tool.
