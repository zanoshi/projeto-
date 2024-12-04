# projeto
import pygame
import random

# Inicializar o pygame
pygame.init()


py
# Definir as cores
WHITE = (
WHITE
255, 255, 255)
BLACK = (
BLACK = 

BLACK

B
0, 0, 0)
RED = (255, 0, 0)
GREEN = (0, 255, 0)
BLUE = (
BLUE = (

BLUE 

BL
0, 0, 255)

# Definir a largura e a altura da tela
LARGURA = 
LARGURA =

LARG
800
ALTURA = 
ALTURA =

ALTU
600
screen = pygame.display.set_mode((LARGURA, ALTURA))
pygame.display.set_caption(
screen = pygame.display.set_mode((LARGURA, ALTURA))
pygame.display.set_capti

screen = pygame.display.set_mode((LARGURA, ALTURA))
pygame.display.set_

screen = pygame.display.set_mode((LARGURA, ALTURA))
pygame.displa

screen = pygame.display.set_mode((LARGURA, ALTURA))
pygame

screen = pygame.display.set_mode((LARGURA, ALTURA)

screen = pygame.display.set_mode((LARGURA,

screen =

scree

sc
"Jogo de Moto")

# Definir a velocidade do jogo
clock = pygame.time.Clock()
FPS = 
clock = pygame.time.Clock()

clock = pygame.time.

clock = pyg

cl
60

# Classe para a moto

c
class Moto:
    
  
def __init__(self, x, y):
        self.x = x
        self.y = y
        self.largura = 
        self.x = x
        self.y = y
        self.larg

        self.x = x
        self.y = y
       

        self.x = x
   

        self
50
        self.altura = 
        self.altura =

        self.al

        
100
        self.velocidade = 
        self.velocid

        sel

 
5

    

def mover(self, esquerda, direita):
        
     
if esquerda:
            self.x -= self.velocidade
        
            self.x -= self.velocidade
 

            self.x -= self.velocidad

            self.x -= self.veloci

            self.x -= self.vel

            self.x -= self

            self.x -= 

            self.x

        

    
if direita:
            self.x += self.velocidade

    
            self.x += self.velocidade

   

            self.x += self.veloc

            self.x +=

         

     
def desenhar(self):
        pygame.draw.rect(screen, BLUE, (self.x, self.y, self.largura, self.altura))


        pygame.draw.rect(screen, BLUE, (self.x, self.y, self.largura, self.altura)

        pygame.draw.rect(screen, BLUE, (self.x, self.y, self.largura, self.alt

        pygame.draw.rect(screen, BLUE, (self.x, self.y, sel

        pygame.draw.rect(screen, BLUE, (self.x, self.y, 

        pygame.draw.rect(screen, BLUE, (self.x, self.

        pygame.draw.rect(screen, BLUE, (self.x, se

        pygame.draw.rect(screen, BLUE, (self.x

        pygame.draw.rect(screen, BLUE, (se

        pygame.draw.rect(screen, BLUE,

        pygame.draw.rect(screen, 

        pygame.draw.rect(scr

        pygame.draw.re

        p

   
# Classe para os obstáculos (carros)

cl
class Obstaculo:
    
   
def __init__(self):
        self.x = random.randint(
        self.x = random.randint(

        self.x = random.rand

        self.x = random

        self.x = r

        self

        s

     

 
0, LARGURA - 50)
        self.y = -
        self.y =

        sel

      
100  # Começam fora da tela
        self.largura = 
        self.

        se

       
50
        self.altura = 
        self.altura = 

        self
100
        self.velocidade = random.randint(
        self.velocidade = random.randint(

        self.velocidade = random.ra

        self.velocidade = ran

        self.velocidad

        self.v

     
4, 8)

    

    de


  
def mover(self):
        self.y += self.velocidade

    
        self.y += self.velocidade

    

        self.y += self.velocidad

        self.y += self.v

        se

    
def desenhar(self):
        pygame.draw.rect(screen, RED, (self.x, self.y, self.largura, self.altura))

    
        pygame.draw.rect(screen, RED, (self.x, self.y, self.largura, self.altura))

    de

        pygame.draw.rect(screen, RED, (self.x, self.y, self.largura, self.altura))

  

        pygame.draw.rect(screen, RED, (self.x, self.y, self.largura, self.altura)

        pygame.draw.rect(screen, RED, (self.x, self.y, self.largura, self.al

        pygame.draw.rect(screen, RED, (self.x, self.y, self.largura, s

        pygame.draw.rect(screen, RED, (self.x, self.y, self.

        pygame.draw.rect(screen, RED, (self.x, self.y, se

        pygame.draw.rect(screen, RED, (self.x, self.y,

        pygame.draw.rect(screen, RED

        pygame.draw.rect(screen, 

        pygame.draw.rect(scree

        pygame.draw.rect(sc

        pygame.draw.rect

        pygame.draw.

        pygame.d

        pyg

      
def fora_da_tela(self):
        
        retu

       

  
return self.y > ALTURA

# Função principal
def game():
    rodando = 
    rodando = 

    rodand

    r
True
    pontos = 
    po

   
0
    moto = Moto(LARGURA // 
    moto = Moto

    moto = Mo

    moto =

    mot

    
2 - 25, ALTURA - 120)  # Posição inicial da moto
    obstaculos = []
    esquerda = direita = 
    obstaculos = []
    esquerda = direita =

    obstaculos = []
    esquerda = di

    obstaculos = []
    esque

    obstaculos = []
    e

    obstaculos = []
 

    obstaculos =
False

    

    w
while rodando:
        screen.fill(WHITE)
        
        
        screen.fill(WHITE)
        
     

        screen.fill(WHITE)
        

        screen.fi

        screen

        scr

        

    
# Verificar eventos (como o fechamento da janela)
        for evento in pygame.event.get():
            
         
if evento.type == pygame.QUIT:
                rodando = 
                rodando = Fal

                rodando

                r

          

  
False
            
           

       

  
if evento.type == pygame.KEYDOWN:
                
            
if evento.key == pygame.K_LEFT:
                    esquerda = 
                    e

               

         

  
True
                
           

 
if evento.key == pygame.K_RIGHT:
                    direita = 
                    direita 

                    direi

                    di

                   

                

            

        

   
True
            if evento.type == pygame.KEYUP:
                
              

      
if evento.key == pygame.K_LEFT:
                    esquerda = 
                    esquerda

               

       
False
                
            

  
if evento.key == pygame.K_RIGHT:
                    direita = 
                    direita = 

                    direita

                    dire

                    

                

            

       

 
False
        
        
        
       

        

   
# Mover e desenhar a moto
        moto.mover(esquerda, direita)
        moto.desenhar()

        
        moto.mover(esquerda, direita)
        moto.desenhar()

    

        moto.mover(esquerda, direita)
        moto.desenhar()

        moto.mover(esquerda, direita)
        moto.desenhar

        moto.mover(esquerda, direita)
        moto.dese

        moto.mover(esquerda, direita)
        moto.

        moto.mover(esquerda, direita)
        

        moto.mover(esquerda, direita)
   

        moto.mover(esquerda, direit

        moto.mover(esquerda,

        moto.mover(es

        m

     
# Gerar obstáculos e movê-los
        
        

     

 
if random.randint(1, 60) == 1:  # Chance de gerar um novo obstáculo
            obstaculos.append(Obstaculo())
        
        
            obstaculos.append(Obstaculo())
        
     

            obstaculos.append(Obstaculo())
        
  

            obstaculos.append(Obstaculo())
        

            obstaculos.append(Obstaculo())
     

            obstaculos.append(Obstaculo())
 

            obstaculos.append(Obstaculo(

            obstaculos.append(Obstac

            obsta

            ob

           

        

    
for obstaculo in obstaculos[:]:
            obstaculo.mover()
            obstaculo.desenhar()

            
            obstaculo.mover()
            obstaculo.desenhar()

            

            obstaculo.mover()
            obstaculo.desenhar()

      

            obstaculo.mover()
            obstaculo.desenhar()

 

            obstaculo.mover()
            obstaculo.desenhar

            obstaculo.mover()
           

            obstaculo.mover()
        

            obstaculo.mover()
     

            obstaculo.mover()
  

            obstaculo.mover(

            obstaculo.mo

            obstacul

            obs

   
# Checar colisão
            
         

      

  
if (moto.x < obstaculo.x + obstaculo.largura and moto.x + moto.largura > obstaculo.x and
                moto.y < obstaculo.y + obstaculo.altura 
                moto.y < obstaculo.y + obstaculo.altura 

                moto.y < obstaculo.y + obstaculo.al

                moto.y < obstaculo.y + obstacu

                moto.y < obstaculo.y 

                moto.y < obstaculo

               

            

         

      

  
and moto.y + moto.altura > obstaculo.y):
                
                p

             

        

  
print("Você perdeu!")
                rodando = 
                rodando = Fals

                rodando = F

                rodando 

                roda

                

           

      
False

            

       
# Remover obstáculos que saíram da tela
            
          

      

  
if obstaculo.fora_da_tela():
                obstaculos.remove(obstaculo)
                pontos += 
                obstaculos.remove(obstaculo)
          

                obstaculos.remove(obstaculo)
       

                obstaculos.remove(obstaculo)
    

                obstaculos.remove(obstaculo)
 

                obstaculos.remove(obstacul

                obstaculos.remove(obst

                obstaculos.remove

                obstaculos.r

                obstac

                

         

     
1

        

   


# Exibir o número de pontos
        fonte = pygame.font.SysFont(
        fonte = pygame.font

        fonte = pygame.f

        fonte = pygam

        fonte = py

        fonte 

        fo

     
None, 35)
        texto = fonte.render(
        texto = fonte.render

        t

      

   
f"Pontos: {pontos}", True, BLACK)
        screen.blit(texto, (
        screen.blit(texto, 

        screen.blit(text

      

   
10, 10))

        pygame.display.update()
        clock.tick(FPS)

    pygame.quit()



        pygame.display.update()
        clock.tick(FPS)

    pygame.quit()


        pygame.display.update()
        clock.tick(FPS)

    pygame.q


        pygame.display.update()
        clock.tick(FPS)

    py


        pygame.display.update()
        clock.tick(FPS)


        pygame.display.update()
        clock.tic


        pygame.display.update()
   


        pygame.display.update


        pygame.dis


        pygame
# Iniciar o jogo
game()
