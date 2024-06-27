# Large Language Models

A **Large Language Model (LLM)** is an advanced form of artificial intelligence designed to understand and generate human language like humans. These models use complex algorithms and are trained on huge sets of data — hence the name "large." LLMs are built on machine learning, they are able to recognize and interpret human language because they have previously been trained using thousands or millions of examples (often gathered from the Internet). In order to understand how characters, words and sentences work together, LLMs use “deep learning” which allows them to recognize differences and similarities without the need of human intervention.
Large Language Models (LLMs) do not have genuine comprehension abilities. Instead, they operate by analyzing statistical patterns. LLMs rely on statistical analysis rather than true understanding to process and generate language.

They can generate original and creative texts, read, understand and translate a vast amount of text in different languages, answer your questions in a clear and informative way, even if they are open-ended, complex, or strange.

There are different types of LLMs, with different characteristics: ChatGPT (by OpenAI), Llama2 (by Meta), Mistral (by Mistral AI), Gemini (by Google DeepMind).


Large Language Models were essential for the development of our project. We tried to use multiple models and the most effective ones were ChatGPT, Mistral and Gemini. All of them were useful in order to achieve different specific results and compare their functions.

We used LLMs to create the definitions of the cultural heritage we examined in this project, to create some of the queries that we used in the first part of the project, and especially to check if the ones that we created were the right ones. We also used them to explain us something that we didn’t understand. 

#### 2. ChatGPT

ChatGPT, acronym of Generative Pretrained Transformer, is a sophisticated language model created by OpenAI. Its primary function is to assist users by generating human-like text based on the prompts and questions it receive.
It can understand and generate text in multiple languages, provide detailed responses on a wide range of topics, and help with tasks like writing, brainstorming, translating, and answering factual questions. 
During our research we discovered that, among the other Large Language Models, ChatGPT is the most accurate and the most updated. When asking the same questions to the other LLMs, ChatGPT was the one that gave us the most relevant and precise answers. For this reason, maybe, it is the most popular of them.

#### Prompt Engineering

We used several engineering prompts to achieve our purposes. Prompt engineering is the process of structuring an instruction that can be interpreted and understood by a generative AI model. So, a prompt is natural language text describing the task that an AI should perform.
Prompt engineering may involve phrasing a query, specifying a style, providing relevant context or assigning a role to the AI.

There are different types of prompt engineers: zero-shot prompting, few-shot prompting, chain-of-thought, generated-knowledge prompting, prompt chaining and tree-of-thought. We used several of them. 

Here are some examples of how we decided to use them:

<table width="200" height="300">
Q: "Give me a description of Palazzo Poggi in Bologna in English." 

This was a **zero-shot prompting**, that contains no examples or demonstrations and directly tells the model to perform a task without additional examples to guide it.

A: "Palazzo Poggi is a historical building located in Bologna, Italy. It was constructed in the mid-16th century and showcases Renaissance architecture. Originally built for the Poggi family, it later became the seat of the University of Bologna. The palazzo now houses several university museums, including the Museum of Palazzo Poggi, which features collections related to natural history, physics, anatomy, and astronomy. The interior is renowned for its elaborate frescoes by prominent artists of the period, such as Pellegrino Tibaldi and Niccolò dell’Abbate. Palazzo Poggi is a significant cultural and educational landmark, reflecting Bologna's rich history in art and science.
 
</table>

<table width="200" height="300">
Then I asked the same question, but adding something more specific.

Q: Give me a description of Palazzo Poggi in Bologna in English and divide the answer in some parts.

This was a **prompt chaining**, that breaks down tasks into its subtasks, in order to improve the understanding and the performance of the model. 

A: Palazzo Poggi: 

#### A Historical and Architectural Gem in Bologna 

Palazzo Poggi, located in the heart of Bologna, Italy, is a renowned historical palace that now serves as the headquarters of the University of Bologna. This magnificent building is not only a center of academic life but also a treasure trove of history, art, and architecture.


#### Historical Background

The construction of Palazzo Poggi began in the mid-16th century under the commission of Alessandro Poggi, a prominent figure of the time. Designed by the renowned architect Bartolomeo Triachini, the palace was initially intended to serve as a private residence for the Poggi family. Over the centuries, it has undergone several transformations, reflecting the rich tapestry of Bologna's cultural and academic evolution.
In the late 18th century, the palace was acquired by the Institute of Sciences, and later, in the 19th century, it became part of the University of Bologna. Today, it houses the University Museums, including the Museo di Palazzo Poggi, which showcases a wide array of scientific collections, artworks, and historical artifacts.


#### Architectural Features

Palazzo Poggi is a splendid example of Renaissance architecture with its elegant facade and intricate interior design. The building's exterior is characterized by its symmetrical proportions, grand entrance, and decorative elements that reflect the architectural trends of the period. Inside, visitors can marvel at the beautifully frescoed ceilings, majestic staircases, and richly adorned rooms. The Hall of Maps, a highlight of the palace, features stunning frescoes depicting various maps and celestial charts, illustrating the scientific knowledge and artistic skill of the time. Another notable room is the Hall of Hercules, which is adorned with frescoes narrating the mythological tales of Hercules.


