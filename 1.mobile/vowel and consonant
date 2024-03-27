%{
#include <stdio.h>
int vowel_count = 0;
int consonant_count = 0;
%}

%%
[aeiouAEIOU]    { vowel_count++; }
[a-zA-Z]        { consonant_count++; }
.|\n            ;

%%

int main() {
    char sentence[1000];
    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);

    // Call the scanner to count vowels and consonants
    yy_scan_string(sentence);
    yylex();

    printf("Number of vowels: %d\n", vowel_count);
    printf("Number of consonants: %d\n", consonant_count);

    return 0;
}

int yywrap() {
    return 1;
}
