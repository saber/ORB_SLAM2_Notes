1、vector<KeyFrame*> KeyFrameDatabase::DetectRelocalizationCandidates(Frame *F) 在该函数内部 278 行左右。pKF2->mRelocScore 这个值在关键帧建立时没有清零0，导致这里为垃圾值。所以在计算 accScore 时不准确。自己在代码中已经更改了 在这个函数 Compute similarity score 哪个循环中已经解决了。bug 已经提交到 github 上，暂时没有给出回复！

2、