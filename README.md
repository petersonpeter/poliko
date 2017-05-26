Code used for the demo http://poliko.adhorn.me

![Poliko in action](https://pbs.twimg.com/media/DAgoPnHXkAAbJZF.jpg:large)

This code uses Cognito to permit access to AI services (Rekognition and Polly)

**What is Amazon Cognito?**
Amazon Cognito lets you easily add user sign-up and sign-in to your mobile and web apps. With Amazon Cognito, you also have the options to authenticate users through social identity providers such as Facebook, Twitter, or Amazon, with SAML identity solutions, or by using your own identity system. In addition, Amazon Cognito enables you to save data locally on users devices, allowing your applications to work even when the devices are offline. You can then synchronize data across users devices so that their app experience remains consistent regardless of the device they use.


**What is Amazon Rekognition?**
Amazon Rekognition is a service that makes it easy to add image analysis to your applications. With Rekognition, you can detect objects, scenes, faces; search and compare faces; and identify inappropriate content in images. Rekognition’s API enables you to quickly add sophisticated deep learning-based visual search and image classification to your applications.

**What is Amazon Polly?**
Amazon Polly is a service that turns text into lifelike speech. Amazon Polly lets you create applications that talk, enabling you to build entirely new categories of speech-enabled products. Amazon Polly is an Amazon AI service that uses advanced deep learning technologies to synthesize speech that sounds like a human voice. Amazon Polly includes dozens of lifelike voices across a variety of languages, so you can select the ideal voice and build speech-enabled applications that work in many different countries.


**How to Setup the demo?**

Read this page is you want to use Route53 and a shorter domain name for your demo.
http://docs.aws.amazon.com/AmazonS3/latest/dev/website-hosting-custom-domain-walkthrough.html

Edit the bucket name you want to use in the file `setup_cognito.sh`

Run the configuration scripts. 
The following will create a cognito federated identity pool allowing for unauthenticated access and update the `ai.js` file with the cognitio ID created. 

```
sh setup_cognito.sh
```

This will setup an S3 bucket, turn it into a website and give it the correct policy.

```
sh setup_website.sh
```

Browse to the URL outputed by the script. 

Happy demo!
