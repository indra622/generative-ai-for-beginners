<!-- # Getting Started with this course -->
# 과정 시작하기

<!-- We are very excited for you to start this course and see what you get inspired to build with Generative AI! -->
저희는 독자들이 이 과정을 시작해서 생성형 AI에 대한 어떤 영감을 얻기를 바랍니다.

<!-- To make your time successful, we have created this page that outlines any setup steps, technical requirements, and how to get help when you need it. -->
성공적인 과정 실습을 위해, 저희는 여기에 설치, 기술적 배경지식에 대한 개요와 함께 도움이 될만한 내용을 넣었습니다.

<!-- ## Setup Steps -->
## 설치 과정

<!-- To start taking this course, you will need to complete the following steps. -->
이 과정을 시작하기 위해서 아래 과정을 완료해야 합니다.

<!-- ### 1. Fork this Repo -->
### 1. 레포지토리를 fork하세요

<!-- [Fork this entire repo](https://github.com/microsoft/generative-ai-for-beginners/fork?WT.mc_id=academic-105485-koreyst) to your own GitHub account to be able to change any code and complete the challenges. You can also [star (🌟) this repo](https://docs.github.com/en/get-started/exploring-projects-on-github/saving-repositories-with-stars?WT.mc_id=academic-105485-koreyst) to find it and related repos easier. -->

이 레포지토리 전체를 자신의 GitHub 계정에 포크하면 (필요 시) 코드를 변경하면서 실습을 진행할 수 있습니다. 그리고 star를 눌러 주시면 관련된 저장소를 더 쉽게 찾을 수 있습니다.

<!-- ### 2. Create a codespace -->
### 2. 코드스페이스를 만드세요

<!-- To avoid any dependency issues when running the code, we recommend running this course in a GitHub codespace. -->
의존성 문제를 피하기 위해서 Github 코드스페이스에서 작업하는 것을 추천합니다.

<!-- This can be created by selecting the `Code` option on your forked version of this repo and selecting the **Codespaces** option. -->
포크한 레포에서 'Code' 옵션을 설정해서 만들고 'Codespaces'옵션을 선택하세요.

<!-- ### 3. Storing Your API Keys -->
### 3. 당신의 API 키를 저장하세요

<!-- Keeping your API keys safe and secure is important when building any type of application. We encourage you not to store any API keys directly in the code you are working with as committing those details to a public repository could result in unwanted costs and issues. -->
당신의 API키를 안전하게 보관하세요. 보안은 어떤 application을 구축할때도 중요한 요소입니다. 예기치못한 비용이나 다른 문제가 발생하지 않도록 API 키를 공용 레포지토리에 있는 코드에 바로 기입해 놓지 마세요.

![Dialog showing buttons to create a codespace](./images/who-will-pay.webp)

<!-- ## How to Run locally on your computer -->
## 로컬에서 실행시키는 방법

<!-- To run the code locally on your computer, you would need to have some version of [Python installed](https://www.python.org/downloads/?WT.mc_id=academic-105485-koreyst). -->

로컬에서 실행시키고자 한다면 특정 버전의 [python](https://www.python.org/downloads/)이 설치되어 있어야 합니다.


<!-- To then use the repository, you need to clone it: -->
그 이후에 레포지토리를 사용하기 위해서 clone을 할 필요가 있습니다.

```shell
git clone https://github.com/microsoft/generative-ai-for-beginners
cd generative-ai-for-beginners
```

<!-- Now you have everything checked out and can start learning and work with the code. -->
이제 코드를 실행하며 학습할 수 있게 되었습니다!

<!-- ### Installing miniconda (optional step) -->
### miniconda 설치 (선택사항)

<!-- There are advantages to installing  **[miniconda](https://conda.io/en/latest/miniconda.html?WT.mc_id=academic-105485-koreyst)** - it is rather lightweight installation that supports `conda` package manager for different Python **virtual environments**. `conda` makes it easy to install and switch between different Python versions and packages, and also to install packages that are not available via `pip`. -->
miniconda를 설치할 때 장점은 다음과 같습니다. 서로 다른 가상 환경(virtual environments)의 python을 사용할 수 있는 `conda`를 사용하는 경량화 버전입니다. `conda`는 쉽게 설치가 가능하고 서로 다른 python 버전을 사용 가능하며, `pip`에서 사용 불가능한 패키지를 설치할 수 있습니다.

<!-- After you install miniconda, you need to clone the repository (if you haven't already done so) and create a virtual environment to be used for this course: -->
miniconda를 설치한 후에, 이 강의 코스를 위한 가상 환경을 만들 필요가 있습니다.

<!-- Before running the below step, ensure that you first have an *environment.yml* file. The *environment.yml* file is used to create a conda environment with the necessary dependencies and can look like so: -->
다음 단계로 넘어가기 전에, 먼저 environment.yml 파일을 정의해야 합니다. 이 파일은 필요한 패키지들을 미리 가진 conda환경을 만드는 데 사용됩니다.

```yml
name: <environment-name>
channels:  
 - defaults
dependencies:  
- python=<python-version>  
- openai  
- python-dotenv
```

<!-- You can replace `<environment-name>` with the name of your conda environment, and `<python-version>` with the version of Python you want to use. Place your created *environment.yml* file in the *.devcontainer* folder of your repo. -->
`<environment-name>`은 conda environment의 이름을 입력하면 되고, `<python-version>` 에는 사용하고자 하는 python version을 넣으면 됩니다. *environment.yml*파일은 레포지토리에 이미 만들어져 있는 *.devcontainer*에 넣으시면 됩니다.

<!-- Now that you've hopefully created a *environment.yml* file, you can create a conda environment with the following command: -->
이제 *environment.yml* 파일이 만들어졌다면, conda environment를 아래 명령어를 통해 만들어 봅시다.


```bash
conda env create --name ai4beg --file .devcontainer/environment.yml
conda activate ai4beg
```

<!-- Refer to this link on creating a [conda environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html?WT.mc_id=academic-105485-koreyst) if you run into trouble. -->
하다가 문제가 생겼다면 [conda environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) 를 참고하세요.


<!-- ### Using Visual Studio Code with Python Extension -->
### Visual Studio Code의 Python Extension 사용하기

<!-- Probably the best way to use the curriculum is to open it in [Visual Studio Code](http://code.visualstudio.com/?WT.mc_id=academic-105485-koreyst) with [Python Extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python&WT.mc_id=academic-105485-koreyst). -->
아마 이 커리큘럼은 [Visual Studio Code](http://code.visualstudio.com/)의 [Python Extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python)을 사용하는게 가장 좋은 방법일 것입니다.

<!-- > **Note**: Once you clone and open the directory in VS Code, it will automatically suggest you to install Python extensions. You would also have to install miniconda as described above. -->
> **Note**: 일단 VSCode로 레포지토리를 열면, 자동으로 Python extension들이 설치될 겁니다. 또한 위에 설명했던 miniconda를 설치했어야 합니다.

<!-- > **Note**: If VS Code suggests you to re-open the repository in container, you need to decline this to use local Python installation.  -->
> **Note**: 만일 VSCode가 컨테이너에서 레포지토리를 다시 열라고 한다면, 로컬에 설치된 python을 사용하기 위해 거절해야 합니다.

<!-- ### Using Jupyter in the Browser -->
### 브라우저에서 Jupyter 사용하기

<!-- You can also use Jupyter environment right from the browser on your own computer. Actually, both classical Jupyter and Jupyer Hub provide quite convenient development environment with auto-completion, code highlighting, etc. -->
컴퓨터 브라우저에서 바로 Jupyter 환경을 사용할 수 있습니다. 사실, 클래식한 Jupyter와 Jupyter Hub 모두 상당히 편리한 개발 환경(ex> 자동완성, 코드 하이라이팅 등)을 제공합니다.

<!-- To start Jupyter locally, go to the directory of the course, and execute: -->
Jupyter를 로컬에서 시작하기 위해서는 디렉토리로 이동한다음에 아래를 실행시키시면 됩니다.


```bash
jupyter notebook
```

or

```bash
jupyterhub
```

<!-- You then can navigate to any of the `.ipynb` files, open them and start working. -->
그리고 나서 `.ipynb`파일을 하나 만들어서 열고 작업하시면 됩니다.

<!-- ### Running in container -->
### 컨테이너에서 실행시키기

<!-- An alternative to Python installation would be to run the code in container. Since our repository contains special `.devcontainer` folder that instructs how to build a container for this repo, VS Code would offer you to re-open the code in container. This will require Docker installation, and also would be more complex, so we recommend this to more experienced users. -->
Python 설치의 대안으로 container에서 코드를 실행시킬수도 있습니다. 레포지토리가 `.devcontainer` 폴더를 가지고 있고, 이것이 이 레포지토리에서 컨테이너를 어떻게 만들 수 있는지 안내해줍니다. VSCode는 컨테이너에서 코드를 다시 열 수 있는 기능을 제공할 겁니다. Docker설치가 필요할 것입니다. 이 과정은 좀 더 복잡하기 때문에, 어느 정도 숙련된 사용자가 이 과정을 수행하는 것을 추천합니다.

<!-- One of the best ways to keep your API keys secure when using GitHub Codespaces is by using Codespace Secrets. Please follow this guide on how to [manage secrets for your codespaces](https://docs.github.com/en/codespaces/managing-your-codespaces/managing-secrets-for-your-codespaces?WT.mc_id=academic-105485-koreyst). -->
GitHub Codespaces를 사용하면서 당신의 API 키들을 안전하게 보관하는 가장 좋은 방법은 Codespace Secretes를 사용하는 방법입니다. [Codespace에 대한 보안 관리 가이드](https://docs.github.com/en/codespaces/managing-your-codespaces/managing-secrets-for-your-codespaces)를 참고하세요.

<!-- ## Lessons and Technical Requirements -->
## 수업 소개 및 준비물

<!-- The course has 6 concept lessons and 6 coding lessons. -->
이 코스는 6개의 컨셉 레슨과 6개의 코딩 레슨으로 이루어져 있습니다.

<!-- For the coding lessons, we are using the Azure OpenAI Service. You will need access to the Azure OpenAI service and an API key to run this code. You can apply to get access by [completing this application](https://azure.microsoft.com/products/ai-services/openai-service?WT.mc_id=academic-105485-koreyst). -->
코딩 레슨은 Azure OpenAI Service를 사용합니다. 학습자는 Azure OpenAI service를 사용할 수 있어야 하고 API key를 사용해서 코드를 실행시킬 수 있어야 합니다. [여기](https://azure.microsoft.com/products/ai-services/openai-service)에서 등록할 수 있습니다.

<!-- While you wait for your application to be processed, each coding lesson also includes a `README.md` file where you can view the code and outputs. -->
어플리케이션이 실행되는걸 기다리는 동안에, 각 코딩 레슨에 포함된 `README.md` 파일을 통해 코드와 예상 출력을 볼 수 있습니다.

<!-- ## Using the Azure OpenAI Service for the First Time -->
## 처음으로 Azure OpenAI Service를 사용하기

<!-- If this is your first time working with the Azure OpenAI service, please follow this guide on how to [create and deploy an Azure OpenAI Service resource.](https://learn.microsoft.com/azure/ai-services/openai/how-to/create-resource?pivots=web-portal&WT.mc_id=academic-105485-koreyst) -->
Azure OpenAI service를 처음 동작시켜본다면, [Azure OpenAI service 리소스 생성 및 배포](https://learn.microsoft.com/azure/ai-services/openai/how-to/create-resource?pivots=web-portal)를 참고하세요.

<!-- ## Meet Other Learners -->
## 다른 학습자들 만나기

<!-- We have created channels in our official [AI Community Discord server](https://aka.ms/genai-discord?WT.mc_id=academic-105485-koreyst) for meeting other learners. This is a great way to network with other like-minded entrepreneurs, builders, students, and anyone looking to level up in Generative AI. -->
공식 [AI Community Discord server](https://aka.ms/genai-discord)를 통해 다른 학습자들을 만나보세요. 기업가, 개발자, 학생 그리고 생성형AI 수준을 높이고 싶은 여러 다른 사람들과 소통할 수 있는 좋은 방법입니다.

[![Discord 채널 참여](https://dcbadge.vercel.app/api/server/ByRwuEEgH4)](https://aka.ms/genai-discord)

<!-- The project team will also be on this Discord server to help any learners. -->
이 프로젝트 팀은 Discord 서버에 있으면서 학습자들에게 도움을 줄 겁니다.

<!-- ## Contribute -->
## 이 프로젝트에 기여

<!-- This course is an open-source initiative. If you see areas of improvement or issues, please create a [Pull Request](https://github.com/microsoft/generative-ai-for-beginners/pulls?WT.mc_id=academic-105485-koreyst) or log a [GitHub issue](https://github.com/microsoft/generative-ai-for-beginners/issues?WT.mc_id=academic-105485-koreyst). -->
이 과정은 오픈소스로 계획되었습니다. 개선 방안이나 이슈가 있다면, [Pull Request](https://github.com/microsoft/generative-ai-for-beginners/pulls)를 생성하거나 [GitHub issue](https://github.com/microsoft/generative-ai-for-beginners/issues)를 남겨주세요.

<!-- The project team will be tracking all contributions and contributing to open source is an amazing way to build your career in Generative AI. -->
이 프로젝트 팀은 모든 기여 사항을 추적하고 있으며, 오픈소스에 기여하는 것은 당신의 생성형 AI 커리어를 만드는 훌륭한 방법입니다.

<!-- Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution. For details, visit [CLA, Contributor License Agreement website](https://cla.microsoft.com?WT.mc_id=academic-105485-koreyst). -->
대부분의 기여들은 Contributor License Agreement (CLA)에 동의 하는것으로 간주하며, 이 권리를 지킵니다. 자세한 내용은 [CLA, Contributor License Agreement website](https://cla.microsoft.com)를 방문해서 확인 바랍니다.

<!-- Important: when translating text in this repo, please ensure that you do not use machine translation. We will verify translations via the community, so please only volunteer for translations in languages where you are proficient. -->
중요: 이 repo의 내용을 번역할때는 기계 번역을 사용하지 말아주세요. 우리는 커뮤니티를 통해 번역을 점검할 것이니, 언어 번역에 자원봉사로 참여해주세요.

<!-- When you submit a pull request, a CLA-bot will automatically determine whether you need to provide a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions provided by the bot. You will only need to do this once across all repositories using our CLA. -->
pull request를 올릴땐, CLA-bot이 자동으로 CLA를 적용하고 PR을 적절히 다듬을 필요가 있는지 결정할 것입니다. 단순히 bot의 안내를 따라 주세요. CLA를 사용하는 모든 저장소 통틀어 한번만 하면 됩니다.

<!-- This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/?WT.mc_id=academic-105485-koreyst). For more information read the Code of Conduct FAQ or contact [Email opencode](opencode@microsoft.com) with any additional questions or comments. -->
이 프로젝트는 [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)를 채택했습니다. 더 자세한 정보는 Code of Conduct FAQ or contact [Email opencode](opencode@microsoft.com)를 통해 추가적인 질문이나 코멘트 남겨주세요.

<!-- ## Let's Get Started -->
## 시작해봅시다

<!-- Now that you have completed the needed steps to complete this course, let's get started by getting an [introduction to Generative AI and LLMs](../01-introduction-to-genai/README.md?WT.mc_id=academic-105485-koreyst). -->
이제 이 수업들을 완료하기 위해 필요한 과정을 마쳤습니다. [Introduction to Generative AI and LLMs](../01-introduction-to-genai/README.md)로 이동합시다.
