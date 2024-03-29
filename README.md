# How to Insert Analytical Library-computing Intelligent (ALI) to a Java Project in Intellij IDEA
These steps can be run after open the Java Project file

**Open File menu and select Project Structure option**

<img width="150" alt="Jepretan Layar 2024-01-07 pukul 23 36 08" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/88ecf6a0-a010-45a5-b51d-36d009134cdf">

**When Project Structure is open, select Modules in Project Settings section**

<img width="150" alt="Jepretan Layar 2024-01-07 pukul 23 42 31" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/fcf079c7-1dd1-46fc-b074-fa3490c3653e">

**Open Dependencies tab in Modules page, then click + button to select** ***JARs or Directories*** **option**

<img width="230" alt="Jepretan Layar 2024-01-07 pukul 23 43 08" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/e7c2a0f0-554c-4bef-9f69-7f0e0b6d1e1f">

**Select ALI JAR file from local storage in the computer. After export process is success, there is new line on list of dependency like this**

<img width="230" alt="Jepretan Layar 2024-01-07 pukul 23 54 33" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/ceffa9c2-423e-45f4-b266-6853530af9d8">

**The functionalities can be called and used**

<img width="230" alt="Jepretan Layar 2024-01-08 pukul 00 08 16" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/bb506389-99c2-47f6-8aa7-e0ef9e6a9a26">

# How to Call The Functionalities

## Read Image Dataset

Deep learning models are mathematical in nature and require numerical input. Each pixel in an image can be represented by its intensity values, and in the case of RGB (Red, Green, Blue) images, each pixel has three values corresponding to the intensity of red, green, and blue channels. 

<img width="700" alt="Jepretan Layar 2024-01-08 pukul 00 17 02" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/df985f43-0438-4822-a933-580f18473126">

*But, we must arrange the image dataset like this*

<img width="139" alt="Jepretan Layar 2024-01-08 pukul 00 25 04" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/bfe1164b-1b90-4711-98f4-9de071930c09">

For the ImageReader functionality, there are three main parameter that can be explored.

| Parameter | Options |
| :---: | :----: |
| mode | "rgb" or "grayscale" |
| normalization | *true* or *false* |
| alpha | *true* or *false* |

## Input Layer

The input layer defines the shape and size of the input data that the neural network expects by specifying the number of features or dimensions in the input data. In this module, InputLayer doesn't need special parameters to set up.

<img width="558" alt="Jepretan Layar 2024-01-08 pukul 09 09 55" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/115af000-da00-4653-86be-979a19910749">

## Convolution Layer

Convolutional layer is a fundamental building block of Convolutional Neural Networks that designed to learn spatial hierarchies of features from the input data adaptively.

<img width="777" alt="Jepretan Layar 2024-01-08 pukul 09 10 21" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/88349255-b3ed-4022-83d6-254baa3097e3">

For the Convolution layer functionality, the are eight main parameter that can be explored.

| Parameter | Options |
| :---: | :----: |
| filter | filter 2d in the form of 2x2, 3x3, 5x5 |
| activation | "relu", "leaky relu", "elu", "selu", "binary step", "tanh", "arc tan", "prelu", "soft plus", "soft sign", "linear" |
| strides | [*vertical*, *horizontal*] |
| dilations | [*vertical*, *horizontal*] |
| epoch | 20, 40, 100, until infinity |
| erroType | "mse" or "mae" |
| learningRate | 0 until 1 |
| weightInitial | "xavier", "he", or "standard" |

## Filter

Filter is a small-sized matrix used for the convolution operation. During the training process, the network adjusts the values of the filter's weights to minimize the difference between the predicted output and the actual target. 

<img width="420" alt="Jepretan Layar 2024-01-08 pukul 08 46 36" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/9c053ab7-71ee-40c1-ab9e-f22d53e6a984">

## Subsample

It is down-sampling operation to reduce the spatial dimensions of the input volume and subsequently decrease the computational complexity of the network.

<img width="901" alt="Jepretan Layar 2024-01-08 pukul 09 11 13" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/64216081-c52f-4916-b8ef-10aa7627e9bf">

For the Subsample layer functionality, there are four main parameter that can be explored.

