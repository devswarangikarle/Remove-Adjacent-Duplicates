# Remove-Adjacent-Duplicates

You’ve found an ancient parchment with a mysterious string of letters, but it appears cluttered with pairs of adjacent repeating characters. To reveal its true message, you need to clean up the string by removing any consecutive duplicate letters until no two adjacent characters are the same. Can you simplify the string to uncover the hidden message?

def simplify_string(s):

    stack = []
    for c in s:
        if stack and stack[-1] == c:
            continue
        else:
            stack.append(c)
    return ''.join(stack)

if __name__ == "__main__":
    s = input().strip()
    result = simplify_string(s)
    print(result)
