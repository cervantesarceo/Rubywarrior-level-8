Rubywarrior-level-8
===================

level 8
class Player
  def play_turn(warrior)
    # cool code goes here
  
  if warrior.feel.enemy?
    warrior.attack!
  elsif warrior.feel.captive?
    warrior.rescue!
  elsif warrior.health<20  
    if warrior.health<@health
      warrior.walk!
    elsif warrior.feel.enemy?
      warrior.attack!
    elsif warrior.look.any? { |space| space.enemy? }
      warrior.shoot!
    else warrior.rest!
    end
  elsif warrior.feel.empty?
    warrior.walk!
  end 
    @health = warrior.health
    
  end
  end
