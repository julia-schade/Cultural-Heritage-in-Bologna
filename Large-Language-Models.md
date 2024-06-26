# Large Language Models

A Large Language Model (LLM) is an advanced form of artificial intelligence designed to understand and generate human language like humans. These models use complex algorithms and are trained on huge sets of data — hence the name "large." LLMs are built on machine learning, they are able to recognize and interpret human language because they have previously been trained using thousands or millions of examples (often gathered from the Internet). In order to understand how characters, words and sentences work together, LLMs use “deep learning” which allows them to recognize differences and similarities without the need of human intervention.
Large Language Models (LLMs) do not have genuine comprehension abilities. Instead, they operate by analyzing statistical patterns. LLMs rely on statistical analysis rather than true understanding to process and generate language.

Chat GPT ange


#### 3. Mistral

For the purposes of this project, Mistral.ai was employed as well. Mistral.ai is a large language model developed by a team of researchers and engineers at the French company Hugging Face. The model is designed to generate human-like text based on input prompts, and it is capable of understanding and responding to a wide variety of natural language queries and commands. Its key features include: advanced architecture, high performance, scalability and versatility. Its size and complexity make it one of the most advanced language models available today.

Scalability: 
Mistral's models are scalable, allowing for deployment in various applications from chatbots to complex data analysis tools.
Large: top reasoning capacities
Next: prototype model with extra concision
Small: fast and cost-effective
Codestral: fast and specialized in code
All models were explored, the same question was asked with a different model to observe potential changes in the results. The most accurate and complete model resulted to be “Large” and was the one used the most. 

Use:
Searching for information related to the cultural events of interest, generation of queries (inaccurate), inspiration for the enrichment of the knowledge graph. 

#### 4. Gemini
Gemini is a family of large language models developed by Google DeepMind. Gemini’s strengths include code comprehension and generation, multilingualism and, most importantly, multimodal capabilities. This is what really sets Gemini apart: unlike most LLMs trained solely on text, Gemini can process various data formats simultaneously, including text, images, audio, video, and even computer code. This allows it to understand and respond to information in richer ways.
Versions: 
Gemini Ultra: excelling in scientific tasks and code comprehension
Gemini Pro: offering a good balance of capabilities for various tasks.
Gemini Flash: Optimized for speed, ideal for real-time applications.
Gemini Nano: Designed for use on smaller devices with lower processing power.
As of today, Gemini 1.5 is the latest version, boasting an extended context window for improved understanding and response generation, especially in complex tasks. This was the version we decided to utilize for the purposes of this project. 
Use:
Searching for information related to the cultural events of interest and their descriptions, generation of queries (inaccurate), inspiration for the enrichment of the knowledge graph. 

#### Searching for information  
Gemini and Mistral were not always updated and accurate in giving information. For example, we were not sure whether the Collezione Marsili was exposed in Museo di Palazzo Poggi because there was little information about it on the Internet so we asked LLMs for help. 

Which notable pieces of the Marsili collection are held in the museum Palazzo Poggi? (Zero-shot prompting: no examples provided of what the desired output should look like) 
Mistral AI: I apologize for any confusion, but the Marsili Collection is not housed in the Museum of Palazzo Poggi in Bologna. The museum primarily focuses on the Aldrovandi Collection and other collections related to the history of the University of Bologna and its scientific and artistic achievements.

Gemini: The information available suggests that Palazzo Poggi doesn't house a collection specifically by Luigi Ferdinando Marsili himself.

However, we found out that the museum does host the collection thanks to the Arco ontology and received confirmation by ChatGPT. 

#### Descriptions:
To find fitting descriptions, we asked LLMs to help us and noticed that their replies were fine tuned according to the input they received. They remained generic and did not satisfy us when using zero-shot prompts, on the contrary when we asked more specific questions we received the answers we aimed at. 

Give me a brief history of the Istituto delle Scienze (Alma Mater Studiorum of Bologna) in Palazzo Poggi and its foundation, in chronological steps. (Chain-Of-Thought-  Prompting-> Encourage the model to follow a multi-step reasoning process to arrive at an answer.)

Mistral: 
Construction of Palazzo Poggi (16th century): Palazzo Poggi was built in the 16th century by the Bolognese architect Alfonso Torreggiani for the Poggi family, who were prominent Bolognese nobles.
Foundation of the Istituto delle Scienze (1711): The Istituto delle Scienze was founded in 1711 by Pope Clement XI, who issued a papal bull establishing the Institute of Sciences and Arts in Bologna. The new institution was created to promote scientific research and education in the city.
Acquisition of Palazzo Poggi (1714): In 1714, the Istituto delle Scienze acquired Palazzo Poggi from the Poggi family. The palace was chosen as the new home of the Institute due to its size and central location in the city.
Expansion and Renovation (18th-19th centuries): Over the centuries, the Istituto delle Scienze expanded and added new buildings to Palazzo Poggi to accommodate the growing number of students and faculty. The palace underwent several renovations and expansions during this period, including the addition of new classrooms, libraries, and laboratories.
Modern Era (20th century-present): In the 20th century, the Istituto delle Scienze became part of the Alma Mater Studiorum - University of Bologna, which is one of the oldest and most prestigious universities in the world. The institution continues to use Palazzo Poggi as its main administrative and teaching facility, and the palace remains a symbol of the university's rich history and cultural heritage.
Present Day (21st century): Today, the Istituto delle Scienze is a leading center for scientific research and education in Italy and Europe. Its facilities in Palazzo Poggi include state-of-the-art laboratories, libraries, and museums, and it offers a wide range of programs in fields such as physics, chemistry, biology, and geology.
Some of the information provided by Mistral was not exact (the architect is wrong for example), for this reason we checked everything and the final description is a mixture of information from Mistral, ChatGPT, the web and our own corrections. 
We decided not to use Gemini for this phase because when asking for descriptions of places we were interested in, it assumed we were tourists and tended to give practical tips and information such as the opening hours of the museum and the admission prices and this was not our goal.


#### Inspiration for the enrichment of the knowledge graph:

What information could I add on the Arco Knowledge Graph related to Palazzo Poggi? 

Tabella su documento 12

We decided to break down the prompt into smaller sub-prompts and generate answers for each of them in order to build up a tree of thought that covers different topics and ideas we were interested in exploring (Tree-Of-Thought Prompting). In particular, we asked about the commissioner and architect of Palazzo Poggi (respectively Giovanni Poggi/the Poggi Family and Pellegrino Tibaldi and/or Bartolomeo Triachini). We proceeded to check if they were linked to Palazzo Poggi on the Arco Ontology and realized they were not.

Comparison of LLMs:

Tabella

<br />

> 🧭
> - [Next ⏭](Conclusion.md)
> - [Previous ⏮](Museo-Della-Specola.md)
> - [Home 🏠](index.md) 
