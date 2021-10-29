# Flappy Dragon
Flappy Dragon game from "Hands on Rust".

## Design Notes
### Obstacles

**Obstacle Initialization**
Obstacle gaps are centered around a random `y-axis` location and stored in the `gap_y` attribute. The size of the gap is a maximum of 20, but is reduced each time by subtracting the current score.

```rust
Obstacle {
            x,
            gap_y: random.range(10, 40),
            size: i32::max(2, 20 - score)
        }
```

The image below shows how the above values are related to one another.
![Obstacle dimensions and gap size](./diagrams/obstacle-gap-size.png)

