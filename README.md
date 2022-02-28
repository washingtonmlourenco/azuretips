                                                   ##Dicas Microfoft Azure.

## Caso tenha mais de uma Subscription no seu Azure, para que não haja confusão na hora de criar um Resource Group, e atrelar novos recursos a esse resource  group.
## Podemos setar a nossa subscription como principal, assim sempre que criar um serviço, já ficará setada sua assinatura principal.
## Step by Step:

**BEGIN TRAN**

   - Utilizando o **Cloud Shell** ou **Azure CLI(Command Line Interface)**.
     
     **##Login no Azure CLI:**
         **Digite:** 
          
          -> az --version >> Verifica a versão e se o azure cli foi instalado corretamente.
          -> az --login >> Faz Login localmente no CLI do Azure.
          
         -- **Setando Subscription como Principal:**
          -> az account list >> Lista todas as Subscriptions.
          -> az account set --subscription 'mySubscription' >> Seta sua subscription como principal.

​    -- **Criando um Resource Group:**

   - Um Grupo de Recursos é uma container associada a todas as soluções criadas no Azure, todas vezes que criamos um serviço no Azure temos que associar esse serviço a um Resource Group. 
          -> **az group create --location 'mylocation' -- name myRG** >> Cria um novo grupo de recursos, onde **location** -> é a região onde ficam as zonas de disponibilidade do Azure Próximas a você e **myRG** é o nome que você vai dar para seu novo grupo de recursos.
          
**COMMIT;**
