# TODO - RAG Document Assistant Debug & Cleanup

## Phase 1: Fix Core Issues

### 1. Fix pages/1_Chat.py - Add missing embed_text function
- [ ] Add embed_text function to core/embeddings.py that generates embeddings for text chunks

### 2. Fix ingestion/pipeline.py - Add missing imports and remove debug code
- [ ] Add imports: load_document, create_vectorstore, generate_answer
- [ ] Remove debug print statements: print(type(documents)), print(documents)

## Phase 2: Clean Up Architecture

### 3. Decide on single chat implementation
- [ ] Keep app.py's Chat page (using core/rag_pipeline.py) as the main implementation
- [ ] Option: Remove or disable pages/1_Chat.py to avoid confusion

### 4. Fix any import inconsistencies
- [ ] Ensure all imports are consistent across files

## Phase 3: Add Missing Dependencies

### 5. Update requirements.txt
- [ ] Add: langchain
- [ ] Add: langchain-core
- [ ] Add: langchain-google-genai
- [ ] Add: langchain-community
- [ ] Add: pytesseract (for OCR)
- [ ] Add: pdf2image (for OCR)

## Phase 4: Testing

### 6. Verify the application runs
- [ ] Test the Streamlit app
- [ ] Verify document upload and chat functionality works
