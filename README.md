# Lisa-s-Workbook
Repo

Hello people,
I'm uploading some code on lisa's workspace please do share the changes.
Thank you.

import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int chapter;
        int max_questions_per_page;
        
        chapter=sc.nextInt();
        max_questions_per_page=sc.nextInt();
        int total_questions[]=new int[chapter];
        int questions_per_page;
        
        for(int i=0;i<chapter;i++){
            total_questions[i]=sc.nextInt();
        }
        
        
        int current_page_no=1;
        int max_questions_per_chapter;
        int temp_page;
        int special_number=0;
        int total_page_track=1;
       
        for(int i=0;i<chapter;i++){
            max_questions_per_chapter = total_questions[i];
            
            if(i!=0){
                current_page_no++;
            }
            
            temp_page=1;
            total_page_track=1;
            
            loop:while(temp_page<=max_questions_per_chapter && total_page_track<=max_questions_per_page){
                
                    if(temp_page==current_page_no){
                        special_number++;
                        temp_page++;
                        total_page_track++;
                    }
                
                    else{
                        temp_page++;
                        total_page_track++;
                    }
                
                    if(temp_page <= max_questions_per_chapter && total_page_track>max_questions_per_page){
                        current_page_no++;
                        total_page_track=1;
                        continue loop;
                    }
                    
                  }
              
            }
        
        System.out.println(special_number);                
        }
        
    }
