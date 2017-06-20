# Opencv Training using LFW dataset

Opencv dataset for training

3070 positive samples, 6085 negative samples

# Create Vector

`opencv_createsamples -info info.txt -num 3070 -w 40 -h 40 -vec positives.vec`

# Train Cascade

`nohup opencv_traincascade -data data -vec positives.vec -bg neg.txt -numPos 2500 -numNeg 1000 -numStages 20 -w 40 -h 40 -minHitRate 0.999 -maxFalseAlarmRate 0.5 &`
