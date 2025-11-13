using System;

namespace GiaiPhuongTrinhBac2_OOP
{
    class PTBac1
    {
        protected double a, b;

        public PTBac1(double a, double b)
        {
            this.a = a;
            this.b = b;
        }

        public virtual void Giai()
        {
            Console.WriteLine("\n--- Giai phuong trinh bac 1: ax + b = 0 ---");
            if (a == 0)
            {
                if (b == 0)
                    Console.WriteLine("Phuong trinh co vo so nghiem.");
                else
                    Console.WriteLine("Phuong trinh vo nghiem.");
            }
            else
            {
                double x = -b / a;
                Console.WriteLine($"Phuong trinh co nghiem x = {x:F2}");
            }
        }
    }

    class PTBac2 : PTBac1
    {
        private double c;

        public PTBac2(double a, double b, double c) : base(a, b)
        {
            this.c = c;
        }

        public override void Giai()
        {
            Console.WriteLine("\n--- Giai phuong trinh bac 2: ax² + bx + c = 0 ---");
            if (a == 0)
            {
                Console.WriteLine("Vi a = 0 nen phuong trinh tro thanh bac 1:");
                PTBac1 pt1 = new PTBac1(b, c);
                pt1.Giai();
                return;
            }

            double delta = b * b - 4 * a * c;
            Console.WriteLine($"Δ = {delta:F2}");

            if (delta < 0)
            {
                Console.WriteLine("Phuong trinh vo nghiem thuc.");
            }
            else if (delta == 0)
            {
                double x = -b / (2 * a);
                Console.WriteLine($"Phuong trinh co nghiem kep x₁ = x₂ = {x:F2}");
            }
            else
            {
                double x1 = (-b + Math.Sqrt(delta)) / (2 * a);
                double x2 = (-b - Math.Sqrt(delta)) / (2 * a);
                Console.WriteLine("Phuong trinh co hai nghiem phan biet:");
                Console.WriteLine($"x₁ = {x1:F2}");
                Console.WriteLine($"x₂ = {x2:F2}");
            }
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            Console.OutputEncoding = System.Text.Encoding.UTF8;
            Console.WriteLine("=== CHUONG TRINH GIAI PHUONG TRINH BAC 2 (OOP - KE THUA) ===");

            Console.Write("Nhap a = ");
            double a = double.Parse(Console.ReadLine() ?? "0");

            Console.Write("Nhap b = ");
            double b = double.Parse(Console.ReadLine() ?? "0");

            Console.Write("Nhap c = ");
            double c = double.Parse(Console.ReadLine() ?? "0");

            PTBac2 pt2 = new PTBac2(a, b, c);
            pt2.Giai();

            Console.WriteLine("\nNhan phim bat ki de ket thuc...");
            Console.ReadKey();
        }
    }
}
