方法:一般的CNN模型(4個卷積層、4個池化層)、DenseNet跟ResNet分別訓練。

流程:預處理部分，先將training、test、valid set的每一個照片都做resize成224*224，接著建立剛剛說的三個模型分別去做訓練，會生成一個h5檔。
     測試時將其import並做預測將結果寫至指定的excel檔

想法:經過三個模型的訓練，我發現ResNet的訓練成果最好，Valid Set的準確度可到53%，但之後就會在40到50%之間震盪，valid loss也不會再下降，但其實雖說是最好，但也沒到太好。
     其餘兩個模型的訓練結果如資料夾附圖，連Training set的準確度都不高於75%。但是ResNet的準確度到後面會在90到95%，但我覺得是我的三個model都建立的不太好

附圖有我用經典CNN、DenseNet跟ResNet的訓練結果
