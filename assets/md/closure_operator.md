```kotlin
interface Monoid<F> {

    fun F.combine(b: F): F

    fun empty(): F

    operator fun F.plus(b: F): F = this.combine(b)
    // monoidA.combine(monoidB) → monoidA + monoidB
}
```