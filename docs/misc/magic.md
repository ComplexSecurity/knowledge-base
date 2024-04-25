Magic bytes are specific patterns at the beginning of a file used to indicate the file format, independent of file extensions. These patterns, typically a sequence of bytes, are unique to various file types and are used by software to determine the file's format and how to process it.

Magic bytes are used to identify the format of a file, such as an image, document, audio, or video file. They serve as a signature for the file format. These bytes are usually located at the beginning of a file, known as the file header.

- For example, JPEG image files often start with the bytes `FF D8 FF`, and PNG image files begin with `89 50 4E 47 0D 0A 1A 0A`.
- PDF documents typically start with `%PDF-`

Operating systems and applications use magic bytes to determine how to handle a file. This is particularly useful when file extensions are missing or incorrect. Web servers and browsers often use magic bytes for [[MIME-Type|MIME type]] detection, influencing how a file is rendered or processed.

Magic bytes are used in security to validate file types. For instance, an upload filter might check a file's magic bytes to ensure it matches its declared file type, helping to prevent certain types of malicious file uploads. In digital forensics, magic bytes can be used to identify and recover file types from disk images or fragments.

While useful, magic bytes are not foolproof. Files can be crafted with misleading magic bytes for malicious purposes, like disguising an executable file as a benign file type.