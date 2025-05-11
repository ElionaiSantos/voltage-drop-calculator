# voltage-drop-calculator\

def calcular_queda_tensao(L, I, A, material):
    resistividade = 0.0175 if material.lower() == "cobre" else 0.0282
    Vd = (2 * L * I * resistividade) / A
    return Vd

def main():
    print("🔌 Calculadora de Queda de Tensão")
    L = float(input("Comprimento do cabo (m): "))
    I = float(input("Corrente (A): "))
    A = float(input("Secção do cabo (mm²): "))
    material = input("Material (cobre/alumínio): ").strip()

    Vd = calcular_queda_tensao(L, I, A, material)
    print(f"\n⚠️ Queda de tensão: {Vd:.2f} V")

if __name__ == "__main__":
    main()
