namespace pet_fuggvenyek2
{
    class Program
    {

        struct Sorsolas
        {
            public int szam;
            public bool paros;
        }
        static Random rand = new Random();
        
        static void Main(string[] args)
        {
            Sorsolas[] szamok = new Sorsolas[100];
            for(int i = 0; i < 100; i++)
            {
                szamok[i] = sorsol();
            }

            listaz(szamok);

            

            Console.ReadLine();
        }

        static char oszlop(int a)
        {
            char eredmeny = ' ';
            switch (a % 3)
            {
                case 0: eredmeny = 'D';
                    break;
                case 1: eredmeny = 'P';
                    break;
                case 2: eredmeny = 'M';
                    break;
            }
            return eredmeny;
        }

        static void listaz(Sorsolas[] szamok_tomb)
        {
            for(int i = 0; i < 100; i++)
            {
                string paritas;
                if(szamok_tomb[i].paros == true)
                {
                    paritas = "páros";
                }
                else
                {
                    paritas = "páratlan";
                }
                Console.WriteLine("{0}. szám: {1}\tParitás: {2}  Oszlop: {3}",i+1,szamok_tomb[i].szam, paritas,oszlop(szamok_tomb[i].szam));

            }
        }

        static Sorsolas sorsol()
        {
            Sorsolas szamom = new Sorsolas();
            szamom.szam = rand.Next(1,37);

            if(szamom.szam % 2 == 0)
            {
                szamom.paros = true;
            }
            else
            {
                szamom.paros = false;
            }
            return szamom;

        }
    }
}
