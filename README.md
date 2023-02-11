# ImageCaptioning_Hindi

 For our B.tech major project, we are creating a image captioning model that will be able to generate image captions in hindi language. 
 Here is Google drive link for more information : https://drive.google.com/drive/u/0/folders/1auVu2to_xCe2QAYo3UPeIRlk_PsaqmSz

** -> steps to follow

For english captions :-

1. flikr 8k dataset = (<https://www.kaggle.com/adityajn105/flickr8k>)
**(for images download from here, just simple kaggle dataset)

For hindi Captions :-

1. Not official - Flickr8k Hindia dataset = 
(https://github.com/rathiankit03/ImageCaptionHindi/tree/master/Flickr8kHindiDataset)
**(from here download the captions files)


2. https://github.com/nayeem8527/Chitra-VarNan (done by convering Ms coco dataset captions to hindi using Google api before training) (Not good results)

-------------------------------------------------------------------------------------
Research Papers: -

1. Deep learning approach for Image captioning
in Hindi language = ( https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9223087)  (using flickr8k hindi)

or 

(http://norma.ncirl.ie/3869/1/ankitrathi.pdf) both are same (but this is large)
**(This is our base research paper)

2. Show, attend and tell : neural image caption generation with visual attention = (https://arxiv.org/pdf/1502.03044.pdf)
**(Scope of extension and making it better)

----------------------------------------------------------------------

Tutorials: -

1. Pytorch image captioning tutorial with attention (english - MScoco or flickr 8k or 30k) = 
(https://github.com/sgrvinod/a-PyTorch-Tutorial-to-Image-Captioning)

Show, attend and tell : neural image caption generation with visual attention = (https://arxiv.org/pdf/1502.03044.pdf)

2. Pytorch image captioning tutorial without attention (english - flickr 8k) = (https://www.youtube.com/watch?v=y2BaTt1fxJU)
**(I followed this pytorch tutuorial for image captioning)

and implementation (https://github.com/aladdinpersson/Machine-Learning-Collection/tree/master/ML/Pytorch/more_advanced/image_captioning)

3. How to build custom Datasets for Text in Pytorch = (https://www.youtube.com/watch?v=9sHcLvVXsns)


----------------------------------------------
Learnings: -

Cnn - neural networks that uses convolutions (filters), usually for analyzing images

Rnn - neural networks that generartes outputs that feeds back into its own input.
-------
- attention mechanism is good but it is somewhat complex and requires more computations power

- hence encoder - decoder method will also only slightly lower results (less complex and requires less computational power).

pretrained cnn to encode image features and LSTM-RNN is used to encode text-features.

---------
monolingual models are better than dual language model.

- 2 ways to create image captioning dataset 
1) collecting captiosn from crowdsourcing 
2) collections captions usign machine translation

- in chinese language
accuracy of model using machine translation > acc using crowsourcing and human translator (because these are more fluent)(have cultural gap) (not good results) (need time and money) (hence we will use machine translated captions).

- human evaluation method is the best evaluation method in the field of image captioning (but due to time and budget, can use BLEU score)

- decoder takes comb of {word sequence vector, Image feature vector} to predict next probable word in sequence.

- RNN-LSTM is used to encode text data and Pretrained cnn to encode image data.

- addition is used to combine two encoded inputs (iamge feature vector and word vector).

- images are converted into feature vector (using pretrianed CNN or vgg 16) model before feeding into model

- removing stop words.

training -
	image feature input, text feature input
	merge and prediction output

## Final file structure

ImageCaptioning_Hindi is our main folder it contains the code and model.
Data folder contains our data, subfolder /images contains the images (from kaggle dataset) and /test_examples contains some test images for our model.
/Data folder has our image captions files also .txt format.

../

    ImageCaptioning_Hindi/
       get_laoder.py
       Image_annotations_Hindi.ipynb
       utils.py
    Data/
        flickr8k/
            images/
            test_examples/
            captions.txt
            Clean-1Sentences_withComma.txt
            Clean-5Sentences_withComma.txt
            Unclean-1Sentence.txt
            Unclean-5Sentence.txt
            
