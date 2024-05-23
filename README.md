# AI4_C_datasets
The sets contain labelled images and can be used to support training or testing of tools and models that support tasks such as colour detection and pattern detection. These datasets were created as part of the [AI4Culture project.](https://pro.europeana.eu/project/ai4culture-an-ai-platform-for-the-cultural-heritage-data-space).

All images were normalised to the .jpg file format and reduced to a maximum dimension of 400 pixels. 
The annotation format is based on the COCO format, used by the COCO (Common Objects in Context) dataset and annotations. It contains the following sections:
* Info: general info concerning the dataset
* Images
  * unique identifier
  * filename
  * license given by the content provider
  * source: image provenance
* Annotations
  * unique identifier
  * image identifier
  * category identifier
* Categories
  * unique identifier
  * name a unique identifier referring to a linke data resource (e.g. Wikidata, European Fashion Thesaurus or the Art & Architecture Thesaurus)
  * label (not part of the COCO format),  


## Pattern dataset
### Description
The [textile pattern dataset](https://github.com/datable-be/AI4_C_datasets/tree/main/textile_pattern_dataset) is a set of images that is labeled with the pattern that is printed on or woven into the textile of the object. The represented object can be a piece of textile (e.g. a sample or a piece of tissue), or a fashion object such as a dress. The fashion object can be photographed individually or in a context, e.g. as worn by a model in a fashion show. The dataset can be used to train image classification models that classify images of textiles or fashion objects by their pattern, but may also be applied to other subject areas (e.g. design).
Sources and creation
The images were retrieved from the following sources:
* Fashion Museum Antwerp
* Fashionpedia
* National Museum of World Cultures Foundation

The dataset was created using a human in the loop methodology, in which a larger set of images was classified with a zero shot classifier. The zero shot classifier was instructed to predict a class for each of the images in the corpus. Next, the predictions were reviewed by a human validator. The validation involved each predicted class being either approved, corrected, or rejected.

### License
**Warning**
The dataset is published with a permissive license, but images may be licensed as well. The license of each image is included in the metadata

### Classes
The images are labelled with one of each of the 6 classes, with reference to the AAT linked data authority. 
|Class label|AAT URI|Description|
|-----------|-------|-----------|
|floral/plant pattern|https://vocab.getty.edu/aat/300164599|design elements that are plant-derived, including flowers, leafs etc.|
|geometric pattern|https://vocab.getty.edu/aat/300165213|patterns consisting of distinguishable, repetitive geometric shapes|
|striped pattern|https://vocab.getty.edu/aat/300010230 |Long, narrow bands, typically of a different color.|
|checker pattern|https://vocab.getty.edu/aat/300010111 |A bold geometric pattern of regularly placed alternating squares or lozenges of contrasting colors or textures.|
|plaid pattern|https://vocab.getty.edu/aat/300411863 |The characteristic pattern known from plaid textiles, consisting of bars or stripes of various colors crossing each other at right angles over a contrasting background color.|
|dotted pattern|https://vocab.getty.edu/aat/300417972|Round dots of uniform size repeated at regular intervals so as to form a pattern.|

### Statistics
The dataset contains 1245 labelled images, with the following labels:

|label|number of labels|
|-----|----------------|
|checkered pattern|77|
|dots pattern|95|
|floral/plant pattern|483|
|geometric pattern|176|
|plaid pattern|167|
|striped pattern|247|

