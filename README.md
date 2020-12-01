# Adventure-Game
import java.util.*;
import java.util.Scanner;
/**
 * Find the treasure in the dungeon.
 *
 * @author (Kai.W)
 * @version (1.0)
 */
public class AdventureGAME
{
    public static void main(String args[])
  {
   Scanner inputScanner = new Scanner(System.in);
    Scanner input = new Scanner(System.in);
    Scanner myScanner = new Scanner(System.in);
    System.out.print('\u000C');
    Random gen = new Random();
    int rand = gen.nextInt();
    
    System.out.println("Hello welcome to Kai's Adventure Game");
    System.out.println("What is your name?");
    String n = input.nextLine ();
    
    String playAgain = "yes";
    
    while (playAgain.equals("yes") || playAgain.equals("Yes"))
    {
    System.out.println("Hello "+ n + " ");
    
    System.out.println("The goal of this game is to find a treasure in a dungeon");
    
    System.out.println("Now, are you ready to enter the dungeon?");
    System.out.println("Type Yes or No");
    String answer = myScanner.nextLine();
    
    if (answer.equals("Yes") )
    {
        System.out.println("Okay, lets get going!");
        
    }
    else if (answer.equals("No") )
    {
        System.out.println("Okay, come back when you are ready.");
        String answer10009 = myScanner.nextLine();
    }

   System.out.println("(After 5 minnutes of walking");
   System.out.println("Oh no look, there is a goblin");
   System.out.println("You have 2 options");
   System.out.println("punch: Does 15 damange");
   System.out.println("charge: Will make the next attack do 3x damage");
   System.out.println("But, will take away 10 hp from you (Can not use it in a row)");
   System.out.println("The goblin will try to attack you after two of your attacks");
   System.out.println("Goblin HP: 50, Goblins Attack: 25, Your HP: 100");
   System.out.println("Now type punch or charge");
   String answer1 = myScanner.nextLine();
   
   int p = 15 ;
   int c = 10;
   int Gob_HP = 50;
   int Your_HP = 100;
   int Gob_Att = 25;
   
   
   if (answer1.equals("punch"))
   {
      System.out.println("You choose punch");
      System.out.println("...");
      System.out.println("Nice, you were able to hit him");
      Gob_HP = Gob_HP - p;
      System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
      System.out.println("Now type punch or charge");
      String answer2 = myScanner.nextLine();
      if (answer2.equals("punch"))
      {
          System.out.println("You choose punch");
          System.out.println("...");
          System.out.println("Nice, you were able to hit him");
          Gob_HP = Gob_HP - p;
          System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
          System.out.println("Oh no, the goblin attacked us");
          Your_HP = Your_HP - Gob_Att;
          System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
          System.out.println("Now type punch or charge");
          String answer4 = myScanner.nextLine();
          if (answer4.equals("punch"))
          {
              System.out.println("You choose punch");
              System.out.println("...");
              System.out.println("Nice, you were able to hit him");
              Gob_HP = Gob_HP - p;
              System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
              System.out.println("Now type punch or charge");
              String answer6 = myScanner.nextLine();
              if (answer6.equals("punch"))
              {
                  System.out.println("You choose punch");
                  System.out.println("...");
                  System.out.println("Nice, you were able to hit him");
                  Gob_HP = Gob_HP - p;
                  System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
                  System.out.println("Good job " + n + " you defeated the goblin");
                }
              else if (answer6.equals("charge"))
              {
                  System.out.println("You choose charge");
                  System.out.println("...");
                  System.out.println("Oh no, the goblin attacked us");
                  Your_HP = Your_HP - Gob_Att;
                  System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
                  System.out.println("Now type punch");
                  String answer7 = myScanner.nextLine();
                  if (answer7.equals("punch"))
                  {
                      System.out.println("You choose punch");
                      System.out.println("...");
                      Gob_HP = Gob_HP - (3 * p);
                      Your_HP = Your_HP - c;
                      System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
                      System.out.println("Good job " + n + " you defeated the goblin");
                    }
                }
          }
          else if (answer4.equals("charge"))
          {
              System.out.println("You choose charge");
              System.out.println("...");
              System.out.println("Now type punch");
              String answer9 = myScanner.nextLine();
              if (answer9.equals("punch"))
              {
                  System.out.println("You choose punch");
                  System.out.println("...");
                  Gob_HP = Gob_HP - (3 * p);
                  Your_HP = Your_HP - c;
                  System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
                  System.out.println("Good job " + n + " you defeated the goblin");
                }
            }
        }
      else if (answer2.equals("charge"))
      {
          System.out.println("You choose charge");
          System.out.println("...");
          System.out.println("Oh no, the goblin attacked us");
          Your_HP = Your_HP - Gob_Att;
          System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
          System.out.println("Now type punch");
          String answer5 = myScanner.nextLine();
          if (answer5.equals("punch"))
          {
              System.out.println("You choose punch");
              System.out.println("...");
              Gob_HP = Gob_HP - (3 * p);
              Your_HP = Your_HP - c;
              System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
              System.out.println("Good job " + n + " you defeated the goblin");
            }
        }
   }
   else if (answer1.equals("charge"))
   {
       System.out.println("You choose charge");
       System.out.println("...");
       System.out.println("Now type punch");
       String answer3 = myScanner.nextLine();
       if (answer3.equals("punch"))
       {
           System.out.println("You choose punch");
           System.out.println("...");
           Gob_HP = Gob_HP - (3 * p);
           Your_HP = Your_HP - c;
           System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
           System.out.println("Oh no, the goblin attacked us");
           Your_HP = Your_HP - Gob_Att;
           System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
           System.out.println("Now type punch or charge");
           String answer6 = myScanner.nextLine();
           if (answer6.equals("punch"))
           {
              System.out.println("You choose punch");
              System.out.println("...");
              System.out.println("Nice, you were able to hit him");
              Gob_HP = Gob_HP - p;
              System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
              System.out.println("Good job " + n + " you defeated the goblin");
            }
            else if (answer6.equals("charge"))
           {
              System.out.println("You choose charge");
              System.out.println("...");
              System.out.println("Now type punch");
              String answer8 = myScanner.nextLine();
              if (answer8.equals("punch"))
              {
                  System.out.println("You choose punch");
                  System.out.println("...");
                  Gob_HP = Gob_HP - (3 * p);
                  Your_HP = Your_HP - c;
                  System.out.println("Goblin HP: " + Gob_HP + ", Your HP: " + Your_HP );
                  System.out.println("Good job " + n + " you defeated the goblin");
                }
            }
        }
   }
   System.out.println("Lets keep on going "+ n + "!");
   System.out.println("(After 5 minutes of walking");
   System.out.println("Oh it looks like there are two paths");
   System.out.println("Type left or right");
   String answer10 = myScanner.nextLine();
   
   int Z_Att = 30;
   int Z_HP = 150;
   int s = 40;
   int m = 30;
   int Z_AttM = 15;
   if (answer10.equals("left"))
   {
       System.out.println("Oh look, there is a sword");
       System.out.println("Lets keep on going "+ n + "!");
       System.out.println("Oh no look, there is a zombie");
       System.out.println("You have 2 options");
       System.out.println("sword: Does 40 damange");
       System.out.println("charge: Will make the next attack do 3x damage");
       System.out.println("But, will take away 10 hp from you (Can not use it in a row)");
       System.out.println("The zombie will try to attack you every two rounds");
       System.out.println("Zombie HP: 150, Zombies Attack: 30, Your HP: " + Your_HP);
       System.out.println("Now type sword or charge");
       String answer11 = myScanner.nextLine();
       if (answer11.equals("sword"))
       {
           System.out.println("You choose sword");
           System.out.println("...");
           Z_HP = Z_HP - s;
           System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
           System.out.println("Now type sword or charge");
           String answer13 = myScanner.nextLine();
           if (answer13.equals("sword"))
           {
               System.out.println("You choose sword");
               System.out.println("...");
               Z_HP = Z_HP - s;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Oh no, the zombie attacked you");
               Your_HP = Your_HP - Z_Att;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Now type sword or charge");
               String answer17 = myScanner.nextLine();
               if (answer17.equals("sword"))
               {
                   System.out.println("You choose sword");
                   System.out.println("...");
                   Z_HP = Z_HP - s;
                   System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                   System.out.println("Now type sword or charge");
                   String answer19 = myScanner.nextLine();
                   if (answer19.equals("sword"))
                   {
                       System.out.println("You choose sword");
                       System.out.println("...");
                       Z_HP = Z_HP - s;
                       System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                    }
                   if (answer19.equals("charge"))
                   {
                       System.out.println("You choose charge");
                       System.out.println("...");
                       System.out.println("Oh no, the zombie attacked you");
                       Your_HP = Your_HP - Z_Att;
                       System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                       System.out.println("Now type sword");
                       String answer21 = myScanner.nextLine();
                       if (answer21.equals("sword"))
                       {
                           System.out.println("You choose sword");
                           System.out.println("...");
                           Your_HP = Your_HP - c;
                           Z_HP = Z_HP - (3 * s);
                           System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                        }
                    }
                }
               if (answer17.equals("charge"))
               {
                   System.out.println("You choose charge");
                   System.out.println("...");
                   System.out.println("Now type sword");
                   String answer20 = myScanner.nextLine();
                   if (answer20.equals("sword"))
                   {
                       System.out.println("You choose sword");
                       System.out.println("...");
                       Your_HP = Your_HP - c;
                       Z_HP = Z_HP - (3 * s);
                       System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                    }
                }
            }
           if (answer13.equals("charge"))
           {
               System.out.println("You choose charge");
               System.out.println("...");
               System.out.println("Oh no, the zombie attacked you");
               Your_HP = Your_HP - Z_Att;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Oh no, the zombie attacked you");
               Your_HP = Your_HP - Z_Att;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Now type sword");
               String answer18 = myScanner.nextLine();
               if (answer18.equals("sword"))
               {
                    System.out.println("You choose sword");
                    System.out.println("...");
                    Your_HP = Your_HP - c;
                    Z_HP = Z_HP - (3 * s);
                    System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                }
            }
        }
       if (answer11.equals("charge"))
       {
           System.out.println("You choose charge");
           System.out.println("...");
           System.out.println("Now type sword");
           String answer14 = myScanner.nextLine();
           if (answer14.equals("sword"))
           {
               System.out.println("You choose sword");
               System.out.println("...");
               Your_HP = Your_HP - c;
               Z_HP = Z_HP - (3 * s);
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Oh no, the zombie attacked you");
               Your_HP = Your_HP - Z_Att;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Now type sword or charge");
               String answer22 = myScanner.nextLine();
               if (answer22.equals("sword"))
               {
                   System.out.println("You choose sword");
                   System.out.println("...");
                   Z_HP = Z_HP - s;
                   System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                }
               else if (answer22.equals("charge"))
               {
                   System.out.println("You choose charge");
                   System.out.println("...");
                   System.out.println("Now type sword");
                   String answer23 = myScanner.nextLine();
                   if (answer23.equals("sword"))
                   {
                       System.out.println("You choose sword");
                       System.out.println("...");
                       Your_HP = Your_HP - c;
                       Z_HP = Z_HP - (3 * s);
                       System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                    }
                }
            }
        }
    }
   else if (answer10.equals("right"))
   {
       System.out.println("Oh look, there is a magic wand");
       System.out.println("Oh look, there is a sword");
       System.out.println("Lets keep on going "+ n + "!");
       System.out.println("Oh no look, there is a zombie");
       System.out.println("You have 2 options");
       System.out.println("magic: Does 30 damange and reduces the opponents attack by 50%");
       System.out.println("charge: Will make the next attack do 3x damage");
       System.out.println("But, will take away 10 hp from you (Can not use it in a row)");
       System.out.println("The zombie will try to attack you every round");
       System.out.println("Zombie HP: 150, Goblins Attack: 30, Your HP: " + Your_HP );
       System.out.println("Now type magic or charge");
       String answer29 = myScanner.nextLine();
       if (answer29.equals("magic"))
       {
           System.out.println("You choose sword");
           System.out.println("...");
           Z_HP = Z_HP - m;
           System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
           System.out.println("Now type magic or charge");
           String answer30 = myScanner.nextLine();
           if (answer30.equals("magic"))
           {
               System.out.println("You choose magic");
               System.out.println("...");
               Z_HP = Z_HP - m;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Oh no, the zombie attacked you");
               Your_HP = Your_HP - Z_AttM;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Now type magic or charge");
               String answer31 = myScanner.nextLine();
               if (answer31.equals("magic"))
               {
                   System.out.println("You choose sword");
                   System.out.println("...");
                   Z_HP = Z_HP - m;
                   System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                   System.out.println("Now type magic or charge");
                   String answer32 = myScanner.nextLine();
                   if (answer32.equals("magic"))
                   {
                       System.out.println("You choose magic");
                       System.out.println("...");
                       Z_HP = Z_HP - m;
                       System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                       System.out.println("Oh no, the zombie attacked you");
                       Your_HP = Your_HP - Z_AttM;
                       System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                       System.out.println("Now type magic or charge");
                       String answer50 = myScanner.nextLine();
                       if (answer50.equals("magic"))
                       { 
                           System.out.println("You choose magic");
                           System.out.println("...");
                           Z_HP = Z_HP - m;
                           System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );                          
                        }
                       if (answer50.equals("charge"))
                       {
                           System.out.println("You choose charge");
                           System.out.println("...");
                           System.out.println("Now type magic");
                           String answer51 = myScanner.nextLine();
                           if (answer51.equals("magic"))
                           {
                               System.out.println("You choose magic");
                               System.out.println("...");
                               Z_HP = Z_HP - (3 * m);
                               Your_HP = Your_HP - c;
                               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                           }
                        }
                    }
                   if (answer32.equals("charge"))
                   {
                       System.out.println("You choose charge");
                       System.out.println("...");
                       System.out.println("Oh no, the zombie attacked you");
                       Your_HP = Your_HP - Z_AttM;
                       System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                       System.out.println("Now type magic");
                       String answer33 = myScanner.nextLine();
                       if (answer33.equals("magic"))
                       {
                           System.out.println("You choose magic");
                           System.out.println("...");
                           Z_HP = Z_HP - (3 * m);
                           Your_HP = Your_HP - c;
                           System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                        }
                    }
                }
               if (answer31.equals("charge"))
               {
                   System.out.println("You choose charge");
                   System.out.println("...");
                   System.out.println("Now type magic");
                   String answer34 = myScanner.nextLine();
                   if (answer34.equals("magic"))
                   {
                       System.out.println("You choose magic");
                       System.out.println("...");
                       Your_HP = Your_HP - c;
                       Z_HP = Z_HP - (3 * m);
                       System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                    }
                }
            }
           if (answer30.equals("charge"))
           {
               System.out.println("You choose charge");
               System.out.println("...");
               System.out.println("Oh no, the zombie attacked you");
               Your_HP = Your_HP - Z_AttM;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Oh no, the zombie attacked you");
               Your_HP = Your_HP - Z_AttM;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Now type magic");
               String answer18 = myScanner.nextLine();
               if (answer18.equals("magic"))
               {
                    System.out.println("You choose magic");
                    System.out.println("...");
                    Your_HP = Your_HP - c;
                    Z_HP = Z_HP - (3 * m);
                    System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                    System.out.println("Now type magic or charge");
                    String answer52 = myScanner.nextLine();
                    if (answer52.equals("magic"))
                    {
                        System.out.println("You choose magic");
                        System.out.println("...");
                        Z_HP = Z_HP - m;
                        System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                        System.out.println("Oh no, the zombie attacked you");
                        Your_HP = Your_HP - Z_AttM;
                        System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                    }
                    else if (answer52.equals("charge"))
                    {
                        System.out.println("You choose charge");
                        System.out.println("...");
                        System.out.println("Oh no, the zombie attacked you");
                        Your_HP = Your_HP - Z_AttM;
                        System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                        System.out.println("Now type magic");
                        String answer53 = myScanner.nextLine();
                        if (answer53.equals("magic"))
                        {
                            System.out.println("You choose magic");
                            System.out.println("...");
                            Your_HP = Your_HP - c;
                            Z_HP = Z_HP - (3 * m);
                            System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                        }
                    }    
                }
            }
        }
       if (answer29.equals("charge"))
       {
           System.out.println("You choose charge");
           System.out.println("...");
           System.out.println("Now type magic");
           String answer40 = myScanner.nextLine();
           if (answer40.equals("magic"))
           {
               System.out.println("You choose magic");
               System.out.println("...");
               Z_HP = Z_HP - (3 * m);
               Your_HP = Your_HP - c;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Oh no, the zombie attacked you");
               Your_HP = Your_HP - Z_AttM;
               System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
               System.out.println("Now type magic or charge");
               String answer41 = myScanner.nextLine();
               if (answer41.equals("magic"))
               {
                   System.out.println("You choose magic");
                   System.out.println("...");
                   Z_HP = Z_HP - m;
                   System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                   System.out.println("Now type magic or charge");
                   String answer55 = myScanner.nextLine();
                   if (answer55.equals("magic"))
                   {
                        System.out.println("You choose magic");
                        System.out.println("...");
                        Z_HP = Z_HP - m;
                        System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                    }
                   if (answer55.equals("charge"))
                   {
                       System.out.println("You choose charge");
                       System.out.println("...");
                       System.out.println("Oh no, the zombie attacked you");
                       Your_HP = Your_HP - Z_AttM;
                       System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                       System.out.println("Now type magic");
                       String answer56 = myScanner.nextLine();
                       if (answer56.equals("magic"))
                       {
                            System.out.println("You choose magic");
                            System.out.println("...");
                            Your_HP = Your_HP - c;
                            Z_HP = Z_HP - (3 * m);
                            System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                        }
                    }
                }
               else if (answer41.equals("charge"))
               {
                   System.out.println("You choose charge");
                   System.out.println("...");
                   System.out.println("Now type magic");
                   String answer42 = myScanner.nextLine();
                   if (answer42.equals("magic"))
                   {
                       System.out.println("You choose magic");
                       System.out.println("...");
                       Z_HP = Z_HP - (3 * m);
                       Your_HP = Your_HP - c;
                       System.out.println("Zombie HP: " + Z_HP + ", Your HP: " + Your_HP );
                    }
                }
            }
        }
    }

    
    
   if (Z_HP < 0)
   {
       System.out.println("Good job " + n + " you defeated the Zombie");
       System.out.println("Oh look, there is the treasure chest");
       System.out.println("Lets open it");
       System.out.println("Type open");
       String answer100 = myScanner.nextLine();
 
       if (answer100.equals("open"))
       {
           System.out.println("Game Clear!");
           System.out.println("Your HP :" + Your_HP);
           System.out.println("Do you want to try again?");
           System.out.println("(Try getting a higher HP)");
           System.out.println("Type Yes or No");
           playAgain = inputScanner.next();
   
        }
    }
   if (Your_HP == 0)
   {
       System.out.println("Game Over");
       System.out.println("Your HP: " + Your_HP);
       
  }
}
}
}
