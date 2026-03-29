# Bilag – Spec2JUnit: AI som sparringspartner til test

## 1. Formål

Dette bilag viser, hvordan AI (fx ChatGPT) kan bruges som **støtteværktøj** til at generere JUnit-tests ud fra en specifikation.

Vigtigt:

> AI erstatter ikke din forståelse – den understøtter den.

---

## 2. Hvad er Spec2JUnit?

Spec2JUnit betyder:

👉 Vi giver en specifikation → og får forslag til JUnit-tests.

Eksempel:

**Specifikation:**
- Name har fornavn og efternavn  
- Ingen må være null eller tomme  
- getFullName returnerer "fornavn efternavn"

**AI kan generere:**
- tests for normale tilfælde  
- tests for grænsetilfælde  
- tests for exception  

---

## 3. Arbejdsproces (meget vigtig)

Brug altid denne rækkefølge:

1. Læs specifikationen  
2. Find regler  
3. Lav testidéer  
4. Brug AI  
5. Vurder og ret output  

👉 AI er trin 4 – ikke trin 1.

---

## 4. Eksempel

### Dine testidéer

- ("Ada", "Lovelace") → "Ada Lovelace"  
- ("A", "L") → "A L"  
- ("", "Lovelace") → exception  
- (null, "Lovelace") → exception  

### Prompt

```
Generér JUnit-tests for en Name-klasse.

Krav:
- Test normale tilfælde
- Test grænsetilfælde
- Test ugyldige input (exception)
```

---

## 5. Vurdering af AI-output

Når du får tests fra AI, skal du kontrollere:

- Dækker testen alle regler?  
- Mangler der grænsetilfælde?  
- Er exception testet?  
- Er testene forståelige?  

👉 AI tester ofte kun “happy path”.

---

## 6. Typiske fejl fra AI

AI glemmer ofte:

- ugyldige input  
- grænsetilfælde  
- flere variationer  
- præcise assertions  

---

## 7. God praksis

✔ Lav altid dine egne testidéer først  
✔ Brug AI til at spare tid  
✔ Ret og forbedr output  
✔ Tænk kritisk  

---

## 8. Dårlig praksis

✘ Kopiér AI-output uden at forstå  
✘ Spring testidéer over  
✘ Stol blindt på resultatet  

---

## 9. Designprincip

> Du er ansvarlig for testen – ikke AI.

AI er et værktøj, ikke en løsning.

---

## 10. Øvelse

1. Lav testidéer for en klasse  
2. Brug AI til at generere tests  
3. Sammenlign  
4. Ret AI-output  

---

## Afslutning

Spec2JUnit gør det muligt at:

- arbejde hurtigere  
- få inspiration  
- strukturere tests  

Men kun hvis du:

👉 forstår problemet først

👉 og vurderer output bagefter
