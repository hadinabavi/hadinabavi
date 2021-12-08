
from kivy.app import App
from kivy.uix.floatlayout import FloatLayout
from kivy.uix.slider import Slider
from kivy.graphics import Color, Bezier, Line
from kivy.uix.button import Button
from kivy.uix.textinput import TextInput
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.floatlayout import FloatLayout
from kivy.uix.label import Label
from kivy.graphics import Rectangle, Color
import arabic_reshaper
from bidi.algorithm import get_display



class amlakiyan(App):
    def build(self):
        box = FloatLayout()
        with box.canvas:
            Rectangle(source="G:\\python\\asd.png",size=(200,200),pos=(0,0))
        boxx = BoxLayout(width=200,height=50,size_hint=(None, None))
        with boxx.canvas:
             Rectangle(source="G:\python\Capture.PNG",size=(250,200),pos=(720,455))
        boxxx = BoxLayout(width=200,height=50,size_hint=(None, None))
        with boxxx.canvas:
            Rectangle(source="G:\\python\\asd.png",size=(200,200),pos=(1450,700))
        box.add_widget(boxxx)
        #boxxxx = BoxLayout(width=200,height=50,size_hint=(None, None))
        #with boxxxx.canvas:
            #Rectangle(source="D://P_pngfa_ir_t1_5f4629383f6ac_1.png",size=(200,200),pos=(200,700))
        #box.add_widget(boxxxx)
        boxxxxx = BoxLayout(width=200,height=50,size_hint=(None, None))
        with boxxxxx.canvas:
            Rectangle(source="G:\\python\\ax.png",size=(300,300),pos=(700,630))
        box.add_widget(boxxxxx)
        #textinput = TextInput(width=200,height=50,size_hint=(None, None),pos=(850,698),text='user name', multiline=False)
        def on_focus(instance, value):
            instance.text = ""
        #box.add_widget(textinput)
        #textinput.bind(focus=on_focus)
        textinput = TextInput(width=200,height=50,size_hint=(None, None),pos=(740,230),text='', multiline=False)
        box.add_widget(textinput)
        #kjkjkjjk = TextInput(width=200,height=50,size_hint=(None, None),pos=(850,898),text='phone number', multiline=False)
        #textinput.bind(focus=on_focus)
        reshaped_text = arabic_reshaper.reshape('ثبت')
        bidi_textttttt = get_display(reshaped_text)
        button = Button(size_hint=(None, None),pos=(790,100),text=bidi_textttttt,font_name="C:\\Users\\Jannesari\\Downloads\\2 Titr Bold.ttf")
        box.add_widget(button)
        #hhhh = TextInput(width=200,height=50,size_hint=(None, None),pos=(850,298),text='repasword', multiline=False)
        reshaped_text = arabic_reshaper.reshape('محله')
        bidi_texttt = get_display(reshaped_text)
        h = Label(text=bidi_texttt,font_name="C:\\Users\\Jannesari\\Downloads\\2 Titr Bold.ttf",pos=(120,325))   
        #box.add_widget(hhhh)
        #box.add_widget(kjkjkjjk)
        boxxxxxx = BoxLayout(width=200,height=50,size_hint=(None, None))
        with boxxxxxx.canvas:
            Rectangle(source="G:\\python\\ax.png",size=(300,300),pos=(700,550))
        box.add_widget(boxxxxxx)
        reshaped_text = arabic_reshaper.reshape('شهر')
        bidi_textt = get_display(reshaped_text)
        k = Label(text=bidi_textt,font_name="C:\\Users\\Jannesari\\Downloads\\2 Titr Bold.ttf",pos=(120,400))
        box.add_widget(h)
        box.add_widget(k)
        reshaped_text = arabic_reshaper.reshape('آدرس خانه در نقشه')
        bidi_text = get_display(reshaped_text)
        t = Label(text=bidi_text,font_name="C:\\Users\\Jannesari\\Downloads\\2 Titr Bold.ttf",pos=(90,250))
        box.add_widget(t)
        reshaped_text = arabic_reshaper.reshape('تصاوير ملک')
        bidi_texttttt = get_display(reshaped_text)
        tt = Label(text=bidi_texttttt,font_name="C:\\Users\\Jannesari\\Downloads\\2 Titr Bold.ttf",pos=(90,20))
        box.add_widget(tt)
        box.add_widget(boxx)
        boxxxxxxo = BoxLayout(width=200,height=50,size_hint=(None, None))
        with boxxxxxxo.canvas:
            Rectangle(source="G:\python\P_pngfa_ir_t1_5f4629383f6ac_1.png",size=(150,150),pos=(770,290))
        box.add_widget(boxxxxxxo)
        reshaped_text = arabic_reshaper.reshape('متراژ')
        bidi_textttt = get_display(reshaped_text)
        tth = Label(text=bidi_textttt,font_name="C:\\Users\\Jannesari\\Downloads\\2 Titr Bold.ttf",pos=(120,-130))
        box.add_widget(tth)
        return box





if __name__ == '__main__':
  amlakiyan ().run()
   
