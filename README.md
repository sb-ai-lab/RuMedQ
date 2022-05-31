# Dataset Card for RuMedQ

## Dataset Summary
Russian Medical Quastions Dataset (RuMedQ) is a synthetic dataset containing pairs of "symptom" - "medical question regarding this symptom", as well as a label, if the question generated by RuGPT3 corresponds to this symptom (1) or not (0).
The dataset was synthesized using the RuGPT3 model trained on a small corpus of symptom-question pairs. 
After generation, the dataset was cleared of syntactically incorrect questions, some typos and gross errors of generation were corrected, an annotation of the correspondence of the question to the symptom was carried out. 
This dataset can be used for the following tasks:
1. To train models to generate medical questions from given symptoms,
2. As a benchmark in a Natural Language Inference task, where the symptom and the question act as a pair of sentences to be matched.

## Languages
Russian

## Dataset Structure
Data Instances

    {
        "symptom": "low mood",
        "question": "Does apathy often bother you?",
        "isCorrectQ": 1
    }

Data Fields
- symptom: a string feature
- question: a string feature
- isCorrectQ: a int32 feature (0 or 1)

Data Shape
6053 lines, 3 columns
## Dataset Creation
The dataset was synthesized using the RuGPT3 model trained on a small corpus of symptom-question pairs. After generation, the dataset was cleared of syntactically incorrect questions, some typos and gross errors of generation were corrected, an annotation of the correspondence of the question to the symptom was carried out. 

## Annotations
Annotation process
The dataset is marked up by 2 annotators, whose task was to determine whether the question corresponds to the proposed symptom or not. By correspondence is understood that the question should be asked in such a way as to clarify whether the subject being asked has this particular symptom. The annotators marked up disjoint subsets of symptom-question pairs, so each pair is marked up by one annotator. In addition to the markup, the annotators made minor stylistic and grammatical corrections in the questions to bring them into the correct form.

Who are the annotators?
The annotators were specialists with medical or pharmaceutical education.

## Licensing Information
The dataset is distributed under a license [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.en)

## Citation Information
    @misc{Nesterov_RuMedQ_2021,
        author = {Nesterov, Alexandr and Zubkova, Galina},
        month = {11},
        title = {{RuMedQ}},
        url = {https://github.com/sb-ai-lab/RuMedQ},
        version = {1.0.0},
        year = {2021}
    }

# Contributions
This dataset was prepared by Alexander Nesterov, DS at Sber AI Lab  
This dataset was annotated by Galina Zubkova, PM at Sber AI Lab and Alexander Nesterov, DS at Sber AI Lab


# Dataset Card for RuMedQ

## Dataset Summary
Russian Medical Quastions Dataset (RuMedQ) это синтетический датасет содержащий пары "симптом" - "медицинский вопрос, содержащий этот симптом", а также метку, соответствует ли вопрос исходному симптому (1) или нет (0). Датасет синтезирован при помощи модели RuGPT3 обученной на небольшом корпусе пар симптом-вопрос. После генерации датасет очищен от синтаксически некорректных вопросов, исправлены некоторые опечатки и грубые ошибки генерации, проведена аннотация соответствия вопроса исходному симптому. Данный датасет может использоваться в нескольких задачах: 
1. Для обучения моделей для генерации медицинских вопросов из заданных симптомов,
2. В качестве бенчмарка в задаче Natural Language Inference, где симптом и вопрос выступают в качестве пары предложений, соответствие которых нужно определить.

## Languages
Russian

## Dataset Structure
Data Instances

    {
        "symptom": "Сниженное настроение",
        "question": "Часто ли вас беспокоит апатия?",
        "isCorrectQ": 1
    }

Data Fields
- symptom: a string feature
- question: a string feature
- isCorrectQ: a int32 feature (0 or 1)

Data Shape
6053 строки, 3 колонки


## Dataset Creation
Датасет синтезирован при помощи модели RuGPT3 обученной на небольшом корпусе пар симптом-вопрос. После генерации датасет очищен от синтаксически некорректных вопросов, исправлены некоторые опечатки и грубые ошибки генерации, проведена аннотация соответствия вопроса исходному симптому.

## Annotations
Annotation process
Датасет размечен 2 аннотаторами, задачей которых было определение, соответствует ли вопрос исходному симптому или нет. Под соответствием понимается, что вопрос должен быть задан таким образом, чтобы уточнить, есть ли исходный симптом у субъекта, которому задается вопрос. Аннотаторы размечали не пересекающиеся подмножества пар симптом-вопрос, таким образом каждая пара аннотирована одним аннотатором. Кроме разметки аннотаторы выполняли небольшие стилистические и грамматические исправления в вопросах, для приведения из в корректную форму.

Who are the annotators?
В качестве аннотаторов выступали специалисты, имеющие медицинское или фармацевтическое образование.

## Licensing Information
Датасет распространяется по лицензии [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.en)

## Citation Information
    @misc{Nesterov_RuMedQ_2021,
        author = {Nesterov, Alexandr and Zubkova, Galina},
        month = {11},
        title = {{RuMedQ}},
        url = {https://github.com/sb-ai-lab/RuMedQ},
        version = {1.0.0},
        year = {2021}
    }

# Contributions
Датасет создан Нестеровым Алекстандром, ведущим исследователем данных лаборатории по искусственному интеллекту Сбера  
Датасет аннотирован Зубковой Галиной, менеджером проектов лаборатории по искусственному интеллекту Сбера и Нестеровым Александром
