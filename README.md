import webbrowser
import platform

def main():
    # التحقق من نظام التشغيل
    current_os = platform.system()

   # تحديد الرابط المناسب بناءً على نظام التشغيل
    if current_os == 'Linux':
        if 'android' in platform.platform().lower():  # التحقق مما إذا كانت المنصة تعمل بنظام Android
            url = 'https://www.android.com/'
    elif current_os == 'Windows':
        url = 'https://gymtech.sa/'
    elif current_os == 'Darwin' or current_os == 'iOS':  # تم إضافة التعرف على نظام التشغيل iOS هنا
        url = 'https://apps.apple.com/sa/app/gym-tech/id6444655942?l=ar'
    else:
        print("نظام التشغيل غير معروف. يتم توجيهك تلقائيًا إلى https://gymtech.sa/")
        url = 'https://gymtech.sa/'

    # فتح المتصفح لعرض الرابط
    webbrowser.open(url)

    # إضافة رسالة لتوجيه المستخدم
    print("يتم فتح المتصفح. يُرجى الانتظار ...")

if __name__ == "__main__":
    main() 
    





