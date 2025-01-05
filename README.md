# Custom Hooks Collection

A collection of reusable React custom hooks to simplify state management, data fetching, and more.

## Features

This library provides the following hooks:

1. **`useDebounce`**: Delays the update of a value until after a specified delay.
```javascript
const [search, setSearch] = useState('');
const debouncedSearch = useDebounce(search, 500);

useEffect(() => {
  if (debouncedSearch) {
    console.log(`Search for: ${debouncedSearch}`);
  }
}, [debouncedSearch]);

```
2. **`useLocalStorage`**: A hook for managing state synchronized with `localStorage`.
```javascript
const [name, setName] = useLocalStorage('name', 'John Doe');
```
3. **`useFetch`**: A simple data-fetching hook.
```javascript
const { data, loading, error } = useFetch('https://api.example.com/data');
if (loading) return <p>Loading...</p>;
if (error) return <p>Error: {error.message}</p>;
return <p>Data: {JSON.stringify(data)}</p>;
```
4. **`useToggle`**: A hook for toggling between boolean states.
```javascript
const [isVisible, toggleVisibility] = useToggle(false);
```
5. **`usePrevious`**: Tracks the previous value of a state or prop.
```javascript
const [count, setCount] = useState(0);
const previousCount = usePrevious(count);
```

---

## Installation

To use these hooks in your project:

1. Clone the repository:
```bash
git clone https://github.com/your-username/custom-hooks-collection.git
```

2. Navigate to the project folder and install dependencies (if required for future extensions):
```bash
npm install
```

3. Import the desired hook into your project:
```javascript
import { useDebounce } from './src/hooks/useDebounce';
```
