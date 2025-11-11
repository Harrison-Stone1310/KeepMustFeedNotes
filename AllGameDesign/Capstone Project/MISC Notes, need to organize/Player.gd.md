
class_name Player
extends CharacterBody2D

@onready
var animations= $AnimationPlayer
@onready
var sprites=$Animations

@onready
var state_machine= $Statemachine

func _ready():
	
	state_machine.init(self, animations, sprites)
	#attack_machine.init(self, attackAnimation)
	
func _unhandled_input(event: InputEvent)-> void:
	state_machine.processInput(event)
	#attack_machine.processInput(event)
func _physics_process(delta: float) ->void:
	state_machine.processPhysics(delta)
	#attack_machine.processPhysics(delta)
func _process(delta: float)->void:
	state_machine.processFrame(delta)
	#attack_machine.processFrame(delta)
