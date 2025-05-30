# Module_3_discussion
using Sytem;
using Sytem.Collections.Generic;

enum StockSector
{
    Technology;
    Finance;
    Healthcare;
    Energy
}
public class Stock
{
    public decimmal CurrentPrice {get; set;}
    public decimal SharesOwned {get; set;}

    public decimal Worth => CurrentPrice * SharesOwned

    public StockSector Sector {get; set;}
    public string Name {get; set;}

    public void Print()
    {
        Console.WriteLine($"Stock: {Name}");
        Console.WriteLine($"Sector: {Sector});
        Console.WriteLine($"Shares Owned: {ShareOwned}");
        Console.WriteLine($"Current Price: ${CurrentPrice}");
        Console.WriteLine($Total Worth: ${Worth}");
        Console.WriteLine();
    }
}
class Program
{
    static void Main()
    {
        List<Stock> portfolio = new List<Stock>
        {
            new Stock {Name = "Apple", CurrentPrice = 180.50m, SharedOwned = 10, Sector = StockSector.Technology},
            new Stock {name = "Pfizer", CurrentPrice = 45.25m, SharesOwned = 20, Sector = StockSector.Healthcare},
            new Stock {"ExxonMobil", CurrentPrice = 95.75m, SharesOwned = 15, Sector = StockSector.Energy}
        };
        foreach (var stock in portfolio)
        {
            stock.Print();
        }
    }
}
