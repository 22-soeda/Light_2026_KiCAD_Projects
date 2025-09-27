2026 ３月のROBO-ONE light 向けの回路CAD

工大祭(2025 11月頭)に向けて
 - main esp32e can
   - esp32とPCをwifiで接続して、GUIでロボットをデバッグ
   - Serial2をTTL変換して、zhコネクタで6ポート出力
   - 7.4VDCDC,12V 強電の系をまとめてスイッチング
   - canを2ポート搭載
   - 終端抵抗はブリッジで選択
   - BNO055はUART(Serial1)で実装
   - 5V reg, 3.3V DCDCを搭載
 - FSR to can
   - ATmega328P-AUをマイコンとする
   - 外部16MHz
   - FSRのシグナルをRail to Rail OPAMPで増幅、アナログ値を読み取り(4ポート)
   - MCP2515、MCP2561でcanを実装
   - 12V電源入力で、5Vregで降圧