#### Cultural and Academic role

Palazzo Poggi is not only an architectural masterpiece but also a hub of cultural and academic activity. It hosts a variety of exhibitions, conferences, and events that contribute to the vibrant intellectual life of Bologna. The Museo di Palazzo Poggi is located within the palace.


#### Visitor Information

The palace is open to the public, with guided tours available for those who wish to delve deeper into its historical and architectural significance. Whether you are an architecture enthusiast, a history buff, or simply looking to explore the cultural heritage of Bologna, Palazzo Poggi promises an enriching and memorable experience.
Palazzo Poggi is a must-visit destination in Bologna. With its stunning architecture, rich history, and ongoing commitment to scientific research and education, the palace is a true gem of the city and a testament to the enduring legacy of the University of Bologna."
</table>


We also used the LLMs to enrich the knowledge graph and to check if the information that we got from the Arco ontology was actually true. 

So, we used ChatGPT to check if there was any information about Pellegrino Tibaldi (one of the possible architects) contained in the Arco ontology: 

Q: "Is there a page on Arco ontology knowledge graph about Pellegrino Tibaldi?" (zero-shot prompt)

A: "There doesn't appear to be a specific page on the Arco ontology knowledge graph about Pellegrino Tibaldi. You might want to directly search the Arco project site or contact them for detailed information."

And then we asked: 

Q: "Give me a query using Sparql in order to check if there is a page about Pellegrino Tibaldi on the Arco Ontology."

A: "To query the Arco Ontology to check if there is a page about Pellegrino Tibaldi, you can use the following SPARQL query:

````SPARQL
PREFIX foaf: <http://xmlns.com/foaf/0.1/>
PREFIX arco: <http://www.arco-project.org/ontology/>
SELECT ?person ?name
WHERE {
  ?person a foaf:Person ;
       foaf:name ?name .
  FILTER (regex(?name, "Pellegrino Tibaldi", "i"))
}
````

This query does the following:
Defines the necessary prefixes for foaf (Friend of a Friend vocabulary) and arco.

Selects the ?person and ?name variables.

Looks for instances where ?person is a foaf:Person and has a foaf:name.
Filters the results to include only those whose name matches "Pellegrino Tibaldi", ignoring case sensitivity.
You can run this query using a SPARQL endpoint provided by the Arco project or any other tool that allows you to run SPARQL queries."

We asked it to use ASK:

A: "ASK query form in SPARQL will allow you to check if a certain piece of information exists without retrieving all the details. Here is how you can structure an ASK query to check if there is any mention of Pellegrino Tibaldi in the Arco Ontology:

PREFIX foaf: <http://xmlns.com/foaf/0.1/>

PREFIX arco: <http://www.arco-project.org/ontology/>

ASK {

  ?person a foaf:Person ;
  
          foaf:name ?name .
 
  FILTER (regex(?name, "Pellegrino Tibaldi", "i"))

}

This query does the following:
1.	Defines the necessary prefixes for foaf (Friend of a Friend vocabulary) and arco.
2.	Uses the ASK query form to return a boolean value.
3.	Checks for instances where ?person is a foaf:Person and has a foaf:name.
4.	Applies a filter to match the name "Pellegrino Tibaldi" (case insensitive).

This query will return true if there is at least one instance of a person named "Pellegrino Tibaldi" in the ontology, and false otherwise."

We run the query on Sparql and it appeared to be “False”, so there is no instance of a person named Pellegrino Tibaldi" in the ontology



#### 3. Mistral

For the purposes of this project, Mistral.ai was employed as well. Mistral.ai is a large language model developed by a team of researchers and engineers at the French company Hugging Face. The model is designed to generate human-like text based on input prompts, and it is capable of understanding and responding to a wide variety of natural language queries and commands. Its key features include: advanced architecture, high performance, scalability and versatility. Its size and complexity make it one of the most advanced language models available today.

#### Scalability: 

Mistral's models are scalable, allowing for deployment in various applications from chatbots to complex data analysis tools.

**Large**: top reasoning capacities

**Next**: prototype model with extra concision

**Small**: fast and cost-effective

**Codestral**: fast and specialized in code

All models were explored, the same question was asked with a different model to observe potential changes in the results. The most accurate and complete model resulted to be “Large” and was the one used the most. 


#### Use:
Searching for information related to the cultural events of interest, generation of queries (inaccurate), inspiration for the enrichment of the knowledge graph. 

#### 4. Gemini
Gemini is a family of large language models developed by Google DeepMind. Gemini’s strengths include code comprehension and generation, multilingualism and, most importantly, multimodal capabilities. This is what really sets Gemini apart: unlike most LLMs trained solely on text, Gemini can process various data formats simultaneously, including text, images, audio, video, and even computer code. This allows it to understand and respond to information in richer ways.

