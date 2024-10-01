#include <stdio.h>
#include <time.h>
#include <unistd.h>
#include <stdlib.h>
#include <windows.h>

int main() {
    time_t s, val = 1;
    struct tm* current_time;

    s = time(NULL);
    current_time = localtime(&s);

    int hour = current_time->tm_hour;
    int minute = current_time->tm_min;
    int second = current_time->tm_sec;

    printf("Current Time: %02d:%02d:%02d\n", hour, minute, second);

    int alarm_hour, alarm_minute, alarm_second;
    printf("Enter alarm hour (0-23): ");
    scanf("%d", &alarm_hour);
    printf("Enter alarm minute (0-59): ");
    scanf("%d", &alarm_minute);
    printf("Enter alarm second (0-59): ");
    scanf("%d", &alarm_second);

    while(1) {
        system("cls");
        printf("Current Time: %02d:%02d:%02d\n", hour, minute, second);
        printf("Alarm Time: %02d:%02d:%02d\n", alarm_hour, alarm_minute, alarm_second);
        s = time(NULL);
        current_time = localtime(&s);
        hour = current_time->tm_hour;
        minute = current_time->tm_min;
        second = current_time->tm_sec;

        if(hour == alarm_hour && minute == alarm_minute && second == alarm_second) {
            printf("\nAlarm!\n");
            Beep(500,900);
            Sleep(100);
            break;
        }
        sleep(1);  
    }
    return 0;
}
