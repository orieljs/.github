<p align="center">
  <img src="oriel-mark.png" width="96" height="96" alt="Oriel">
</p>

<h1 align="center">Oriel</h1>

<p align="center">
  A Laravel-style, full-stack TypeScript framework for Node and Bun.
</p>

<p align="center">
  <a href="https://orieljs.vercel.app">Website</a> ·
  <a href="https://www.npmjs.com/package/@orieljs/framework">npm</a>
</p>

---

Routing, models, queues, mail, validation and auth arrive together, designed as one typed toolkit, so you can build
the whole app and not just the API.

```ts
// routes/web.ts
Route.get('/', () => inertia('Welcome'))
Route.resource('posts', PostController)

// app/Http/Controllers/PostController.ts
export class PostController extends Controller {
  async store() {
    const data = await StorePostRequest.validate()
    const post = await Post.create(data)
    return redirect().route('posts.show', post)
  }
}
```

### What's in the box

- **HTTP and routing:** named routes, groups, middleware and model binding, with typed route names
- **Database:** an Eloquent-style ORM on Postgres, MySQL and SQLite, with migrations, factories and seeders
- **Validation:** Laravel's rule strings and form requests that return typed data
- **Auth and sessions:** guards, hashing, encrypted cookies and API tokens
- **Queues and scheduling:** jobs, batches and retries on Redis or your database
- **Mail and notifications**, **cache**, **events**, **files and logs**, **views** and a **console**
- **Frontends:** Inertia with React, Vue, Svelte, Solid or Angular, or server-driven Live components

### Status

Oriel is in early alpha. The core is done and the components are being built now; the first alpha is on npm as
`@orieljs/framework`. Follow along on the [website](https://orieljs.vercel.app).
