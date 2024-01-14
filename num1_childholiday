m, n = map(int, input().split())
t, z, y = map(list, zip(*[map(int, input().split()) for _ in range(n)]))
low = 0
high = 1000000001
mid = (low + high) // 2


def bal_t(time):
    answ = 0
    for i in range(n):
        time1 = t[i] * z[i] + y[i]
        balloon1 = (time // time1) * z[i]

        if time % time1 > time1 - y[i]:
            balloon2 = ((time % time1) - (y[i] - abs(time1 - time % time1))) // t[i]
        else:
            balloon2 = (time % time1) // t[i]
        sum = balloon1 + balloon2
        answ = answ + sum
    if answ < m:
        return True
    else:
        return False


while low < high:
    if bal_t(mid):
        low = mid + 1

    else:
        high = mid

    mid = (low + high) // 2
print(mid)
# all tests completed!
