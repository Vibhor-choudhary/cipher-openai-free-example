# Vector Store Guide

Cipher can use a remote or local vector database for memory:

**Local Qdrant via Docker:**
- Install with Docker:
```bash
docker run -p 6333:6333 -p 6334:6334 qdrant/qdrant
```
- Set in `.env`:
```env
VECTOR_STORE_TYPE=qdrant
QDRANT_URL=http://localhost:6333
```

**Qdrant Cloud:**
- Sign up at [qdrant.tech](https://qdrant.tech/)
- Use your cloud endpoint/API key.

**Chroma/Milvus:**  
- Check Cipher docs for adapter support and config syntax.

> The memory section in `cipher.yml` can remain empty for local memory, or you can point to a cloud vector DB for cross-device/project sharing. 