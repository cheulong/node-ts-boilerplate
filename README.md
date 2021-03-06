# node-ts-boilerplate

## Express

```bash
  yarn add express morgan cors

  yarn add -D @types/express @types/morgan @types/cors
```

### Example

```js
import express, { Application, Request, Response } from 'express';
import cors from 'cors';

const PORT = process.env.PORT || 8080;
const app: Application = express();

app.use(cors());
app.use(express.json());
app.use(morgan('dev'));

app.get('/', (req: Request, res: Response) => {
  res.send('It is working!');
});

app.listen(PORT, () => console.log(`The server is running on port ${PORT}`));
```
