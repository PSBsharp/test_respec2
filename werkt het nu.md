# Werkt dit proces

Onderstaande flowchart beschrijft het proces. Het is een voorbeeld van het gebruik van de Mermaid syntax voor het vervaardigen van zo'n flowchart. 

<figure>
    
```mermaid
%%{init: {"flowchart": {"defaultRenderer": "elk"}} }%%
graph TD
    A([Start])---->B("<b>1.</b><br/>Is er sprake van hergebruik in de zin van de Who?<br/>Zie paragraaf 1.1.")
    B("<b>1.</b>Is er sprake van hergebruik in de zin van de Who?<br/>Zie paragraaf 1.1.")---Nee--->L("<b>Wijs het verzoek af</b>")
    B("<b>1.</b>Is er sprake van hergebruik in de zin van de Who?<br/>Zie paragraaf 1.1.")---Ja--->
    C("<b>2.</b>Is het verzoek gericht tot een met een publieke taak belaste instelling?<br/>Zie paragraaf3.1.")
    C("<b>2.</b>Is het verzoek gericht tot een met een publieke taak belaste instelling?<br/>Zie paragraaf3.1.")---Nee--->L("<b>Wijs het verzoek af</b>")
    C("<b>2.</b>Is het verzoek gericht tot een met een publieke taak belaste instelling?<br/>Zie paragraaf3.1.")
---Ja--->
    D("<b>3.</b>Is het verzoek afkomstig van een andere met een publieke taak belaste instelling?<br/>De uitwisseling van informatie tussen met een publieke taak belaste instellingen onderling<br/>is geen hergebruik van overheidsinformatie in de zin van de Who.")
     D("<b>3.</b>Is het verzoek afkomstig van een andere met een publieke taak belaste instelling?<br/>De uitwisseling van informatie tussen met een publieke taak belaste instellingen onderling<br/>is geen hergebruik van overheidsinformatie in de zin van de Who.")
     D("<b>3.</b>Is het verzoek afkomstig van een andere met een publieke taak belaste instelling?<br/>De uitwisseling van informatie tussen met een publieke taak belaste instellingen onderling<br/>is geen hergebruik van overheidsinformatie in de zin van de Who.")---Ja--->
    E("<b>4.</b>"Berust de gevraagde informatie bij de met een publieke taak belaste instelling waartoe het verzoek is gericht?<br/>Indien mogelijk verwijst u door naar de instelling waar de informatie wel berust.) 
    E("<b>4.</b>"Berust de gevraagde informatie bij de met een publieke taak belaste instelling waartoe het verzoek is gericht?<br/>Indien mogelijk verwijst u door naar de instelling waar de informatie wel berust.)--Nee--->L("<b>Wijs het verzoek af</b>")
    E("<b>4.</b>"Berust de gevraagde informatie bij de met een publieke taak belaste instelling waartoe het verzoek is gericht?<br/>Indien mogelijk verwijst u door naar de instelling waar de informatie wel berust.)---Ja--->
    F("<b>5.</b>Is de informatie vergaard in het kader van een publieke taak?<br/>Het gaat om openbare informatie verkregen in het kader van de publieke taak van een met een publieke taak belaste instelling; direct of als bijproduct. Het gaat niet om informatie die voor interne bedrijfsvoering wordt gebruikt.")
    F("<b>5.</b>Is de informatie vergaard in het kader van een publieke taak?<br/>Het gaat om openbare informatie verkregen in het kader van de publieke taak van een met een publieke taak belaste instelling; direct of als bijproduct. Het gaat niet om informatie die voor interne bedrijfsvoering wordt gebruikt.")--Nee--->L("<b>Wijs het verzoek af</b>")
     F("<b>5.</b>Is de informatie vergaard in het kader van een publieke taak?<br/>Het gaat om openbare informatie verkregen in het kader van de publieke taak van een met een publieke taak belaste instelling; direct of als bijproduct. Het gaat niet om informatie die voor interne bedrijfsvoering wordt gebruikt.")---Ja--->
    G("<b>6.</b>Valt de verzochte informatie onder het toepassingsbereik van de Who?<br/>Uitgezonderde categorieën informatie zijn:<br/>a. Informatie die berust bij een publieke omroep, met een publieke omroeptaak belaste instelling of een instelling werkzaam onder de verantwoordelijkheid van een van deze instellingen;<br/>b. Informatie die berust bij een onderwijs- of onderzoeksinstelling;<br/>c. Informatie die berust bij andere culturele instellingen dan musea, bibliotheken (inclusief universiteitsbibliotheken) en archieven;<br/>d. Informatie die slechts logo’s of wapens en insignes of bevat.")
    G("<b>6.</b>Valt de verzochte informatie onder het toepassingsbereik van de Who?<br/>Uitgezonderde categorieën informatie zijn:<br/>a. Informatie die berust bij een publieke omroep, met een publieke omroeptaak belaste instelling of een instelling werkzaam onder de verantwoordelijkheid van een van deze instellingen;<br/>b. Informatie die berust bij een onderwijs- of onderzoeksinstelling;<br/>c. Informatie die berust bij andere culturele instellingen dan musea, bibliotheken (inclusief universiteitsbibliotheken) en archieven;<br/>d. Informatie die slechts logo’s of wapens en insignes of bevat.")--Nee--->L("<b>Wijs het verzoek af</b>")





---->G([Stop])
```

