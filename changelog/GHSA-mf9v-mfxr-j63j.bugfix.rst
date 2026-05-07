Fixed two high-severity security issues where decompression-bomb safeguards of the streaming API were bypassed:


1. When ``HTTPResponse.drain_conn()`` was called after the response had been read and decompressed partially.
2. During the second ``HTTPResponse.read(amt=N)`` or ``HTTPResponse.stream(amt=N)`` call when the response was decompressed using the official `Brotli <https://pypi.org/project/brotli/>`__ library.

See `GHSA-mf9v-mfxr-j63j <https://github.com/urllib3/urllib3/security/advisories/GHSA-mf9v-mfxr-j63j>`__ for details.
