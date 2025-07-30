# 🧪 Postgresql Helm Chart

This repository hosts a Helm chart for deploying postgresql using the custom Bitnami Helm chart as a base.

---

## 📦 How This Chart Was Packaged

### 1. Pull the Bitnami Chart

```bash
helm pull bitnami/postgresql --untar
```

### 2. Package the Chart

```bash
helm package postgresql --destination charts/
```

### 3. Generate `index.yaml`

```bash
helm repo index charts/ --url https://hardikpatel29.github.io/postgresql-chart
```

### 4. Move Files to `docs/` Directory

```bash
mkdir -p docs
cp charts/* docs/
```

### 5. Push to GitHub

```bash
git add .
git commit -m "Add packaged chart and index"
git push origin master
```

---

## 🌐 Enable GitHub Pages

1. Go to your GitHub repository.
2. Navigate to **Settings** → **Pages**.
3. Under **Source**, choose:
   - **Branch**: `main`
   - **Folder**: `/docs`
4. Click **Save**.

> This will publish your Helm chart repo at:  
> `https://hardikpatel29.github.io/postgresql-chart/`

---

## 🚀 How to Use This Helm Repository

### Add the Repository

```bash
helm repo add postgresql https://hardikpatel29.github.io/postgresql-chart/
```

### Update Repositories

```bash
helm repo update
```

### Search Charts

```bash
helm search repo postgresql
```

---


