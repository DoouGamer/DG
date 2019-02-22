
public class equipe implements Listener{
	@EventHandler
	public void onClick(InventoryClickEvent e) {
		Player p = (Player) e.getWhoClicked();
		if (e.getClickedInventory().getTitle().contains("§a§lEquipe")) {
			
		 e.setCancelled(true);
	 }
		if (e.getCurrentItem().getItemMeta().getDisplayName().contains("§c§lVoltar")) {
				  
				
			p.openInventory(equipe.inv(p));
		}

	}

	public static Inventory inv(Player p){

	
		Inventory i = Bukkit.createInventory(null, 6*9, "§3§lEquipe");
		
		SkullMeta diretor = (SkullMeta) Bukkit.getItemFactory().getItemMeta(Material.SKULL_ITEM);
		
		ItemStack master = new ItemStack(Material.SKULL_ITEM, 1, (byte) 3);
		master.setItemMeta(diretor);
		diretor.setOwner("CommandBlock");
		diretor.setDisplayName("§6§lDiretor");
		ArrayList<String> lore = new ArrayList<>();
		lore.add("§e§lVeja a equipe de direção");
		diretor.setLore(lore);
		master.setItemMeta(diretor);
		
		SkullMeta grt = (SkullMeta) Bukkit.getItemFactory().getItemMeta(Material.SKULL_ITEM);
		ItemStack gerente = new ItemStack(Material.SKULL_ITEM, 1, (byte) 3);
		gerente.setItemMeta(grt);
		grt.setOwner("CommandBlock");
		grt.setDisplayName("§4§lGerente");
		ArrayList<String> lore1 = new ArrayList<>();
		lore1.add("§e§lVeja a equipe de gerenciamento");
		grt.setLore(lore1);
		gerente.setItemMeta(grt);
		
		SkullMeta adm = (SkullMeta) Bukkit.getItemFactory().getItemMeta(Material.SKULL_ITEM);
		ItemStack admin = new ItemStack(Material.SKULL_ITEM, 1, (byte) 3);
		admin.setItemMeta(adm);
		adm.setOwner("CommandBlock");
		adm.setDisplayName("§c§lAdministrador");
		ArrayList<String> lore2 = new ArrayList<>();
		lore2.add("§e§lVeja a equipe de administração");
		adm.setLore(lore2);
		admin.setItemMeta(adm);
		
		SkullMeta mod = (SkullMeta) Bukkit.getItemFactory().getItemMeta(Material.SKULL_ITEM);
		ItemStack moderador = new ItemStack(Material.SKULL_ITEM, 1, (byte) 3);
		moderador.setItemMeta(mod);
		mod.setOwner("CommandBlock");
		mod.setDisplayName("§2§lModerador");
		ArrayList<String> lore3 = new ArrayList<>();
		lore3.add("§e§lVeja a equipe de moderação");
		mod.setLore(lore3);
		moderador.setItemMeta(mod);
		
		SkullMeta ajd = (SkullMeta) Bukkit.getItemFactory().getItemMeta(Material.SKULL_ITEM);
		ItemStack ajudante = new ItemStack(Material.SKULL_ITEM, 1, (byte) 3);
		ajudante.setItemMeta(ajd);
		ajd.setOwner("CommandBlock");
		ajd.setDisplayName("§e§lAjudate");
		ArrayList<String> lore4 = new ArrayList<>();
		lore4.add("§e§lVeja a equipe de ajudantes");
		ajd.setLore(lore4);
		ajudante.setItemMeta(ajd);
		
		SkullMeta dev = (SkullMeta) Bukkit.getItemFactory().getItemMeta(Material.SKULL_ITEM);
		ItemStack desenvolvedor = new ItemStack(Material.SKULL_ITEM, 1, (byte) 3);
		desenvolvedor.setItemMeta(dev);
		dev.setOwner("CommandBlock");
		dev.setDisplayName("§9§lDesenvolvedor");
		ArrayList<String> lore5 = new ArrayList<>();
		lore5.add("§e§lVeja a equipe de desenvolvedores");
		dev.setLore(lore5);
		desenvolvedor.setItemMeta(dev);
		
		ItemStack voltar = new ItemStack(Material.ARROW);
		ItemMeta back = voltar.getItemMeta();
		back.setDisplayName("§c§lVoltar");
		back.addEnchant(Enchantment.DAMAGE_ALL, 1, true);
		back.addItemFlags(ItemFlag.HIDE_ENCHANTS);
		voltar.setItemMeta(back);
		
		i.setItem(49, voltar);
		i.setItem(33, desenvolvedor);
		i.setItem(31, ajudante);
		i.setItem(29, moderador);
		i.setItem(23, admin);
		i.setItem(21, gerente);
		i.setItem(13, master);
		return i;
	}

}