#### Versions: 

**Gemini Ultra**: excelling in scientific tasks and code comprehension

**Gemini Pro**: offering a good balance of capabilities for various tasks.

**Gemini Flash**: Optimized for speed, ideal for real-time applications.

**Gemini Nano**: Designed for use on smaller devices with lower processing power.

As of today, Gemini 1.5 is the latest version, boasting an extended context window for improved understanding and response generation, especially in complex tasks. This was the version we decided to utilize for the purposes of this project. 

#### Use:
Searching for information related to the cultural events of interest and their descriptions, generation of queries (inaccurate), inspiration for the enrichment of the knowledge graph. 

#### Searching for information  
Gemini and Mistral were not always updated and accurate in giving information. For example, we were not sure whether the Collezione Marsili was exposed in Museo di Palazzo Poggi because there was little information about it on the Internet so we asked LLMs for help. 

Which notable pieces of the Marsili collection are held in the museum Palazzo Poggi? (Zero-shot prompting: no examples provided of what the desired output should look like) 

**Mistral AI**: I apologize for any confusion, but the Marsili Collection is not housed in the Museum of Palazzo Poggi in Bologna. The museum primarily focuses on the Aldrovandi Collection and other collections related to the history of the University of Bologna and its scientific and artistic achievements.


**Gemini**: The information available suggests that Palazzo Poggi doesn't house a collection specifically by Luigi Ferdinando Marsili himself.

However, we found out that the museum does host the collection thanks to the Arco ontology and received confirmation by ChatGPT. 

#### Descriptions:
To find fitting descriptions, we asked LLMs to help us and noticed that their replies were fine tuned according to the input they received. They remained generic and did not satisfy us when using zero-shot prompts, on the contrary when we asked more specific questions we received the answers we aimed at. 

Give me a brief history of the Istituto delle Scienze (Alma Mater Studiorum of Bologna) in Palazzo Poggi and its foundation, in chronological steps. (**Chain-Of-Thought-  Prompting**-> Encourage the model to follow a multi-step reasoning process to arrive at an answer.)


Mistral: 

#### Construction of Palazzo Poggi (16th century): 
Palazzo Poggi was built in the 16th century by the Bolognese architect Alfonso Torreggiani for the Poggi family, who were prominent Bolognese nobles.

#### Foundation of the Istituto delle Scienze (1711): 
The Istituto delle Scienze was founded in 1711 by Pope Clement XI, who issued a papal bull establishing the Institute of Sciences and Arts in Bologna. The new institution was created to promote scientific research and education in the city.
#### Acquisition of Palazzo Poggi (1714): 
In 1714, the Istituto delle Scienze acquired Palazzo Poggi from the Poggi family. The palace was chosen as the new home of the Institute due to its size and central location in the city.
Expansion and Renovation (18th-19th centuries): Over the centuries, the Istituto delle Scienze expanded and added new buildings to Palazzo Poggi to accommodate the growing number of students and faculty. The palace underwent several renovations and expansions during this period, including the addition of new classrooms, libraries, and laboratories.
#### Modern Era (20th century-present): 
In the 20th century, the Istituto delle Scienze became part of the Alma Mater Studiorum - University of Bologna, which is one of the oldest and most prestigious universities in the world. The institution continues to use Palazzo Poggi as its main administrative and teaching facility, and the palace remains a symbol of the university's rich history and cultural heritage.
#### Present Day (21st century): 
Today, the Istituto delle Scienze is a leading center for scientific research and education in Italy and Europe. Its facilities in Palazzo Poggi include state-of-the-art laboratories, libraries, and museums, and it offers a wide range of programs in fields such as physics, chemistry, biology, and geology.

Some of the information provided by Mistral was not exact (the architect is wrong for example), for this reason we checked everything and the final description is a mixture of information from Mistral, ChatGPT, the web and our own corrections. 
We decided not to use Gemini for this phase because when asking for descriptions of places we were interested in, it assumed we were tourists and tended to give practical tips and information such as the opening hours of the museum and the admission prices and this was not our goal.


#### Inspiration for the enrichment of the knowledge graph:

What information could I add on the Arco Knowledge Graph related to Palazzo Poggi? 

Tabella su documento 12

We decided to break down the prompt into smaller sub-prompts and generate answers for each of them in order to build up a tree of thought that covers different topics and ideas we were interested in exploring (**Tree-Of-Thought Prompting**). In particular, we asked about the commissioner and architect of Palazzo Poggi (respectively Giovanni Poggi/the Poggi Family and Pellegrino Tibaldi and/or Bartolomeo Triachini). We proceeded to check if they were linked to Palazzo Poggi on the Arco Ontology and realized they were not.

Comparison of LLMs:

Tabella

<br />

> 🧭
> - [Next ⏭](Conclusion.md)
> - [Previous ⏮](Museo-Della-Specola.md)
> - [Home 🏠](index.md) 
