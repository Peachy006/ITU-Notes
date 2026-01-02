Når du skal vende en string om skal man først have følgende:

din string
den string du skaber
og en tom char som du kan bruge til at midlertidigt gemme din character du er nået til

        String s = "Geeks"; 
        String r = "";
        char ch;

        for (int i = 0; i < s.length(); i++) {
          	
          	// extracts each character
            ch = s.charAt(i);
          
          	// adds each character in
            // front of the existing string
            r = ch + r; 
        }
      
        System.out.println(r);
    }
}