| Parameter | Options |
| :---: | :----: |
| type | "min", "max", or "average" |
| kernel | [*vertical*, *horizontal*] |
| strides | [*vertical*, *horizontal*] |
| dilations | [*vertical*, *horizontal*] |

## Flatten

The purpose of the flatten operation is to transition from the spatial representation of features in the convolutional and pooling layers to a format that can be fed into traditional fully connected layers.

<img width="622" alt="Jepretan Layar 2024-01-08 pukul 09 11 48" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/9dc8e46f-32da-4654-b78b-11beb88704f3">

In this module, InputLayer functinality doesn't need special parameters to set up.

## Fully Connected

Fully Connected is a type of layer where each neuron or node is connected to every neuron in the previous and the next layers. Unlike convolutional and pooling layers, which operate on local regions of the input, fully connected layers process the entire input. 

<img width="817" alt="Jepretan Layar 2024-01-08 pukul 09 42 44" src="https://github.com/oktaviacitra/dl-ali-doc/assets/49669018/463a2ea3-3205-4e33-a850-736292f99fb3">

For the Fully Connected layer functionality, the are six main parameter that can be explored.

| Parameter | Options |
| :---: | :----: |
| unit | numerical array |
| activation | "relu", "leaky relu", "elu", "selu", "binary step", "tanh", "arc tan", "prelu", "soft plus", "soft sign", "linear" |
| epoch | 20, 40, 100, until infinity |
| erroType | "mse" or "mae" |
| learningRate | 0 until 1 |
| weightInitial | "xavier", "he", or "standard" |

# Sample Code

        String path = "/Users/oktaviacitra/cifar/";
        String[] labels = new LabelReader(path + "train/").getClasses();
        ImageReader reader = ImageReader.getInstance(labels, "grayscale").normalization(true);
        RandomState randomState = new RandomState();

        double[][][][] trainImages = reader.retrieve(path + "/train");
        double[][] trainTargets = reader.getTargets();
        trainImages = randomState.generate(trainImages, trainTargets);
        trainTargets = randomState.getTarget();

        double[][][][] testImages = reader.retrieve(path + "/test");
        double[][] testTargets = reader.getTargets();

        Input2DLayer inputLayer = Input2DLayer.getInstance("layer 2");
        double[][][][][] trainFeatures = inputLayer.transform(trainImages);
        double[][][][][] testFeatures = inputLayer.transform(testImages);

        double[][][] filter = new double[][][]{
                Filter2D.Kernel3x3.HORIZONTAL_LINES_DETECTION,
                Filter2D.Kernel2x2.ROBERTS_HORIZONTAL
        };

        Convolution2DLayer convolution2DLayer = Convolution2DLayer.getInstance("layer 2", filter)
                .activation("relu")
                .dilations(new int[]{1, 2})
                .strides(new int[]{2, 1})
                .epoch(20)
                .errorType("mae")
                .learningRate(0.01)
                .weightInitial("xavier");
        trainFeatures = convolution2DLayer.train(trainFeatures, testFeatures, true);
        testFeatures = convolution2DLayer.getTestOutputs();

        SubSample2DLayer subSample2DLayer = SubSample2DLayer.getInstance("layer 3", "max", new int[]{3, 3})
                .strides(new int[]{2, 2})
                .dilations(new int[]{2, 2});
        trainFeatures = subSample2DLayer.transform(trainFeatures);
        testFeatures = subSample2DLayer.transform(testFeatures);

        Flatten2DLayer flatten2DLayer = Flatten2DLayer.getInstance("layer 4");
        double[][] trainFlatten = flatten2DLayer.transform(trainFeatures);
        double[][] testFlatten = flatten2DLayer.transform(testFeatures);

        FullyConnectedLayer fullyConnectedLayer = FullyConnectedLayer
                .getInstance("layer 5", new int[]{32, 16, 10}, new String[]{"relu", "relu", "softmax"})
                .learningRate(0.01)
                .errorType("mae")
                .epoch(20)
                .weightInitial("he");
        double[][] trainOutputs = fullyConnectedLayer
                .train(trainFlatten, testFlatten, trainTargets, testTargets, true);
        double[][] testOutputs = fullyConnectedLayer.getTestOutputs();

