# Sistema de reconhecimento facial e identificação de vítmas de catástrofes de grandes proporções.
# Facial recognition system for large-scale catastrophes

Objetivo:

- O propósito desta aplicação é fornecer uma plataforma e uma interface de análise de imagens que proporcione o treinamento e uso de um modelo de reconhecimento facial para ser aplicado sobre imagens das vítimas em vida e as imagens dos corpos encontrados na tragédia.

- O projeto objetiva somente um meio de ajudar e auxiliar e adiantar o procesos de identificação dos corpos e trazer o mínimo de alento as famílias e amigos das vítiamas.


- Ajude Brumadinho doando pelo Banco do Brasil
[Ajude Brumadinho Banco do Brasil Conta Oficial](https://www.bb.com.br/pbb/pagina-inicial/ajude-brumadinho)

- Este projeto é um fork do projeto: [FaceID](https://github.com/chaos4455/faceID) , porém com objetivo de conter melhorias e adequações para o uso em caso específico.

Ajude Brumadinho
Você pode ajudar os moradores de Brumadinho realizando doações na conta exclusiva para esse fim.

 Juntos podemos ajudar diversas pessoas em estado de necessidade.
Faça sua contribuição para quem mais precisa.

Agência: 1669-1 (Brumadinho)
Conta-Corrente: 200-3 (SOS Brumadinho)
CNPJ: 18.363.929/0001-40

- Contato para ajudar com o projeto: oeliasandrade@gmail.com

![](http://img1-azrcdn.newser.com/image/1220280-0-20190128092544.jpeg)


- Updates:

30/01/2019 15:57

Recebido retorno e reposta sobre encaminhamento da mensagem aos responsáveis pelos trabalhos.


30/01/2019 01:06

Enviado E-mail ofertando o uso da ferramenta pra a chefe do gabinete de crise geral da Pc de MG.



# Informações técnicas


## Requisitos
- Ubuntu 16.04
- Python 3.5
- OpenCV
- Keras
- TensorFlow(backend)


## Getting Started
Criando virtualenv
```bash
$ cd FRSFLSC
$ virtualenv env --python=python3.5
$ source env/bin/activate
```

Instalando dependências 
```bash
$ pip install -r requirements.txt
```

Executando
```bash
$ python main.py
```

#### Como se usa?
```python
import dlib, cv2

fileName = 'rosto.jpg'
img = cv2.imread(fileName)
predictorPath = 'face_detection/shape_predictor_68_face_landmarks.dat'

detector = dlib.get_frontal_face_detector()
predictor = dlib.shape_predictor(predictorPath)
dets = detector(img, 1)

print("Number of faces detected: {}".format(len(dets)))
for i, d in enumerate(dets):
    print("Detection {}: Left: {} Top: {} Right: {} Bottom: {}".format(
        i, d.left(), d.top(), d.right(), d.bottom()))
    shape = predictor(img, d)
    print("Part 0: {}, Part 1: {} ...".format(shape.part(0),
                                              shape.part(1)))
```


## Reconhecimento Facial 
- Implementação do modelo CNN em Python3, Keras(Tensorflow backend)

