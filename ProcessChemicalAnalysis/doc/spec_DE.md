<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entität: Chemische Analyse verarbeiten  
======================================<!-- /10-Header -->  
<!-- 15-License -->  
[Offene Lizenz](https://github.com/smart-data-models//dataModel.IndustrialProcess/blob/master/ProcessChemicalAnalysis/LICENSE.md)  
[automatisch generiertes Dokument](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Globale Beschreibung: **Schema für chemische Analysen aus Industrieprozessen**  
Version: 0.1.0  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Liste der Eigenschaften  

<sup><sub>[*] Wenn kein Typ in einem Attribut angegeben ist, liegt das daran, dass es mehrere Typen oder unterschiedliche Formate/Muster haben könnte</sub></sup>  
- `address[object]`: Die Postanschrift  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: Das Land. Zum Beispiel Spanien  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)  
	- `addressLocality[string]`: Die Ortschaft, in der sich die Straßenadresse befindet, und die sich in der Region befindet  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)  
	- `addressRegion[string]`: Die Region, in der sich der Ort befindet, und die sich im Land befindet  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)  
	- `district[string]`: Ein Bezirk ist eine Art von Verwaltungseinheit, die in einigen Ländern von der lokalen Regierung verwaltet wird.    
	- `postOfficeBoxNumber[string]`: Die Postfachnummer für Postfachadressen. Zum Beispiel 03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)  
	- `postalCode[string]`: Die Postleitzahl. Zum Beispiel 24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)  
	- `streetAddress[string]`: Die Straßenadresse  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)  
	- `streetNr[string]`: Nummer, die ein bestimmtes Grundstück an einer öffentlichen Straße identifiziert    
