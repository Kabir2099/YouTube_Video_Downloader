# YouTube_Video_Downloader
    root=Tk()
    root.geometry('500x300')
    root.resizable(0,0)
    root.title("Youtube Video Downloader")
    Label(root,text='Youtube Video Downloader',font='arial 15 bold').pack()
    speak("Sir...Enter the Video link")
    link=StringVar()
    Label(root,text="Paste Link Here",font='arial 15 bold').place(x=160,y=60)
    Entry(root,width=70,textvariable=link).place(x=32,y=90)

    def videoDownloader():
        url=YouTube(str(link.get()))
        video=url.streams.first()
        video.download('C:\\Users\\KABIR\\Desktop\\My Video')
        Label(root,text='Downloaded',font='arial 15 bold').place(x=180,y=210)
    
    Button(root,text='Download',font='arial 15 bold',bg='pale violet red',padx=2,command=videoDownloader).place(x=180,y=150)
    root.mainloop()
    speak("Video Download successfully")
    os.startfile("C:\\Users\\KABIR\\Desktop\\My Video")
    speak("Here is your video")
