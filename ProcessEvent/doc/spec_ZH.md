<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
实体：ProcessEvent  
===============<!-- /10-Header -->  
<!-- 15-License -->  
[开放许可证](https://github.com/smart-data-models//dataModel.IndustrialProcess/blob/master/ProcessEvent/LICENSE.md)  
[自动生成的文档](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
全局描述：**工业流程中通用事件的模式**  
版本: 0.1.0  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 属性列表  

<sup><sub>[*] 如果属性中没有类型，那是因为它可能有几种类型或不同的格式/模式</sub></sup>  
- `address[object]`: 邮寄地址  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: 国家。例如，西班牙  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)  
	- `addressLocality[string]`: 街道地址所在的地区，以及该地区所在的区域  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)  
	- `addressRegion[string]`: 该地区位于该地，并位于该国  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)  
	- `district[string]`: 区是一种行政区划类型，在一些国家由地方政府管理。    
	- `postOfficeBoxNumber[string]`: 邮政信箱地址的邮政信箱号码。例如，03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)  
	- `postalCode[string]`: 邮政编码。例如，24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)  
	- `streetAddress[string]`: 街道地址  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)  
	- `streetNr[string]`: 识别公共街道上特定房产的编号    
- `alternateName[string]`: 此物品的另一个名称  - `areaServed[string]`: 提供服务或商品的地理区域  . Model: [https://schema.org/Text](https://schema.org/Text)- `dataProvider[string]`: 识别协调数据实体提供者的字符序列  - `dateCreated[date-time]`: 实体创建时间戳。这通常由存储平台分配。  - `dateModified[date-time]`: 实体的最后修改时间戳。这通常由存储平台分配  - `dateObserved[date-time]`: 用户定义的被观察实体的日期  - `description[string]`: 该商品的描述  - `heatNumber[number]`: 相关生产热号  - `id[*]`: 实体的唯一标识符  - `location[*]`: 指向该项目的 GeoJSON 参考。它可以是 Point、LineString、Polygon、MultiPoint、MultiLineString 或 MultiPolygon  - `name[string]`: 此物品的名称  - `owner[array]`: 一个列表，包含一个JSON编码的字符序列，该序列引用所有者（们）的唯一ID。  - `processEvent[string]`: 事件名称或标识符  - `processName[string]`: 相关生产过程的名称或标识符  - `seeAlso[*]`: 指向有关该项目的其他资源的 URI 列表  - `source[string]`: 一串字符，给出实体数据的原始来源，形式为一个URL。建议使用来源提供者的完全限定域名，或指向来源对象的URL。  - `type[string]`: NGSI实体类型。它必须是ProcessEvent。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
必需属性  
- `id`  - `processEvent`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
此数据模型提供与流程工厂中发生的通用工艺相关事件有关的数据。该数据模型是根据炼钢的需求开发的，但类似的数据结构预计也适用于其他应用领域。该工艺可以是批处理工艺或连续工艺。  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 数据模型属性描述  
按字母顺序排序（单击查看详情）  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
ProcessEvent:    
  description: Schema for generic events in industrial processes    
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
    processEvent:    
      description: Name or identifier of the event    
      type: string    
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
      description: NGSI Entity type. It has to be ProcessEvent    
      enum:    
        - ProcessEvent    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - processEvent    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2023 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.IndustrialProcess/blob/master/ProcessEvent/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.ProcessIndustry/ProcessEvent/schema.json    
  x-model-tags: ''    
  x-version: 0.1.0    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## 示例载荷  
#### ProcessEvent NGSI-v2 键值对示例  
以下是 ProcessEvent 的 JSON-LD 格式示例，以键值对形式呈现。当使用 `options=keyValues` 时，这与 NGSI-v2 兼容，并且返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:ProcessEvent:PlantZ:UnitProcessX:45612389",  
  "type": "ProcessEvent",  
  "dateObserved": "2025-07-17T14:07:00Z",  
  "processName": "unit_process_x",  
  "heatNumber": 10001,  
  "processEvent": "heat_end"  
}  
```  
</details>  
#### ProcessEvent NGSI-v2 规范化示例  
这是一个以JSON-LD格式标准化的ProcessEvent示例。当不使用选项时，它与NGSI-v2兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:ProcessEvent:PlantZ:UnitProcessX:45612389",  
  "type": "ProcessEvent",  
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
  "processEvent": {  
    "type": "Text",  
    "value": "heat_end"  
  }  
}  
```  
</details>  
#### ProcessEvent NGSI-LD 键值对示例  
这是一个 ProcessEvent 的 JSON-LD 格式示例，以键值对的形式呈现。当使用 `options=keyValues` 时，它与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "@context": [  
    "https://raw.githubusercontent.com/smart-data-models/incubated/refs/heads/smartmanufacturing-processindustry/SMARTMANUFACTURING/ProcessIndustry/context.jsonld"  
  ],  
  "id": "urn:ngsi-ld:ProcessEvent:PlantZ:UnitProcessX:45612389",  
  "type": "ProcessEvent",  
  "dateObserved": "2025-07-17T14:07:00Z",  
  "processName": "unit_process_x",  
  "heatNumber": 10001,  
  "processEvent": "heat_end"  
}  
```  
</details>  
#### ProcessEvent NGSI-LD 规范化示例  
下面是一个JSON-LD格式的ProcessEvent示例，经过了标准化处理。在不使用选项的情况下，它与NGSI-LD兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "@context": [  
    "https://raw.githubusercontent.com/smart-data-models/incubated/refs/heads/smartmanufacturing-processindustry/SMARTMANUFACTURING/ProcessIndustry/context.jsonld"  
  ],  
  "id": "urn:ngsi-ld:ProcessEvent:PlantZ:UnitProcessX:45612389",  
  "type": "ProcessEvent",  
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
  "processEvent": {  
    "type": "Property",  
    "value": "heat_end"  
  }  
}  
```  
</details><!-- /80-Examples -->  
<!-- 90-FooterNotes -->  
这些数据模型是在ALCHIMIA项目——数据与去中心化人工智能，以促进具有竞争力和绿色环保的欧洲冶金行业——中开发的。该项目已获得欧盟“展望2020”研究与创新计划的资助，资助协议号为101070046。请访问 https://alchimia-project.eu/  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
参阅[常见问题解答 10](https://smartdatamodels.org/index.php/faqs/)，获取有关如何处理幅度单位的答案。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
