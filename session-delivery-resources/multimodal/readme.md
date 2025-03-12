# Demo 4 - Multimodal

#### Description
In this demo you are going to show the multimodal capabilities (image and text) using the playground in Azure AI Foundry with GPT-4o Model deployed.

#### Required access and products
- Azure AI Foundry
- Model GPT-4o or GPT-4o-Mini deployed


## Demo 4.1: Holiday Home

- [Backup video recording](https://aka.ms/AArw3if)
- [Demo files](https://github.com/microsoft/aitour-generative-ai-in-azure/tree/main/session-delivery-resources/multimodal/holiday-home)


**Add the 4 images to the prompt**
```
Create a tagline and short description for this rental home advertisement.
- The first picture is from the home
- The other pictures are from sights nearby
- In the description use the features of the house and make the ad more compelling with the sights. 
- Do not talk about features not visible in the images.
- If you have information about the location of the images, use that information in the description
```

```
이 임대 주택 광고에 대한 태그라인과 간단한 설명을 만드세요.
- 첫 번째 사진은 집에서 찍은 것입니다
- 다른 사진들은 근처에서 찍은 것입니다
- 설명에서는 집의 특징을 사용하여 광고를 더 매력적으로 만듭니다. 
- 이미지에 보이지 않는 기능에 대해 이야기하지 마세요.
- 이미지 위치에 대한 정보가 있는 경우 설명에 있는 해당 정보를 사용하세요
```

Discuss the prompt and the outputs.


## Demo 4.2: Context is everything

- [Backup video recording](https://aka.ms/AArvo23)
- [Demo files](https://github.com/microsoft/aitour-generative-ai-in-azure/tree/main/session-delivery-resources/multimodal/context-is-everything)

For this next demo, we have an obstructed image. I purposefully put the bounding boxes there to make it not clear so you don't have the full context. 
This is my example where context is everything. And GPT-4o is the first large-scale model that actually bakes context in. 
   

**Add [image1](https://github.com/microsoft/aitour-generative-ai-in-azure/blob/main/session-delivery-resources/multimodal/context-is-everything/demo-4-context-001.png) to the prompt.**
```
prompt: What is that?    
```

If I asked anyone in this room, "Hey, what is this?" Everyone would probably really struggle to come up with what that text is. 
This is the classic computer vision problem with optical character recognition. Is if you were looking at that word in isolation, what is the actual word?
   
If I ask GPT-4o with Vision, "What is that?" It says, "The text is not clearly readable due to the handwritten nature. It could be a signature like 'Mark’.” 
The other interesting thing is it actually knows, hey, "There appears to be portions of the text that are blocked out and cannot be read.
   
**Add [image2](https://github.com/microsoft/aitour-generative-ai-in-azure/blob/main/session-delivery-resources/multimodal/context-is-everything/demo-4-context-002.png) to the prompt.**    
``` 
Prompt: Extract all the texts from the image. Explain what you think this is.
```   
  
If I reveal a little bit more, I have one person who's been able to figure out what this was at this point, but it's still pretty challenging to say what is this.  In this case, I changed the prompt a little bit. Extract all the texts from the image. Explain what you think this is.
And GPT-4 Turbo with Vision responded back with this, it said, "This is milk, steak" and it appears to be a shopping list. It basically makes the note that the image is still obscured, which is interesting. 
   
**Add [image3](https://github.com/microsoft/aitour-generative-ai-in-azure/blob/main/session-delivery-resources/multimodal/context-is-everything/demo-4-context-003.png) to the prompt.**    
```
Prompt: Extract all the texts from the image. Explain what you think this is.
```   

We can see,  GPT-4 Turbo with Vision is actually correct, and it is indeed a shopping list when I reveal the whole thing.
it's able to perfectly translate what I'm trying to say there, "mayo, organic bread" Even more interesting is the note at the bottom. It actually gets the subtleties of what's going on. It says, where is it? 
"The note on the beer item suggests a reminder or emphasis on moderation or limiting the purchase quantity."
