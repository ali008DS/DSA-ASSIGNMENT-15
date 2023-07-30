from collections import deque

class DataStream:
    def __init__(self, value, k):
        self.stream = deque()
        self.value = value
        self.k = k

    def consec(self, num):
        self.stream.append(num)
        if len(self.stream) > self.k:
            self.stream.popleft()

        return len(self.stream) == self.k and all(x == self.value for x in self.stream)

# Example
ds = DataStream(2, 3)
print(ds.consec(1))  # Output: False
print(ds.consec(2))  # Output: False
print(ds.consec(2))  # Output: True
print(ds.consec(2))  # Output: True
print(ds.consec(1))  # Output: False
