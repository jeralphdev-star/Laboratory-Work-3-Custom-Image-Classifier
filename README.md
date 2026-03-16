# Laboratory-Work-3-Custom-Image-Classifier
### Google Colab Link: https://drive.google.com/drive/folders/1i5dKCphkb1pti-N52QTxtATy_89fs4yN?usp=drive_link

### Guide Questions (Student Explanation & Reflection)

#### Visualization & Overfitting
##### 1. What signs indicated overfitting in your first model?
##### Answer: What I observed during the training was that my model was performing exceptionally well on the training data, but as soon as I tested it with validation images, it was struggling. While the accuracy of the training data was constantly increasing, the accuracy of the validation data was not improving or was even decreasing. This was also the case with the loss function, as it was constantly decreasing in the training data, while in the validation data, it was constantly increasing. In other words, my model was getting too comfortable with the training data.

##### 2. How did data augmentation affect validation accuracy?
##### Answer: Once I added data augmentation, the validation accuracy was more stable and started improving. This was because, with the addition of data augmentation, the model was now seeing different variations of the images, flipped, rotated, and zoomed. This helped the model learn to identify the plants from different directions and positions. Also, the difference between the training accuracy and validation accuracy was now smaller, which was an indication that the model was indeed learning something.

##### 3. What is the purpose of dropout layers?
##### Answer: Dropout, essentially, is telling the model to not be lazy. When training the model, it randomly turns off some of the neurons so that the model doesn't always take the same shortcuts. This forces the model to be more flexible and not overfit by distributing what it has learned across more neurons. It's kind of like learning something without relying on the same notes every time, and you'll find that you know the information better.

##### 4. Why does data augmentation improve generalization?
##### Answer: The model only looks at the images it has been trained on so many times, and if they are too similar, it basically ends up learning very specific details that are not applicable in the real world. However, with data augmentation, this problem is solved by creating different versions of the images, like flipping, rotating, and zooming, so that the model gets to see more variety without having to be shown more images. It has basically learned to get used to seeing different looks and angles of images.

#### Performance Comparison
##### 5. Compare accuracy before and after improvements.
##### Answer: As can be seen, before the improvements, the model looked great in theory because of the high training accuracy, but the validation accuracy was much lower, indicating that the model was not performing that well. After the improvements, the validation accuracy caught up to the training accuracy. While not a dramatic increase in numbers, the numbers became much more reliable.

##### 6. Which technique contributed most to improvement?
##### Answer: The biggest improvement came from using data augmentation. This was the biggest improvement to address the biggest problem, which was the lack of diversity in the training images. The dropout helped as well, as it prevented the model from overfitting to individual neurons. However, without the added diversity of images, the dropout itself might not have been enough to address the problem. The dropout and the augmentation worked well together, but the augmentation was the more significant improvement.

#### Deployment & Application
##### 7. Why is saving the model important?
##### Answer: It also takes a lot of time and computer power to train a model, and it wouldn't make a lot of sense to do that every time you want to use your model. By saving it, you can bring it back up instantly when you need to use it, whether that's tomorrow, next week, or even on a different computer. It also lets you use your model in an application or system, which was the whole reason to make the model in the first place

##### 8. How can this model be deployed in a real-world system?
##### Answer: There are a couple of ways this model can be applied in the real world. The first one would be to develop it into a mobile application where the user simply has to take a picture of a plant and get the identification right away. This would require the model to be developed into TensorFlow Lite so that it can be run on a mobile device. Another way would be to develop it on a web server using a framework such as Flask, where users can upload their pictures from a web browser. The idea in either case is the same: to make plant identification quick, easy, and helpful for people like farmers, students, or nature lovers.
