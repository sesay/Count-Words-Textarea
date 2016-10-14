# Count-Words-Textarea
Counts words in TextArea


$('textarea').keyup(function () {
            var wordArray = this.value.split(/[\s\.\?]+/); //Split based on regular expression for spaces
            var maxWords = 5; //max number of words
            var total_words = wordArray.length; //current total of words
            var newString = "";
            //Roll back the textarea value with the words that it had previously before the maximum was reached
            if (total_words > maxWords+1) {
                 for (var i = 0; i < maxWords; i++) {
                    newString += wordArray[i] + " ";
                }
                this.value = newString;
            }

        });
