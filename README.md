
def moving_average(numbers, window):
    if window <= 0 or window > len(numbers):
        return []

    averages = []

    for index in range(len(numbers) - window + 1):
        chunk = numbers[index:index + window]
        averages.append(sum(chunk) / window)

    return averages


if __name__ == "__main__":
    values = [10, 20, 30, 40, 50]
    window = 3

    print("Values:", values)
    print("Window:", window)
    print("Moving averages:", moving_average(values, window))
