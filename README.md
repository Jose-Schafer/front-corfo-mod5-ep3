# How to start
Install packages
```sh
nvm use 23
npm install
```

Start dev server
```sh
npm run dev
```

open `http://localhost:5173`

# Preguntas
## 1. Uso de useState para la Gestión de Estado (1.5 puntos)
Ver `src/views/contact/form.tsx` donde se usa `useForm` para gestionar el formulario.

## 2. Uso de useEffect para la Gestión de Efectos Secundarios (1.5
Ver `src/views/medical-team/index.jsx` para ver como se usa useEffect para mostrar a los doctores y filtrar cada vez que cambia un valor en el input.

## 3. Construcción de un Hook Personalizado (1.5 puntos)
Ver `src/providers/AuthContext.tsx` para el hook `useAuth`

## 4. Manejo de Errores en la Aplicación (1.5 puntos)
Ver `src/views/contact/form.tsx` para el manejo de errores de formulario con el siguiente código:

El siguiente código valida el formulario y también maneja un error para mostrarle al usuario un mensaje customizado más explicativo.
```javascript
const formSchema = z.object({
  name: z.string().min(2, {
    message: "El nombre debe tener a lo menos dos caracteres.",
  }),
  email: z.string().email({
    message: "Debe ingresar un correo valido.",
  }),
  doctorId: z.string().refine((value) => value !== "", {
    message: "Debe seleccionar un doctor para continuar.",
  }),
  schedule: z.string().refine((value) => value !== "", {
    message: "Debe seleccionar un horario.",
  }),
})
```

## 5. Aplicación Correcta de las Reglas de los Hooks (1 punto)
Ver `src/views/medical-team/index.jsx` para ver como se usa el hook `useDoctors` dentro de useEffect y condicionales
