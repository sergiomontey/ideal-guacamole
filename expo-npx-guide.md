# 🚀 Using `npx` with Expo – A Quick Guide

## What is `npx`?

`npx` is a command-line utility that comes with **Node.js** (v5.2.0 and up). It allows you to **run Node.js packages without installing them globally**. This is especially useful for tools like Expo where you may want to avoid version conflicts or unnecessary global installs.

---

## 📦 What Does This Mean for Expo?

Instead of installing Expo tools globally with:

```bash
npm install -g create-expo-app
```

You can use `npx` like this:

```bash
npx create-expo-app myApp
```

### Explanation:
- **`npx`** → Runs the tool directly from the npm registry
- **`create-expo-app`** → Official Expo project scaffolding tool
- **`myApp`** → Your new project’s directory name

---

## 🛠 Example Workflow

```bash
# 1. Create a new Expo app
npx create-expo-app myCoolProject

# 2. Navigate to your project
cd myCoolProject

# 3. Start the development server
npx expo start
```

---

## ✅ Benefits of Using `npx`

| Use Case                            | Why Use `npx`                      |
|-------------------------------------|------------------------------------|
| First-time project setup            | ✔ No global install needed         |
| Always get the latest tool version  | ✔ Pulls directly from npm          |
| Cleaner development environment     | ✔ Avoids cluttering global space   |
| CI/CD and scripting                 | ✔ Great for automation             |

---

## 🧠 Bonus Tip: Global vs `npx`

| Situation                       | Recommendation      |
|----------------------------------|---------------------|
| Temporary or one-time usage      | Use `npx`           |
| Repeated local use               | Consider global install |
| Working in CI/CD environments    | Use `npx`           |
| Want latest version every time   | Use `npx`           |

---

## 🧭 Related Resources

- [Expo Documentation](https://docs.expo.dev/)
- [npx on npm Docs](https://docs.npmjs.com/cli/v9/commands/npx)

---

## 📂 Optional: Update `.zshrc` for Expo

If you use Expo regularly, consider adding this to your `~/.zshrc`:

```zsh
# Add Expo CLI tools to PATH
export PATH="$HOME/.npm-global/bin:$PATH"

# Optional Alias
alias expostart="npx expo start"
```

Then reload your terminal:

```bash
source ~/.zshrc
```

---

_This guide was created for quick reference and is suitable for new React Native developers working with Expo and Zsh-based environments._