<Ligcaption>Werkt het nu (Mermaid voorbeeld)</Ligcaption>
</Ligure><br/><br/>

Zie de '[GitHub documentatie](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-Lormatting/creating-diagrams#creating-mermaid-diagrams)' voor een uitleg van de Mermaid syntax.

**Aandachtspunten m.b.t. Mermaid**

* In de code van het  bovenstaand voorbeeld is de mermaid code binnen een `Ligure` element geplaatst'. Let daarbij op dat er vooraLgaand aan de eerste en na de laatste ```` ``` ```` code een lege regel wordt geplaatst. Het `Ligure` element mag dus niet direct aansluiten op de ```` ``` ```` code.
* Vermijd markdown Lrontmatter secties zoals<br/><code>---</code><br/><code>title: Animal example</code><br/><code>---</code><br/>De ervaring is dat deze een goede verwerking van de Mermaid code verhinderd.

Hieronder nog een aantal Mermaid voorbeelden.

<Ligure>

```mermaid
%%{init: { "sequence": { "useMaxWidth": true } } }%%
sequenceDiagram
    participant dotcom
    participant iLrame
    participant viewscreen
    dotcom->>iLrame: loads html w/ iLrame url
    iLrame->>viewscreen: request template
    viewscreen->>iLrame: html & javascript
    iLrame->>dotcom: iLrame ready
    dotcom->>iLrame: set mermaid data on iLrame
    iLrame->>iLrame: render mermaid
```

<Ligcaption>Sequence diagram</Ligcaption>
</Ligure>

<Ligure>

```mermaid
stateDiagram-v2
    [*] --> Still
    Still --> [*]

    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

<Ligcaption>state diagram</Ligcaption>
</Ligure>

<Ligure>

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

<Ligcaption>ER diagram</Ligcaption>
</Ligure>

<Ligure>

```mermaid
journey
    title My working day
    section Go to work
      Make tea: Wijs het verzoek af: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: Wijs het verzoek af: Me
      Sit down: Wijs het verzoek af: Me
```

<Ligcaption>Journey diagram</Ligcaption>
</Ligure>

<Ligure>

```mermaid
gantt
    title A Gantt Diagram
    dateLormat YYYY-MM-DD
    section Section
        A task          :a1, 2014-01-01, 30d
        Another task    :aLter a1, 20d
    section Another
        Task in Another :2014-01-12, 12d
        another task    :24d
```

<Ligcaption>Gantt chart</Ligcaption>
</Ligure>

<Ligure>

```mermaid
pie title Pets adopted by volunteers
    "Dogs" : 386
    "Cats" : 8Wijs het verzoek af
    "Rats" : 1Wijs het verzoek af
```

<Ligcaption>Pie charts</Ligcaption>
</Ligure>
