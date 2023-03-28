# Система уравнений:
def Coullet(XYZ, t, alpha, beta, zeta, delta):
    x, y, z = XYZ
    x_dt = y
    y_dt = z
    z_dt = alpha*x + beta*y + zeta*z + delta*x**3
    return x_dt, y_dt, z_dt

# Параметры системы и начальные условия:
alpha = 0.8
beta = -1.1
zeta = -0.4
delta = -1

x_0, y_0, z_0 = 0.1, 0, 0

# Максимальное время и общее количество
# временных точек:
tmax, n = 200, 20000

# Интегрируем систему уравнений в каждой точке
# временного интервала t:
t = np.linspace(0, tmax, n)
f = odeint(Coullet, (x_0, y_0, z_0), t,
           args=(alpha, beta, zeta, delta))
