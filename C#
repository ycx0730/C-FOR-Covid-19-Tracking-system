#include<stdio.h>
#include<stdlib.h>
#include<ctype.h>
#pragma warning(disable:4996)

//FUNCTION DECLARATION : 
//FIRST DAY IS FIRST DAY CASES
//INPUT CASES FOR USER TYPE HOW MANY OF CASES IN THAT DAY
//CASE TRACKING FOR CALCULATE AND TRACK ALL TOTAL DAY  
void firstDay();
void inputCases();
void casesTracking();

//GLOBAL DECLARATION
int numOfLocalCases, numOfImportCases, numOfTotalNewCases;
int numOfDeaths, numOfRecovered;

//DECLARE AN CONSTANT INT VARIABLE TO ACCUMULATE THE NUMBERS
const int day1Cases = 9;
const int day1TotalCases = 100;
const int day1TotalDeaths = 2;
const int day1TotalRecovered = 10;
const int day1UnderTreatment = 88;
double day1DeathRate, day1RecoveredRate, day1UnderTreatmentRate;

//DECLARE AN INT VARIABLE TO ACCUMULATE THE NUMBERS
int day = 1;

void main() {

	//DECLARE AN INT VARIABLE TO ACCUMULATE THE NUMBERS
	int selection = 0;
	int mysteryNumber = 0;
	int mysteryNumber2 = 0;
	
	//USE A LOOP REPEATEDLY VALIDATIE IS CORRECT NUMBER OR NOT
	do {
		//CLEAR SCREEN FUNCTIONALITY
		system("cls");

		//STARTING POINT FOR GOING ON TO NEXT LEVEL
		printf("******************************************************************\n");
		printf("C O R O N A V I R U S   C A S E S   T R A C K I N G   S Y S T E M\n");
		printf("******************************************************************\n\n");
		printf("1 ----->  STARTING INPUT CASES\n\n");
		printf("2 ----->  EXIT\n\n");
		printf("3 ----->  MYSTERY ENTRY\n\n");

		//PROMPT USER FOR AN CHOICE
		printf("ENTER YOUR CHOICE >>> ");
		scanf("%d", &selection);
		rewind(stdin);

		switch (selection) {

		case 1:
	        //CALLING FUNCTION
			firstDay();
			casesTracking();
			break;

		case 2:

			printf("\nWISH YOU HAVE A NICE DAY <3 <3\n\n");
			break;
		
		case 3:

			//JUST A JOKE LIKES A GAME
			//PROMPT USER FOR 2 NUMBER
			printf("\nENTER 2 NUMBER AT THE SAME TIME [ 3 OR 6 ]\n\n");

			printf("ENTER MYSTERY NUMBER >>> ");
			scanf("%d %d", &mysteryNumber,&mysteryNumber2);

			//CHECK THE VARIABLE MYSTERYNUMBER CONDITION
			if (mysteryNumber && mysteryNumber2 == 3) {
				//CALLING FUNCTION
				firstDay();
				casesTracking();
			}
			else if (mysteryNumber && mysteryNumber2 == 6) {
				printf("\nJUST A JOKE ^_^ YOU MAY TRY TO TYPE NUMBER 3 AT THE SAME TIME\n\n");
			}
			else if (mysteryNumber && mysteryNumber2 != 3 && mysteryNumber && mysteryNumber2 != 6) {
				printf("\nNOTHING !!! YOU MAY TRY TO TYPE ANOTHER NUMBER <3\n\n");
			}
			break;	
		}

	} while (selection != 1 && selection != 2 && selection != 3);

	system("pause");
}

void firstDay() {

	//CLEAR SCREEN FUNCTIONALITY
	system("cls");

	//DAY 1 COMPUTATION  
	day1DeathRate = day1TotalCases * day1TotalDeaths / 100;
	day1RecoveredRate = day1TotalCases * day1TotalRecovered / 100;
	day1UnderTreatmentRate = day1TotalCases * day1UnderTreatment / 100;

	//DISPLAY DAY 1 AMOUNT CASES
	printf(">>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>[  COVID-19 CASES Tracking System  ]<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<\n\n");
	printf("\tFirst day amount - (Day 1) : \n");
	printf("+-------------------+-------------------++------------------+-------------------+------------------+\n");
	printf("|     First day     |      Total        ||      Total       |      Total        |      Under       |\n");
	printf("|       Cases       |      Cases        ||      Deaths      |     Recovered     |     Treatment    |\n");
	printf("+-------------------+-------------------++------------------+-------------------+------------------+\n");
	printf("|        %3d        |        %3d        ||        %3d       |        %3d        |        %3d       |\n", day1Cases, day1TotalCases, day1TotalDeaths, day1TotalRecovered, day1UnderTreatment);
	printf("+---------------------------------------++---------------------------------------------------------+\n");
	printf("                                        ||   %7.1lf%%       |    %7.1lf%%       |   %7.1lf%%       |\n", day1DeathRate, day1RecoveredRate, day1UnderTreatmentRate);
	printf("                                        ++---------------------------------------------------------+\n\n");

}

