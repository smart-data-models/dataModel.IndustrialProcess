<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
エンティティ: 素材追加  
============<!-- /10-Header -->  
<!-- 15-License -->  
'[オープンライセンス](https://github.com/smart-data-models//dataModel.IndustrialProcess/blob/master/MaterialAddition/LICENSE.md)'  
[自動生成されたドキュメント](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
グローバル説明: **工業プロセスへの材料追加のスキーマ**  
バージョン: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## プロパティのリスト  

<sup><sub>[*] 属性に型がない場合、それは複数の型または異なる形式/パターンを持つ可能性があるためです</sub></sup>  
- `addedMaterials[array]`: プロセスに追加された材料  - `address[object]`: 郵送先住所  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: 国。例えば、スペイン  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)  
	- `addressLocality[string]`: 通りの住所がある地域、そしてその地域が属する地域  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)  
	- `addressRegion[string]`: その場所が位置する地域であり、かつ国の中にある地域  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)  
	- `district[string]`: 行政区画の一種であり、国によっては地方政府によって管理される区域を指します。    
	- `postOfficeBoxNumber[string]`: 私書箱の住所における私書箱番号。例：03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)  
	- `postalCode[string]`: 郵便番号。例えば、24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)  
	- `streetAddress[string]`: 番地  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)  
	- `streetNr[string]`: 公道上の特定の物件を識別する番号    
- `alternateName[string]`: このアイテムの別名  - `areaServed[string]`: サービスまたは提供される品物が提供される地理的な範囲  . Model: [https://schema.org/Text](https://schema.org/Text)- `dataProvider[string]`: 調和されたデータエンティティのプロバイダーを識別する一連の文字  - `dateCreated[date-time]`: エンティティ作成タイムスタンプ。通常、ストレージプラットフォームによって割り当てられます。  - `dateModified[date-time]`: エンティティが最後に変更されたタイムスタンプ。通常はストレージプラットフォームによって割り当てられます。  - `dateObserved[date-time]`: ユーザーが定義した観測対象の日付  - `description[string]`: この商品の説明  - `heatNumber[number]`: 関連生産熱数  - `id[*]`: エンティティの一意の識別子  - `location[*]`: アイテムへのGeojson参照。Point、LineString、Polygon、MultiPoint、MultiLineString、またはMultiPolygonのいずれかになります。  - `name[string]`: このアイテムの名前  - `owner[array]`: 所有者の一意のIDを参照するJSONエンコードされた文字シーケンスを含むリスト  - `processName[string]`: 関連する製造プロセスの名前または識別子  - `seeAlso[*]`: アイテムに関する追加リソースを指すURIのリスト  - `source[string]`: エンティティデータの元のソースをURLとして示す文字列のシーケンス。ソースプロバイダーの完全修飾ドメイン名、またはソースオブジェクトへのURLにすることを推奨します。  - `type[string]`: NGSIエンティティタイプ。MaterialAdditionである必要があります。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
必須プロパティ  
- `addedMaterials`  - `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
このデータモデルは、プラントプロセスにおける材料投入に関連するデータを提供します。このデータモデルは製鋼のニーズから開発されましたが、同様のデータ構造は他の応用分野でも適切であると期待されています。プロセスはバッチプロセスでも連続プロセスでも構いません。  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## プロパティのデータモデルの説明  
アルファベット順に並べ替え (詳細はこちらをクリック)  
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
## サンプルペイロード  
#### MaterialAddition NGSI-v2 キー値の例  
JSON-LD形式のマテリアル追加の例をキーと値のペアで示します。これは`options=keyValues`を使用する場合のNGSI-v2と互換性があり、個々のエンティティのコンテキストデータを返します。  
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
#### MaterialAddition NGSI-v2 正規化された例  
ここに、正規化されたJSON-LD形式のMaterialAdditionの例を示します。これはオプションを使用しない場合、NGSI-v2と互換性があり、個々のエンティティのコンテキストデータを返します。  
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
#### MaterialAddition NGSI-LD キーと値の例  
これは、JSON-LD形式でkey-valuesとして表されたMaterialAdditionの例です。 `options=keyValues`を使用する場合、NGSI-LDと互換性があり、個々のエンティティのコンテキストデータを返します。  
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
#### MaterialAddition NGSI-LD 正規化された例  
以下は、正規化されたJSON-LD形式のマテリアル追加（MaterialAddition）の例です。オプションを使用しない場合、NGSI-LDと互換性があり、個々のエンティティのコンテキストデータを返します。  
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
これらのデータモデルは、競争力があり環境に配慮したヨーロッパの冶金産業のためのデータと分散型人工知能に関するプロジェクトALCHIMIAで開発されました。本プロジェクトは、欧州連合のHorizon 2020研究・イノベーションプログラムから、助成金協定No 101070046の下で資金提供を受けています。https://alchimia-project.eu/ をご覧ください。  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
大きさの単位の扱い方については、[FAQ 10](https://smartdatamodels.org/index.php/faqs/)をご覧ください。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
