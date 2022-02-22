**super-home-restock-ressuply**

This script will execute the following actions, in the following order:

```md
1. Use Detecting Hidden, and only continue if no hidden players are found
2. Unload misc items (items that dont have a shelf for it)
3. Drop the following items in their respective Tome:
   - tmaps
   - resource maps (all types)
   - Drop skill scrolls in the Skill Scroll Tome
   - Aspect Items (cores, extracts, destils and philacteries)
   - Rare Cloths
   - All types of dyes
   - Inscription Runes
4. Use a repair bench if there is one nearby
5. Drop gold in the Bank Deposit Box / Personal Container
6. Deposit gold from all char pack animals
7. Restock Storage Shelf using self
8. Restock Storage Shelf using all pack animals
9. Restock Resource Stockpile using self
10. Restock Resource Stockpile using all pack animals
11. Restock Garden Shelf using self
12. Dump magic items in the Recycler
13. Shelf Ressuply
```

**SETUPS**

**Ground Setup (Default/Recommended Setup)**

All destinations (shelfs, stockpiles, tomes...) secured/locked down in the ground, within 2 tiles of the char.

**Containers/Subcontainers Setup**

This is manly for people who dont have enough secures/lockdowns to use the recommended setup.
In this setup the script searches for your Tomes inside a container instead of directly on the ground
It can also be set to not deposit gold on the vault if you preffer to store your gold in a container on the house.
If you dont have enough secures/lockdowns to use the recommended setup, you can set the destination for all items yourself, by setting one of each following options:

- **unload_misc_items_ground_container** OR **unload_misc_items_in_subcontainer**
- **use_gold_deposit_ground_container** OR **use_gold_deposit_subcontainer**
- **use_tomes_ground_container** OR **use_tomes_subcontainer**

For any of the **subcontainers** options, you will also need to set your **main_unload_container**, witch it will use to search for all the subcontainers. The script will only ask you to select any container again if it cant find it within 2 tiles.

**OTHER OPTIONS**:

- **object_delay**
  Delay for all actions
- **unload_misc_items**
  If should also unload misc items (skill orbs, RMs...)

**PS: All options are available at the top of the file**

#####################################################################################

# PT_BR

Este script vai executar as seguintes ações, na seguinte ordem:

```md
1. Jogar todos os mapas da bag em seus respectivos tomes
2. Jogar Skill Scrolls no tome de scroll
3. Jogar Itens de Aspecto (cores, extratos, phylacteries) no tome de aspecto
4. Jogar tecido no Rare Cloth Tome
5. Jogar tintas (cabelo, fortuniture, carpet) no Dyes Tome
6. Usar a repair bench se encontrar uma perto
7. Jogar ouro no cofre se encontrar ouro na bag e o cofre no chao
8. Restocar a shelf pra jogar os regs do char nela
9. Restocka a shelf com todos os pack animals que encontrar perto do char
10. Restocar a shelf de recurso se encontrar uma perto
11. Restocka a shelf de recurso com todos os pack animals que encontrar perto do char
12. Restocar a shelf de jardin se encontrar uma perto
13. Por fim, dar ressuply na shelf pra reabastecer o char
```

A intenção é permitir que o player chegue em casa do farm e guarde tudo e reabasteça novamente com apenas 1 clique.
Apesar de realizar varias ações, tudo acontece bem rapido, cerca de 1 segundo para executar o script todo.

Para isto funcionar, voce deve deixar todos os containers a até 2 tiles do char
