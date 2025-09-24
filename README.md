# Session-4-Lab-Activity-1---State-Management

When I ran the Ephemeral State example, I saw that the counter only worked inside the widget where the button was. If I left the screen or the widget refreshed, the counter went back to zero. That made me realize this kind of state is temporary and only belongs to that widget.

In the Scoped Model example, the counter felt more reliable. The value stayed the same even when I moved between different widgets, as long as the model was still active. This showed me that the state can be shared across the whole app, not just one place.

So the main difference I noticed is that ephemeral state is local and resets easily, while ScopedModel provides one shared model that widgets can listen to. When the model changes, it notifies everything that depends on it so the UI updates automatically. This makes the state more consistent and easier to keep track of.

This becomes really useful in bigger apps. For example, user authentication needs to be available across every screen, a shopping cart should keep items updated no matter where you are, and things like themes or favorites need to stay the same throughout the app. Ephemeral state can’t handle that well, but app-wide state management with ScopedModel (or similar approaches) makes it much easier.

In short, ephemeral state is fine for small things that only matter in one widget, but app state management is the better choice when your app grows and you need data to be shared and consistent everywhere.