- `alternateName[string]`: Ein alternativer Name für diesen Artikel  - `areaServed[string]`: Das geografische Gebiet, in dem eine Dienstleistung oder ein angebotener Artikel bereitgestellt wird.  . Model: [https://schema.org/Text](https://schema.org/Text)- `chemicalAnalysis[object]`: Informationen über die durchgeführte chemische Analyse  	- `chemicalConcentration[array]`: Die Bestandteile in der chemischen Zusammensetzung des Materials    
	- `sampleNumber[number]`: Probenummer, wenn während eines Prozesses mehrere Proben entnommen werden    
- `dataProvider[string]`: Eine Zeichenfolge zur Identifizierung des Anbieters der harmonisierten Dateneinheit  - `dateCreated[date-time]`: Zeitstempel der Entitätserstellung. Dieser wird normalerweise von der Speicherplattform zugewiesen.  - `dateModified[date-time]`: Zeitstempel der letzten Modifikation der Entität. Dieser wird üblicherweise von der Speicherplattform vergeben.  - `dateObserved[date-time]`: Datum der vom Benutzer definierten beobachteten Entität  - `description[string]`: Eine Beschreibung dieses Artikels  - `heatNumber[number]`: Zugehörige Produktionsschmelzennummer  - `id[*]`: Eindeutige Kennung der Entität  - `location[*]`: GeoJSON-Referenz auf das Element. Es kann ein Point, LineString, Polygon, MultiPoint, MultiLineString oder MultiPolygon sein.  - `name[string]`: Der Name dieses Artikels  - `owner[array]`: Eine Liste, die eine JSON-kodierte Zeichenfolge enthält, die auf die eindeutigen IDs des/der Eigentümer(s) verweist.  - `processName[string]`: Name oder Kennung des zugehörigen Produktionsprozesses  - `seeAlso[*]`: Liste von URIs, die auf zusätzliche Ressourcen zu dem Element verweisen  - `source[string]`: Eine Zeichenkette, die die ursprüngliche Quelle der Entitätsdaten als URL angibt. Es wird empfohlen, den vollqualifizierten Domänennamen des Quellanbieters oder die URL zum Quellobjekt zu verwenden.  - `type[string]`: NGSI Entitätstyp. Es muss ProcessChemicalAnalysis sein.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Erforderliche Eigenschaften  
- `chemicalAnalysis`  - `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
Dieses Datenmodell liefert Daten zu chemischen Analysen, die in einer Prozessanlage durchgeführt wurden. Das Datenmodell wurde aus den Bedürfnissen der Stahlherstellung entwickelt, aber ähnliche Datenstrukturen werden voraussichtlich auch in anderen Anwendungsbereichen geeignet sein. Der Prozess kann ein Batch-Prozess oder ein kontinuierlicher Prozess sein.  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Datenmodell-Beschreibung von Eigenschaften  
Alphabetisch sortiert (zum Details anzeigen klicken)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
ProcessChemicalAnalysis:    
  description: Schema for chemical analyses from industrial processes    
  properties:    
    address:    
      description: The mailing address    
      properties:    
        addressCountry:    
          description: The country. For example, Spain    
          type: string    
          x-ngsi:    
            model: https://schema.org/addressCountry    
            type: Property    
        addressLocality:    
          description: The locality in which the street address is, and which is in the region    
          type: string    
          x-ngsi:    
            model: https://schema.org/addressLocality    
            type: Property    
        addressRegion:    
          description: The region in which the locality is, and which is in the country    
          type: string    
          x-ngsi:    
            model: https://schema.org/addressRegion    
            type: Property    
        district:    
          description: A district is a type of administrative division that, in some countries, is managed by the local government    
          type: string    
          x-ngsi:    
            type: Property    
        postOfficeBoxNumber:    
          description: The post office box number for PO box addresses. For example, 03578    
          type: string    
          x-ngsi:    
            model: https://schema.org/postOfficeBoxNumber    
            type: Property    
        postalCode:    
          description: The postal code. For example, 24004    
          type: string    
          x-ngsi:    
            model: https://schema.org/https://schema.org/postalCode    
            type: Property    
        streetAddress:    
          description: The street address    
          type: string    
          x-ngsi:    
            model: https://schema.org/streetAddress    
            type: Property    
        streetNr:    
          description: Number identifying a specific property on a public street    
          type: string    
          x-ngsi:    
            type: Property    
      type: object    
      x-ngsi:    
        model: https://schema.org/address    
        type: Property    
    alternateName:    
      description: An alternative name for this item    
      type: string    
      x-ngsi:    
        type: Property    
    areaServed:    
      description: The geographic area where a service or offered item is provided    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    chemicalAnalysis:    
      description: Information about the chemical analysis performed    
      properties:    
        chemicalConcentration:    
          description: The components in the chemical composition of the material    
          items:    
            properties:    
              percentage:    
                description: Percentage of the chemical substance    
                maximum: 1    
                minimum: 0    
                type: number    
                x-ngsi:    
                  type: Property    
              substance:    
                description: Chemical substance name or identifier, preferably the chemical symbol    
                type: string    
                x-ngsi:    
                  type: Property    
            required:    
              - substance    
              - percentage    
            type: object    
          type: array    
          x-ngsi:    
            type: Property    
        sampleNumber:    
          description: Sample number if multiple samples are taken during a process    
          type: number    
          x-ngsi:    
            type: Property    
      required:    
        - chemicalConcentration    
      type: object    
      x-ngsi:    
        type: Property    
    dataProvider:    
      description: A sequence of characters identifying the provider of the harmonised data entity    
      type: string    
      x-ngsi:    
        type: Property    
    dateCreated:    
      description: Entity creation timestamp. This will usually be allocated by the storage platform    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateModified:    
      description: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateObserved:    
      description: Date of the observed entity defined by the user    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    description:    
      description: A description of this item    
      type: string    
      x-ngsi:    
        type: Property    
    heatNumber:    
      description: Related production heat number    
      type: number    
      x-ngsi:    
        type: Property    
    id:    
      anyOf:    
        - description: Identifier format of any NGSI entity    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
          x-ngsi:    
            type: Property    
        - description: Identifier format of any NGSI entity    
          format: uri    
          type: string    
          x-ngsi:    
            type: Property    
      description: Unique identifier of the entity    
      x-ngsi:    
        type: Relationship    
    location:    
      description: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon    
      oneOf:    
        - description: Geojson reference to the item. Point    
          properties:    
            bbox:    
              description: BBox of the  Point    
              items:    
                type: number    
              minItems: 4    
              type: array    
              x-ngsi:    
                type: Property    
            coordinates:    
              description: Coordinates of the Point    
              items:    
                type: number    
              minItems: 2    
              type: array    
              x-ngsi:    
                type: Property    
            type:    
              enum:    
                - Point    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON Point    
          type: object    
          x-ngsi:    
            type: GeoProperty    
        - description: Geojson reference to the item. LineString    
          properties:    
            bbox:    
              description: BBox coordinates of the LineString    
              items:    
                type: number    
              minItems: 4    
              type: array    
              x-ngsi:    
                type: Property    
            coordinates:    
              description: Coordinates of the LineString    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              minItems: 2    
              type: array    
              x-ngsi:    
                type: Property    
            type:    
              enum:    
                - LineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON LineString    
          type: object    
          x-ngsi:    
            type: GeoProperty    
        - description: Geojson reference to the item. Polygon    
          properties:    
            bbox:    
              description: BBox coordinates of the Polygon    
              items:    
                type: number    
              minItems: 4    
              type: array    
              x-ngsi:    
                type: Property    
            coordinates:    
              description: Coordinates of the Polygon    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 4    
                type: array    
              type: array    
              x-ngsi:    
                type: Property    
            type:    
              enum:    
                - Polygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON Polygon    
          type: object    
          x-ngsi:    
            type: GeoProperty    
        - description: Geojson reference to the item. MultiPoint    
          properties:    
            bbox:    
              description: BBox coordinates of the LineString    
              items:    
                type: number    
              minItems: 4    
              type: array    
              x-ngsi:    
                type: Property    
            coordinates:    
              description: Coordinates of the MulitPoint    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              type: array    
              x-ngsi:    
                type: Property    
            type:    
              enum:    
                - MultiPoint    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON MultiPoint    
          type: object    
          x-ngsi:    
            type: GeoProperty    
        - description: Geojson reference to the item. MultiLineString    
          properties:    
            bbox:    
              description: BBox coordinates of the LineString    
              items:    
                type: number    
              minItems: 4    
              type: array    
              x-ngsi:    
                type: Property    
            coordinates:    
              description: Coordinates of the MultiLineString    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 2    
                type: array    
              type: array    
              x-ngsi:    
                type: Property    
            type:    
              enum:    
                - MultiLineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON MultiLineString    
          type: object    
          x-ngsi:    
            type: GeoProperty    
        - description: Geojson reference to the item. MultiLineString    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              description: Coordinates of the MultiPolygon    
              items:    
                items:    
                  items:    
                    items:    
                      type: number    
                    minItems: 2    
                    type: array    
                  minItems: 4    
                  type: array    
                type: array    
              type: array    
              x-ngsi:    
                type: Property    
            type:    
              enum:    
                - MultiPolygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON MultiPolygon    
          type: object    
          x-ngsi:    
            type: GeoProperty    
      x-ngsi:    
        type: GeoProperty    
    name:    
      description: The name of this item    
      type: string    
      x-ngsi:    
        type: Property    
    owner:    
      description: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)    
      items:    
        anyOf:    
          - description: Identifier format of any NGSI entity    
            maxLength: 256    
            minLength: 1    
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
            type: string    
            x-ngsi:    
              type: Property    
          - description: Identifier format of any NGSI entity    
            format: uri    
            type: string    
            x-ngsi:    
              type: Property    
        description: Unique identifier of the entity    
        x-ngsi:    
          type: Relationship    
      type: array    
      x-ngsi:    
        type: Property    
    processName:    
      description: Name or identifier of the related production process    
      type: string    
      x-ngsi:    
        type: Property    
    seeAlso:    
      description: list of uri pointing to additional resources about the item    
      oneOf:    
        - items:    
            format: uri    
            type: string    
          minItems: 1    
          type: array    
        - format: uri    
          type: string    
      x-ngsi:    
        type: Property    
    source:    
      description: A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: NGSI Entity type. It has to be ProcessChemicalAnalysis    
      enum:    
        - ProcessChemicalAnalysis    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - chemicalAnalysis    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2023 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.IndustrialProcess/blob/master/ProcessChemicalAnalysis/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.ProcessIndustry/ProcessChemicalAnalysis/schema.json    
  x-model-tags: ''    
  x-version: 0.1.0    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Beispiel-Payloads    
#### ProcessChemicalAnalysis NGSI-v2 Schlüssel-Wert-Paare Beispiel  
Hier ist ein Beispiel für eine ProcessChemicalAnalysis im JSON-LD-Format als Schlüssel-Werte. Dies ist mit NGSI-v2 kompatibel, wenn `options=keyValues` verwendet wird, und gibt die Kontextdaten einer einzelnen Entität zurück.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:ProcessChemicalAnalysis:PlantZ:UnitProcessX:32781",  
  "type": "ProcessChemicalAnalysis",  
  "dateObserved": "2025-07-17T14:07:00Z",  
  "processName": "unit_process_x",  
  "heatNumber": 10001,  
  "chemicalAnalysis":  
  {  
    "sampleNumber": 1,  
    "chemicalConcentration" :  
    [  
      {  
          "substance": "Fe",  
          "percentage": 0.9973  
      },  
      {  
          "substance": "Cu",  
          "percentage": 0.0005  
      }  
    ]  
  }  
}  
```  
</details>  
#### ProcessChemicalAnalysis NGSI-v2 normalisiertes Beispiel  
Hier ist ein Beispiel für eine ProcessChemicalAnalysis im JSON-LD-Format, wie sie normalisiert wurde. Dies ist kompatibel mit NGSI-v2, wenn keine Optionen verwendet werden, und gibt die Kontextdaten einer einzelnen Entität zurück.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:ProcessChemicalAnalysis:PlantZ:UnitProcessX:32781",  
  "type": "ProcessChemicalAnalysis",  
  "dateObserved": {  
    "type": "DateTime",  
    "value": "2025-07-17T14:07:00Z"  
  },  
  "processName": {  
    "type": "Text",  
    "value": "unit_process_x"  
  },  
  "heatNumber": {  
    "type": "Number",  
    "value": 10001  
  },  
  "chemicalAnalysis" : {  
    "type": "StructuredValue",  
    "value": {  
      "sampleNumber": {  
        "type": "Number",  
        "value": 1  
      },  
      "chemicalConcentration": {  
        "type": "StructuredValue",  
        "value": [  
          {  
            "type": "StructuredValue",  
            "value": {  
              "substance": {  
                "type": "Text",  
                "value": "Fe"  
              },  
              "percentage": {  
                "type": "Number",  
                "value": 0.9973  
              }  
            }  
          },  
          {  
            "type": "StructuredValue",  
            "value": {  
              "substance": {  
                "type": "Text",  
                "value": "Cu"  
              },  
              "percentage": {  
                "type": "Number",  
                "value": 0.0005  
              }  
            }  
          }  
        ]  
      }  
    }  
  }  
}  
```  
</details>  
#### Prozesschemische Analyse NGSI-LD Schlüssel-Werte Beispiel    
Hier ist ein Beispiel für eine ProzesschemischeAnalyse im JSON-LD-Format als Schlüssel-Werte. Dies ist mit NGSI-LD kompatibel, wenn `options=keyValues` verwendet wird, und liefert die Kontextdaten einer einzelnen Entität.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "@context": [  
    "https://raw.githubusercontent.com/smart-data-models/incubated/refs/heads/smartmanufacturing-processindustry/SMARTMANUFACTURING/ProcessIndustry/context.jsonld"  
  ],  
  "id": "urn:ngsi-ld:ProcessChemicalAnalysis:PlantZ:UnitProcessX:32781",  
  "type": "ProcessChemicalAnalysis",  
  "dateObserved": "2025-07-17T14:07:00Z",  
  "processName": "unit_process_x",  
  "heatNumber": 10001,  
  "chemicalAnalysis":  
  {  
    "sampleNumber": 1,  
    "chemicalConcentration" :  
    [  
      {  
          "substance": "Fe",  
          "percentage": 0.9973  
      },  
      {  
          "substance": "Cu",  
          "percentage": 0.0005  
      }  
    ]  
  }  
}  
```  
</details>  
#### ProzessChemischeAnalyse NGSI-LD normalisiertes Beispiel  
Hier ist ein normalisiertes Beispiel einer ProcessChemicalAnalysis im JSON-LD-Format. Dies ist kompatibel mit NGSI-LD, wenn keine Optionen verwendet werden, und gibt die Kontextdaten einer einzelnen Entität zurück.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "@context": [  
    "https://raw.githubusercontent.com/smart-data-models/incubated/refs/heads/smartmanufacturing-processindustry/SMARTMANUFACTURING/ProcessIndustry/context.jsonld"  
  ],  
  "id": "urn:ngsi-ld:ProcessChemicalAnalysis:PlantZ:UnitProcessX:32781",  
  "type": "ProcessChemicalAnalysis",  
  "dateObserved": {  
    "type": "Property",  
    "value": {  
      "@type": "DateTime",  
      "@value": "2025-07-17T14:07:00Z"  
    }  
  },  
  "processName": {  
    "type": "Property",  
    "value": "unit_process_x"  
  },  
  "heatNumber": {  
    "type": "Property",  
    "value": 10001  
  },  
  "chemicalAnalysis" : {  
    "type": "Property",  
    "value": {  
      "sampleNumber": {  
        "type": "Property",  
        "value": 1  
      },  
      "chemicalConcentration": {  
        "type": "Property",  
        "value": [  
          {  
            "type": "Property",  
            "value": {  
              "substance": {  
                "type": "Property",  
                "value": "Fe"  
              },  
              "percentage": {  
                "type": "Property",  
                "value": 0.9973  
              }  
            }  
          },  
          {  
            "type": "Property",  
            "value": {  
              "substance": {  
                "type": "Property",  
                "value": "Cu"  
              },  
              "percentage": {  
                "type": "Property",  
                "value": 0.0005  
              }  
            }  
          }  
        ]  
      }  
    }  
  }  
}  
```  
</details><!-- /80-Examples -->  
<!-- 90-FooterNotes -->  
Diese Datenmodelle wurden im Projekt ALCHIMIA – Daten und dezentrale Künstliche Intelligenz für eine wettbewerbsfähige und grüne europäische Metallurgieindustrie – entwickelt. Dieses Projekt wurde aus dem Forschungs- und Innovationsprogramm Horizont 2020 der Europäischen Union im Rahmen der Finanzhilfevereinbarung Nr. 101070046 gefördert. Siehe https://alchimia-project.eu/  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
Siehe [FAQ 10](https://smartdatamodels.org/index.php/faqs/), um eine Antwort darauf zu erhalten, wie man mit Größeneinheiten umgeht.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
