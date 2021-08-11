# useForm Hook

Example:
```
import {useForm} from './hooks/useForm';

const data = {  //example of objet data
  name: '',
  email: '',
  password: ''
};  

const [values, handleInputChange, reset] = useForm(data);



//Example of Form with useForm hook

const {name, email, password } = values;

const handleSubmit = (e)=>{
  e.preventDefault();
  console.log(name, email, password);
}

<form onSubmit={ handleSubmit }>

  <h1>FormWithCustomHook</h1>
  <hr />

  <div className="form-group">
      <input 
          type="text"
          name="name"
          className="form-control"
          placeholder="Tu nombre"
          autoComplete="off"
          value={ name }
          onChange={ handleInputChange } 
      />
  </div>

  <div className="form-group">
      <input 
          type="text"
          name="email"
          className="form-control"
          placeholder="email@gmail.com"
          autoComplete="off"
          value={ email }
          onChange={ handleInputChange }
      />
  </div>

  <div className="form-group">
      <input 
          type="password"
          name="password"
          className="form-control"
          placeholder="*****"
          value={ password }
          onChange={ handleInputChange }
      />
  </div>

  <button 
      type="submit" 
      className="btn btn-primary">
      Guardar
  </button>

</form>
```