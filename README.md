	#include<stdio.h>
	#include<unistd.h>

    int main()
    {
    
    char name[30],section,grade;
    int standard,mathsScore,englishScore,hindiScore,scienceScore,sscScore,totalScore;
    
    printf("\n______________________________________________________\n");
    printf("____________REPORT CARD APP GENERATOR_________________\n");
    printf("______________________________________________________\n\n");
    
    sleep(3);
	printf("\nEnter your name:\n");
	scanf("%[^\n]%*c",name);
	
	printf("\nEnter your standard in which you are studing:");
	scanf("%d",&standard);
	
	printf("\nEnter your section in which you are studing:");
	scanf("%c",&section);
	while ((getchar()) != '\n');
	
	puts("\nEnter marks secured in Mathematics: ");
    scanf("%d", &mathsScore);

    puts("\nEnter marks secured in English: ");
    scanf("%d", &englishScore);

    puts("\nEnter marks secured in Hindi: ");
    scanf("%d", &hindiScore);

    puts("\nEnter marks secured in Science: ");
    scanf("%d", &scienceScore);

    puts("\nEnter marks secured in Social Science: ");
    scanf("%d", &sscScore);

    totalScore = mathsScore + englishScore + hindiScore + scienceScore + sscScore;
    
     if (totalScore > 500 || totalScore < 0) {
    	puts("Total score cannot not be greater than 500. Please try again!");
    	exit(0);
    }
    
      if (totalScore >= 450 && totalScore <= 500) {
        grade = 'A';
    } else if (totalScore >= 400 && totalScore < 450) {
        grade = 'B';
    } else if (totalScore >= 350 && totalScore < 400) {
        grade = 'C';
    } else if (totalScore >= 300 && totalScore < 350) {
        grade = 'D';
    } else if (totalScore >= 200 && totalScore < 300) {
        grade = 'E';
    } else { 
        grade = 'F';
    }
    
    puts("\nGenerating Report Card! Please wait.... ");
    sleep(3);
	
	puts("------------------------------------------\n");
    puts("\tJawahar Navodaya Vidyalaya \n");
    puts("\t    Annual Report Card \n");

    printf("\tName: %s \n", name);
    printf("\tStandard: %d \n", standard);
    printf("\tSection: %c \n", section);

    puts("\n\tMarks Secured out of 100\n");

    printf("\tMathematics: %d \n", mathsScore);
    printf("\tEnglish: %d \n", englishScore);
    printf("\tHindi: %d \n", hindiScore);
    printf("\tScience: %d \n", scienceScore);
    printf("\tSocial Science: %d \n", sscScore);

    printf("\n\tTotal marks secured: %d \n", totalScore);

    printf("\tGrade: %c \n", grade);
    puts("------------------------------------------\n");

	return 0;
	} 
