專案內容：
1. 用來理解預分頻器(Pre-scalar, PSC)、自動裝載暫存器(Auto-Reload Register, ARR)與計數器(Counter, CNT)的作業方式。
2. 如果要用UART讀取__HAL_TIM_GET_COUNTER的值，NUCLEO-F446RE的外部高速輸入源最多只能8Mhz(釐清中)。
3. 本次採用TIM2與UART2，兩者分別於APB1與APB2匯流排上，時鐘頻率都設定為90MHz；PSC設定為8999(由0開始數，分頻1/9000倍)；ARR設定為9999(由0開始數，1/10000倍)。
4. 90(MHz) / PSC = 10000(Hz), 10000(Hz) / 10000 = 1(秒)
