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
金俪人美容馆，一家位于青海海东乐都区的专业美容院，温馨明亮的室内环境，墙上挂着“深耕美业10年”的宣传标语，护理师穿着洁白工服，面带微笑，正在为顾客进行专业的皮肤管理护理，顾客躺在干净舒适的美容床上，盖着柔软毛毯，闭着眼睛享受服务，身旁摆放着精致的护肤产品和仪器设备。背景是干净整洁的店面，玻璃橱窗透出柔和阳光，室内布置典雅温馨，墙面色调柔和，有绿植点缀，营造出放松与疗愈氛围，画面体现“正确护理 · 健康美丽”的理念，拍摄角度像是顾客自拍或朋友拍摄，记录下她享受护理的温暖时刻。
生成图片时生成店铺内容在左上角，第一行字是“金俪人美容馆”，第二行小字是“健康美丽你值得拥有”，只出现文字即可，文字周围不要任何其它小图案。
比例 「9:16」
```

## 主题-视频脚本生成
```text
<主题> 早安心灵鸡汤、人生哲理。<关于视频脚本的要求> 最终生成视频脚本文案结构为早安的问侯鸡汤+最后Slogan。鸡汤字数不要超过50字，鸡汤内容和美容、健康、美丽结合再一起；Slogan为“金俪人美容馆，健康美丽你值得拥有”。
```

```text
<主题> 晚安心灵鸡汤、人生哲理。<关于视频脚本的要求> 最终生成视频脚本文案结构为晚安的问侯鸡汤+最后Slogan。鸡汤字数不要超过50字，鸡汤内容和美容、健康、美丽结合再一起；Slogan为“金俪人美容馆，健康美丽你值得拥有”。
```


## 测试接口
```json
// http://127.0.0.1:8080/api/v1/video
{
    "video_subject": "<主题> 晚安心灵鸡汤、人生哲理。<关于视频脚本的要求> 最终生成视频脚本文案结构为晚安的问侯鸡汤+最后Slogan。鸡汤字数不要超过50字，鸡汤内容和美容、健康、美丽结合再一起；Slogan为“金俪人美容馆，健康美丽你值得拥有”。",
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
            "url": "D:\\workspace\\video\\MoneyPrinterTurbo\\storage\\local_videos\\e3660bea-bb3b-47ce-b096-a18304809f18_屏幕截图 2025-05-25 232836.png",
            "duration": 0
        },
        {
            "provider": "local",
            "url": "D:\\workspace\\video\\MoneyPrinterTurbo\\storage\\local_videos\\64b7804a-7fc6-4acc-91c9-1ae40269204b_屏幕截图 2025-05-25 232849.png",
            "duration": 0
        },
        {
            "provider": "local",
            "url": "D:\\workspace\\video\\MoneyPrinterTurbo\\storage\\local_videos\\73fd281c-565f-4ceb-841e-703864f1ce96_屏幕截图 2025-05-25 232901.png",
            "duration": 0
        },
        {
            "provider": "local",
            "url": "D:\\workspace\\video\\MoneyPrinterTurbo\\storage\\local_videos\\bae89c33-c7e4-4250-b919-a1924c2f826d_屏幕截图 2025-05-25 232914.png",
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


