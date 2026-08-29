# Kanji Cards

- Kanji
- QR -> Jisho.org search
- Rank
  - ? = ??
  - E = N5
  - D = N4
  - C = N3
  - B = N2
  - A = N1
  - S = SPECIAL
- and stroke count
- Gamified design
- PDF Export (if can)

```json
{
  "cards": [
    {
      "id": "KFL",
      "kanji": "愛",
      "rank": "C",
      "strokes": 13,
      "created": "2026-08-14"
    }
  ]
}
```

```cs
public enum KanjiTier {
    Unknown = 0,
    E       = 1,
    D       = 2,
    C       = 3,
    B       = 4,
    A       = 5,
    S       = 6,
}
```

```cs
// 1. The base alphabet (no digits, no ambiguous chars)
public static class KanjiAlphabet {
    public const string Letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
}

// 2. The Value Object for your short code
public readonly record struct KanjiCode {
    public string Value { get; init; }

    // Private constructor enforces validation
    private KanjiCode() {}

    // --- Factory Methods ---

    // Random: for temporary or non-sequential codes
    public static KanjiCode GenerateRandom() {
        var random = Random.Shared;
        var chars = new char[3];
        for (int i = 0; i < 3; i++)
            chars[i] = (char)('A' + random.Next(26));
        var value = new string(chars);

        return new KanjiCode { Value = value };
    }

    // FROM_STRING
    // if (string.IsNullOrEmpty(value) || value.Length != 3)
    //   throw new ArgumentException("KanjiCode must be exactly 3 characters.");
    // if (!value.All(c => c >= 'A' && c <= 'Z'))
    //   throw new ArgumentException("KanjiCode must contain only uppercase A-Z.");
}
```
