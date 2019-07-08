## Common

1. Square

  private:

  1. m_type : int

  1. m_index : int

  public:

  1. setType(int type) : void

  1. getType() : int

  1. setIndex(int index) : void

  1. getIndex() : int

1. Floor

  private:

  1. m_index : int

  1. m_squares : Square[11][11]

  public:

  1. saveFloor(String filename) : void

  1. loadFloor(String filename) : void

  1. getIndex() : int

  1. setIndex(int index) : void

  1. setSquare(int type, int index, int x, int y) : void

1. FloorSet

  private:

  1. m_floors : vector<Floor>

  1. m_floorNum : int

  public:

  1. loadFloorSet(String filename) : void

  1. saveFloorSet(String filename) : void

  1. getFloorNum() : int

  1. setFloorNum(int floorNum) : void

1. Enemy

  private:

  1. m_hp : int

  1. m_atk : int

  1. m_def : int

  1. m_name : String

  public:

  1. getHp() : int

  1. getAtk() : int

  1. getDef() : int

  1. getName() : int

  1. setHp(int value, int method) : void   // method = 0：赋值；method = 1：增减

  1. setAtk(int value, int method) : void

  1. setDef(int value, int method) : void

  1. setName(String value) : void

1. Item

  private:

  1. m_name : String

  1. m_addAtk : int

  1. m_addDef : int

  1. m_addExp : int

  1. m_specialIndex : int   

  1. m_addHp : int

  1. m_walkable : bool

  public:

  1. getName() : String

  1. setName(String name) : void

  1. getAddAtk() : int

  1. getAddDef() : int

  1. getAddExp() : int

  1. getSpecialIndex() : int

  1. getAddHp() : int

  1. getWalkable() : bool

  1. setWalkable(bool wkb) : void

1. FloorFileSet

  private:

  1. filenameSet : vector<String>

  public:

  1. getFilename(int index) : String

  1. getFileNumber() : int

## Model

1. EnemyList

  private:

  1. m_enemyFile : String

  1. m_enemies : vector<Enemy>

  1. m_enemyNumber : int

  public:

  1. intialize() : void

  1. addEnemy(int atk, int def, int hp, int exp) : void

  1. getEnemy(int index) : Enemy

1. ItemList

  private:

  1. m_itemFile : String

  1. m_items : vector<Item>

  1. m_itemNumber : int

  public:

  1. initialize() : void

  1. addItem(int atk, int def, int exp, int hp, int specialIndex) : void

  1. getItem(int index) : Item

1. Hero

  private:

  1. m_playerX : int

  1. m_playerY : int

  1. m_direction : int

  1. m_exp : int

  1. m_level : int

  1. m_atk : int

  1. m_def : int

  1. m_hp : int

  1. m_weapon : int

  1. m_equip : int

  public:

  1. addExp(int value) : void

  1. fight(int enmAtk, int enmDef, int enmHp, int enmExp) : bool

  1. getItem(int index) : void

  1. getItem(int addAtk, int addDef, int addExp, int addHp)

  1. 待补充

## ViewModel

1. GameViewModel

  private:

  1. m_hero : Hero

  1. mp_floor : shared_ptr<Floor>

  1. m_keyNumber : int[3]

  1. m_floorSet : FloorSet

  1. 火眼金睛等等

  public:

  1. move(int directionKey) : bool

  1. changeFloor(shared_ptr<Floor>) : void

1. EditorViewModel

  private:

  1. m_floorFileSet : FloorFileSet

  1. m_floor : Floor

  public:

  1. setFloorSquare(int x, int y, int type, int index) : void

  1. saveFloor(String filename) : void

  1. loadFloor(String filename) : void

  1. generateFloorSet(vector<Floor> floors, String filename) : void

  1. changeFloor(int index) : void

## View

## Window

1. SelectWindow

1. GameWindow

1. EditWindow

1. FormWindow

## App

1. MagicTowerApp
