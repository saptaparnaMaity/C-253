#include<ezButton.h>

const int button1 = 4;
const int button2 = 22;

//  defining a variable
int count = 0;

//  creating a button object
ezButton push_button1(button1);
ezButton push_button2(button2);


void setup()
{
  Serial.begin(115200);
  push_button1.setDebounceTime(50);  //  debounce time = 50 ms
  push_button2.setDebounceTime(50);
}

void loop()
{
  //  loop the push_button : continuous polling, reading button1 again and again
  push_button1.loop();
  push_button2.loop();
  
  if (push_button1.isPressed())
  {
    count++;
    Serial.print("Number : ");
    Serial.println(count);
  }

  else if (push_button2.isPressed())
  {
    Serial.print("Table of ");
    Serial.println(count);
    for (int i = 1; i <= 10; i++)
    {
      Serial.print(count);
      Serial.print('*');
      Serial.print(i);
      Serial.print('\t');
      Serial.print('=');
      Serial.print('\t');
      Serial.println(count*i);
    }

    // reset the variable
    count = 0;
  }
 
}
