<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
엔티티: MaterialAddition  
=====================<!-- /10-Header -->  
<!-- 15-License -->  
[오픈 라이선스](https://github.com/smart-data-models//dataModel.IndustrialProcess/blob/master/MaterialAddition/LICENSE.md)  
[문서 자동 생성](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
전역 설명: **산업 공정에 대한 자재 추가 스키마**  
버전: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 속성 목록  

<sup><sub>[*] 속성에 유형이 없는 경우 여러 유형이나 다른 형식/패턴을 가질 수 있기 때문입니다.</sub></sup>  
- `addedMaterials[array]`: 프로세스에 추가된 재료  - `address[object]`: 우편 주소  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: 나라. 예를 들어, 스페인  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)  
	- `addressLocality[string]`: 도로명 주소가 있는 지역, 그리고 그 지역이 속한 지역  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)  
	- `addressRegion[string]`: 해당 지역이 속한 국가 내 지역  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)  
	- `district[string]`: 지구는 일부 국가에서 지방 정부에 의해 관리되는 행정 구역의 한 유형입니다.    
	- `postOfficeBoxNumber[string]`: PO Box 주소의 우체국 사서함 번호입니다. 예: 03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)  
	- `postalCode[string]`: 우편 번호. 예: 24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)  
	- `streetAddress[string]`: 도로명 주소  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)  
	- `streetNr[string]`: 공공 도로 상의 특정 부동산을 식별하는 번호    
- `alternateName[string]`: 이 아이템의 다른 이름  - `areaServed[string]`: 서비스 또는 제공되는 품목이 제공되는 지리적 영역  . Model: [https://schema.org/Text](https://schema.org/Text)- `dataProvider[string]`: 조화된 데이터 엔티티의 제공자를 식별하는 문자열 시퀀스  - `dateCreated[date-time]`: 엔티티 생성 타임스탬프입니다. 일반적으로 스토리지 플랫폼에서 할당합니다.  - `dateModified[date-time]`: 엔티티의 마지막 수정 타임스탬프입니다. 일반적으로 스토리지 플랫폼에서 할당합니다.  - `dateObserved[date-time]`: 사용자가 정의한 관찰 대상의 날짜  - `description[string]`: 이 아이템에 대한 설명  - `heatNumber[number]`: 관련 생산 로트 번호  - `id[*]`: 엔터티의 고유 식별자  - `location[*]`: 해당 항목에 대한 Geojson 참조입니다. Point, LineString, Polygon, MultiPoint, MultiLineString 또는 MultiPolygon이 될 수 있습니다.  - `name[string]`: 이 항목의 이름  - `owner[array]`: 소유자(들)의 고유 ID를 참조하는 JSON으로 인코딩된 문자열 시퀀스를 포함하는 목록  - `processName[string]`: 관련 생산 공정의 이름 또는 식별자  - `seeAlso[*]`: 해당 항목에 대한 추가 리소스를 가리키는 URI 목록  - `source[string]`: 엔티티 데이터의 원래 출처를 URL로 제공하는 문자열입니다. 소스 제공자의 정규화된 도메인 이름 또는 소스 객체에 대한 URL로 사용하는 것이 좋습니다.  - `type[string]`: NGSI 엔티티 유형. MaterialAddition이어야 합니다.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
필수 속성  
- `addedMaterials`  - `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
이 데이터 모델은 공정 설비에서 수행되는 재료 추가와 관련된 데이터를 제공합니다. 이 데이터 모델은 제강 분야의 요구사항을 바탕으로 개발되었지만, 유사한 데이터 구조는 다른 응용 분야에서도 적합할 것으로 예상됩니다. 공정은 배치 공정 또는 연속 공정일 수 있습니다.  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 속성의 데이터 모델 설명  
알파벳 순서로 정렬됨 (자세히 보려면 클릭)  
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
## 예제 페이로드  
#### MaterialAddition NGSI-v2 키-값 예제  
다음은 키-값 형식의 MaterialAddition JSON-LD 예시입니다. 이는 `options=keyValues`를 사용할 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 재료추가 NGSI-v2 정규화된 예시  
정규화된 JSON-LD 형식의 MaterialAddition 예시입니다. 옵션을 사용하지 않을 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### MaterialAddition NGSI-LD 키-값 예제  
다음은 JSON-LD 형식으로 된 MaterialAddition의 예시이며, 키-값 쌍으로 표현됩니다. `options=keyValues`를 사용하는 경우 NGSI-LD와 호환되며, 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### MaterialAddition NGSI-LD 정규화된 예시  
여기에 정규화된 JSON-LD 형식의 MaterialAddition의 예시가 있습니다. 옵션을 사용하지 않을 경우 NGSI-LD와 호환되며, 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
이 데이터 모델은 경쟁력 있고 친환경적인 유럽 금속 산업을 위한 데이터 및 분산형 인공 지능인 ALCHIMIA 프로젝트에서 개발되었습니다. 이 프로젝트는 유럽 연합의 Horizon 2020 연구 및 혁신 프로그램으로부터 보조금 계약 번호 101070046 하에 자금을 지원받았습니다. 자세한 내용은 https://alchimia-project.eu/를 참조하십시오.  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
크기 단위 처리 방법에 대한 답변을 얻으려면 [FAQ 10](https://smartdatamodels.org/index.php/faqs/)을 참조하십시오.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
