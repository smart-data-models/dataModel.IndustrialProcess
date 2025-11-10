<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entidad: MaterialAddition  
=========================<!-- /10-Header -->  
<!-- 15-License -->  
[Licencia Abierta](https://github.com/smart-data-models//dataModel.IndustrialProcess/blob/master/MaterialAddition/LICENSE.md)  
[documento generado automáticamente](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Descripción global: **Esquema para adiciones de materiales a procesos industriales**  
versión: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Lista de propiedades  

<sup><sub>[*] Si no hay un tipo en un atributo es porque podría tener varios tipos o diferentes formatos/patrones</sub></sup>  
- `addedMaterials[array]`: Los materiales añadidos al proceso  - `address[object]`: La dirección postal  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: El país. Por ejemplo, España  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)  
	- `addressLocality[string]`: La localidad en la que se encuentra la dirección postal, y que está en la región  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)  
	- `addressRegion[string]`: La región en la que se encuentra la localidad, y que está en el país  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)  
	- `district[string]`: Un distrito es un tipo de división administrativa que, en algunos países, es administrado por el gobierno local.    
	- `postOfficeBoxNumber[string]`: El número de apartado postal para las direcciones de apartado postal. Por ejemplo, 03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)  
	- `postalCode[string]`: El código postal. Por ejemplo, 24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)  
	- `streetAddress[string]`: La dirección  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)  
	- `streetNr[string]`: Número que identifica una propiedad específica en una vía pública    
