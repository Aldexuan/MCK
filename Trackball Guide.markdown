---
layout: default
title: Trackball Guide
permalink: /Trackball Guide/
has_children: false
nav_order: 4
---
## 请认真看完玩法说明，关于轨迹球所有的用法都在这里，建议把这里从头到尾都看完

### 注意:
* 连接电脑的数据线要插在右手有轨迹球的那一侧<br/>
<br/>
* v1版本 trs音频线连接：拔插中间的连接线需要先把连接电脑的数据线拔掉，不要带电拔插，不管是插上还是拔掉，都要在数据线没有连接电脑的情况下，因为带电拔插会打坏主控,导致一半的键盘不能使用<br/>
<br/>
* v2版本采用ctc数据线连接，支持带电拔插中间连接线，解决v1版本出现的问题，pcb现在已全部升级v2版本<br/>

## Trackball键盘轨迹球有17个关于轨迹球的自定义按键
key_code:<br/>
![key_code](/static/trackball/key_code.jpeg){: width="100%" }<br/>

## 一：鼠标模式(就是正常的鼠标移动，只能移动，其他操作切换到其他模式即可)：
* 16 个加减阶梯，以 200 DPI 为增量， DPI的意思光标移动的速度，数字越大越快<br/>

* 总范围从 400 到 3,400 (400 → 600 → 800 → … → 3,400) 循环<br/>

* DPI+:鼠标模式下可以对dpi进行加操作<br/>

* DPI-:鼠标模式下可以对dpi进行减操作<br/>

## 二：阻击模式(以很低的dpi进行移动，这个模式主要是为了防止频繁切换dpi,如果需要光标速度降低，可以直接切换到这个模式就行，这样不用一直在鼠标模式，频繁调dpi):
* 适合比较慢的操作，切换到这个模式就不需要在鼠标模式下切换dpi，需要鼠标慢点的操作直接切换到这个模式就行<br/>
操作完，再切回鼠标模式，这样很方便不需要单纯的在鼠标模式下一直切换不同的dpi<br/>
* 4 个加减阶梯,以 100 DPI 为增量<br/>

* 总范围从 200 到 500（200 → 300 → 400 → 500）循环<br/>
 
* Snp：长按这个按键进入阻击模式，松开变回鼠标模式，该按键需要长按才能触发，需要一直按这个键才行，才能以阻击模式的低dpi进行移动鼠标<br/>

* SnpT：单击进入阻击模式，这个按键和上面的区别是，不需要长按，按一下就可以进入阻击模式，需要你使用完阻击模式后，再按一下返回鼠标模式<br/>

* 5.Snp+：单独增加阻击模式的dpi，不会干扰到鼠标模式下的dpi<br/>

* Snp-: 单独减少阻击模式的dpi，不会干扰到鼠标模式下的dpi<br/>

## 三：滚动模式(相当于正常鼠标中间那个滚轮，支持水平滚动以及垂直滚动)
* 5个加减阶梯,以 100 DPI 为增量<br/>

* 总范围从 100 到 5000（100 → 200 → 300→ 400→ 500）循环<br/>

* Drg: 长按这个按键进入滚动模式，松开变回鼠标模式，该按键需要长按才能触发，需要一直按这个键才行<br/>

* DrgT：单击进入滚动模式，这个按键和上面的区别是，不需要长按，按一下就可以进入滚动模式，再按一下返回鼠标模式<br/>

* Drg+:单独增加滚动模式的dpi，不会干扰到鼠标模式下的dpi<br/>

* .Drg-:单独减少阻击模式的dpi，不会干扰到鼠标模式下的dpi<br/>


## 四：自动切层(Automatic Mouse Layer):
* 鼠标层在最后一层，在vial里面标数字 5 的那一层就是鼠标层，自动切层：滚动轨迹球把当前层切到鼠标层<br/>

* 注意:如果本身就是新手，甚至连vial都还没玩熟，我个人建议先别开自动切层，如果说自己已经玩的很熟了，需要自动切层，可以打开<br/>

* 该功能可以开启和关闭，看个人喜好，不适应的可以自己关闭<br/>

* ATG：开启和关闭自动切层功能，按一下打开，再按一下关闭<br/>

* 自动切层相关参数设置说明：<br/>
* * 设置时，可以使用 TIinfo 按键来看实时设置的参数（这个按键的说明在最后）<br/>
* * 5-1：A50：自动切层停留时间，每次增加50毫秒，增加超过3000毫秒自动从0开始，时间范围是0-3000毫秒<br/>
* * A50-：自动切层停留时间，每次减小50毫秒，减小超过0毫秒循环到3000，时间范围是0-3000毫秒<br/>
* * A100：自动切层停留时间，每次增加100毫秒，增加超过3000毫秒自动从0开始，时间范围是0-3000毫秒<br/>

* * ATV：调节轨迹球滚动触发阈值，这个是调节滚动轨迹球幅度触发自动切层的，数字从0-7，数字越小越灵敏，简单来说，0代表碰一下轨迹球就能触发自动切层，7代表大幅度滚动轨迹球才能触发自动切层，这个可以根据个人习惯调节，每按下一次增加1<br/>

* T_SAVE: 设置好自动切层的超时时间和滚动触发阈值参数后，按下这个键，就能保存设置到主控里面，这样即使键盘断电重插，设置的记录也会正常存在，
之所以不设置自动保存，是因为这个需要调节的自动保存会频繁刷写eeprom 对主控不好，只需要自己调节好参数最终统一进行保存就行，避免重复刷写主控的eeprom
注意，这个按键只是保存自动切层的设置的，不会保存整个键盘的所有设置，不会保存键盘键位设计等



## 五：鼠标相关设置信息OLED显示
default画面:<br/>                                                 
![oled1](/static/trackball/oled1.jpeg){: width="100%" }<br/> 
* 默认OLED显示是上图这种，主手是右边Bongo Cat，会根据打字速度变化形态，副手是左边最上边是键盘名称，中间是修饰键状态，按下对应修饰键会变色，再下面会显示当前切的层，如果开始自动切层功能，滚动轨迹球这个会自动变为 mouse层，停止滚动会变化原来所在的层。最后是Luna小狗<br/>

* TIinfo:鼠标当前设置参数的显示开关，按下按键可以在右手主图显示当前鼠标的各项参数，下面是相关画面：<br/>
TIinfo画面:<br/>
![oled](/static/trackball/oled.jpeg){: width="100%" }<br/>
* * AutoL: 0或者1，代表关闭和开启自动切层<br/>
* * M-DPI：代表鼠标模式的当前dpi<br/>
* * ATV: 显示的就是轨迹球触发灵敏度阈值，也就是通过 ATV 设置的值<br/>
* * AUTO-MS：显示的就是轨迹球切层超时时间，也就是通过 A50, A50-, A100 设置的值<br/>
* * SNP-T：0或者1，代表关闭和开启阻击模式<br/>
* * SNP-DPI：代表当前阻击模式的dpi<br/>
* * DRG-T：0或者1，代表关闭和开启滚动模式<br/>
* * DRG-DPI：代表当前滚动模式的dpi<br/>

