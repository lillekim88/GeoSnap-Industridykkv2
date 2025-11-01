# GeoSnap-Industridykk v2 - Installasjonsveiledning

## Innholdsfortegnelse
- [Oversikt](#oversikt)
- [Systemkrav](#systemkrav)
- [Installasjon for utviklere](#installasjon-for-utviklere)
- [Installasjon for sluttbrukere](#installasjon-for-sluttbrukere)
- [Feilsøking](#feilsøking)

## Oversikt

GeoSnap-Industridykk v2 er en applikasjon som lar deg ta bilder med automatisk innbakt tekst som viser:
- Navn på gate/vei/bro
- Himmelretning
- GPS-koordinater
- Geografisk posisjon

## Systemkrav

### For Android
- Android 8.0 (API nivå 26) eller nyere
- Minimum 2 GB RAM
- Kameratilgang
- GPS/Posisjonstilgang
- Internett-tilgang (for kartdata)

### For iOS
- iOS 12.0 eller nyere
- Minimum 2 GB RAM
- Kameratilgang
- Posisjonstilgang
- Internett-tilgang (for kartdata)

## Installasjon for utviklere

### Forutsetninger

#### For Android-utvikling
```bash
# Installer Node.js (versjon 16 eller nyere)
# Last ned fra https://nodejs.org/

# Installer Android Studio
# Last ned fra https://developer.android.com/studio

# Installer Java Development Kit (JDK) 11 eller nyere
```

#### For iOS-utvikling (kun macOS)
```bash
# Installer Xcode fra App Store
# Installer CocoaPods
sudo gem install cocoapods
```

### Oppsett av utviklingsmiljø

1. **Klon repositoriet**
```bash
git clone https://github.com/lillekim88/GeoSnap-Industridykkv2.git
cd GeoSnap-Industridykkv2
```

2. **Installer avhengigheter**
```bash
npm install
# eller
yarn install
```

3. **Konfigurer miljøvariabler**

Opprett en `.env` fil i rotmappen:
```
# Erstatt med dine egne API-nøkler
MAPS_API_KEY=din_google_maps_api_nøkkel_her
LOCATION_SERVICE_URL=https://api.example.com/location
```

4. **Kjør applikasjonen**

For Android:
```bash
npm run android
# eller
yarn android
```

For iOS:
```bash
cd ios && pod install && cd ..
npm run ios
# eller
yarn ios
```

### Bygg for produksjon

#### Android APK/AAB
```bash
cd android
./gradlew assembleRelease
# APK finnes i: android/app/build/outputs/apk/release/

# For Android App Bundle (AAB):
./gradlew bundleRelease
# AAB finnes i: android/app/build/outputs/bundle/release/
```

#### iOS IPA
```bash
# Åpne Xcode
open ios/GeoSnap.xcworkspace

# Velg Product > Archive
# Følg eksportveiviseren for å generere IPA-fil
```

## Installasjon for sluttbrukere

### Android

#### Metode 1: Google Play Store (når tilgjengelig)
1. Åpne Google Play Store
2. Søk etter "GeoSnap Industridykk"
3. Trykk "Installer"
4. Godta nødvendige tillatelser

#### Metode 2: APK-fil
1. Last ned APK-filen fra [Releases](https://github.com/lillekim88/GeoSnap-Industridykkv2/releases)
2. Aktiver "Ukjente kilder" i Android-innstillingene:
   - Gå til Innstillinger > Sikkerhet
   - Aktiver "Ukjente kilder" eller "Installer ukjente apper"
3. Åpne nedlastet APK-fil
4. Følg installasjonsveiledningen
5. Godta nødvendige tillatelser

### iOS

#### Metode 1: App Store (når tilgjengelig)
1. Åpne App Store
2. Søk etter "GeoSnap Industridykk"
3. Trykk "Last ned"
4. Godta nødvendige tillatelser

#### Metode 2: TestFlight (for beta-testing)
1. Installer TestFlight fra App Store
2. Åpne invitasjonslenken du har mottatt
3. Godta invitasjonen
4. Last ned appen fra TestFlight

### Nødvendige tillatelser

Applikasjonen krever følgende tillatelser:
- **Kamera**: For å ta bilder
- **Posisjon/GPS**: For å hente GPS-koordinater og stedsnavner
- **Lagring**: For å lagre bilder
- **Internett**: For å hente kartdata og stedsnavner

## Første gangs oppsett

1. Åpne GeoSnap-appen
2. Godta tillatelser når du blir spurt
3. Kalibrér kompasset ved å bevege telefonen i en åttetallsbevegelse
4. Appen er klar til bruk!

## Bruk av applikasjonen

1. **Ta et bilde**:
   - Åpne appen
   - Rett kameraet mot ønsket objekt
   - GPS-koordinater, retning og stedsnavn vises automatisk
   - Trykk på utløserknappen

2. **Lagrede bilder**:
   - Bilder lagres automatisk i enhetens bildegalleri
   - Bilder inneholder innbakt tekst med posisjonsinformasjon

## Feilsøking

### GPS-data vises ikke
- Kontroller at posisjonstillatelser er aktivert
- Kontroller at GPS er aktivert på enheten
- Prøv å gå ut i åpent terreng for bedre GPS-signal

### Kompass viser feil retning
- Kalibrér kompasset ved å bevege telefonen i en åttetallsbevegelse
- Hold enheten vekk fra magnetiske objekter

### Stedsnavn vises ikke
- Kontroller internettforbindelsen
- Kontroller at appen har tillatelse til å bruke internett

### Appen krasjer ved oppstart
- Avinstaller og installer appen på nytt
- Kontroller at enheten oppfyller systemkravene
- Slett cache og data (Android: Innstillinger > Apper > GeoSnap > Lagring)

### Kamera fungerer ikke
- Kontroller at kameratillatelse er gitt
- Start enheten på nytt
- Kontroller at ikke andre apper bruker kameraet

## Oppdateringer

### Android
- Automatiske oppdateringer via Google Play Store (hvis installert derfra)
- Manuell oppdatering: last ned ny APK og installer

### iOS
- Automatiske oppdateringer via App Store (hvis installert derfra)
- Manuell oppdatering: last ned ny versjon fra App Store

## Support

For spørsmål eller problemer:
- Opprett en issue på [GitHub](https://github.com/lillekim88/GeoSnap-Industridykkv2/issues)
- Se [README.md](README.md) for mer informasjon

## Lisens

Se [LICENSE](LICENSE) fil for lisensdetaljer.

## Bidrag

Vi setter pris på bidrag! Se [CONTRIBUTING.md](CONTRIBUTING.md) for retningslinjer.

---

Laget med ❤️ for industridykkere og feltarbeidere
