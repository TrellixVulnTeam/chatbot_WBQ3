# chatbot

Python�汾����̫�£�һЩ�ɰ汾��������������python���°汾��3.6�ȽϺ�
����Ҫ��64λ�ģ�32λ�ڴ���ܲ���

��װspacy��Ҫ�Թ���Ա�������cmd����������ִ������
pip install spacy
python -m spacy download en_core_web_md
https://blog.csdn.net/u012436149/article/details/79321112
��⣺import spacy��import en_core_web_md

��װrasa_nlu�Լ���Ӧ��������
https://github.com/RasaHQ/rasa_nlu
https://stackoverflow.com/questions/46713653/installing-rasa-on-windows
��⣺
�ȿ�¡������git clone https://github.com/RasaHQ/rasa_nlu.git
Ȼ�󿴿��ܲ���˳��������������
from rasa_nlu.training_data import load_data
from rasa_nlu.config import RasaNLUModelConfig
from rasa_nlu.model import Trainer
from rasa_nlu import config
trainer = Trainer(config.load(��D:\\...\\rasa_nlu\\sample_configs\\config_spacy.yml��))
training_data = load_data(��D:\\...\\rasa_nlu\\data\\examples\\rasa\\demo-rasa.json��)
interpreter = trainer.train(training_data)
�����Ӣ�İ����죬����͹��ˣ�ֻ��Ҫ�Լ���дһ���Լ�ר�õ�.json�ļ��Ϳ�����

���������İ棺
��װjieba

��װcmake��mitie��git����Ҫ��gitbash�������У�cmd�޷����У�
https://blog.csdn.net/m0_37407756/article/details/79790417
https://blog.csdn.net/ld326/article/details/80965689

����total_word_feature_extractor_zh.dat��total_word_feature_extractor_chi.dat�����Ǹ�300���׵�ѵ������������ַ�����ᵽ�İٶ�����������
http://www.crownpku.com/2017/07/27/��Rasa_NLU�����Լ�������NLUϵͳ.html

clone rasa_nlu_chi�����������Ǹ���ַ

��rasa_nlu_chi ��sample_configs�ļ��У��ҵ�config_jieba_mitie_sklearn.yml��������model��������ݸĳ�300����.dat�ļ�����ϸ·�����磺
"D:/EE/data/total_word_feature_extractor_zh.dat"

�Լ���д.jsonѵ������
