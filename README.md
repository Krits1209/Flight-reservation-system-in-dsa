# Flight-reservation-system-in-dsa
project in which I use data structures , linked list .
#include <stdio.h>  
#include <stdlib.h>  
#include <string.h>  
// Define a structure for a flight 
struct Flight {    
int code;     
char 
destination[20];    
 int serial;     
 int price;  
struct Flight* next;  
};  
// Function to create a new flight node struct Flight* createFlight(int serial, int 
code, const char* destination, int price)  
{     
struct Flight* newFlight = (struct Flight*)malloc(sizeof(struct 
Flight));    
 newFlight->serial = serial;    
 newFlight->code = code;  
strcpy(newFlight->destination, destination);     
newFlight->price = price;    
 newFlight->next 
= NULL;     return newFlight;  
}  
// Function to add a new flight to the linked list  
struct Flight* addFlight(struct Flight* head, int serial, int code, const char*  
destination, int price) {  
struct Flight* newFlight = createFlight(serial, code, destination, price);     
if (head == NULL) {         
return newFlight;  
} else {  
struct Flight* current = head;         
while (current->next != NULL) {             
current = current->next;  
}  
current->next = newFlight;         
return head;  
}  
}  
// Function to search for a flight by serial number and return the corresponding 
code  
int findFlightCode(struct Flight* head, int serial) {     
struct Flight* current = head;     while (current != 
NULL) {        
 if (current->serial == serial) {             
return current->code;  
}  
current = current->next;  
}  
return -1; // Flight not found  
}  
int main() {     
struct Flight* 
head = NULL;     // Add flights 
to the linked list  
head = addFlight(head, 101, 74575, "Mumbai", 12000);     
head = addFlight(head, 102, 74589, "Mumbai", 10000);     
head = addFlight(head, 103, 74596, "Mumbai", 15000);     
head = addFlight(head, 122, 84886, "Chennai", 11000);     head 
= addFlight(head, 123, 84887, "Chennai", 10000);     head = 
addFlight(head, 124, 84890, "Chennai", 15000);  
// Add more flights here  
int choice;  
int p, co, age, payment;     
char name[20];     char 
date[10];    
 char 
from[20];  
char gender;    
int seriol;    
 do {         ----------------\n");        
 char destination[20];     
printf("\n-----------
 printf("  Airline 
Ticket booking\n");        -----------------\n");        
Booking\n");         
 printf("----------
 printf(" 1 
printf(" 2 Price\n");         
printf(" 3 View Ticket details\n");         
printf(" 4 Payment confirmation\n");         
printf(" 5 Cancel your booking\n");         
printf(" 0 Exit\n");        
 printf("Enter 
scanf("%d", 
your Choice: ");         
&choice);        
 switch (choice) {  
// Rest of the code for user interactions, booking, pricing, payment, and 
cancellation  
}  
} while (choice != 0);     
return 0; 
