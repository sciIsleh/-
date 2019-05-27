# -
это "программа"-тест написанная на pyton3 я сделал для сдачи индивидуального проекта по информатике 


#импорт библеотек #
from tkinter import *
from tkinter import ttk
#
#функции(def)
class MyCounter:
    def __init__(self, value=None):
        self.value = value or 0

    def increment(self):
        self.value += 1

    def decrement(self):
        self.value -= 1

def change_label_text(lbl_element, counter):
    return lbl_element.config(text='BALLS:{}'.format(counter.value))


def increase_counter(counter):
    counter.increment()


def decrease_counter(counter):
    counter.decrement()


def redraw_message(lbl_element, counter, func):
    func(counter)
    change_label_text(lbl_element, counter)


def main():
    root = Tk()
    root.title('TEST')
    root.geometry("1000x600")
    my_count = MyCounter()
    wrapper_frame = Frame(root)
    wrapper_frame.pack()
#

#тело программы

    #**************
    message_lbl = Label(wrapper_frame, text='BALLS:{}'.format(my_count.value))
    message_lbl.grid(row=0, column=0, columnspan=2)
    #*********
    
    questions_1label=Label(text="1)Кто создал первый\nпаровой\nдвигатель в мире?")
    questions_1label.place(x=0,y=68)
    #
    questions_2label=Label(text="2)Что такое\nдиэлектрик\nдля физика?")
    questions_2label.place(x=0,y=200)
    #
    questions_3label=Label(text="3)Какая жидкость\nсамая легкая?")
    questions_3label.place(x=0,y=330)
    
    questions_4label=Label(text="4)кто придумал формулу E=mc2?")
    questions_4label.place(x=0,y=440)
    #
    questions_5label=Label(text="5)Модель идеального газа\nпредполагает, что?")
    questions_5label.place(x=300,y=68)
    ##
    questions_6label=Label(text="6)Какие физические величины\nотносятся к термодинамическим\nпараметрам идеального газа?")
    questions_6label.place(x=300,y=180)
    ##
    questions_7label=Label(text="7)Ускорение — это……?")
    questions_7label.place(x=300,y=305)
    ##
    questions_8label=Label(text="8)Какими носителями электрического\nзаряда создаётся электрический\nток в растворах электролитов?")
    questions_8label.place(x=300,y=400)
    ##
    questions_9label=Label(text="9)Чем вызвано давление газа на стенки сосуда?")
    questions_9label.place(x=650,y=68)
    ##
    questions_10label=Label(text="10)Как изменится внутренняя энергия\nидеального газа при его адиабатном расширении?")
    questions_10label.place(x=650,y=165)
    ##
    questions_11label=Label(text="11)Сила 10 Н сообщает телу ускорение\n2  м/с2. Чему равна масса тела?")#т. к. m = F / a
    questions_11label.place(x=650,y=280)
    ##
    questions_12label=Label(text="12)Количество частиц, находящихся\nв одном моле любого вещества равно")#N=6,02.1023(1моль)
    questions_12label.place(x=650,y=395)
    ##
   
    button1_1questions=Button(text="a)Иван Ползунов",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button1_1questions.place(x=0,y=120)
    button2_1questions=Button(text="b)Азарёнок Василий")
    button2_1questions.place(x=0,y=145)
    button3_1questions=Button(text="c)Акинин Петр Викторович")
    button3_1questions.place(x=0,y=170)
    #
    button1_2questions=Button(text="a)кислота")
    button1_2questions.place(x=0,y=250)
    button2_2questions=Button(text="b)h2o(вода)",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button2_2questions.place(x=0,y=275)
    button3_2questions=Button(text="c)сяляная кислота")
    button3_2questions.place(x=0,y=300)
    #
    button1_3questions=Button(text="a)cжиженный водород",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button1_3questions.place(x=0,y=365)
    button2_3questions=Button(text="b)жидкий азот")
    button2_3questions.place(x=0,y=390)
    button3_3questions=Button(text="c)водяной пар")
    button3_3questions.place(x=0,y=415)
    
    button1_4questions=Button(text="a)Луи Пастер")
    button1_4questions.place(x=0,y=460)
    button2_4questions=Button(text="b)Никола Тесла")
    button2_4questions.place(x=0,y=485)
    button3_4questions=Button(text="c)Альберт Эйнштейн",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button3_4questions.place(x=0,y=510)
    #
    button1_5questions=Button(text="a)молекулы не взаимодействуют друг с другом",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button1_5questions.place(x=300,y=105)
    button2_5questions=Button(text="b)молекулы не имеют размеров")
    button2_5questions.place(x=300,y=130)
    button3_5questions=Button(text="c)молекулы неподвижны")
    button3_5questions.place(x=300,y=155)
    #
    button1_6questions=Button(text="a)температура и давление")
    button1_6questions.place(x=300,y=230)
    button2_6questions=Button(text="b)объём, давление, молярная масса")
    button2_6questions.place(x=300,y=255)
    button3_6questions=Button(text="c)объём, давление, температура",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button3_6questions.place(x=300,y=280)
    #
    button1_7questions=Button(text="a)изменение положения тела с течение времени")
    button1_7questions.place(x=300,y=325)
    button2_7questions=Button(text="b)изменение скорости тела за единицу времени",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button2_7questions.place(x=300,y=350)
    button3_7questions=Button(text="c)изменение положения тела относительно других тел")
    button3_7questions.place(x=300,y=375)
    #
    button1_8questions=Button(text="aтолько электронами)")
    button1_8questions.place(x=300,y=450)
    button2_8questions=Button(text="b)положительными и отрицательными ионами",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button2_8questions.place(x=300,y=475)
    button3_8questions=Button(text="c)электронами и положительными ионами")
    button3_8questions.place(x=300,y=500)
    #
    button1_9questions=Button(text="a)существованием сил взаимодействия между молекулами")
    button1_9questions.place(x=650,y=90)
    button2_9questions=Button(text="b)столкновением молекул газа со стенками сосуда",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button2_9questions.place(x=650,y=115)
    button3_9questions=Button(text="c)столкновением молекул газа друг с другом")
    button3_9questions.place(x=650,y=140)
    #
    button1_10questions=Button(text="a)уменьшится")
    button1_10questions.place(x=650,y=200)
    button2_10questions=Button(text="b)внутренняя энергия идеального газа всегда равна нулю")
    button2_10questions.place(x=650,y=225)
    button3_10questions=Button(text="c)не изменится",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button3_10questions.place(x=650,y=250)
    #
    button1_11questions=Button(text="a)0,2 кг")
    button1_11questions.place(x=650,y=315)
    button2_11questions=Button(text="b)20 кг")
    button2_11questions.place(x=650,y=340)
    button3_11questions=Button(text="c)5кг",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button3_11questions.place(x=650,y=365)
    
    button1_12questions=Button(text="a)постоянной Больцмана")
    button1_12questions.place(x=650,y=430)
    button2_12questions=Button(text="b)постоянной Авогадро",command=lambda : redraw_message(message_lbl, my_count, increase_counter))
    button2_12questions.place(x=650,y=455)
    button3_12questions=Button(text="c)универсальной газовой постоянной")
    button3_12questions.place(x=650,y=480)
    
    

    root.mainloop()
#
#активируем функцию main()
main()
#
