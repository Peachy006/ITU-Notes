Here line is the string


 StringTokenizer st = new StringTokenizer(line);

        while (st.hasMoreTokens()) {
            String word = st.nextToken();           // one word at a time
            System.out.println("Word: " + word);
        }


    