# Inlämning 1
Gruppinlämning, i Utveckling och driftsättning i molnmiljö

**Mål**: Skapa ett serverlöst filhanteringssystem där användare kan ladda upp, organisera och hämta filer lagrade i AWS S3 med hjälp av AWS Lambda och ett webbgränssnitt.
Så du ska kunna ladda upp en fil till AWS S3 från ditt webbgränssnitt, samt kunna hämta filer som ligger där.

**Exempel på projekt**: Dina bästa vänner som inte kan ett dugg teknik gifter sig. De har valt att förlita sig på sina gäster att dokumentera den stora dagen. Dock kan det bli körigt att samla alla bilder som de får in från alla olika håll å kanter. Det är här NI kommer in! Ni har ju precis haft en kurs i AWS och skulle kunna sätta upp en bucket åt turturduvorna och en liten webbapplikation där alla gäster kan ladda upp sina foton från den stora dagen. Sen vill ju gärna gästerna också se de andras foton som redan ligger uppe på hemsidan. Kanske är deras nya tinderbild där liksom.

### G-kriterier:
 
**Skapa en S3-bucket**: Använd AWS Management Console eller AWS CLI, skapa en S3-bucket där användare kan lagra filer.

**Skapa en AWS Lambda-funktion**:
   - Gå till AWS Lambda Console.
   - Skapa en ny Lambdafunktion.
   - Välj en trigger: S3.
   - Konfigurera S3-utlösaren för att titta efter objektskapande, modifieringar och raderingar i din S3-bucket.

**Skriv lambdafunktionskod**:
   - Skriv en Lambda-funktion i node.js.
   - När en fil laddas upp till S3-bucket bör Lambda-funktionen utlösas.
   - Implementera logik för att organisera filer i mappar baserat på användardefinierade regler (t.ex. filtyp, datum).
   - *Implementera extrahering av filmetadata (t.ex. filstorlek, MIME-typ) och lagra det i en databas (t.ex. LowDb eller NeDb, ).* (Frivilligt)

**Skapa ett webbgränssnitt**:
   - Utveckla ett webbaserat användargränssnitt där användare kan:
     - Ladda upp filer till S3-hinken.
     - Bläddra och visa uppladdade filer.
   - Använd AWS SDK eller AWS Amplify för att interagera med AWS-tjänster från din webbapp. (Frivilligt)

### VG-kriterier:

**Ange behörigheter**:
   - Se till att din Lambda-funktion och webbapplikation har de nödvändiga IAM-behörigheterna för att komma åt din S3-bucket och andra nödvändiga AWS-tjänster.
   - 
**I webbgränssnittet**:
   - Sök efter filer baserat på metadata.

     
#### Level-up:
**Övervakning och felhantering**:
   - Implementera loggning, felhantering och undantagsrapportering i din Lambdafunktion och webbapplikation.
   - Ställ in CloudWatch Alarms för att övervaka nyckeltal.

**Rengöring**:
    - Glöm inte att radera alla resurser du skapat för att undvika pågående avgifter.



Den här inlämningen är ett mer omfattande projekt som involverar filhantering, organisering, extrahering av metadata och användarinteraktion via ett webbgränssnitt. Det kommer att ge värdefull erfarenhet av att bygga en serverlös applikation med AWS Lambda och S3.
