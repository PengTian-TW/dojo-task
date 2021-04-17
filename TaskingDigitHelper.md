1. Test 1: **input 1 -> output 1**
    **Code**
    ```
    int sum = 1;
     return sum;
     ```
    **TestCase:**
    ```
    ```
    @Test
    void should_return_1_in_the_string(){
    assertEquals(1, DigitsHelper.sumDigits("1"));}
    ```
    **Test result**
2. Test 2 **input a -> output 0**
    **Code**
    ```
    int sum = 0;
	if(text=="a") {
    		return sum;
	}else{
    		return 1;
	}
	```
    **TestCase**
    ```
    @Test
	void should_return_0_in_the_string() {
    	assertEquals(0, DigitsHelper.sumDigits(“a"));}
	```
    **Test result**
3. Test 3 **input 1a -> output 1**
    **Code**
    ```
    int sum = 0;
    	for (int i = 0; i < text.length(); i++) {
        if(text.charAt(i)==(int)('1')){
            sum += 1;
        }else {
            sum += 0;
        }
    	}
    	return sum;
	}
	```
    **TestCase**
    ```
    @Test
    void should_return_number_in_the_string() {
    assertEquals(1, DigitsHelper.sumDigits("1a"));}
    ```
    **Test result**
4. Test 4 **input 1a2b -> output 3**
    **Code**
    ```
    int sum = 0;
    for (int i = 0; i < text.length(); i++) {
    if(text.charAt(i)>=(int)('0') && text.charAt(i)<=(int)('9')){
        sum += (int) text.charAt(i) - (int) ('0');
    }
    }
    return sum;
    ```
    **TestCase**
    ```
    @Test
    void should_return_two_sum_of_numbers_when_mixed_with_other_characters() {
    assertEquals(6, DigitsHelper.sumDigits("5a1b"));}
    ```
    **Test result**
5. Test 5 **input “”(empty) ->output 0**
    **Code**
    ```
    int sum = 0;
    for (int i = 0; i < text.length(); i++) {
    if(text.charAt(i)>=(int)('0') && text.charAt(i)<=(int)('9')){
        sum += (int) text.charAt(i) - (int) ('0');
    }
    }
    return sum;
    ```
    **TestCase**
    `@Test
    void should_return_zero_if_there_is_no_number() {
    assertEquals(0, DigitsHelper.sumDigits(""));
    }`
    **Test result**
6. Test 6 **input null->output IllegalArgumentException**
    **Code**
    ```
    if(text==null){
   	 throw new IllegalArgumentException("Illegal input.");
	}
	int sum = 0;
	for (int i = 0; i < text.length(); i++) {
    	if(text.charAt(i)>=(int)('0') && text.charAt(i)<=(int)('9')){
        sum += (int) text.charAt(i) - (int) ('0');
    }
	}
	return sum;
	}
	```
    **TestCase**
    ```
    @Test
	void should_throw_if_text_is_null() {assertThrows(IllegalArgumentException.class,() -> DigitsHelper.sumDigits(null));}
	```
    **Test result**

