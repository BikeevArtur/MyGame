#include <vector>
#include <iostream>

enum Light_Side {Jedi_Master_ID = 0, Jedi_Knight_ID, Padavan_ID, Battleship_ID, Mega_Cruiser_ID,
                 Lend_Speeder_ID, Medical_Droid_ID, Republic_Infantryman_ID};

enum Dark_Side {Master_of_Swords_ID = 0, Dark_Lord_of_Sith_ID, Shadow_Killer_ID, Heavy_Tank_ID,
                 Star_Fighter_ID, Battle_Droid_ID, Sith_Berserker_ID, Mega_Battle_Droid_ID};


enum player_ID {Light = 0, Dark};



class Unit
{
public:
    virtual ~Unit(){};
    virtual void Information() const = 0;
protected:
    int speed;
    int attack;
    int defense;
    int hit_points;
};



class Space_Ship: public Unit
{
protected:
    int force_shields;
    int capacity;
};

class Ground_Machines: public Unit
{
protected:
    int force_shields;
};

class Warrior: public Unit
{
protected:
    int morale;
    int force;
};

// Light Side Units

class Jedi_Master: public Warrior
{
public:
    virtual void Information() const override{std::cout << "Jedi_Master " << attack  << std::endl;}
    Jedi_Master() {speed = 10, attack = 50, defense = 60, hit_points = 200, morale = 8, force = 30;}
};

class Jedi_Knight: public Warrior
{
public:
    virtual void Information() const override{std::cout << "Jedi_Knight " << attack  << std::endl;}
    Jedi_Knight() {speed = 9, attack = 42, defense = 50, hit_points = 140, morale = 7, force = 18;}
};

class Padavan: public Warrior
{
public:
    virtual void Information() const override{std::cout << "Padavan " << attack  << std::endl;}
    Padavan() {speed = 9, attack = 32, defense = 30, hit_points = 80, morale = 7, force = 10;};
};

class Battleship: public Space_Ship
{
public:
    virtual void Information() const override{std::cout << "Battleship " << attack  << std::endl;}
    Battleship() {speed = 15, attack = 160, defense = 135, hit_points = 2000, force_shields = 300, capacity = 10;}
};

class Mega_Cruiser: public Space_Ship
{
public:
    virtual void Information() const override{std::cout << "Mega_Cruiser " << attack  << std::endl;}
    Mega_Cruiser() {speed = 10, attack = 250, defense = 200, hit_points = 3500,  force_shields = 500, capacity = 18;}
};

class Lend_Speeder: public Ground_Machines
{
public:
    virtual void Information() const override{std::cout << "Lend_Speeder " << attack  << std::endl;}
    Lend_Speeder() {speed = 20, attack = 30, defense = 40, hit_points = 400, force_shields = 80;}
};

class Medical_Droid: public Ground_Machines
{
public:
    virtual void Information() const override{std::cout << "Medical_Droid " << attack  << std::endl;}
    Medical_Droid() {speed = 5, attack = 5, defense = 50, hit_points = 200, force_shields = 10;}
};

class Republic_Infantryman: public Warrior
{
public:
    virtual void Information() const override{std::cout << "Republic_Infantryman " << attack  << std::endl;}
    Republic_Infantryman() {speed = 4, attack = 20, defense = 10, hit_points = 35, morale = 4, force = 0;}
};

// Dark Side Units
class Dark_Lord_of_Sith: public Warrior
{
public:
    virtual void Information() const override{std::cout << "Dark_Lord_of_Sith " << attack  << std::endl;}
    Dark_Lord_of_Sith() {speed = 10, attack = 70, defense = 35, hit_points = 175, morale = 7, force = 40;}
};

class Master_of_Swords: public Warrior
{
public:
    virtual void Information() const override{std::cout << "Master_of_Swords " << attack  << std::endl;}
    Master_of_Swords() {speed = 12, attack = 100, defense = 50, hit_points = 160, morale = 5, force = 10;}
};

class Shadow_Killer: public Warrior
{
public:
    virtual void Information() const override{std::cout << "Shadow_Killer " << attack  << std::endl;}
    Shadow_Killer() {speed = 10, attack = 70, defense = 60, hit_points = 200, morale = 3, force = 30;}
};

class Heavy_Tank: public Ground_Machines
{
public:
    virtual void Information() const override{std::cout << "Heavy_Tank " << attack  << std::endl;}
    Heavy_Tank() {speed = 6, attack = 300, defense = 160, hit_points = 1500, force_shields = 120;}
};

