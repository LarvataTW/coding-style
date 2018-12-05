## Cloud

###Azure

0. 皆採用小駝峰式命名法(lower camel case)
0. Resource groups命名規則,類型+環境(-商戶)
  - 範例:sportServiceStaging、sportDevopsStaging-larvata
0. 服務命名規則,應用+序號+環境(-商戶)(-子元件)
  - 範例:ap1Staging、rproxy2Staging-larvata-disk2
0. Virtual Network命名規則,同Resource groups name(序號)
  - 範例:sportServiceStaging、sportServiceStaging-larvata
0. __禁止使用空白字元。__
0. __序號起始為1__
