# No-6th-Day
"I might be back... but the duplicates won’t be."
# no_6thday.py

> _"I might be back... but the duplicates won’t be."_

This script eliminates duplicate entries from a plain text file, saving a clean, unique list to a new file. Named after the 2000 Schwarzenegger movie "The 6th Day," because you *only need one copy*, not clones. 🧬💀

---

### 📜 What It Does
- Reads `duplicates.txt`
- Splits content by line
- Converts list to a `set()` to remove duplicates
- Writes unique values to `unique.txt`

---

### 🐍 Example Usage
```bash
python no_6thday.py
```

**Input file (`duplicates.txt`):**
```
apple
banana
apple
orange
banana
```

**Output file (`unique.txt`):**
```
orange
banana
apple
```
(Note: Set order is not guaranteed)

---

### 🧠 Why It's Funny
You’ve seen "The 6th Day" — and if you haven’t, just know this script is what happens when you *actually* say no to cloning.

---

### 💬 One-Liner
"This ain’t your grandma’s list cleaner — it’s a Schwarzenegger-approved duplicate deleter."

---

### 🛠️ Code
```python
with open('duplicates.txt', 'r') as file:
    data = file.read()
    data_list = data.split('\n')
    unique_list = list(set(data_list))
    unique_data = "\n".join(unique_list)

with open('unique.txt', 'w') as file:
    file.write(unique_data)
```

---

### 🔥 Pro Tip
Wanna preserve order? Use `dict.fromkeys()` instead of `set()`:
```python
unique_list = list(dict.fromkeys(data_list))
```
Because sometimes the order *does* matter — just not to Arnold.

---

📂 Part of the **Pointless Scripts Collection™** — because why not automate things you’ll only do once. ❤️