class Star_Fighter: public Space_Ship
{
public:
    virtual void Information() const override{std::cout << "Star_Fighter " << attack << std::endl;};
    Star_Fighter() {speed = 30, attack = 100, defense = 75, hit_points = 700, force_shields = 120, capacity = 6;}
};

class Battle_Droid: public Ground_Machines
{
public:
    virtual void Information() const override{std::cout << "Battle_Droid " << attack << std::endl;}
    Battle_Droid() {speed = 3, attack = 30, defense = 40, hit_points = 100, force_shields = 20;}
};

class Sith_Berserker: public Warrior
{
public:
    virtual void Information() const override{std::cout << "Sith_Berserker " << attack << std::endl;}
    Sith_Berserker() {speed = 8, attack = 90, defense = 25, hit_points = 110, morale = 10, force = 5;}
};

class Mega_Battle_Droid: public Ground_Machines
{
public:
    virtual void Information() const override{std::cout << "Mega_Battle_Droid " << attack << std::endl;}
    Mega_Battle_Droid() {speed = 5, attack = 120, defense = 60, hit_points = 600, force_shields = 100;}
};

class Factory
{
public:
    virtual Unit* create_unit(int id) = 0;
};


class Light_Side_Factory:public Factory
{
public:
    virtual Unit* create_unit(int id) override;
};


class Dark_Side_Factory:public Factory
{
public:
    virtual Unit* create_unit(int id) override;
};



Unit* Light_Side_Factory::create_unit(int id)
{
    Unit* unit;
    switch(id)
    {
    case Jedi_Master_ID:
        unit = new Jedi_Master;
        break;
    case Jedi_Knight_ID:
        unit  = new Jedi_Knight;
        break;
    case Padavan_ID:
        unit = new Padavan;
        break;
    case Battleship_ID:
        unit = new Battleship;
        break;
    case Mega_Cruiser_ID:
        unit = new Mega_Cruiser;
        break;
    case Lend_Speeder_ID:
        unit = new Lend_Speeder;
        break;
    case Medical_Droid_ID:
        unit = new Medical_Droid;
        break;
    case Republic_Infantryman_ID:
        unit = new Republic_Infantryman;
        break;
    }
    return unit;
}


Unit* Dark_Side_Factory::create_unit(int id)
{
    Unit* unit;
    switch(id)
    {
    case Master_of_Swords_ID:
        unit = new Master_of_Swords;
        break;
    case Dark_Lord_of_Sith_ID:
        unit  = new Dark_Lord_of_Sith;
        break;
    case Shadow_Killer_ID:
        unit = new Shadow_Killer;
        break;
    case Heavy_Tank_ID:
        unit = new Heavy_Tank;
        break;
    case Star_Fighter_ID:
        unit = new Star_Fighter;
        break;
    case Battle_Droid_ID:
        unit = new Battle_Droid;
        break;
    case Sith_Berserker_ID:
        unit = new Sith_Berserker;
        break;
    case Mega_Battle_Droid_ID:
        unit = new Mega_Battle_Droid;
        break;
    }
    return unit;
}


class Game
{
private:
    std::vector<Unit*> Units;
    Factory* F;
    int Unit_Count;
public:
    Game(int id);
    ~Game(){};
    void Build_Unit(int ID);
    void Information();
};

Game::Game(int id)
{
    Unit_Count = 0;
    switch (id)
    {
    case Light:
        F = new Light_Side_Factory;
        break;
    case Dark:
        F = new Dark_Side_Factory;
        break;
    }
};

void Game::Build_Unit(int ID)
{
    Unit_Count++;
    Unit* Unit = F->create_unit(ID);
    Units.push_back(Unit);
};

void Game::Information()
{
    for (int i = 0; i < Unit_Count; i++)
    {
        Units[i]->Information();
    }
};


int main()
{
    int fraction_id;
    fraction_id = Light;
    Game* game = new Game(fraction_id);
    game->Build_Unit(Padavan_ID);
    game->Build_Unit(Jedi_Master_ID);
    game->Build_Unit(Padavan_ID);
    game->Build_Unit(Battleship_ID);
    game->Build_Unit(Mega_Battle_Droid_ID);
    game->Build_Unit(Battleship_ID);
    game->Build_Unit(Medical_Droid_ID);
    game->Information();
    delete game;

    fraction_id = Dark;
    Game* Newgame = new Game(fraction_id);
    Newgame->Build_Unit(Sith_Berserker_ID);
    Newgame->Build_Unit(Sith_Berserker_ID);
    Newgame->Build_Unit(Heavy_Tank_ID);
    Newgame->Build_Unit(Sith_Berserker_ID);
    Newgame->Information();
    delete Newgame;
    return 0;
}
