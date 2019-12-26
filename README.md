# ObjectC_bundle
動態繫結

動態類型和動態繫結在 OOP 設計中應用很廣泛。在物件導向 C 中，id 類型是一個獨特的資料類型，它可以轉為任何資料類型。

id 類型的定義方式

                      id 變數名稱;
                      
                      
傳回 id 類型方法的定義方式，其中方法分為有參和無餐。

    
                     -(id) 方法名稱;
   

動態繫結的實作


QQQ.h

                #import<Foundation/Foundation.h>
                
                @interface QQQ: NSObject
                {
                
                  NSString *p;
                
                }
                
                -(void)setP;
                -(void)printP;
                
                @end

KKK.h

               #import <Foundtaion/Fundation.h>
               
               @interface KKK: NSObject
               {
               
                  NSString *p;
               
               }
               
               -(void)setP;
               -(void)printP;
               
               @end

QQQ.m

              #import"QQQ.h"
              
              @implementation QQQ
              -(void)setP
              {
              
                 p=@"QQQ";
              
              }
              
              -(void)printP
              {
              
                NSlog(@"%@", p);
              
              }
              
              @end

KKK.m

              #import"KKK.h"
              
              @implementation KKK
              
              -(void)setP
              {
              
                p=@"KKK"
              
              }
              
              -(void)printP
              {
              
                NSLog(@"%@", p);
              
              }
             
             @end


main.m


           #import<Foundation/Foundation.h>
           #import"QQQ.h"
           #import"KKK.h"
           
           int main(int argc, const char * argv[])
           {
           
             id eee; ------> 可以呼叫任何類別的型態容器
             
             QQQ *fff=[[QQQ alloc]init];
             eee = fff;
             [eee setP];
             [eee printP];
             
             KKK *iii=[[KKK alloc]init];
             eee = iii;
             [eee setP];
             [eee printP];             
             
              return 0;       
           
           }      
