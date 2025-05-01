# Permierofor
Learning 
from fpdf import FPDF

class PDF(FPDF):
    def header(self):
        self.set_font("Arial", "B", 14)
        self.cell(0, 10, "Premierofor: Презентация платформы", ln=True, align="C")
        self.ln(10)

    def chapter_title(self, title):
        self.set_font("Arial", "B", 12)
        self.set_text_color(30, 30, 120)
        self.cell(0, 10, title, ln=True)
        self.ln(2)

    def chapter_body(self, body):
        self.set_font("Arial", "", 11)
        self.set_text_color(0, 0, 0)
        self.multi_cell(0, 8, body)
        self.ln()

pdf = PDF()
pdf.add_page()

# Введение
pdf.chapter_title("О проекте")
pdf.chapter_body(
    "Premierofor — это цифровая платформа, сочетающая в себе философию, искусство, криптовалюту и мультимедийный манифест Перемирия. "
    "Проект представляет 21 главу, написанную на множестве языков, с визуальными, звуковыми и интерактивными элементами."
)

# Основные функции
pdf.chapter_title("Основные функции платформы")
pdf.chapter_body(
    "- Платформа доступна как веб-сайт, PWA-приложение (iOS / Android / Desktop).\n"
    "- 21 глава, включающая транскрипции, переходы между языками, аудио сопровождение.\n"
    "- 3D-модели книги и токена PosserCoin, с контролируемой скоростью вращения.\n"
    "- Кнопка доната через BTC и PosserCoin.\n"
    "- Тестовая кнопка оплаты и открытия контента.\n"
)

# Оплата и доступ
pdf.chapter_title("Система оплаты и доступа")
pdf.chapter_body(
    "Доступ к главам книги и мультимедийному контенту осуществляется за BTC или PosserCoin. "
    "Каждая глава может быть открыта отдельно, либо доступен полный доступ за фиксированную сумму."
)

# Технические особенности
pdf.chapter_title("Технические особенности")
pdf.chapter_body(
    "- Мультиязычный интерфейс (латынь, греческий, арабский, финикийский и др.)\n"
    "- Возможность установки как PWA-приложения.\n"
    "- Прямая интеграция с криптокошельками.\n"
    "- Звуковое оформление и анимация при переходах.\n"
)

# Заключение
pdf.chapter_title("Контакт и поддержка")
pdf.chapter_body(
    "Вы можете следить за развитием проекта через сайт Premierofor (ссылка будет предоставлена). "
    "Принимаются предложения, поддержка и партнёрства. Добро пожаловать в эпоху Перемирия."
)

output_path = "/mnt/data/Premierofor_Presentation.pdf"
pdf.output(output_path)

output_path
