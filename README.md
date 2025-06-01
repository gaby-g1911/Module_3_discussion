# Module_3_discussion
public enum FurColor
{
    White,
    Brown,
    Black,
    Spotted
}

public class Bunny
{
    public string? Name;
    public bool LikesCarrots;
    public bool LikesHumans;
    public  FurColor Color;

    public Bunny() {}

    public Bunny(string name)
    {
        Name = name;
    }

    public void Describe()
    {
        Console.WriteLine($"Bunny: {Name}");
        Console.WriteLine($"Likes Carrots: {LikesCarrots}");
        Console.WriteLine($"Likes Humans: {LikesHumans}");
        Console.WriteLine($"Fur Color: {Color}");
        Console.WriteLine();
    }
}

class Program
{
    static void Main()
    {
        Bunny b1 = new Bunny("Bo") 
        { 
            LikesCarrots = true, 
            LikesHumans = false,
            Color = FurColor.White
        };

        Bunny b2 = new Bunny("Luna")
        {
            LikesCarrots = true,
            LikesHumans = true,
            Color = FurColor.Spotted
        };

        b1.Describe();
        b2.Describe();
    }
}
