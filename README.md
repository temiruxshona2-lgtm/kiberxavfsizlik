# kiberxavfsizlik

```mermaid
classDiagram
    class Message {
        +bytes data
        +encode()
    }

    class PublicKey {
        +import_key()
    }

    class Signature {
        +bytes sign
        +read()
    }

    class Hasher {
        +SHA256.new()
        +digest()
    }

    class Verifier {
        +verify(hash, signature)
    }

    Message --> Hasher : "hash yaratadi"
    PublicKey --> Verifier : "kalit orqali"
    Signature --> Verifier : "imzo yuboradi"
    Hasher --> Verifier : "xesh yuboradi"

```mermaid
