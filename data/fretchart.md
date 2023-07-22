# Fret Chart

In order to input our data, we need to input our values

The left column is the fret number.
Fret number starts at 0, the note that the string plays when there is NO finger on it.

The colums are the string values in standard tuning.

Each cell has three values.
The left number is the index number that will be used to identify which fret to hold.
The Middle number is the MIDI number.
The right value is the key.
We did it this way to check our values and wouldn't get lost or make major errors.

Notice that between E and A, A and D, D and G, and B and e, the values increase by a value of five.
The difference between G and B is a value of 4.

Our [chord list](chordlist.md) will use the index number such that we can enter our data more efficiently.

Take note that the range of MIDI values on a guitar with 22 frets is between 40 (E2) and 86 (D6).
If Middle C has a value of 60 (C4), that give us 20 notes below Middle C to play with and 26 notes above middle C to play with. This is adequate.

|    |      E        |      A        |      D        |      G        |      B        |      e        |
|----|---------------|---------------|---------------|---------------|---------------|---------------|
|  0 |   0:40:E2     |   1:45:A2     |   2:50:D3     |   3:55:G3     |   4:59:B3     |   5:64:E4     |
|  1 |   6:41:F2     |   7:46:Bb/A#2 |   8:51:Eb/D#3 |   9:56:Ab/G#3 |  10:60:C4     |  11:65:F4     |
|  2 |  12:42:F#/Gb2 |  13:47:B2     |  14:52:E3     |  15:57:A3     |  16:61:C#/Db4 |  17:66:F#/Gb4 |
|  3 |  18:43:G2     |  19:48:C3     |  20:53:F3     |  21:58:Bb/A#3 |  22:62:D4     |  23:67:G4     |
|  4 |  24:44:Ab/G#2 |  25:49:C#/Db3 |  26:54:F#/Gb3 |  27:59:B3     |  28:63:Eb/D#4 |  29:68:Ab/G#4 |
|  5 |  30:45:A2     |  31:50:D3     |  32:55:G3     |  33:60:C4     |  34:64:E4     |  35:69:A4     |
|  6 |  36:46:Bb/A#2 |  37:51:Eb/D#3 |  38:56:Ab/G#3 |  39:61:C#/Db4 |  40:65:F4     |  41:70:Bb/A#4 |
|  7 |  42:47:B2     |  43:52:E3     |  44:57:A3     |  45:62:D4     |  46:66:F#/Gb4 |  47:71:B4     |
|  8 |  48:48:C3     |  49:53:F3     |  50:58:Bb/A#3 |  51:63:Eb/D#4 |  52:67:G4     |  53:72:C5     |
|  9 |  54:49:C#/Db3 |  55:54:F#/Gb3 |  56:59:B3     |  57:64:E4     |  58:68:Ab/G#4 |  59:73:C#/Db5 |
| 10 |  60:50:D3     |  61:55:G3     |  62:60:C4     |  63:65:F4     |  64:69:A4     |  65:74:D5     |
| 11 |  66:51:Eb/D#3 |  67:56:Ab/G#3 |  68:61:C#/Db4 |  69:66:F#/Gb4 |  70:70:Bb/A#4 |  71:75:Eb/D#5 |
| 12 |  72:52:E3     |  73:57:A3     |  74:62:D4     |  75:67:G4     |  76:71:B4     |  77:76:E5     |
| 13 |  78:53:F3     |  79:58:Bb/A#3 |  80:63:Eb/D#4 |  81:68:Ab/G#4 |  82:72:C5     |  83:77:F5     |
| 14 |  84:54:F#/Gb3 |  85:59:B3     |  86:64:E4     |  87:69:A4     |  88:73:C#/Db5 |  89:78:F#/Gb5 |
| 15 |  90:55:G3     |  91:60:C4     |  92:65:F4     |  93:70:Bb/A#4 |  94:74:D5     |  95:79:G5     |
| 16 |  96:56:Ab/G#3 |  97:61:C#/Db4 |  98:66:F#/Gb4 |  99:71:B4     | 100:75:Eb/D#5 | 101:80:Ab/G#5 |
| 17 | 102:57:A3     | 103:62:D4     | 104:67:G4     | 105:72:C5     | 106:76:E5     | 107:81:A5     |
| 18 | 108:58:Bb/A#3 | 109:63:Eb/D#4 | 110:68:Ab/G#4 | 111:73:C#/Db5 | 112:77:F5     | 113:82:Bb/A#5 |
| 19 | 114:59:B3     | 115:64:E4     | 116:69:A4     | 117:74:D5     | 118:78:F#/Gb5 | 119:83:B5     |
| 20 | 120:60:C4     | 121:65:F4     | 122:70:Bb/A#4 | 123:75:Eb/D#5 | 124:79:G5     | 125:84:C6     |
| 21 | 126:61:C#/Db4 | 127:66:F#/Gb4 | 128:71:B4     | 129:76:E5     | 130:80:Ab/G#5 | 131:85:C#/Db6 |
| 22 | 132:62:D4     | 133:67:G4     | 134:72:C5     | 135:77:F5     | 136:81:A5     | 137:86:D6     |

