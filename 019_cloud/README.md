## Cloud

### Azure

1. 皆採用小駝峰式命名法 (lowerCamelCase)
2. Resource groups 命名規則：類型+環境(-商戶)
    - 範例：sportServiceStaging、sportDevopsStaging-larvata
3. 服務命名規則：應用+序號+環境(-商戶)(-子元件)
    - 範例：ap1Staging、rproxy2Staging-larvata-disk2
4. Virtual Network 命名規則同 Resource groups (序號)
    - 範例：sportServiceStaging、sportServiceStaging-larvata
5. __禁止使用空白字元__
6. __序號起始為 1__
