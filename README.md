# pet_fuggvenyek
//ELSO PÉLDA BEVEZETÉS ÖSSZEADAS------------------------------------------------
asdasdasd
asd

static int osszead(int elso_szam, int masodik_szam)
        {
            int osszeg;
            osszeg = elso_szam + masodik_szam;

            return osszeg;
        }

        static void Main(string[] args)
        {
            int fugv_osszeg;
            int a, b;

            Console.Write("a értéke: ");
            a = int.Parse(Console.ReadLine());
            Console.Write("b értéke: ");
            b = int.Parse(Console.ReadLine());

            fugv_osszeg = osszead(a, b);

            Console.WriteLine(fugv_osszeg);





            Console.ReadLine();

