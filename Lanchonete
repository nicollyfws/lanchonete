import tkinter as tk
from tkinter import messagebox


def adicionar_lanche():
    lanche = entrada_lanche.get() 
    if lanche:
        lista_lanche.insert(tk.END, lanche) 
        entrada_lanche.delete(0, tk.END)
    else:
        messagebox.showwarning("Entrada inválida", "Por favor, insira um lanche.") 

def excluir_lanche():
    try:
        lanche_selecionado = lista_lanche.curselection()  
        lista_lanche.delete(lanche_selecionado)
    except:
        messagebox.showwarning("Seleção inválida", "Por favor, selecione um lanche para excluir.")

def concluir_lanche():
    try:
        lanche_selecionado = lista_lanche.curselection()  
        lanche = lista_lanche.get(lanche_selecionado) 
        lista_lanche.delete(lanche_selecionado) 
        lista_concluidos.insert(tk.END, lanche)  
    except:
        messagebox.showwarning("Seleção inválida", "Por favor, selecione um lanche para concluir.")

janela = tk.Tk()
janela.title("Lista de Compras")

entrada_lanche = tk.Entry(janela, width=40)
entrada_lanche.grid(row=0, column=0, padx=10, pady=10)

tk.Button(janela, text="Adicionar lanche", width=20, command=adicionar_lanche).grid(row=0, column=1, padx=10, pady=10)
tk.Button(janela, text="Excluir lanche", width=20, command=excluir_lanche).grid(row=1, column=0, padx=10, pady=10)
tk.Button(janela, text="Comprar lanche", width=20, command=concluir_lanche).grid(row=1, column=1, padx=10, pady=10)

lista_lanche = tk.Listbox(janela, height=10, width=50)
lista_lanche.grid(row=2, column=0, padx=10, pady=10)

lista_concluidos = tk.Listbox(janela, height=10, width=50)
lista_concluidos.grid(row=2, column=1, padx=10, pady=10)

janela.mainloop()
