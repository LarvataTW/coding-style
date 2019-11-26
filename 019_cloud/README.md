## Cloud

### Azure

1. 皆採用小駝峰式命名法 (lowerCamelCase)
2. Resource groups 命名規則：類型+環境(-商戶)
    - 範例：sportServiceStaging、sportDevopsStaging-larvata
3. 服務命名規則：應用+序號+環境(-商戶)(-子元件)
    - 範例：ap1Staging、rproxy2Staging-larvata-disk2
4. Virtual Network 命名規則類似 Resource groups，但是以 vnet 作為前綴
    - 範例：vnetSportServiceStaging、vnetSportServiceStaging-larvata
5. __禁止使用空白字元__
6. __序號起始為 1__
