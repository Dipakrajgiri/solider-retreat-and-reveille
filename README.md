# solider-retreat-and-reveille-time
 source code:

  
       #include<iostream>
       #include<limits>
     using namespace std;
     int read()
      {
       int i;
      while (true)
      {
      cin >> i;
      if (!cin)
      {
      cout << "bad input,try again " << endl;
      cin.clear();
         cin.ignore(numeric_limits<streamsize>::max(), '\n');
      continue;
      }
      else break;
      }
     return i;
    }
      int main()
     {
     int rt,rv,sd,z,x,u,y;
     cout<<"please enter reveille time\n";
    retry:
      rv=read();

     if(rv>=0&&rv<=2399)
      {
      x=rv;
         x=x%1000;
     x=x%100;
     if(x>=0&&x<=59)
      {
       u=u/100;
      printf("reveille time %04d accepted\n",rv);  
      }
      else
      {
     cout<<"minutes must be between 00 and 59,try again\n";
      goto retry;
     }
 
     }
     else
    {
     cout<<"hour must be between oo and 23,try again\n";
    goto retry;
    }
    cout<<"please enter sleep duration\n";
    retrya:
     sd=read();

    if(sd>=0&&sd<=2399)
    {
      z=sd;
        y=sd;
       y=y%1000;
       y=y%100;
       if(y>=0&&y<=59)
      {
        z=z/100;
       printf("sleep duration of %d hours and %02d minutes accepted\n",z,y);  
     }
      else
       {
      cout<<"minutes must be between 00 and 59,try again\n";
     goto retrya;
      }
 
      }
        else
      {
       cout<<"hour must be between oo and 23,try again\n";
       goto retrya;
     }
      int h,m,h1,m1;
     h=(rv/100)-(sd/100);
      m=((rv%1000)%100)-((sd%1000)%100);
     if(h<=0)
      {
       h=23+h;
       if(m<0)
       {
       m=60+m;
       }
      if(m<0)
      {
       m=60+m;
       h=h-1;
      }
     h1=h;
     m1=m;
     if(h1>12)
       {
          h1=h1-12;
       }

        printf("retreat time is %02d%02d or(%d:%02d)",h,m,h1,m1);
        cout<<"\nlights out soldier";
        return 0;
         }