void inputCases() {

	//VARIABLE DECLARATION
	numOfLocalCases = 0;
	numOfImportCases = 0;
	numOfDeaths = 0;
	numOfRecovered = 0;

	//STARTING INPUT CASES IN WHAT DAY
	printf("[ Day %d ]\n\n", day);
	printf("Key in New Day DATA:\n");

	do {

		printf("    Number of New Local CASES       : ");
		scanf("%d", &numOfLocalCases);
		rewind(stdin);

		while(numOfLocalCases <= -1 && numOfLocalCases >= -9999) {

			if (numOfLocalCases != 0) {
				
				numOfLocalCases = 0;

				printf("\n    PLEASE ENTER DIGIT TO PROCEED AND NOT NEGATIVE DIGIT <3\n\n");
			}
		} 

		//VALIDATING USER IS INPUTING NUMBER OR NOT
	} while (numOfLocalCases == 0 );
		
	do {

		printf("    Number of New Imported CASES    : ");
		scanf("%d", &numOfImportCases);
		rewind(stdin);

		while (numOfImportCases <= -1 && numOfImportCases >= -999) {
			if (numOfImportCases != 0) {
				numOfImportCases = 0;

				printf("\n    PLEASE ENTER DIGIT TO PROCEED AND NOT NEGATIVE DIGIT <3\n\n");
			}
		}

		//VALIDATING USER IS INPUTING NUMBER OR NOT
	} while (numOfImportCases == 0);

	//CALCULATION
	numOfTotalNewCases = numOfLocalCases + numOfImportCases;

	printf("    Total Number of New CASES       = %d ", numOfTotalNewCases);
	printf("        ( INCREASED by 1 from YESTERDAY )\n");

	do {

		printf("Number of DEATHS    = ");
		scanf("%d", &numOfDeaths);
		rewind(stdin);

		while (numOfDeaths <= -1 && numOfDeaths >= -999) {
			if (numOfDeaths != 0) {
				numOfDeaths = 0;

				printf("\nPLEASE ENTER DIGIT TO PROCEED AND NOT NEGATIVE DIGIT <3\n\n");
			}
		}

		//VALIDATING USER IS INPUTING NUMBER OR NOT
	} while (numOfDeaths == 0);

	do {

		printf("Number of RECOVERED = ");
		scanf("%d", &numOfRecovered);
		rewind(stdin);

		while (numOfRecovered <= -1 && numOfRecovered >= -999) {
			if (numOfRecovered != 0) {
				numOfRecovered = 0;

				printf("\nPLEASE ENTER DIGIT TO PROCEED AND NOT NEGATIVE DIGIT <3\n\n");
			}
		}

		//VALIDATING USER IS INPUTING NUMBER OR NOT
	} while (numOfRecovered == 0);

}

