<!-- # Introduction to Generative AI and Large Language Models -->
# 생성형 AI와 Large Language Models (LLM) 소개

[![Introduction to Generative AI and Large Language Models](./images/01-lesson-banner.png)](https://youtu.be/vf_mZrn8ibc)

<!-- *(Click the image above to view video of this lesson)* -->
*(이미지를 클릭해서 이번 강의를 수강하세요)*

<!-- Generative AI is artificial intelligence capable of generating text, images and other types of content. What makes it a fantastic technology is that it democratizes AI, anyone can use it with as little as a text prompt, a sentence written in a natural language. There's no need for you to learn a language like Java or SQL to accomplish something worthwhile, all you need is to use your language, state what you want and out comes a suggestion from an AI model. The applications and impact for this is huge, you write or understand reports, write applications and much more, all in seconds. -->
생성형 AI 는 text, 이미지를 포함한 여러 가지 콘텐츠를 생성할 수 있는 인공지능(AI)를 말합니다. 이 놀라운 기술은 AI의 민주화에 기여하였고, 때문에 어떤 사람이건 text prompt와 자연어로 된 문장을 조금 입력하기만 하면 사용할 수 있습니다. Java나 SQL같은 언어를 따로 공부할 필요도 없고, 그냥 사용자의 언어로 원하는 것을 입력하면 AI 모델로부터 제안을 받을 수 있습니다. 이러한 응용과 임팩트는 아주 거대하며, 당신은 보고서나 개발을 하는 등의 여러 작업을 몇 초 안에 수행할 수 있습니다.

<!-- In this curriculum, we’ll explore how our startup leverages generative AI to unlock new scenarios in the education world and how we address the inevitable challenges associated with the social implications of its application and the technology limitations. -->
이 커리큘럼에서 스타트업이 어떻게 교육계에서 새로운 시나리오를 열기 위해 생성형AI를 조정하는지, 그리고 생성형 AI 적용에 대한 사회적 영향, 기술적 한계와 관련된 피할 수 없는 문제를 어떻게 조정하는지 살펴보겠습니다.

<!-- ## Introduction -->
## 소개

<!-- This lesson will cover: -->
이번 수업은 아래와 같은 내용을 다룹니다.

<!-- * Introduction to the business scenario: our startup idea and mission. -->
* 비지니스 시나리오 소개: 스타트업의 아이디어와 미션
<!-- * Generative AI and how we landed on the current technology landscape. -->
* 생성형 AI와 어떻게 현재 기술 환경에 정착했는지
<!-- * Inner working of a large language model. -->
* large language model의 내부 작동
<!-- * Main capabilities and practical use cases of Large Language Models. -->
* Large language model의 주요 기능 및 실용적인 use case들

<!-- ## Learning Goals -->
## 학습 목표

<!-- After completing this lesson, you will understand: -->
이 수업이 끝나면, 아래와 같은 내용을 이해할 수 있습니다:

<!-- * What generative AI is and how Large Language Models work. -->
* 생성형 AI가 무엇인지와 LLM 동작 방식이 어떻게 되는지
<!-- * How you can leverage large language models for different use cases, with a focus on education scenarios. -->
* 교육 분야에서, LLM을 서로 다른 use case에 대해 어떻게 다룰 수 있는지

<!-- ## Scenario: our educational startup  -->
## 시나리오: 교육 관련 스타트업

<!-- Generative Artificial Intelligence (AI) represents the pinnacle of AI technology, pushing the boundaries of what was once thought impossible. Generative AI models have several capabilities and applications, but for this curriculum we'll explore how it's revolutionizing education through a fictional startup. We'll refer to this startup as *our startup*. Our startup works in the education domain with the ambitious mission statement of  -->
생성형 AI는 AI 기술의 정점으로, 한때 불가능했다고 여겨진 한계를 벗어났습니다. 생성형 AI 모델들은 몇 가지 기능과 응용들이 있지만, 이 과정에서는 교육 분야에 있어서의 혁명을 생성형 AI로 어떻게 했는지 가상의 스타트업을 통해서 살펴보겠습니다. 이 회사를 '우리 스타트업'이라고 해봅시다. 우리 스타트업은 교육 분야에서 아래와 같은 비전을 가지고 일하고 있습니다.

<!-- > *improving accessibility in learning, on a global scale, ensuring equitable access to education and providing personalized learning experiences to every learner, according to their needs*. -->
> *모든 학습자들에게 개개인의 요구 사항에 맞추어진 개인화된 학습 경험과 교육의 평등을 글로벌 스케일로 개선한다.*

<!-- Our startup team is aware we’ll not be able to achieve this goal without leveraging one of the most powerful tools of modern times – Large Language Models (LLMs). -->
우리 스타트업 팀은 이 시대 가장 강력한 도구인 LLM없이는 이 목적을 달성할 수 없다는 걸 알고 있습니다.

<!-- Generative AI is expected to revolutionize the way we learn and teach today, with students having at their disposal virtual teachers 24 hours a day who provide vast amounts of information and examples, and teachers able to leverage innovative tools to assess their students and give feedback. -->
생성형 AI는 우리가 배우고 가르치는 방법에 혁명을 일으킬 것으로 기대됩니다. 학생들은 자기들이 원하는 가상 선생님에게 하루 24시간동안 다양한 정보와 예시들을 배울 것이고, 선생들은 혁신적인 도구들을 통해서 학생들을 가르치고 피드백을 받을 수 있습니다.

![Five young students looking at a monitor - image by DALLE2](./images/students-by-DALLE2.png)

<!-- To start, let’s define some basic concepts and terminology we’ll be using throughout the curriculum. -->
시작하기위해서 이 과정에서 사용할 기본 컨셉과 용어들을 정의해 봅시다.

<!-- ## How did we get Generative AI? -->
## 어떻게 생성형 AI를 쓸 수 있을까요?

<!-- Despite the extraordinary *hype* created lately by the announcement of generative AI models, this technology is decades in the making, with the first research efforts dating back to 60s. We're now at a point with AI having human cognitive capabilities, like conversation as shown by for example [OpenAI ChatGPT](https://openai.com/chatgpt) or [Bing Chat](https://www.microsoft.com/edge/features/bing-chat?WT.mc_id=academic-105485-koreyst), which also uses a GPT model for the web search Bing conversations. -->
완전 규격 외의 과대광고들이(할루시네이션 말하는듯) 생성형 AI에서 발생한다 하더라도, 이 기술은 60년대 이후 수십년간 개발되어 왔습니다. 이제는 AI가 인간의 인지 능력을 거의 따라왔다고 보고 있고, [OpenAI ChatGPT](https://openai.com/chatgpt)나 [Bing Chat](https://www.microsoft.com/edge/features/bing-chat) 같이 GPT 모델을 사용해서 검색이나 대화를 할 수 있습니다.

<!-- Backing up a bit, the  very first prototypes of AI consisted of typewritten chatbots, relying on a knowledge base extracted from a group of experts and represented into a computer. The answers in the knowledge base were triggered by keywords appearing in the input text. -->
조금 더 말하자면, AI의 프로토타입은 전문가들로부터 얻어낸 지식들을 기반으로 컴퓨터에 입력한 챗봇들로 구성되었습니다. 정답은 knowledge base로 이루어져 있었는데, 입력 텍스트의 키워드에 따라서 답변했습니다.

<!-- However, it soon became clear that such approach, using typewritten chatbots, did not scale well. -->
그러나, 확장성이 떨어지는 문제가 있었습니다.

<!-- ### A statistical approach to AI: Machine Learning -->
### AI의 통계적 접근: 머신러닝

<!-- A turning point arrived during the 90s, with the application of a statistical approach to text analysis. This led to the development of new algorithms – known with the name of machine learning - able to learn patterns from data, without being explicitly programmed. This approach allows a machine to simulate human language understanding: a statistical model is trained on text-label pairings, enabling the model to classify unknown input text with a pre-defined label representing the intention of the message. -->
90년대의 터닝포인트는 텍스트 분석에 통계적 접근을 적용했다는 점입니다. 이 터닝포인트는 머신 러닝이라고 불리게 되는 새로운 알고리즘의 개발로 이어졌으며, 별도의 프로그래밍 작업 없이 데이터의 패턴을 학습할 수 있게 됩니다. 이런 접근 방식은 기계로 하여금 인간의 언어 이해 체계를 모방할 수 있게 되었습니다. 통계적 모델은 text와 label의 쌍으로 이루어진 학습 데이터로 학습되었으며, 모델로 하여금 모르는 입력 텍스트를 어떠한 의미가 담긴 사전 정의된 label로 분류할 수 있게 됩니다. 

<!-- ### Neural networks and modern virtual assistants -->
### Neural networks와 가상 비서

<!-- In more recent times, the technological evolution of the hardware, capable of handling larger amounts of data and more complex computations, encouraged research in the AI fields, leading to the development of advanced machine learning algorithms – called neural networks or deep learning algorithms. -->
최근에, 하드웨어의 기술적 발전으로 인해, 많은 양의 데이터와 연산 장치의 발전으로, AI 분야의 연구가 발전하면서, 발전된 형태의 머신러닝 알고리즘이 개발되었습니다. 이것을 neural network 혹은 딥 러닝 알고리즘이라고 부릅니다.

<!-- Neural networks (and in particular Recurrent Neural Networks – RNNs) significantly enhanced natural language processing, enabling the representation of the meaning of text in a more meaningful way, valuing the context of a word in a sentence. -->
Neural network, 정확히는 Recurrent neural network(RNN)은 병확히 발전된 자연어처리 모델이며, 텍스트의 의미를 문장의 단어들의 context 정보를 사용해 명확한 방법으로 표현한다.

<!-- This is the technology that powered the virtual assistants born in the first decade of the new century, very proficient in interpreting the human language, identifying a need, and performing an action to satisfy it – like answering with a pre-defined script or consuming a 3rd party service. -->
이 기술로 인해서 21세기 초에 사람의 언어를 해석할 수 있는 가상 비서가 탄생할 수 있었고, 서드 파티 서비스나 사전에 작성된 시나리오에 대해 답변하는 일들에 대해 꽤 만족스러운 반응을 얻었다. 


<!-- ### Present day, Generative AI -->
### 현재, 생성형 AI

<!-- So that’s how we came to Generative AI today, which can be seen as a subset of deep learning. -->
자 이제 딥러닝의 일부로 보여지는 생성형 AI가 어떻게 왔는지 알아봅시다.

![AI, ML, DL and Generative AI](./images/AI-diagram.png)

<!-- After decades of research in the AI field, a new model architecture – called *Transformer* – overcame the limits of RNNs, being able to get much longer sequences of text as input. Transformers are based on the attention mechanism, enabling the model to give different weights to the inputs it receives, ‘paying more attention’ where the most relevant information is concentrated, regardless of their order in the text sequence. -->
AI분야 연구로부터 수십년, *Transformer* 라고 불리는 새로운 모델이 등장했습니다. RNN의 한계점을 해결하고 더 긴 문장들을 입력으로 받을 수 있게 되었습니다. Transformer는 attention mechanism을 기반으로 해서 모델로 하여금 입력에 대해 '더 주목해야 되는 요소에' 다른 가중치를 줄 수 있게 되었습니다. 따라서 입력 순서에 관계 없이 더 연관 있는 정보에 집중할 수 있게 되었습니다.

<!-- Most of the recent generative AI models – also known as Large Language Models (LLMs), since they work with textual inputs and outputs – are indeed based on this architecture. What’s interesting about these models – trained on a huge amount of unlabeled data from diverse sources like books, articles and websites – is that they can be adapted to a wide variety of tasks and generate grammatically correct text with a semblance of creativity. So, not only did they incredibly enhance the capacity of a machine to ‘understand’ an input text, but they enabled their capacity to generate an original response in human language. -->
텍스트를 입력과 출력으로 삼는, LLM이라고도 불리는 요즘 대부분의 생성형 AI모델들은 Transformer를 기반으로 합니다. 이 모델들의 흥미로운 점은 엄청난 양의 책, 기사, 웹사이트 등과 같은 다양한 곳에서 수집한, unlabeled 데이터를 사용한다는 점입니다. 이 때문에 LLM들은 다양한 일들에 대응할 수 있고 문법적으로 올바르며 창의적인 텍스트를 생성해 낼 수 있게 되었습니다. 그래서, 기계가 입력된 텍스트를 이해하는 능력이 향상될 뿐 아니라 인간의 언어에 대한 고유의 답변들을 만들어낼 수 있게 된 것입니다.

<!-- ## How do large language models work? -->
## LLM은 어떻게 동작합니까?

<!-- In the next chapter we are going to explore different types of Generative AI models, but for now let’s have a look at how large language models work, with a focus on OpenAI GPT (Generative Pre-trained Transformer) models. -->
다음 장에서 우리는 서로 다른 타입의 생성형AI 모델들을 살펴볼 것입니다만, 지금은 어떻게 LLM이 동작하는지 OpenAI GPT 모델을 기준으로 알아봅시다.

<!-- * **Tokenizer, text to numbers**: Large Language Models receive a text as input and generate a text as output. However, being statistical models, they work much better with numbers than text sequences. That’s why every input to the model is processed by a tokenizer, before being used by the core model. A token is a chunk of text – consisting of a variable number of characters, so the tokenizer's main task is splitting the input into an array of tokens. Then, each token is mapped with a token index, which is the integer encoding of the original text chunk. -->
* **Tokenizer를 이용해 텍스트를 숫자로 변환**: LLM은 텍스트를 입력으로 받아서 텍스트를 출력으로 생성합니다. 그러나, 통계적 모델에 대해서는 숫자가 텍스트보다 잘 동작합니다. 왜냐하면 모델의 모든 입력이 모델에 입력되기 전에 tokenizer를 통해 처리되기 때문입니다. 하나의 토큰은 text의 조각으로 구성되어 있는데, 이것은 다양한 숫자의 캐릭터(char)로 구성되어 있습니다. 그래서 tokenizer의 주요 업무는 입력을 token의 array로 나누는 것입니다. 그러고나서, 각각의 토큰은 token index로 매핑되는데, token index는 원래 text chunk에 대한 정수 인코딩입니다.

![Example of tokenization](./images/tokenizer-example.png)

<!-- * **Predicting output tokens**: Given n tokens as input (with max n varying from one model to another), the model is able to predict one token as output. This token is then incorporated into the input of the next iteration, in an expanding window pattern, enabling a better user experience of getting one (or multiple) sentence as an answer. This explains why, if you ever played with ChatGPT, you might have noticed that sometimes it looks like it stops in the middle of a sentence. -->
* **출력 토큰 예측**: 주어진 n개의 입력 토큰들에 대해서 모델은 하나의 토큰을 예측하여 출력합니다. 이 토큰은 다음 차례의 입력이 되며, window pattern을 확장시킵니다. 이로서 정답으로 나오는 출력에 대한 더 나은 사용자 경험을 얻게 됩니다. 이것은 ChatGPT와 같은 것을 사용했을 때, 가끔 문장이 완성되지 않고 중간에 멈추는 이유를 설명할 수 있습니다. 

* **Selection process, probability distribution**: The output token is chosen by the model according to its probability of occurring after the current text sequence. This is because the model predicts a probability distribution over all possible ‘next tokens’, calculated based on its training. However, not always the token with the highest probability is chosen from the resulting distribution. A degree of randomness is added to this choice, in a way that the model acts in a non-deterministic fashion - we do not get the exact same output for the same input. This degree of randomness is added to simulate the process of creative thinking and it can be tuned using a model parameter called temperature.
* **선택 절차, 확률분포**: 출력 토큰은 모델에 의해, 나중에 나올 텍스트들의 확률로 인해 결정됩니다. 


## How can our startup leverage Large Language Models?

Now that we have a better understanding of the inner working of a large language model, let’s see some practical examples of the most common tasks they can perform pretty well, with an eye to our business scenario.
We said that the main capability of a Large Language Model is *generating a text from scratch, starting from a textual input, written in natural language*.

But what kind of textual input and output?
The input of a large language model is known as prompt, while the output is known as completion, term that refers to the model mechanism of generating the next token to complete the current input. We are going to dive deep into what is a prompt and how to design it in a way to get the most out of our model. But for now, let’s just say that a prompt may include:

* An **instruction** specifying the type of output we expect from the model. This instruction sometimes might embed some examples or some additional data.

    1. Summarization of an article, book, product reviews and more, along with extraction of insights from unstructured data.
    
    ![Example of summarization](./images/summarization-example.png?WT.mc_id=academic-105485-koreyst)

    <br>
    
    2. Creative ideation and design of an article, an essay, an assignment or more.
    
    ![Example of creative writing](./images/creative-writing-example.png?WT.mc_id=academic-105485-koreyst)

    <br>
    
* A **question**, asked in the form of a conversation with an agent.
  
![Example of conversation](./images/conversation-example.png?WT.mc_id=academic-105485-koreyst)

<br>

* A chunk of **text to complete**, which implicitly is an ask for writing assistance.
   
![Example of text completion](./images/text-completion-example.png?WT.mc_id=academic-105485-koreyst)

<br>

* A chunk of **code** together with the ask of explaining and documenting it, or a comment asking to generate a piece of code performing a specific task.

![Coding example](./images/coding-example.png?WT.mc_id=academic-105485-koreyst)

<br>

The examples above are quite simple and don’t want to be an exhaustive demonstration of Large Language Models capabilities. They just want to show the potential of using generative AI, in particular but not limited to educational context.

Also, the output of a generative AI model is not perfect and sometimes the creativity of the model can work against it, resulting in an output which is a combination of words that the human user can interpret as a mystification of reality, or it can be offensive. Generative AI is not intelligent - at least in the more comprehensive definition of intelligence, including critical and creative reasoning or emotional intelligence; it is not deterministic, and it is not trustworthy, since fabrications, such as erroneous references, content, and statements, may be combined with correct information, and presented in a persuasive and confident manner. In the following lessons, we’ll be dealing with all these limitations and we’ll see what we can do to mitigate them.

## Assignment

Your assignment is to read up more on [generative AI](https://en.wikipedia.org/wiki/Generative_artificial_intelligence?WT.mc_id=academic-105485-koreyst) and try to identify an area where you would add generative AI today that doesn't have it. How would the impact be different from doing it the "old way", can you do something you couldn't before, or are you faster? Write a 300 word summary on what your dream AI startup would look like and include headers like "Problem", "How I would use AI", "Impact" and optionally a business plan. 

If you did this task, you might even be ready to apply to Microsoft's incubator, [Microsoft for Startups Founders Hub](https://www.microsoft.com/startups?WT.mc_id=academic-105485-koreyst) we offer credits for both Azure, OpenAI, mentoring and much more, check it out!

## Knowledge check

What's true about large language models?

1. You get the exact same response every time.
1. It does things perfectly, great at adding numbers, produce working code etc.
1. The response may vary despite using the same prompt. It's also great at giving you a first draft of something, be it text or code. But you need to improve on the results.

A: 3, an LLM is non-deterministic, the response vary, however, you can control its variance via a temperature setting. You also shouldn't expect it to do things perfectly, it's here to do the heavy-lifting for you which often means you get a good first attempt at something that you need to gradually improve.

## Great Work! Continue the Journey 

After completing this lesson, check out our [Generative AI Learning collection](https://aka.ms/genai-collection?WT.mc_id=academic-105485-koreyst) to continue leveling up your Generative AI knowledge!

Head over to Lesson 2 where we will look at how to [explore and compare different LLM types](../02-exploring-and-comparing-different-llms/README.md?WT.mc_id=academic-105485-koreyst)!
