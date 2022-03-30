*Yodgorov Ahborkhuja*
  =====================
  ### Live in: *Tashkent,Uzbekistan*
   ********************************
   ### Email: **axbor.yodogorov@gmail.com**
   ### Telegram: **@AhborYodgorov**
   ### Discord: **Ahbor (@Ahborkhuja)**
***I'm 18 yeaars old. I study in bachelor's first degree on Software Engineering field.
I have the experience in programming. And I also very interested in what happens inside of OS and Web-severs. Also solve some problems from leetcode in diffrent languages.In general, I'm person who likes self-studying and I'm not participate to some kind of courses or trannings. Also I have IELTS 6.0 and now I study in university where they teach in English and that's cool.***
#### Fields in which I have an experience:
* C++
* HTML
* Java

[That's link to site with problem](https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/)
```
class Solution {
    public List<Integer> findDisappearedNumbers(int[] nums) {
        List<Integer> missing = new ArrayList<>();
        if (nums == null || nums.length == 0) return missing;
        int i=0;
        int seen = 0;

        while (seen < nums.length) {
            if (nums[i] == i+1) {
                i = (i+1) % nums.length;
                seen++;
            } else {
                int j = nums[i] - 1;
                if (nums[i] == nums[j]) {
                    i = (i+1) % nums.length;
                    seen++;
                } else {
                    int tmp = nums[j];
                    nums[j] = nums[i];
                    nums[i] = tmp;
                }
            }
        }
        for (int j=0; j<nums.length; j++) {
            if (nums[j] != j+1) missing.add(j+1);
        }

        return missing;
    }
}
```
