# Intent Classification & Entity Recognition (NER) Project

##  Overview

This project focuses on data annotation for Natural Language Processing (NLP) tasks using Label Studio. It combines **intent classification** and **entity recognition (NER)** to prepare structured datasets for training conversational AI and Large Language Models (LLMs).

---

##  Objectives

* Classify user queries into predefined intents
* Identify and label key entities within the text
* Create high-quality annotated datasets for AI model training

---

##  Tools & Technologies

* Label Studio
* Python (for dataset generation)
* CSV / JSON data formats

---

##  Dataset

The dataset consists of user queries related to:

* Product pricing
* Weather information
* Stock market queries

### Sample Data:

```
What is the price of 5 laptops?
Give me the stock price of AAPL
What will the weather be like today?
```

---

##  Annotation Types

###  1. Intent Classification

Each sentence is labeled with one of the following intents:

* Product Price
* Stock Price
* Weather

---

###  2. Entity Recognition (NER)

Entities labeled within the text include:

* Quantity (e.g., 5, 10)
* Product (e.g., laptops, phones)
* Stock Ticker (e.g., AAPL, TSLA)
* Day / Time (e.g., today, Monday)

---

##  Label Studio Configuration

Custom XML configuration was used to design the annotation interface:

```xml
<View>
  <Labels name="entity_slot" toName="message">
    <Label value="Quantity"/>
    <Label value="Product"/>
    <Label value="Stock Ticker"/>
    <Label value="Day"/>
  </Labels>

  <Text name="message" value="$text"/>

  <Choices name="intent" toName="message" choice="single">
    <Choice value="Stock Price"/>
    <Choice value="Product Price"/>
    <Choice value="Weather"/>
  </Choices>
</View>
```

---

##  Workflow

1. Created dataset using Python scripts
2. Imported data into Label Studio
3. Designed custom labeling interface
4. Annotated intents and entities manually
5. Exported labeled data for model training

---

##  Key Learnings

* Understanding of real-world data annotation workflows
* Experience in intent classification and NER tasks
* Hands-on practice with Label Studio configuration
* Importance of high-quality labeled data for LLM performance

---

##  Future Improvements

* Expand dataset with more diverse queries
* Add more intent categories
* Integrate annotated data into ML model training

---

##  Author
Aditi Sharma
