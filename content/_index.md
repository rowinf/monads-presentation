+++
title = "My presentation"
outputs = ["Reveal"]
+++

# The Surprising Truth

## About Monads

Robert Irwin

---

### Category Theory

{{< figure src="8n1xb7.jpg" title="the search continues..." >}}

---

## 1. Monads

- immaterial substance
- indivisible
- underlie all existence
- hierarchical
- dormant < soul < spirit < monas monadum
- has "personality"

[Monadology](https://en.wikipedia.org/wiki/Monadology)

---

### More about Leibniz

- Partially credited with calculus (with Issac Newton)
- Inspired Einstein's theory of relativity
- May have been the first computer scientist

[Gottfried Wilhelm Leibniz](https://en.wikipedia.org/wiki/Gottfried_Wilhelm_Leibniz)

---

### Pythagoras 600 BC

> From the monad evolved the dyad; from it numbers; from numbers, points; then lines, two-dimensional entities, three-dimensional entities, bodies, culminating in the four elements earth, water, fire and air, from which the rest of our world is built up.

[Monad (philosophy)](https://en.wikipedia.org/wiki/Monad_(philosophy))

---

{{< figure src="8o2ow4.jpg" title="knowledge isn't always power">}}

---

### New definition:

A monad is an encapsulated unit of programming logic with "personality"

---

### In programming
```
class UsersController < ApplicationController
  def create
    resolve("users.create").(safe_params[:user]) do |m|
      m.success do |user|
        render json: user
      end

      m.failure do |code, errors|
        render json: { code: code, errors: errors.to_h }, status: :unprocessable_entity
      end
    end
  end
end
```
Decorate your return type


