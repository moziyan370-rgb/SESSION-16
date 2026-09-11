[README_SESSION_16.md](https://github.com/user-attachments/files/32087500/README_SESSION_16.md)
# Session 16

## Example 1

```python
movies = [
    "Demon Slayer",
    "War 2",
    "Coolie",
    "Avengers",
    "Pushpa 2"
]

movie_iterator = iter(movies)

print(next(movie_iterator))
print(next(movie_iterator))
print(next(movie_iterator))
print(next(movie_iterator))
print(next(movie_iterator))
```

### Output

```text
Demon Slayer
War 2
Coolie
Avengers
Pushpa 2
```

## Example 2

```python
songs = [
    "Kesariya",
    "Believer",
    "Shape of You",
    "Blinding Lights",
    "Excuses",
    "Perfect"
]

for position, song in enumerate(songs, start=1):
    print(position, ".", song)
```

### Output

```text
1 . Kesariya
2 . Believer
3 . Shape of You
4 . Blinding Lights
5 . Excuses
6 . Perfect
```

## Example 3

```python
food_items = ["Pizza", "Burger", "Biryani", "Pasta", "Sandwich"]

prices = [250, 150, 220, 180, 120]

for food, price in zip(food_items, prices):
    print(f"{food} - ₹{price}")
```

### Output

```text
Pizza - ₹250
Burger - ₹150
Biryani - ₹220
Pasta - ₹180
Sandwich - ₹120
```

## Example 4

```python
def insta_posts_generator(posts):
    for post in posts:
        yield post


posts = [
    "My new photo!",
    "Weekend vibes!",
    "Best day ever!",
    "New memories!"
]

post_generator = insta_posts_generator(posts)

try:
    print(next(post_generator))
    print(next(post_generator))
    print(next(post_generator))
    print(next(post_generator))
    print(next(post_generator))

except StopIteration:
    print("All posts have been printed.")
```

### Output

```text
My new photo!
Weekend vibes!
Best day ever!
New memories!
All posts have been printed.
```

## Example 5

```python
def cashback_generator(transactions):
    for amount in transactions:
        cashback = amount * 5 / 100
        yield cashback


transactions = [1000, 500, 2000, 750, 1500]

cashback = cashback_generator(transactions)

for value in cashback:
    print("Cashback: ₹", value)
```

### Output

```text
Cashback: ₹ 50.0
Cashback: ₹ 25.0
Cashback: ₹ 100.0
Cashback: ₹ 37.5
Cashback: ₹ 75.0
```

