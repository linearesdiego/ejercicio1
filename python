class Email:
    __idCuenta= ""
    __dominio= ""
    __tipodominio= ""
    __contrasena= ""
    def __init__(self,idcuenta,dominio,tipodominio,contrasena=None): 
        self.__idCuenta=idcuenta 
        self.__dominio=dominio
        self.__tipodominio=tipodominio
        self.__contrasena=contrasena
    
    def retornaEmail(self):
        return ('{}@{}{}'.format(self.__idCuenta,self.__dominio,self.__tipodominio))

    def getDominio(self):
        return(self.__dominio)
    
    def getContrasena(self):
        return self.__contrasena

    def cambiarContra(self,actual,nueva):
        if(actual==self.__contrasena):
            self.__contrasena=nueva
            print("Guardado Exitosamente")
        else:
            print("ERROR: La contraseña no coincide")

    @staticmethod
    def crearCuenta(correo):
        x=correo.split("@")
        newid=x[0]
        y=x[1].split(".")
        newdom=y[0]
        newtip=y[1]
        return Email(newid,newdom,newtip)


if __name__ == "__main__":
    nom=input("Ingrese su Nombre: ")
    nomu=input("Nombre Usuario: ")
    idd=input("IdCuenta: ")
    dom=input("Dominio: ")
    tdom=input("Tipo de Dominio: ")
    cont=input("Contraseña: ")
    email1 = Email(idd, dom, tdom, cont)
    print(f'Estimado {nom} te enviaremos tus mensajes a la dirección {email1.retornaEmail()}')   
    print("#Modificar Contraseña")
    actual=input("Ingrese Contraseña Actual: ")
    nueva=input("Ingrese Nueva Contraseña: ")
    email1.cambiarContra(actual,nueva)  
    nueco=input("#Ingrese Correo:")
    nuevo=Email.crearCuenta(nueco)
    print(nuevo.retornaEmail())
