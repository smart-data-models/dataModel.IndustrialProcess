<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
개체: 공정 화학 분석  
============<!-- /10-Header -->  
<!-- 15-License -->  
[오픈 라이선스](https://github.com/smart-data-models//dataModel.IndustrialProcess/blob/master/ProcessChemicalAnalysis/LICENSE.md)  
[자동 생성된 문서](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
글로벌 설명: **산업 공정의 화학 분석을 위한 스키마**  
버전: 0.1.0  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 속성 목록  

<sup><sub>[*] 속성에 유형이 없는 이유는 여러 유형 또는 다른 형식/패턴을 가질 수 있기 때문입니다.</sub></sup>  
- `address[object]`: 우편 주소  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: 나라. 예를 들어, 스페인  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)  
	- `addressLocality[string]`: 주소가 있는 지역, 그리고 해당 지역이 속한 도  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)  
	- `addressRegion[string]`: 지역이 위치한 지역, 그리고 그 지역은 국가 안에 있음  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)  
	- `district[string]`: 지구는 일부 국가에서 지방 정부가 관리하는 행정 구역의 한 종류입니다.    
	- `postOfficeBoxNumber[string]`: PO Box 주소의 우체국 사서함 번호입니다. 예: 03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)  
	- `postalCode[string]`: 우편번호. 예를 들어 24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)  
	- `streetAddress[string]`: the street address  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)  
	- `streetNr[string]`: 공공 도로에 있는 특정 부동산을 식별하는 번호    
- `alternateName[string]`: 이 항목의 다른 이름  - `areaServed[string]`: 서비스 또는 제공되는 품목이 제공되는 지리적 영역  . Model: [https://schema.org/Text](https://schema.org/Text)- `chemicalAnalysis[object]`: 수행된 화학 분석에 대한 정보  	- `chemicalConcentration[array]`: 자재의 화학 성분 내 구성 요소    
	- `sampleNumber[number]`: 공정 중에 여러 샘플을 채취하는 경우 샘플 번호    
- `dataProvider[string]`: 조화된 데이터 엔터티의 제공자를 식별하는 문자열  - `dateCreated[date-time]`: 엔티티 생성 타임스탬프. 이는 보통 스토리지 플랫폼에 의해 할당됩니다.  - `dateModified[date-time]`: 엔티티의 최종 수정 타임스탬프입니다. 이 값은 일반적으로 스토리지 플랫폼에 의해 할당됩니다.  - `dateObserved[date-time]`: 사용자가 정의한 관측 개체의 날짜  - `description[string]`: 이 품목에 대한 설명  - `heatNumber[number]`: 생산 관련 용해 번호  - `id[*]`: 엔티티의 고유 식별자  - `location[*]`: 항목에 대한 GeoJSON 참조입니다. 이는 포인트, 라인스트링, 폴리곤, 멀티포인트, 멀티라인스트링 또는 멀티폴리곤이 될 수 있습니다.  - `name[string]`: 이 항목의 이름  - `owner[array]`: 소유자(들)의 고유 ID를 참조하는 JSON 인코딩된 문자열을 포함하는 목록  - `processName[string]`: 관련된 생산 공정의 이름 또는 식별자  - `seeAlso[*]`: 해당 항목에 대한 추가 리소스를 가리키는 URI 목록  - `source[string]`: 엔티티 데이터의 원본 소스를 URL로 제공하는 문자열입니다. 공급자 소스의 정규화된 도메인 이름 또는 소스 개체로의 URL로 권장됩니다.  - `type[string]`: NGSI 엔티티 유형입니다. ProcessChemicalAnalysis여야 합니다.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
필수 속성  
- `chemicalAnalysis`  - `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
이 데이터 모델은 공정 플랜트에서 수행된 화학 분석과 관련된 데이터를 제공합니다. 이 데이터 모델은 철강 제조의 요구 사항에 따라 개발되었지만, 유사한 데이터 구조는 다른 응용 분야에서도 적절할 것으로 예상됩니다. 공정은 배치 공정 또는 연속 공정일 수 있습니다.  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 속성의 데이터 모델 설명  
알파벳순으로 정렬됨 (자세히 보려면 클릭)  
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
## 예시 페이로드  
#### ProcessChemicalAnalysis NGSI-v2 키-값 예시  
Here is an example of a ProcessChemicalAnalysis in JSON-LD format as key-values. This is compatible with NGSI-v2 when using `options=keyValues` and returns the context data of an individual entity.  
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
#### ProcessChemicalAnalysis NGSI-v2 정규화된 예제  
정규화된 JSON-LD 형식의 ProcessChemicalAnalysis 예시입니다. 옵션을 사용하지 않고 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
화학 물질 분석 처리 NGSI-LD 키-값 예시  
다음은 키-값 형태로 된 JSON-LD 형식의 ProcessChemicalAnalysis 예시입니다. 이는 `options=keyValues`를 사용할 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 화학 분석 처리 NGSI-LD 정규화된 예시  
다음은 정규화된 JSON-LD 형식의 ProcessChemicalAnalysis 예시입니다. 이것은 옵션을 사용하지 않을 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
이 데이터 모델들은 경쟁력 있고 친환경적인 유럽 야금 산업을 위한 데이터 및 분산형 인공지능 프로젝트인 ALCHIMIA에서 개발되었습니다. 이 프로젝트는 유럽연합 Horizon 2020 연구혁신 프로그램으로부터 보조금 협약 번호 101070046에 따라 자금 지원을 받았습니다. 자세한 내용은 https://alchimia-project.eu/ 를 참조하십시오.  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
크기 단위를 다루는 방법에 대한 답변을 얻으려면 [FAQ 10](https://smartdatamodels.org/index.php/faqs/)을(를) 참조하십시오.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
