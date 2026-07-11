# Week 3 Assignment 3: Spam Classifier Observations

## Accuracy Results

The spam classifier was tested using four different testing data sizes: `0.1`, `0.2`, `0.3`, and `0.4`.

| Test size | Test samples | Accuracy |
| --- | ---: | ---: |
| 0.1 | 3 | 100.00% |
| 0.2 | 6 | 83.33% |
| 0.3 | 9 | 88.89% |
| 0.4 | 12 | 83.33% |

## Observations

At `test_size=0.1`, the model reached `100.00%` accuracy. This looks perfect, but the test set only contained 3 messages, so the score may not be very reliable. With such a small test set, one lucky split can make the model look stronger than it really is.

At `test_size=0.2`, the accuracy dropped to `83.33%`. This shows that when the model was tested on more unseen messages, it made some mistakes. The report showed strong spam precision, but lower spam recall, meaning some spam messages were classified as ham.

At `test_size=0.3`, the model improved to `88.89%`. This was the best result after the very small 0.1 test split. The model still detected ham messages more consistently than spam messages, but overall performance was good.

At `test_size=0.4`, the accuracy returned to `83.33%`. Since more data was kept for testing, the model had less data available for training. This likely made it harder for the classifier to learn enough word patterns from the training messages.

## Conclusion

The classifier performed well overall, with accuracy staying above `83%` for all larger test sizes. The `0.1` split gave the highest score, but it is less trustworthy because it tested only 3 messages. The `0.3` split gave the strongest balanced result because it tested more messages while still leaving enough data for training.

The main pattern I noticed is that the classifier was better at recognizing normal ham messages than catching every spam message. Some promotional messages, such as discount or offer messages, were predicted as ham because their wording was less aggressive than obvious spam messages like "URGENT", "FREE", or "WINNER".

## Screenshot Evidence

- `0.1` test split: `../Observation Screenshots/test2(0,1).png`
- `0.2` test split: `../Observation Screenshots/test3(0,2).png`
- `0.3` test split: `../Observation Screenshots/test1(0,3).png`
- `0.4` test split: `../Observation Screenshots/test4(0,4).png`