- `alternateName[string]`: Un nombre alternativo para este artículo  - `areaServed[string]`: El área geográfica donde se proporciona un servicio o artículo ofrecido  . Model: [https://schema.org/Text](https://schema.org/Text)- `dataProvider[string]`: Una secuencia de caracteres que identifica al proveedor de la entidad de datos armonizada  - `dateCreated[date-time]`: Marca de tiempo de creación de la entidad. Normalmente, esto será asignado por la plataforma de almacenamiento.  - `dateModified[date-time]`: Marca de tiempo de la última modificación de la entidad. Normalmente, esto será asignado por la plataforma de almacenamiento.  - `dateObserved[date-time]`: Fecha de la entidad observada definida por el usuario  - `description[string]`: Una descripción de este artículo  - `heatNumber[number]`: Número de calor de producción relacionado  - `id[*]`: Identificador único de la entidad  - `location[*]`: Referencia Geojson al elemento. Puede ser Point, LineString, Polygon, MultiPoint, MultiLineString o MultiPolygon  - `name[string]`: El nombre de este artículo  - `owner[array]`: Una lista que contiene una secuencia de caracteres codificada en JSON haciendo referencia a los IDs únicos del(los) propietario(s).  - `processName[string]`: Nombre o identificador del proceso de producción relacionado  - `seeAlso[*]`: lista de URI que apuntan a recursos adicionales sobre el artículo  - `source[string]`: Una secuencia de caracteres que indica el origen original de los datos de la entidad como una URL. Se recomienda que sea el nombre de dominio completo del proveedor de origen, o la URL del objeto de origen.  - `type[string]`: Tipo de entidad NGSI. Debe ser MaterialAddition  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Propiedades requeridas  
- `addedMaterials`  - `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
Este modelo de datos proporciona datos relacionados con las adiciones de materiales realizadas en una planta de procesos. El modelo de datos se ha desarrollado a partir de las necesidades de la siderurgia, pero se espera que estructuras de datos similares sean apropiadas en otras áreas de aplicación. El proceso puede ser un proceso por lotes o continuo.  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Descripción del modelo de datos de propiedades  
Ordenado alfabéticamente (haz clic para ver detalles)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
MaterialAddition:    
  description: Schema for material additions to industrial processes    
  properties:    
    addedMaterials:    
      description: The materials added into the process    
      items:    
        properties:    
          category:    
            description: Material category    
            type: string    
            x-ngsi:    
              type: Property    
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
                  description: 'Chemical substance name or identifier, preferably the chemical symbol'    
                  type: string    
                  x-ngsi:    
                    type: Property    
              type: object    
            type: array    
            x-ngsi:    
              type: Property    
          code:    
            description: Material code or identifier    
            type: string    
            x-ngsi:    
              type: Property    
          mass:    
            description: Mass of material added    
            type: number    
            x-ngsi:    
              type: Property    
              units: kg    
          materialPrice:    
            description: Material price per unit of mass in local currency    
            type: number    
            x-ngsi:    
              type: Property    
              units: 1/kg    
          origin:    
            description: Name or identifier of material origin    
            type: string    
            x-ngsi:    
              type: Property    
          source:    
            description: Name or identifier of material source    
            type: string    
            x-ngsi:    
              type: Property    
          specificEnergy:    
            description: The specific energy of the material    
            type: number    
            x-ngsi:    
              type: Property    
              units: kWh/kg    
          storageAvailability:    
            description: Current storage availability    
            type: number    
            x-ngsi:    
              type: Property    
              units: kg    
          supplier:    
            description: Name or identifier of material supplier    
            type: string    
            x-ngsi:    
              type: Property    
        type: object    
      type: array    
      x-ngsi:    
        type: Property    
    address:    
      description: The mailing address    
      properties:    
        addressCountry:    
          description: 'The country. For example, Spain'    
          type: string    
          x-ngsi:    
            model: https://schema.org/addressCountry    
            type: Property    
        addressLocality:    
          description: 'The locality in which the street address is, and which is in the region'    
          type: string    
          x-ngsi:    
            model: https://schema.org/addressLocality    
            type: Property    
        addressRegion:    
          description: 'The region in which the locality is, and which is in the country'    
          type: string    
          x-ngsi:    
            model: https://schema.org/addressRegion    
            type: Property    
        district:    
          description: 'A district is a type of administrative division that, in some countries, is managed by the local government'    
          type: string    
          x-ngsi:    
            type: Property    
        postOfficeBoxNumber:    
          description: 'The post office box number for PO box addresses. For example, 03578'    
          type: string    
          x-ngsi:    
            model: https://schema.org/postOfficeBoxNumber    
            type: Property    
        postalCode:    
          description: 'The postal code. For example, 24004'    
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
      description: 'Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon'    
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
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object'    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: NGSI Entity type. It has to be MaterialAddition    
      enum:    
        - MaterialAddition    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - addedMaterials    
  type: object    
  x-derived-from: ""    
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2023 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.IndustrialProcess/blob/master/MaterialAddition/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.ProcessIndustry/MaterialAddition/schema.json    
  x-model-tags: ""    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Ejemplos de cargas útiles    
#### Ejemplo de valores clave MaterialAddition NGSI-v2  
Aquí tienes un ejemplo de MaterialAddition en formato JSON-LD como pares clave-valor. Esto es compatible con NGSI-v2 cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:MaterialAddition:PlantZ:UnitProcessX:75545",  
  "type": "MaterialAddition",  
  "dateObserved": "2025-07-17T14:07:00Z",  
  "processName": "unit_process_x",  
  "heatNumber": 10001,  
  "addedMaterials":  
  [  
    {  
      "code": "scrap_type_3",  
      "mass": 40000,  
      "category": "scrap",  
      "chemicalConcentration":  
      [  
        {  
          "substance": "Fe",  
          "percentage": 0.9973  
        },  
        {  
          "substance": "Cu",  
          "percentage": 0.0005  
        }  
      ],  
      "specificEnergy": 1.3,  
      "source": "my-id-1",  
      "origin": "my-id-2",  
      "supplier": "ACME",  
      "materialPrice": 0.02,  
      "storageAvailability": 250000  
    }  
  ]  
}  
```  
</details>  
#### Adición de Material Ejemplo Normalizado NGSI-v2  
Aquí hay un ejemplo de una MaterialAddition en formato JSON-LD tal como está normalizado. Esto es compatible con NGSI-v2 cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:MaterialAddition:PlantZ:UnitProcessX:75545",  
  "type": "MaterialAddition",  
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
  "addedMaterials": {  
    "type": "StructuredValue",  
    "value": [  
      {  
        "type": "StructuredValue",  
        "value": {  
          "code": {  
            "type": "Text",  
            "value": "scrap_type_3"  
          },  
          "mass": {  
            "type": "Number",  
            "value": 40000  
          },  
          "category": {  
            "type": "Text",  
            "value": "scrap"  
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
          },  
          "specificEnergy": {  
            "type": "Number",  
            "value": 1.3  
          },  
          "source": {  
            "type": "Text",  
            "value": "my-id-1"  
          },  
          "origin": {  
            "type": "Text",  
            "value": "my-id-2"  
          },  
          "supplier": {  
            "type": "Text",  
            "value": "ACME"  
          },  
          "materialPrice": {  
            "type": "Number",  
            "value": 0.02  
          },  
          "storageAvailability": {  
            "type": "Number",  
            "value": 250000  
          }  
        }  
      }  
    ]  
  }  
}  
```  
</details>  
#### Ejemplo de clave-valor NGSI-LD de Adición de Material  
Aquí hay un ejemplo de una adición de material en formato JSON-LD como pares clave-valor. Esto es compatible con NGSI-LD cuando se usa `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "@context": [  
    "https://raw.githubusercontent.com/smart-data-models/incubated/refs/heads/smartmanufacturing-processindustry/SMARTMANUFACTURING/ProcessIndustry/context.jsonld"  
  ],  
  "id": "urn:ngsi-ld:MaterialAddition:PlantZ:UnitProcessX:75545",  
  "type": "MaterialAddition",  
  "dateObserved": "2025-07-17T14:07:00Z",  
  "processName": "unit_process_x",  
  "heatNumber": 10001,  
  "addedMaterials":  
  [  
    {  
      "code": "scrap_type_3",  
      "mass": 40000,  
      "category": "scrap",  
      "chemicalConcentration":  
      [  
        {  
          "substance": "Fe",  
          "percentage": 0.9973  
        },  
        {  
          "substance": "Cu",  
          "percentage": 0.0005  
        }  
      ],  
      "specificEnergy": 1.3,  
      "source": "my-id-1",  
      "origin": "my-id-2",  
      "supplier": "ACME",  
      "materialPrice": 0.02,  
      "storageAvailability": 250000  
    }  
  ]  
}  
```  
</details>  
#### Ejemplo normalizado NGSI-LD de Adición de Material  
Aquí hay un ejemplo de una adición de material en formato JSON-LD tal como está normalizado. Esto es compatible con NGSI-LD cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "@context": [  
    "https://raw.githubusercontent.com/smart-data-models/incubated/refs/heads/smartmanufacturing-processindustry/SMARTMANUFACTURING/ProcessIndustry/context.jsonld"  
  ],  
  "id": "urn:ngsi-ld:MaterialAddition:PlantZ:UnitProcessX:75545",  
  "type": "MaterialAddition",  
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
  "addedMaterials": {  
    "type": "Property",  
    "value": [  
      {  
        "type": "Property",  
        "value": {  
          "code": {  
            "type": "Property",  
            "value": "scrap_type_3"  
          },  
          "mass": {  
            "type": "Property",  
            "value": 40000  
          },  
          "category": {  
            "type": "Property",  
            "value": "scrap"  
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
          },  
          "specificEnergy": {  
            "type": "Property",  
            "value": 1.3  
          },  
          "source": {  
            "type": "Property",  
            "value": "my-id-1"  
          },  
          "origin": {  
            "type": "Property",  
            "value": "my-id-2"  
          },  
          "supplier": {  
            "type": "Property",  
            "value": "ACME"  
          },  
          "materialPrice": {  
            "type": "Property",  
            "value": 0.02  
          },  
          "storageAvailability": {  
            "type": "Property",  
            "value": 250000  
          }  
        }  
      }  
    ]  
  }  
}  
```  
</details><!-- /80-Examples -->  
<!-- 90-FooterNotes -->  
Estos modelos de datos se desarrollaron en el proyecto ALCHIMIA - Datos e Inteligencia Artificial descentralizada para una industria metalúrgica europea competitiva y ecológica. Este proyecto ha recibido financiación del programa de investigación e innovación Horizonte 2020 de la Unión Europea en virtud del acuerdo de subvención nº 101070046. Consulte https://alchimia-project.eu/  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
Consulta la [FAQ 10](https://smartdatamodels.org/index.php/faqs/) para obtener una respuesta sobre cómo manejar las unidades de magnitud.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
