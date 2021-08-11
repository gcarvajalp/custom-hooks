# useFetch Hook

Example:
```
import {useFetch} from './hooks/useFetch';

const url = 'https://reqres.in/api/users/2'; //Endpoint de una API
const { data, loading, error} = useFetch(url);

```