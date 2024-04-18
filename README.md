# mlops_get_started
> Machine Learning Engineering for Production (MLOps) Specialization by DeepLearning.AI

- [Link](https://www.coursera.org/specializations/machine-learning-engineering-for-production-mlops#courses)

# Week 1: Intro

## ML lifecycle

1. Scoping
    - define project
2. Data
    - define data
    - label and organize data
3. Modeling
    - select and train
    - perform error analysis
4. Deployment
    - Deploy in production
    - Monitor & maintain system


![](./static/model_maintenance.png)
## Case study: speech recognition

1. Scoping
    - "Decide to work on speech recognition for voice spearch"
    - key metrics: Accuracy, latency, throughput
    - Estimate time schedule to finish this scope
2. Define Data
    - labeled consistently (i.g convention)
    - How much silence before / after each clip?
    - How to perform volume normalization
3. Modeling
    - Code (algo / model)
    - Hyperparameters, Data
    - **ml system = code + data**
4. Deployment
    - edge device -> mobile phone -> microphone -> VAD module to send speech API to the prediction Server
    - **concept / data drift**

## Course outline

1. Deployment
2. Modeling
3. Data
    - (opt) Scoping

# Week 1: Deployment

## Key challenges

- Concept drift and Data drift
    - Q. "How has the data changed?"
    - Gradual change, somtime sudden change (covid-19 affects card data)
    - Concept drift: x -> y, relation change which means "evolution of data that invalidates the data model."

## Deployment patterns

### Common Cases
1. New product / capability
2. Automate /assist with manual task
3. Replace prev ML system


- shadow mode, validate model
- canary deployment(gradually), roll out by small fraction 
- blue / green


### Degrees of automation

Human only -> shadow mode -> HITL( ai assistance -> Partial automation ) -> Full automation

## Monitoring

### Monitoring dashboard

1. Brainstorm the thigns that could go wrong
2. From brainstrom -> pick metrics
3. iterate and choose right set of metrics to monitor

### Examples

- sw metrics: memotry, compute, latency, throughput, server load
- Input metrics(X): Avg input length, Avg input volume, Num missing values, Avg image brightness
- Output mertics(Y): times return null, times user redoes search, times user switches to typing, CTR


## Pipline monitoring
> Metrics to monitor

1. Monitor: sw metrics, input and output mertics
2. How quickly do they change?
    - user dat agenerally has slower drift
    - enterprise data can shift fast (B2B data shifts quickly)



