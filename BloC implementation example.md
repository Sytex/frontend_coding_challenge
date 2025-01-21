# component.ts

```typescript
import { ExampleCubit } from "./cubit";

@Component({
  ...
})
export class ExampleComponent implements OnInit {
  constructor(private _exampleCubit: ExampleCubit) {}

  items = signal<Item[]>([]);

  ngOnInit() {
    this._exampleCubit.addChangeListener(changes => {
      const state = changes.nextState;
      if (state instanceof LoadingState) {
        // handle loading state
        return;
      }
      if (state instanceof LoadedState) {
        this.items.set(state.items);
      }
    });
  }

  getItems() {
    this._exampleCubit.getItems();
  }
}

export type Item = {
  id: string;
  name: string;
}
```

# states.ts

```typescript
export abstract class State {}

export class InitialState extends State {}

export class LoadingState extends State {}

export class LoadedState extends State {
  constructor(public readonly items: Item[]) {
    super();
  }
}
```

# cubit.ts

```typescript
import { Cubit } from "blac";
import { State } from "./states";

@Injectable()
export class ExampleCubit extends Cubit<State> {
  constructor() {
    super(new InitialState());
  }

  getItems(): void {
    this.emit(new LoadingState());

    // get items from repository
    const items = doSomethingToGetItems();

    this.emit(new LoadedState(items));
  }
}
```