void casesTracking() {

	//VARIABLE DECLARATION
	//SUMMARY REPORT
	//ACCUMULATE VALUE
	int sReportCases = 0;
	int sReportTotalCases = 0, sReportTotalDeaths = 0, sReportTotalRecovered = 0, sReportUnderTreatment = 0;
	double sReportDeathRate, sReportRecoveredRate, sReportUnderTreatmentRate;

	int newDayCases = 0, newDayTotalCases = 0, newDayTotalDeath = 0, newDayTotalRecovered = 0, newDayUnderTreatment = 0;
	double newDayDeathRate = 0, newDayRecoveredRate = 0, newDayUnderTreatmentRate = 0;

	//COMPARATIVE REPORT
	//ACCUMULATE VALUE
	int cReportYesterdayNewCases = 0, cReportTodayNewCases = 0, cReportDifferenceNewCases = 0;
	int cReportYesterdayTotalCases = 0, cReportTodayTotalCases = 0, cReportDifferenceTotalCases = 0;
	double cReportYesterdayDeathRate = 0, cReportTodayDeathRate = 0, cReportDifferenceDeathRate = 0;
	double cReportYesterdayRecoveryRate = 0, cReportTodayRecoveryRate = 0, cReportDifferenceRecoveryRate = 0;
	double cReportYesterdayUnTreatRate = 0, cReportTodayUnTreatRate = 0, cReportDifferenceUnTreatRate = 0;
	int cReportYesterday = 1, cReportToday = 2;

	//ASSIGN VALUE
	int highestNumberCases = day1Cases, lowestNumberCases = day1Cases;
	int dayOfHighestCases = 0, dayOfLowestCases = 0;

	int defaultDay = 2, lastDay = 1, totalDayRecorded;

	char continueToNextDay;
	int reportType;

	//USE A LOOP REPEATEDLY WANT TO CONTINUE NEXT DAY OR NOT
	do {
		//USE A LOOP REPEATEDLY WANT TO CONTINUE NEXT DAY OR NOT
		do {
			//CALLING FUNCTION
			day++;
			inputCases();
		
			//CHECK THE DAY CONDITION
			if (day == 2) {
				//ASSIGN VALUE
				sReportCases = numOfTotalNewCases;
				sReportTotalCases = day1TotalCases + numOfTotalNewCases;
				sReportTotalDeaths = day1TotalDeaths + numOfDeaths;
				sReportTotalRecovered = day1TotalRecovered + numOfRecovered;
			}
			else if (day > 2 && day < 10) {
				//ASSIGN VALUE
				sReportCases = numOfTotalNewCases;
				sReportTotalCases += numOfTotalNewCases;
				sReportTotalDeaths += numOfDeaths;
				sReportTotalRecovered += numOfRecovered;
			}
			if (day1Cases > numOfTotalNewCases) {
				lowestNumberCases = numOfTotalNewCases;
				dayOfLowestCases = day;
			}
			//CALCULATION FOR SUMMARY REPORT
			sReportUnderTreatment = sReportTotalCases - sReportTotalDeaths - sReportTotalRecovered;
			sReportDeathRate = (double)sReportTotalDeaths / (double)sReportTotalCases * 100;
			sReportRecoveredRate = (double)sReportTotalRecovered / (double)sReportTotalCases * 100;
			sReportUnderTreatmentRate = (double)sReportUnderTreatment / (double)sReportTotalCases * 100;

			//USE A LOOP REPEATEDLY VALIDATIE IS CORRECT NUMBER OR NOT
			do {
				//SET THE VALUE TO 0
				reportType = 0;

				//PROMPT USER FOR AN REPORT
				printf("\n1. Daily Summary REPORT |>  2. Daily Comparative REPORT |>\n");
				printf("What type of REPORT would you like to view >  ");
				scanf("%d", &reportType);
				rewind(stdin);

				//CHECK THE VARIABLE REPORTTYPE CONDITION
				if (reportType != 1 && reportType != 2) {
					printf("\nPLEASE ENTER 1 OR 2 TO PROCEED <3\n");
				}

			} while (reportType != 1 && reportType != 2);

			if (reportType == 1) {

				//DAILY SUMMARY REPORT
				printf("\n                              Daily Summary Report [ Day %d ] :\n", day);
				printf("+-------------------+-------------------++------------------+-------------------+------------------+\n");
				printf("|      Today's      |      Total        ||      Total       |       Total       |       Under      |\n");
				printf("|      Cases        |      Cases        ||      Deaths      |     Recovered     |     Treatment    |\n");
				printf("+-------------------+-------------------++------------------+-------------------+------------------+\n");
				printf("|      Local   %3d  |                   ||                  |                   |                  |\n", numOfLocalCases);
				printf("|     imported %3d  |                   ||                  |                   |                  |\n", numOfImportCases);
				printf("|              %3d  |       %-4d        ||       %3d        |        %3d        |       %3d        |\n", sReportCases, sReportTotalCases, sReportTotalDeaths, sReportTotalRecovered, sReportUnderTreatment);
				printf("+---------------------------------------++---------------------------------------------------------+\n");
				printf("                                        ||   %6.1f%%        |     %6.1f%%       |    %6.1f%%       |\n", sReportDeathRate, sReportRecoveredRate, sReportUnderTreatmentRate);
				printf("                                        ++---------------------------------------------------------+\n");
				printf("---------------------------------<>  End of Day %d Reporting  <>------------------------------------\n\n", day);
			}
			//CHECK THE DAY CONDITION
			if (cReportYesterday == 1) {
				//ASSIGN VALUE
				cReportYesterdayNewCases = day1Cases;
				cReportYesterdayTotalCases = day1TotalCases;
				cReportYesterdayDeathRate = day1DeathRate;
				cReportYesterdayRecoveryRate = day1RecoveredRate;
				cReportYesterdayUnTreatRate = day1UnderTreatmentRate;
			}

			if (cReportYesterday >= 2) {
				cReportYesterdayNewCases = cReportTodayNewCases;
				cReportYesterdayTotalCases = cReportTodayTotalCases;
				cReportYesterdayDeathRate = cReportTodayDeathRate;
				cReportYesterdayRecoveryRate = cReportTodayRecoveryRate;
				cReportYesterdayUnTreatRate = cReportTodayUnTreatRate;
			}

			//CALCULATION FOR COMPARATIVE REPORT
			cReportTodayNewCases = numOfTotalNewCases;
			cReportTodayTotalCases = sReportTotalCases;
			cReportTodayDeathRate = (double)sReportTotalDeaths / (double)sReportTotalCases * 100;
			cReportTodayRecoveryRate = (double)sReportTotalRecovered / (double)sReportTotalCases * 100;
			cReportTodayUnTreatRate = (double)sReportUnderTreatment / (double)sReportTotalCases * 100;
			
			//CHECK THE REPORTTYPE CONDITION
			if (reportType == 2) {

				//CALCULATION FOR COMPARATIVE REPORT
				cReportDifferenceNewCases = cReportTodayNewCases - cReportYesterdayNewCases;
				cReportDifferenceTotalCases = cReportTodayTotalCases - cReportYesterdayTotalCases;
				cReportDifferenceDeathRate = cReportTodayDeathRate - cReportYesterdayDeathRate;
				cReportDifferenceRecoveryRate = cReportTodayRecoveryRate - cReportYesterdayRecoveryRate;
				cReportDifferenceUnTreatRate = cReportTodayUnTreatRate - cReportYesterdayUnTreatRate;

				printf("\n");

				//DAILY COMPARATIVE REPORT
				printf("                            +-----------------+-----------------++---------------+\n");
				printf("                            |    YESTERDAY    |      TODAY      ||   DIFFERENCE  |\n");
				printf("                            |     Day%3d      |      Day%3d     ||               |\n", cReportYesterday, cReportToday);
				printf("+---------------------------+-----------------+-----------------++---------------+\n");
				printf("|       New Cases           |       %-4d      |       %-4d      ||     [ %-4d]   |\n", cReportYesterdayNewCases, cReportTodayNewCases, cReportDifferenceNewCases);
				printf("+---------------------------+-----------------+-----------------++---------------+\n");
				printf("|       Total Cases         |       %-4d      |       %-4d      ||     [ %-4d]   |\n", cReportYesterdayTotalCases, cReportTodayTotalCases, cReportDifferenceTotalCases);
				printf("+---------------------------+-----------------+-----------------++---------------+\n");
				printf("|       Death Rate          |    %6.1f%%      |    %6.1f%%      ||   [%+6.1f%%]   |\n", cReportYesterdayDeathRate, cReportTodayDeathRate, cReportDifferenceDeathRate);
				printf("+---------------------------+-----------------+-----------------++---------------+\n");
				printf("|       Recovery Rate       |    %6.1f%%      |    %6.1f%%      ||   [%+6.1f%%]   |\n", cReportYesterdayRecoveryRate, cReportTodayRecoveryRate, cReportDifferenceRecoveryRate);
				printf("+---------------------------+-----------------+-----------------++---------------+\n");
				printf("|  Under Treatment Rate     |    %6.1f%%      |    %6.1f%%      ||   [%+6.1f%%]   |\n", cReportYesterdayUnTreatRate, cReportTodayUnTreatRate, cReportDifferenceUnTreatRate);
				printf("+---------------------------+-----------------+-----------------++---------------+\n\n");
				printf("***-----------------------*** End of Day %d Reporting ***----------------------***\n\n", day);

			}

			//USE A LOOP REPEATEDLY VALIDATIE IS CORRECT NUMBER OR NOT
			do {
				rewind(stdin);
				//PROMPT USER FOR CONTINUE TO NEXT DAY
				printf("Continue to next day ? Yes OR No : ");
				scanf("%c", &continueToNextDay);

				if (continueToNextDay != 'Y' && continueToNextDay != 'N' && continueToNextDay != 'y' && continueToNextDay != 'n') {
					printf("PLEASE ENTER Y , y , N , n TO PROCEED <3\n\n");
				}
		    
			} while (continueToNextDay != 'Y' && continueToNextDay != 'N' && continueToNextDay != 'y' && continueToNextDay != 'n');

			//CHECK CONDITION
			if (continueToNextDay != 'N' && continueToNextDay != 'n') {	

				if (day == 2) {
					newDayCases = day1Cases;
				}
				else if (day > 2 && day <= 10) {
					newDayCases = 0;

					newDayCases += newDayTotalCases;
				}

				/*CALCULATION FOR NEW DAY*/
				newDayTotalCases = numOfTotalNewCases;
				newDayTotalDeath = numOfDeaths;
				newDayTotalRecovered = numOfRecovered;
				newDayUnderTreatment = newDayTotalCases - newDayTotalDeath - newDayTotalRecovered;
				newDayDeathRate = (double)newDayTotalDeath / (double)newDayTotalCases * 100;
				newDayRecoveredRate = (double)newDayTotalRecovered / (double)newDayTotalCases * 100;
				newDayUnderTreatmentRate = (double)newDayUnderTreatment / (double)newDayTotalCases * 100;

				printf("\n                              Yesterday's amount - (Day %d) : \n", day);
				printf("+-------------------+-------------------++------------------+-------------------+------------------+\n");
				printf("|    Yesterday's    |      Total        ||      Total       |      Total        |      Under       |\n");
				printf("|      Cases        |      Cases        ||      Deaths      |     Recovered     |     Treatment    |\n");
				printf("+-------------------+-------------------++------------------+-------------------+------------------+\n");
				printf("|       %3d         |        %3d        ||        %3d       |       %3d         |       %3d        |\n", newDayCases, newDayTotalCases, newDayTotalDeath, newDayTotalRecovered, newDayUnderTreatment);
				printf("+---------------------------------------++---------------------------------------------------------+\n");
				printf("                                        ||    %6.1f%%       |    %6.1f%%        |    %6.1f%%       |\n", newDayDeathRate, newDayRecoveredRate, newDayUnderTreatmentRate);
				printf("                                        ++---------------------------------------------------------+\n\n");

				/*ASSIGN VALUE*/
				if (newDayCases < lowestNumberCases) {
					lowestNumberCases = newDayCases;
					dayOfLowestCases = day;
				}
				if (newDayCases > highestNumberCases) {
					highestNumberCases = newDayCases;
					dayOfHighestCases = day;
				}
			    if (newDayTotalCases > highestNumberCases) {
					highestNumberCases = newDayTotalCases;
					dayOfHighestCases = day;
				}
				if (newDayTotalCases < lowestNumberCases) {
					lowestNumberCases = newDayCases;
					dayOfLowestCases = day;
				}
				if (numOfTotalNewCases > newDayTotalCases) {
					highestNumberCases = numOfTotalNewCases;
					dayOfHighestCases = day;
				}
				else if (numOfTotalNewCases < newDayTotalCases) {
					lowestNumberCases = numOfTotalNewCases;
					dayOfHighestCases = day;
				}
				if (day1Cases > numOfTotalNewCases) {
					lowestNumberCases = numOfTotalNewCases;
					dayOfHighestCases = day;
				}
				if (cReportYesterday == 1) {
					if (numOfTotalNewCases > day1Cases) {
						highestNumberCases = numOfTotalNewCases;
					}
				}
			}
			if (day == 10) {
				printf("THAT'S ALL DAY OF CASE TRACKING <3\n");
				printf("I HOPE YOU ENJOYED THIS PROGRAM <3\n\n");
			}

			/*INCREMENT VALUE*/
			cReportYesterday++;
			cReportToday++;
			lastDay++;

		} while (day != 11 && continueToNextDay != 'N' && continueToNextDay != 'n');

		if (continueToNextDay != 'Y' && continueToNextDay != 'y') {

			totalDayRecorded = lastDay - defaultDay + 1;

			printf("\nTOTAL Days RECORDED      = %d Day (Day %d to Day %d)\n",totalDayRecorded,defaultDay,lastDay);
			printf("HIGHEST number of CASES  = %d , happening on Day %d\n", highestNumberCases, dayOfHighestCases);
			printf("LOWEST number of CASES   = %d , happening on Day %d\n\n", lowestNumberCases, dayOfLowestCases);
			printf("HOFULLY YOU'RE SATISFY THIS PROGRAM  ^_^\n");
			printf("BYE BYE AND VERY THANK YOU !!!\n\n");
		}

	} while (day != 11 && continueToNextDay != 'N' && continueToNextDay != 'n');
}
