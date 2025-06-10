from tkinter import Tk, Canvas, messagebox
from random import randrange
from itertools import cycle

# Setup jendela
window = Tk()
window.title("Egg Catcher (Versi Pemula)")

# Ukuran layar
canvas_width = 800
canvas_height = 400

# Membuat canvas
canvas = Canvas(window, width=canvas_width, height=canvas_height, bg="sky blue")
canvas.pack()

# Latar tanah dan matahari
canvas.create_rectangle(0, canvas_height - 100, canvas_width, canvas_height, fill="green", width=0)
canvas.create_oval(-100, -100, 100, 100, fill="orange", width=0)  # Matahari

# Warna telur bergantian
egg_colors = cycle(["red", "yellow", "blue", "pink", "purple"])

# Ukuran telur
egg_width = 40
egg_height = 50

# Variabel skor dan nyawa
score = 0
lives = 3

# Menampilkan skor dan nyawa
score_text = canvas.create_text(10, 10, anchor="nw", fill="darkblue", font=("Arial", 16), text="Score: 0")
lives_text = canvas.create_text(canvas_width - 10, 10, anchor="ne", fill="darkblue", font=("Arial", 16), text="Lives: 3")

# Daftar telur aktif
eggs = []

# Menangkap objek telur
def create_egg():
    x = randrange(10, canvas_width - egg_width - 10)
    y = 0
    color = next(egg_colors)
    egg = canvas.create_oval(x, y, x + egg_width, y + egg_height, fill=color, width=0)
    eggs.append(egg)
    window.after(3000, create_egg)  # buat telur baru setiap 3 detik

def move_eggs():
    for egg in eggs[:]:
        canvas.move(egg, 0, 10)
        x1, y1, x2, y2 = canvas.coords(egg)
        if y2 >= canvas_height:
            eggs.remove(egg)
            canvas.delete(egg)
            lose_life()
    window.after(100, move_eggs)  # gerakkan telur setiap 0.1 detik

def lose_life():
    global lives
    lives -= 1
    canvas.itemconfig(lives_text, text="Lives: " + str(lives))
    if lives == 0:
        messagebox.showinfo("Game Over", f"Skor akhir kamu: {score}")
        window.destroy()

def check_catch():
    catcher_coords = canvas.coords(catcher)
    cx1, cy1, cx2, cy2 = catcher_coords

    for egg in eggs[:]:
        ex1, ey1, ex2, ey2 = canvas.coords(egg)
        if cx1 < ex1 and ex2 < cx2 and abs(cy2 - ey2) < 40:
            eggs.remove(egg)
            canvas.delete(egg)
            increase_score()
    window.after(100, check_catch)

def increase_score():
    global score
    score += 10
    canvas.itemconfig(score_text, text="Score: " + str(score))

# Penangkap telur (catcher)
catcher = canvas.create_arc(350, canvas_height - 100, 450, canvas_height, start=200, extent=140, style="arc", outline="blue", width=5)

# Gerakan kiri dan kanan
def move_left(event):
    x1, y1, x2, y2 = canvas.coords(catcher)
    if x1 > 0:
        canvas.move(catcher, -20, 0)

def move_right(event):
    x1, y1, x2, y2 = canvas.coords(catcher)
    if x2 < canvas_width:
        canvas.move(catcher, 20, 0)

# Menghubungkan tombol panah
canvas.bind_all("<Left>", move_left)
canvas.bind_all("<Right>", move_right)

# Menjalankan fungsi utama
create_egg()
move_eggs()
check_catch()

window.mainloop()
