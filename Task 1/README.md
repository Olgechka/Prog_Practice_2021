Код програми з поясненням
import re #модуль для роботи з постійними виразами

str = input("\nВведіть рядок: ")
word = ''.join([i for i in str if not i.isdigit()]) #генератор списку з умовою та приєднанням елементів
nums = re.findall(r'\d+', str) #надає змогу в пошуку усіх збігів з шаблоном string, тобто цілі числа
nums = [int(i) for i in nums] #генератор списку з додаванням цілих чисел

print("\nРядок без чисел:", word)
print("Числа з рядка:", nums)

WithLarge = ' '.join(word[0].upper() + word[1:-1] + word[-1:].upper() for word in word.split()) #утворення великих літер за допомогою функції пошуку по словам
print("\nРядок після змін:", WithLarge)

nums.remove(max(nums)) #видаляє максимальне значення в масиві чисел nums
numberIndex = [nums[i]**i for i in range(0,len(nums))] #генератор списку з піднесенням масиву чисел до степеню за їхнім індексом

print("Масив чисел в степені за їхнім індексом:", numberIndex)
print("\n")


Результ виконання програм
![image](https://user-images.githubusercontent.com/86926470/124712383-ef732d00-df07-11eb-8a0e-05c5fe1f3cf8.png)


Джерела

![image](https://user-images.githubusercontent.com/86926470/124712916-8d66f780-df08-11eb-8572-bcc04447ccb5.png)
 Посилання: https://tproger.ru/translations/regular-expression-python/ 
 
 https://stackoverflow.com/questions/32930246/python-for-loops-for-i-in-range0-lenlist-vs-for-i-in-list 
