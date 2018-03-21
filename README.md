#include<stdio.h>
 struct process
 {
 char process_name;
 int arrivalTime,BurstTime,ct,WatingTime,Turnaround Time,priority;
 int status;
 }queue[10];
 int limit;
 void Arival_time()
 {
 struct process temp;
 int i,j;
 for(i=0;i<limit;i++)
 {
 for(j=i+1;j<limit;j++)
 {
 if(queue[i].arrivalTime>queue[j].arrivalTime)
 {
 temp=queue[i];
 queue[i]=queue[j];
 queue[j]=temp;
 }
 }
 }
 }
 
