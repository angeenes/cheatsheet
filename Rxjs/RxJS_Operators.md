
1. **map** - Transforms each emitted value based on a provided function.
```typescript
import { of } from 'rxjs';
import { map } from 'rxjs/operators';

of(1, 2, 3).pipe(
  map(value => value * 2)
).subscribe(console.log); // Outputs: 2, 4, 6
```

2. **filter** - Filters emitted values based on a condition, allowing only values that pass the condition.
```typescript
import { of } from 'rxjs';
import { filter } from 'rxjs/operators';

of(1, 2, 3, 4).pipe(
  filter(value => value % 2 === 0)
).subscribe(console.log); // Outputs: 2, 4
```

3. **switchMap** - Replaces the previous Observable with a new one, ideal for handling network requests.
```typescript
import { of } from 'rxjs';
import { switchMap } from 'rxjs/operators';

of('a', 'b', 'c').pipe(
  switchMap(letter => of(`${letter}1`, `${letter}2`))
).subscribe(console.log); // Outputs: a1, a2, b1, b2, c1, c2
```

4. **mergeMap** - Merges Observables without canceling the previous ones, ideal for parallel tasks.
```typescript
import { of } from 'rxjs';
import { mergeMap } from 'rxjs/operators';

of('x', 'y').pipe(
  mergeMap(letter => of(`${letter}1`, `${letter}2`))
).subscribe(console.log); // Outputs: x1, x2, y1, y2
```

5. **concatMap** - Chains Observables in sequence, waiting for each to complete before starting the next.
```typescript
import { of } from 'rxjs';
import { concatMap } from 'rxjs/operators';

of('p', 'q').pipe(
  concatMap(letter => of(`${letter}1`, `${letter}2`))
).subscribe(console.log); // Outputs: p1, p2, q1, q2
```

6. **exhaustMap** - Ignores new Observables until the current one completes, often used to prevent duplicates.
```typescript
import { of, interval } from 'rxjs';
import { exhaustMap, take } from 'rxjs/operators';

interval(500).pipe(
  take(2),
  exhaustMap(() => interval(200).pipe(take(3)))
).subscribe(console.log); // Outputs: 0, 1, 2 after first 500 ms
```

7. **take** - Limits the number of emitted values to a specified count.
```typescript
import { of } from 'rxjs';
import { take } from 'rxjs/operators';

of(1, 2, 3, 4).pipe(
  take(2)
).subscribe(console.log); // Outputs: 1, 2
```

8. **takeUntil** - Continues emitting values until another Observable emits.
```typescript
import { interval, timer } from 'rxjs';
import { takeUntil } from 'rxjs/operators';

interval(1000).pipe(
  takeUntil(timer(3000))
).subscribe(console.log); // Outputs: 0, 1, 2 (stops after 3 seconds)
```

9. **debounceTime** - Delays emissions until a period of inactivity, useful for handling user input.
```typescript
import { fromEvent } from 'rxjs';
import { debounceTime } from 'rxjs/operators';

fromEvent(document, 'click').pipe(
  debounceTime(1000)
).subscribe(() => console.log('Clicked after 1 second'));
```

10. **distinctUntilChanged** - Prevents consecutive duplicate values from being emitted.
```typescript
import { of } from 'rxjs';
import { distinctUntilChanged } from 'rxjs/operators';

of(1, 1, 2, 2, 3, 1).pipe(
  distinctUntilChanged()
).subscribe(console.log); // Outputs: 1, 2, 3, 1
```

11. **catchError** - Catches errors in an Observable and provides an alternative Observable to continue.
```typescript
import { of, throwError } from 'rxjs';
import { catchError } from 'rxjs/operators';

throwError('Error!').pipe(
  catchError(error => of('Handled Error'))
).subscribe(console.log); // Outputs: 'Handled Error'
```

12. **tap** - Performs a side effect without modifying the data, often used for logging or actions.
```typescript
import { of } from 'rxjs';
import { tap } from 'rxjs/operators';

of(5, 6, 7).pipe(
  tap(value => console.log('Side effect:', value))
).subscribe(console.log); // Outputs each value, with side effects logged
```

13. **startWith** - Prepends initial values to an Observable before it starts emitting.
```typescript
import { of } from 'rxjs';
import { startWith } from 'rxjs/operators';

of(1, 2).pipe(
  startWith(0)
).subscribe(console.log); // Outputs: 0, 1, 2
```

14. **scan** - Accumulates emitted values over time, similar to `reduce` but continues emitting.
```typescript
import { of } from 'rxjs';
import { scan } from 'rxjs/operators';

of(1, 2, 3).pipe(
  scan((acc, value) => acc + value, 0)
).subscribe(console.log); // Outputs: 1, 3, 6
```

15. **reduce** - Accumulates all values and emits the final result after completion.
```typescript
import { of } from 'rxjs';
import { reduce } from 'rxjs/operators';

of(1, 2, 3).pipe(
  reduce((acc, value) => acc + value, 0)
).subscribe(console.log); // Outputs: 6
```

16. **combineLatest** - Combines the latest values from multiple Observables, emitting whenever one changes.
```typescript
import { combineLatest, of } from 'rxjs';

combineLatest([
  of(1),
  of(2),
  of(3)
]).subscribe(console.log); // Outputs: [1, 2, 3]
```

17. **withLatestFrom** - Combines values from two Observables, emitting only when the first Observable emits.
```typescript
import { of, interval } from 'rxjs';
import { withLatestFrom, take } from 'rxjs/operators';

interval(1000).pipe(
  take(3),
  withLatestFrom(of('a', 'b', 'c'))
).subscribe(console.log); // Outputs: [0, 'a'], [1, 'b'], [2, 'c']
```

18. **delay** - Delays emissions of an Observable by a specified time.
```typescript
import { of } from 'rxjs';
import { delay } from 'rxjs/operators';

of('Delayed message').pipe(
  delay(1000)
).subscribe(console.log); // Outputs after 1 second
```

19. **share** - Shares a single subscription among multiple subscribers to the same Observable.
```typescript
import { interval } from 'rxjs';
import { take, share } from 'rxjs/operators';

const sharedObservable = interval(1000).pipe(take(2), share());

sharedObservable.subscribe(val => console.log('Subscriber 1:', val));
sharedObservable.subscribe(val => console.log('Subscriber 2:', val));
```

20. **retry** - Retries an Observable if it fails, useful for network requests.
```typescript
import { of, throwError } from 'rxjs';
import { retry, catchError } from 'rxjs/operators';

throwError('Error').pipe(
  retry(2), // Retry twice
  catchError(err => of('Handled after retries'))
).subscribe(console.log); // Outputs 'Handled after retries' after 2 retries
```
