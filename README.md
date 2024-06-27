# Week 3   
參考方法一[Stable Diffusion -- 訓練LoRA](https://vocus.cc/article/642db062fd897800014596ad)及方法二[【Stable Diffusion教學】如何訓練自己的LoRA模型？](https://makerpro.cc/2023/04/how-to-train-your-own-lora-model/)

  
## 準備image  
* 選擇五張狗的照片，裁切為像素 512 x 512，用來生成狗的LoRA模型
  
## LoRA訓練  
### 方法一
* 根據[simple_lora_trainer.ipynb](https://colab.research.google.com/drive/1zsk_LvYyjRilfHauGZ-6_ybuTYgWh_6P#scrollTo=gc6pUTSo6fnI&uniqifier=1)給的空格填入需求，
* 搭配適配的StableDiffusion 模型，到 civitai搜尋，這裡用 [AnyLoRA – Checkpoint](https://civitai.com/models/23900/anylora) 複製網址連結，貼到 model_url，並將sd模型名稱，貼到model_name。
<img width="1470" alt="image" src="https://github.com/mvclab-ntust-course/course3-siouyin/assets/167956367/2ed34e35-95b4-46aa-b124-d97d094124bc">
* 在雲端硬碟建立一個和LoRA模型同名的資料夾後，將訓練素材複製到此路徑。
<img width="1123" alt="image" src="https://github.com/mvclab-ntust-course/course3-siouyin/assets/167956367/b2e7f72a-3d83-4145-80f1-cc28dbaf9c82">
<img width="1053" alt="image" src="https://github.com/mvclab-ntust-course/course3-siouyin/assets/167956367/d72bbdaf-22e3-4d15-9530-8b60ea2e00d6">

### 方法二
* 根據[Lora Trainer](https://colab.research.google.com/drive/1ndFvX7KRk71ckyWyZCv4OIbUPOpfbMJy#scrollTo=vJ8clWTZEu-g) 給的空格填入需求
* result:require GPU,未train成功
<img width="892" alt="image" src="https://github.com/mvclab-ntust-course/course3-siouyin/assets/167956367/02e113de-ce66-4b68-8536-228bc314a8fa">

## 將LoRA模型加入Stable Diffusion  
* 輸入以下指令安裝stable-diffusion-webui  
  ```  
  git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git  
  ```  
* 將我們訓練的模型放入到`stable-diffusion-webui\models\Lora`的資料夾中，選擇我們的模型 
