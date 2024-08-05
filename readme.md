# Мой тестовый проект
## Пробуем маркдаун

Курсив _я текст_ и я **жирный**

# Я заголовок
## Я заголовок поменьше
### Я заголовок еще поменьше

## Ща будет код

'''
public class Solution {
    public bool IsValid(string s) {
        Dictionary<char, char> bracketPairs = new Dictionary<char, char> {
            {')', '('},
            {'}', '{'},
            {']', '['}
        };
        Stack<char> stack = new Stack<char>();
        foreach(char c in s) {
            if (bracketPairs.ContainsKey(c)) {
                char topElement = stack.Count == 0 ? '#' : stack.Pop();
                if (topElement != bracketPairs[c]) {
                    return false;
                }
            }
            else {
                stack.Push(c);
            }
        }
        return stack.Count == 0;
    }
}
'''