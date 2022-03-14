using System;
using System.Linq;

namespace ConsoleApp_Kurs_OOP
{
    class CBookCard
    {
        public CBookCard(string autor, string title, string publish, int year, string udk, int circulation, double raiting)
        {
            Autor = autor;
            Title = title;
            Publish = publish;
            Year = year;
            UDK = udk;
            Cir = circulation;
            Raiting = raiting;
        }

        private string _autor;
        private string _title;
        private string _publish;
        private int _year;
        private string _udk;
        private int _circulation;
        private double _raiting;

        public string Autor
        {
            get { return _autor; }
            set { _autor = value; }   //Автор
        }
        public string Title
        {
            get { return _title; }
            set { _title = value; }   //Название
        }
        public string Publish
        {
            get { return _publish; }
            set { _publish = value; }   //Издательство
        }
        public int Year
        {
            get { return _year; }
            set { _year = value; }   //Год
        }

        public string UDK
        {
            get { return _udk; }
            set { _udk = value; }   //УДК
        }


        public int Cir
        {
            get { return _circulation; }
            set { _circulation = value; }   //Тираж
        }
        
        public double Raiting
        {
            get { return _raiting; }
            set { _raiting = value >= 0 && value <= 7 ? value : 0; } //если рейтинг не в нужном диапазоне, то он равен 0
        }

        public override string ToString()
        {
            return $"{Autor}, {Title}, {Publish}, {Year} г., УДК: {UDK}, {Cir} копий, Рейтинг: {Raiting}";
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            var firstBook = new CBookCard("Джон Скит", "C# для профессионалов", "Вильямс", 2017, "62: Инженерное дело. Техника в целом.", 150000, 6.8);
            var secondBook = new CBookCard("Роберт Лафоре", "Теория вероятностей", "Питер", 2010, "51: Математика", 850000, 7.0);
            Console.WriteLine(firstBook);
            Console.WriteLine(secondBook);

            var bookArr = new[]
            {
               new CBookCard("Джон Скит", "C# для профессионалов", "Вильямс", 2017, "62: Инженерное дело. Техника в целом.", 150000, 6.8)
               {
                   Cir = 150000,
                   UDK = "62",
                   Raiting = 6.8
               },
               new CBookCard("Роберт Лафоре", "Теория вероятностей", "Питер", 2010, "51: Математика", 850000, 7.0)
               {
                   Cir = 850000,
                   UDK = "51",
                   Raiting = 7.0
               },
               new CBookCard("Джон Ульиям", "Матем. статистика", "Калининград", 2012, "51: Математика", 635000, 4.4)
               {
                   Cir = 635000,
                   UDK = "51",
                   Raiting =  4.4
               },
               new CBookCard("Иван Иванович", "ПК: его устройство и ход работы!", "Питер", 2007, "48: Информатика", 295745, 5.8)
               {
                   Cir = 295745,
                   UDK = "48",
                   Raiting = 5.8
               },
           };

            Console.WriteLine("\nМассив книг до сортировки: ");
            foreach (var item in bookArr)
            {
                Console.WriteLine(item);
            }

            bookArr = Sort(bookArr);

            Console.WriteLine("\nМассив книг после сортировки: ");
            foreach (var item in bookArr)
            {
                Console.WriteLine(item);
            }
            Console.ReadKey();
        }

        static CBookCard[] Sort(CBookCard[] bookArr)
        {
            return bookArr.OrderByDescending(b => b.Cir).ToArray();
        }
    }
}
