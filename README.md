# Übung: Bullet Component mit dynamischen Styles

## Aufgabe

Erstelle eine `BulletPoint` Komponente, die verschiedene Varianten und Farben unterstützt.

## Anforderungen

### 1. Props Interface

Die Komponente soll folgende Props akzeptieren:

- `variant`: 'circle' | 'square' (Standard: 'circle')
- `color`: 'blue' | 'green' | 'red' | 'gray' (Standard: 'blue')
- `text`: string (Pflichtfeld)

### 2. Dynamische CSS-Klassen

Erstelle computed Properties für:

- `bulletClasses` - Basis-Klasse + Varianten-Klassen + Farb-Klassen

### 3. CSS-Klassen Schema

- Basis: `bullet`
- Varianten: `bullet--circle`, `bullet--square`
- Farben: `bullet--blue`, `bullet--green`, `bullet--red`, `bullet--gray`

## Starter Code

```vue
<template>
    <div class="bullet-container">
        <!-- TODO: Bullet-Element mit dynamischen Klassen -->
        <div>
            <!-- TODO: Text anzeigen -->
        </div>
    </div>
</template>

<script setup lang="ts">
import { computed } from "vue";

// TODO: Props Interface definieren

// TODO: Props mit Defaults definieren

// TODO: Computed Property für CSS-Klassen
</script>

<style scoped>
.bullet-container {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    margin: 0.25rem 0;
}

.bullet {
    width: 12px;
    height: 12px;
    flex-shrink: 0;
}

/* TODO: Varianten-Styles */
.bullet--circle {
    /* Runde Form */
}

.bullet--square {
    /* Eckige Form */
}

/* TODO: Farben-Styles */
.bullet--blue {
    /* Blaue Farbe */
}

.bullet--green {
    /* Grüne Farbe */
}

.bullet--red {
    /* Rote Farbe */
}

.bullet--gray {
    /* Graue Farbe */
}
</style>
```

## Test-Verwendung

Deine Komponente sollte so verwendet werden können:

```vue
<template>
    <div>
        <BulletPoint text="Standard Bullet" />
        <BulletPoint text="Roter Kreis" variant="circle" color="red" />
        <BulletPoint text="Blaues Quadrat" variant="square" color="blue" />
        <BulletPoint text="Grünes Quadrat" variant="square" color="green" />
    </div>
</template>
```

## Erwartetes Ergebnis

- Verschiedene Bullet-Formen (Kreis/Quadrat)
- Verschiedene Farben (blau/grün/rot/grau)
- Text neben dem Bullet-Punkt

## CSS-Werte als Hilfe

```css
/* Farben */
blue: background-color: #3b82f6
green: background-color: #10b981
red: background-color: #ef4444
gray: background-color: #6b7280

/* Formen */
circle: border-radius: 50%
square: border-radius: 2px
```

