
1. **map**
```typescript
import { of } from 'rxjs';
import { map } from 'rxjs/operators';

of(1, 2, 3).pipe(
  map(value => value * 2)
).subscribe(console.log); // Outputs: 2, 4, 6
```

2. **filter**
```typescript
import { of } from 'rxjs';
import { filter } from 'rxjs/operators';

of(1, 2, 3, 4).pipe(
  filter(value => value % 2 === 0)
).subscribe(console.log); // Outputs: 2, 4
```

3. **switchMap**
```typescript
import { of } from 'rxjs';
import { switchMap } from 'rxjs/operators';

of('a', 'b', 'c').pipe(
  switchMap(letter => of(`${letter}1`, `${letter}2`))
).subscribe(console.log); // Outputs: a1, a2, b1, b2, c1, c2
```

4. **mergeMap**
```typescript
import { of } from 'rxjs';
import { mergeMap } from 'rxjs/operators';

of('x', 'y').pipe(
  mergeMap(letter => of(`${letter}1`, `${letter}2`))
).subscribe(console.log); // Outputs: x1, x2, y1, y2
```

5. **concatMap**
```typescript
import { of } from 'rxjs';
import { concatMap } from 'rxjs/operators';

of('p', 'q').pipe(
  concatMap(letter => of(`${letter}1`, `${letter}2`))
).subscribe(console.log); // Outputs: p1, p2, q1, q2
```

6. **exhaustMap**
```typescript
import { of, interval } from 'rxjs';
import { exhaustMap, take } from 'rxjs/operators';

interval(500).pipe(
  take(2),
  exhaustMap(() => interval(200).pipe(take(3)))
).subscribe(console.log); // Outputs: 0, 1, 2 after first 500 ms
```

7. **take**
```typescript
import { of } from 'rxjs';
import { take } from 'rxjs/operators';

of(1, 2, 3, 4).pipe(
  take(2)
).subscribe(console.log); // Outputs: 1, 2
```

8. **takeUntil**
```typescript
import { interval, timer } from 'rxjs';
import { takeUntil } from 'rxjs/operators';

interval(1000).pipe(
  takeUntil(timer(3000))
).subscribe(console.log); // Outputs: 0, 1, 2 (stops after 3 seconds)
```

9. **debounceTime**
```typescript
import { fromEvent } from 'rxjs';
import { debounceTime } from 'rxjs/operators';

fromEvent(document, 'click').pipe(
  debounceTime(1000)
).subscribe(() => console.log('Clicked after 1 second'));
```

10. **distinctUntilChanged**
```typescript
import { of } from 'rxjs';
import { distinctUntilChanged } from 'rxjs/operators';

of(1, 1, 2, 2, 3, 1).pipe(
  distinctUntilChanged()
).subscribe(console.log); // Outputs: 1, 2, 3, 1
```

11. **catchError**
```typescript
import { of, throwError } from 'rxjs';
import { catchError } from 'rxjs/operators';

throwError('Error!').pipe(
  catchError(error => of('Handled Error'))
).subscribe(console.log); // Outputs: 'Handled Error'
```

12. **tap**
```typescript
import { of } from 'rxjs';
import { tap } from 'rxjs/operators';

of(5, 6, 7).pipe(
  tap(value => console.log('Side effect:', value))
).subscribe(console.log); // Outputs each value, with side effects logged
```

13. **startWith**
```typescript
import { of } from 'rxjs';
import { startWith } from 'rxjs/operators';

of(1, 2).pipe(
  startWith(0)
).subscribe(console.log); // Outputs: 0, 1, 2
```

14. **scan**
```typescript
import { of } from 'rxjs';
import { scan } from 'rxjs/operators';

of(1, 2, 3).pipe(
  scan((acc, value) => acc + value, 0)
).subscribe(console.log); // Outputs: 1, 3, 6
```

15. **reduce**
```typescript
import { of } from 'rxjs';
import { reduce } from 'rxjs/operators';

of(1, 2, 3).pipe(
  reduce((acc, value) => acc + value, 0)
).subscribe(console.log); // Outputs: 6
```

16. **combineLatest**
```typescript
import { combineLatest, of } from 'rxjs';

combineLatest([
  of(1),
  of(2),
  of(3)
]).subscribe(console.log); // Outputs: [1, 2, 3]
```

17. **withLatestFrom**
```typescript
import { of, interval } from 'rxjs';
import { withLatestFrom, take } from 'rxjs/operators';

interval(1000).pipe(
  take(3),
  withLatestFrom(of('a', 'b', 'c'))
).subscribe(console.log); // Outputs: [0, 'a'], [1, 'b'], [2, 'c']
```

18. **delay**
```typescript
import { of } from 'rxjs';
import { delay } from 'rxjs/operators';

of('Delayed message').pipe(
  delay(1000)
).subscribe(console.log); // Outputs after 1 second
```

19. **share**
```typescript
import { interval } from 'rxjs';
import { take, share } from 'rxjs/operators';

const sharedObservable = interval(1000).pipe(take(2), share());

sharedObservable.subscribe(val => console.log('Subscriber 1:', val));
sharedObservable.subscribe(val => console.log('Subscriber 2:', val));
```

20. **retry**
```typescript
import { of, throwError } from 'rxjs';
import { retry, catchError } from 'rxjs/operators';

throwError('Error').pipe(
  retry(2), // Retry twice
  catchError(err => of('Handled after retries'))
).subscribe(console.log); // Outputs 'Handled after retries' after 2 retries
```
