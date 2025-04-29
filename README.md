def factorial(n):
    """
    Calcula el factorial de un número entero no negativo.
    
    Args:
        n (int): Número entero del cual se calculará el factorial.
    
    Returns:
        int: El factorial de n.
    
    Raises:
        ValueError: Si n es negativo.
        TypeError: Si n no es un entero.
    """
    if not isinstance(n, int):
        raise TypeError("El número debe ser un entero.")
    if n < 0:
        raise ValueError("El número no puede ser negativo.")
    if n == 0:
        return 1
    return n * factorial(n - 1)


if __name__ == "__main__":
    # Ejemplo de uso interactivo
    try:
        num = int(input("Ingrese un número para calcular su factorial: "))
        print(f"El factorial de {num} es: {factorial(num)}")
    except (ValueError, TypeError) as e:
        print(f"Error: {e}")
        
