# AI Mood Diary

> 독심술하는 1조
>
> 김용현, 김혜빈, 김희진, 최문선



### final_model.ipynb

전처리 - 모델링 - 시연 전 단계를 포함한 코드입니다.

* package install : 전처리를 위해 필요한 패키지들을 설치하는 코드입니다.

* preprocessing : hanspell과 phkospacing을 활용한 전처리 단계입니다.

  전처리 완료한 파일은 `preprocessing_3emotion_pykospacing.xlsx` 파일로 저장해두었습니다.

* modeling : 전처리가 끝난 `preprocessing_3emotion_pykospacing.xlsx` 파일로 진행합니다.

  원하는 형태로 형태소 분리를 진행하기 위해 `khaiii_tokenized` 함수를 선언하였습니다.

* demo : 시연을 위해 작성한 코드입니다. `KakaoTalk_for_Demo.txt`  파일이 필요합니다. 

  최상단 날짜의 대화만 가져오며 날짜 구분을 위해 하루 대화가 끝나면 '\---------------' 기호가 필요합니다. 대화가 두 줄 이상으로 분리되어 있으면 코드가 동작하지 않을 수 있습니다.

  * `KakaoTalk_for_Demo.txt` 파일은 PC버전 카카오톡에서 대화 내보내기를 진행한 텍스트파일 입니다.

* demo2 : 한 문장씩 분석하기 위한 코드입니다. demo와 동일한 함수`sentiment_predict`를 사용합니다.



### morpheme_analysis_compare.ipynb

mecab와 khaiii 패키지를 비교하기 위해 작성한 코드입니다.

각 패키지로 형태소 분석을 한 후 쉽게 비교하기 위해 형태소 정보를 한글 형태소명으로 변경하여 비교하는 코드입니다.

데이터셋에서 임의로 뽑은 문장들을 담은 `sentence_for_preprocessing_package_choice.txt` 파일이 필요합니다.



### preprocessing_with_hanspell_kospacing.ipynb

다양한 정규표현식을 사용하여 전처리 결과를 비교하기 위해 작성한 코드입니다.

`one_off_conversation_sad.xlsx` 파일과 `one_off_conversation_sad_answer.xlsx` 파일이 필요합니다.

코드 설명은 주석으로 달아두었습니다.