Every year, Canada generates approximately 31 million tonnes of garbage. In fact, a recent study states that Canadians produce more garbage per capita than any other country on earth. Recycling contamination plays a significant role in these astonishing statistics. Last year, more than 52,000 tonnes of non-recyclable materials were put incorrectly in blue bins in Toronto. This means that roughly 26 percent of what is being put in recycling bins is actually garbage, costing not only millions of dollars but the health of our planet as well.

There are 3 main problems that lead to the recycling crisis that we plan to address. One of the biggest issues, of course, is that items are incorrectly tossed in recycling bins when they should be placed elsewhere. Items such as grocery store bags, straws, coffee lids, leftover food waste or liquids are all non-recyclable and are often mistakenly put in blue bins. These contaminants ruin the overall quality of the recycling bales, sometimes rendering the entire batch un-recyclable. Another big issue is that people are often uneducated and unaware of proper recycling methods. There are still things going in the wrong place, simply because people don’t know where the correct place is. Finally, there is the issue of diverse recycling practices across different municipalities. Every city has a different system installed, and what might be deemed recyclable in one region might be very different than what is recyclable in another.

We were inspired to do this project because we recognized this as a global issue that is becoming increasingly relevant with the rise of the climate crisis. The contamination of recycling causes unnecessary waste that is detrimental to both our economy and our planet, issues that are both critically important.

##What it does
ScrapIT is an effective waste management system that uses machine learning to identify recyclables and possible contaminants. Originally, ScrapIT was supposed to have a hardware component that used a camera, raspberry pi, and light to gather data from a recycling bin. For the purpose of this hackathon, however, we decided to focus on application and TensorFlow model development than the hardware components. Although we did not get a chance to make the physical product, we instead generated data using the camera on mobile phones. Our model sorts the object in front of the camera into one of 7 categories, determining whether or not it is supposed to go in the recycling, trash, or compost. This allows the user to make informed decisions and changes to their recycling habits.

How I built it
To build our product, we used a variety of online tools and tutorials. Based on intensive research from similar projects in the past, we learned that the first thing that we had to do was gather our data to train our model. To do this, we first looked at a data set (https://github.com/garythung/trashnet) with various pictures of recycling and waste products, which were sorted into categories. Using Microsoft's Azure platform, we easily uploaded and tagged the pictures from this dataset to classify them based on categories.

We then proceeded to "train" our model using this dataset, and our complete model was eventually able to correctly categorize items with approximately 98% preciseness. Once our model was good to go, it was time to build our app. Due to the accessibility of android, we decided to use Android-Studio to build our application. Using an Azure IoT model image classification program as a reference, we built our app platform and integrated our custom model to it.

Thankfully, it worked almost immediately. Although it was functioning and for the most part was identifying objects correctly, the program was still pretty limited and we felt like we could go further. We wanted to collect more data in order to create a more precise learning model that identified objects with more accuracy. However, there weren't enough already procured datasets out there to satisfy our needs. To solve this problem, we created a python script that scraped photos off the internet and downloaded them to our computer.

We created more categories such as compostable materials and retrained our model to accommodate for this new incoming data. We integrated this new model back into our application, and we were set!

Challenges I ran into
Since this was the first time that either team member had dealt with machine learning and android app development, there were bound to be some issues. Specifically, we had trouble creating multiple "Activities" (or pages) on the app due to the complexities of the program and scripts we were using. We spent hours trying to figure out a way to properly integrate our rewards and consumer information system into our image classification program, but couldn't get it right without breaking something else in the code. However, it was still a learning experience and we definitely learned what NOT to do :)

We also ran low on time and didn't get a chance to do all the things that we had originally planned to do with the project. Due to this, we didn't get a chance to make the hardware component or properly make the complete functioning app (with the user education and rewards system as well).

##Accomplishments that I'm proud of
A lack of experience was largely what made things difficult, but it also made things interesting. Everything was new to us, and we were overjoyed when we got to see what the final product of our hard work was. We were proud of how we were able to use a tool like Azure to organize and classify our data and eventually train our model, something that we always wanted to do. Integrating our model into an android app was also a very rewarding feeling, as we got to see the physical outcome of our idea. In addition, after hours of trying, we finally mastered being able to extract data from the internet using python, and our project was greatly strengthened as a result.

##What we learned
Both members of our team were very unfamiliar with neural networks and working with machine learning, so this was a challenging and lengthy process for us. However, we learned quite a lot and it was an amazing and gratifying experience. Although some lack of technical skills prohibited ScrapIT from reaching its full potential, we each learned a lot about how to train your own image classifying model, building an android app and java programming.

##What's next for ScrapIT
In the future, we plan to build the hardware component to our project and connect it to our app. We also plan on building a rewards system for users, with opportunities to win points by doing quizzes and learning about sustainable living. Another thing that we would love to improve our service is our machine learning model. If we could categorize images further and provide more data to train our model, results would be more accurate. For example, coffee cups, although they are largely made of paper, are often non-recyclable due to the waxy coating on the inside of the cup. The plastic lids, however, are recyclable. In addition, we also want to make our program more region-specific, meaning that we would provide didn't categorizations based on municipality and their recycling practices. For example, black plastic is non-recyclable in the city of Toronto. Having a more well-trained and complex model would allow results to be much more precise, which is something that ScrapIT is striving for.

##Built With
- android-studio
- azure
- java
- python
- tensorflow

## Resources
- Link to [TensorFlow documentation](https://www.tensorflow.org/mobile/)
- Link to [Custom Vision Service Documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/custom-vision-service/home)
