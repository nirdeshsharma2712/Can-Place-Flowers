# 📊 LeetCode Problem: Can Place Flowers

## 🧩 Problem Statement

You have a **long flowerbed** in which some of the plots are **planted**, and some are not. However, flowers cannot be planted in **adjacent plots**.
Given an **integer** array `flowerbed`, return `true` if n new **flowers** can be planted in the flowerbed without violating the **no-adjacent**-flowers rule and `false` otherwise.

> **Note :**
> - containing `0's` and `1's`, where `0` means empty and `1` means not empty, and an integer `n`



## 🧠 Approach: Greedy + Edge Case Handling

- Special case: If the **flowerbed** has only one plot and it's **empty**, plant directly.

- First plot check: If the first **two** plots are empty, plant one.

- Traverse **mid** plots:

> - If current, previous, and next plots are `0`, plant one and mark it as `1`.
> - Last plot check: If the last two plots are **empty**, plant one.

- Count each **planted** flower — if `count ≥ n`, return `true`.



## ✅ Example Walkthrough

### Example 1

##### Input: flowerbed = [1,0,0,0,1], n = 1
##### Output: true


### Example 2

##### Input: flowerbed = [1,0,0,0,1], n = 2
##### Output: false



## 🛠️ Constraints

- `1 <= flowerbed.length <= 2 * 10^4`
- `flowerbed[i]` is `0` or `1`
- There are no two adjacent flowers in `flowerbed`.
- `0 <= n <= flowerbed.length`
