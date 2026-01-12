def longestCommonPrefix(strs):
    if not strs:
        return ""

    prefix = strs[0]

    for s in strs[1:]:
        while not s.startswith(prefix):
            prefix = prefix[:-1]
            if prefix == "":
                return ""

    return prefix


# -------- Main Program --------
n = int(input("Enter number of strings: "))
strs = []

for i in range(n):
    s = input(f"Enter string {i+1}: ")
    strs.append(s)

result = longestCommonPrefix(strs)

print("Longest Common Prefix:", result)
