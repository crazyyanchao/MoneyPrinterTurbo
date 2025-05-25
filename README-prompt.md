# 主题“浪山鲜食汇”视频生成

## 基础参数设置
```text
1、素材图片 9：16
2、生成图片时logo在左上角，logo样式要统一
3、大模型生成文案的模板，文案结构（早安或者晚安的问侯鸡汤、最后Slogan）
	鸡汤：字数不要超过50字，鸡汤内容和饮食餐饮结合在一起，人生心灵鸡汤、和中国饮食文化结合在一起
	Slogan：浪山鲜食汇，火锅烧烤一站购齐，聚会、浪山就找浪山鲜食汇
4、语速现有的1.2倍速
5、语音模型：siliconflow:FunAudioLLM/CosyVoice2-0.5B:anna-女性
6、字幕需要配置：自定义位置（70，表示离顶部70%的位置）
7、字体：MicrosoftYaHeiBold.ttc
```

## 主题-图片生成
```text
一大家子人围坐在城市郊区自家院子里，地上铺着野餐垫，阳光温暖，绿草如茵，孩子在一旁奔跑玩耍，大人围在简易的户外桌旁，开心地吃着热腾腾的火锅和滋滋作响的烧烤，桌上摆满“浪山鲜食汇”的火锅食材：整齐摆盘的牛肉卷、羊肉卷、鲜亮的大虾、各类火锅丸子和新鲜蔬菜，还有烧烤用的串串和调料包；一旁是冰镇饮品和小吃，空气中弥漫着食材香气和欢笑声，画面温馨真实，体现“浪山鲜食汇，火锅烧烤一站购齐”，适合家庭聚会、露营、庭院小聚使用，自拍视角或远景记录，全景镜头，夏日傍晚自然光。
生成图片时生成店铺内容在左上角，第一行字是“浪山鲜食汇”，第二行小字是“火锅烧烤一站购齐”，只出现文字即可，文字周围不要任何其它小图案。
比例 「9:16」
```

## 主题-视频脚本生成
```text
<主题> 早安心灵鸡汤、人生哲理。<关于视频脚本的要求> 最终生成视频脚本文案结构为早安的问侯鸡汤+最后Slogan。鸡汤字数不要超过50字，鸡汤内容和饮食餐饮结合在一起，人生心灵鸡汤、和中国饮食文化结合在一起；Slogan为“浪山鲜食汇，火锅烧烤一站购齐，聚会、浪山就找浪山鲜食汇”。
```

```text
<主题> 晚安心灵鸡汤、人生哲理。<关于视频脚本的要求> 最终生成视频脚本文案结构为晚安的问侯鸡汤+最后Slogan。鸡汤字数不要超过50字，鸡汤内容和饮食餐饮结合在一起，人生心灵鸡汤、和中国饮食文化结合在一起；Slogan为“浪山鲜食汇，火锅烧烤一站购齐，聚会、浪山就找浪山鲜食汇”。
```

## 测试接口
```json
// http://127.0.0.1:8080/api/v1/video
{
    "video_subject": "<主题> 早安心灵鸡汤、人生哲理。<关于视频脚本的要求> 最终生成视频脚本文案结构为早安的问侯鸡汤+最后Slogan。鸡汤字数不要超过50字，鸡汤内容和饮食餐饮结合在一起，人生心灵鸡汤、和中国饮食文化结合在一起；Slogan为“浪山鲜食汇，火锅烧烤一站购齐，聚会、浪山就找浪山鲜食汇”。",
    "video_script": "",
    "video_terms": "",
    "video_aspect": "9:16",
    "video_concat_mode": "random",
    "video_transition_mode": "None",
    "video_clip_duration": 3,
    "video_count": 1,
    "video_source": "local",
    "video_materials": [
        {
            "provider": "local",
            "url": "D:\\workspace\\video\\MoneyPrinterTurbo\\storage\\local_videos\\45a28198-a870-4bed-93e7-a3dd5f50d6a6_屏幕截图 2025-05-25 224437.png",
            "duration": 0
        },
        {
            "provider": "local",
            "url": "D:\\workspace\\video\\MoneyPrinterTurbo\\storage\\local_videos\\91643bcb-bb38-40e2-83a2-290acb39068d_屏幕截图 2025-05-25 224515.png",
            "duration": 0
        },
        {
            "provider": "local",
            "url": "D:\\workspace\\video\\MoneyPrinterTurbo\\storage\\local_videos\\e76bfae2-76a6-4c1d-a6ab-869bc87e6c7f_屏幕截图 2025-05-25 224528.png",
            "duration": 0
        },
        {
            "provider": "local",
            "url": "D:\\workspace\\video\\MoneyPrinterTurbo\\storage\\local_videos\\0e38327d-3c88-4d8d-9ede-33e23696508c_屏幕截图 2025-05-25 224540.png",
            "duration": 0
        }
    ],
    "video_language": "",
    "voice_name": "siliconflow:FunAudioLLM/CosyVoice2-0.5B:anna-Female",
    "voice_volume": 2.0,
    "voice_rate": 1.2,
    "bgm_type": "random",
    "bgm_file": "",
    "bgm_volume": 0.2,
    "subtitle_enabled": true,
    "subtitle_position": "custom",
    "custom_position": 70.0,
    "font_name": "MicrosoftYaHeiBold.ttc",
    "text_fore_color": "#FFFFFF",
    "text_background_color": true,
    "font_size": 60,
    "stroke_color": "#000000",
    "stroke_width": 1.5,
    "n_threads": 2,
    "paragraph_number": 1
}
```


