# python-codes
def greetings():
    print("Hello there, may we know you name sir")
    user= input("Hi Enter your name")     
    print( "Hi "+user+" Welcome to Dmart!!!! Have a Happy Shopping")
global our_items
our_items ={"limca":9,"sprite":10,"maaza":19,"coco_cola":27,"7up":4}    
def items():
	print ("Here are our items")
	y=1
	for x in our_items.keys():
		print (y,x)
		y+=1
def inputs():
    global user_input
    user_input=int(input(""" press 1 for list of items,
    press 5 to exit"""))
def selection():
    
    global basket
    basket={}
    id="p"
    while id!="q":
        items()
        id=(input("""Select the drink in the list or type q to exit"""))
        print("the quantity of your drink is : "+ str(our_items[id]))
        quant_req= int(input("Mention the required no of quantity"))
        while quant_req>our_items[id]:
            print("Required quantity exceeds quantity present please choose again")
            quant_req= int(input("Mention the required no of quantity"))
        print("item added to basket")
        our_items[id]=our_items[id]-quant_req
        basket[id]=quant_req
        
        id=(input("""Select p to proceed with shopping or type q to exit"""))
        
    print ("Here is your cart, thanks for shopping")
    print(basket)
    
        
    

greetings()        
inputs()
while user_input==1:
    
    selection()
    user_input=int(input(""" press 1 for list of items,
    press 5 to exit"""))
    


print ("Here is your cart, thanks for shopping")
print(basket) 
print("Thanks for visiting hope you had a great shopping experience")
    
