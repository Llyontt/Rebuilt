Common

    Square

private:

    m_type : int

    m_index : int

public:

    setType(int type) : void

    getType() : int

    setIndex(int index) : void

    getIndex() : int

    Floor

private:

    m_index : int

    m_squares : Square[11][11]

public:

    saveFloor(String filename) : void

    loadFloor(String filename) : void

    getIndex() : int

    setIndex(int index) : void

    setSquare(int type, int index, int x, int y) : void

    FloorSet

private:

    m_floors : vector

    m_floorNum : int

public:

    loadFloorSet(String filename) : void

    saveFloorSet(String filename) : void

    getFloorNum() : int

    setFloorNum(int floorNum) : void

    Enemy

private:

    m_hp : int

    m_atk : int

    m_def : int

    m_name : String

public:

    getHp() : int

    getAtk() : int

    getDef() : int

    getName() : int

    setHp(int value, int method) : void // method = 0：赋值；method = 1：增减

    setAtk(int value, int method) : void

    setDef(int value, int method) : void

    setName(String value) : void

    Item

private:

    m_name : String

    m_addAtk : int

    m_addDef : int

    m_addExp : int

    m_specialIndex : int

    m_addHp : int

    m_walkable : bool

public:

    getName() : String

    setName(String name) : void

    getAddAtk() : int

    getAddDef() : int

    getAddExp() : int

    getSpecialIndex() : int

    getAddHp() : int

    getWalkable() : bool

    setWalkable(bool wkb) : void

    FloorFileSet

private:

    filenameSet : vector

public:

    getFilename(int index) : String

    getFileNumber() : int

Model

    EnemyList

private:

    m_enemyFile : String

    m_enemies : vector

    m_enemyNumber : int

public:

    intialize() : void

    addEnemy(int atk, int def, int hp, int exp) : void

    getEnemy(int index) : Enemy

    ItemList

private:

    m_itemFile : String

    m_items : vector

    m_itemNumber : int

public:

    initialize() : void

    addItem(int atk, int def, int exp, int hp, int specialIndex) : void

    getItem(int index) : Item

    Hero

private:

    m_playerX : int

    m_playerY : int

    m_direction : int

    m_exp : int

    m_level : int

    m_atk : int

    m_def : int

    m_hp : int

    m_weapon : int

    m_equip : int

public:

    addExp(int value) : void

    fight(int enmAtk, int enmDef, int enmHp, int enmExp) : bool

    getItem(int index) : void

    getItem(int addAtk, int addDef, int addExp, int addHp)

    待补充

ViewModel

    GameViewModel

private:

    m_hero : Hero

    mp_floor : shared_ptr

    m_keyNumber : int[3]

    m_floorSet : FloorSet

    火眼金睛等等

public:

    move(int directionKey) : bool

    changeFloor(shared_ptr) : void

    EditorViewModel

private:

    m_floorFileSet : FloorFileSet

    m_floor : Floor

public:

    setFloorSquare(int x, int y, int type, int index) : void

    saveFloor(String filename) : void

    loadFloor(String filename) : void

    generateFloorSet(vector floors, String filename) : void

    changeFloor(int index) : void

View
Window

    SelectWindow

    GameWindow

    EditWindow

    FormWindow

App

    MagicTowerApp
