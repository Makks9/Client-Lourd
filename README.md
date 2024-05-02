# Application Client-Lourd C#
![Logo LyonPalme](/Images/logo.png)


## Sommaire

- [Description](#description)
- [Diagramme de cas d'utilisation](#case)
- [Diagramme de séquence](#sequence)
- [technologies utilisées](#tehnologies)
- [Installation](#installation)
- [Utilisation](#utilisation)

## Description <a id="description"></a>
L'application Client-Lourd a été programmé en C# sur Visual Studio. L'application a pour utilité de pouvoir gérer un stock et les prêts de matériel, d'une association sportive nommé LyonPalme. Le Responsable va pouvoir suivre le matériel, ainsi que leur historique.

## Diagramme de cas d'utilisation <a id="case"></a>
![UseCase](/Images/usecase_gestion_materiel.png)

## Diagramme de séquence <a id="sequence"></a>
![Diagramme séquence](/Images/diagramme_de_séquence_gestion_matériel.png)

## Technologies utilisées <a id="technologies"></a>

| Ressources | Description |
| ------ | ------ |
| Gitlab | Plateforme de développement collaborative et de partage |
| C# | Langage de programmation commercialisé par Microsoft |
| SQL Server | environnement de développement intégré pour la gestion d'infrastructure SQL |
| Windows Forms | Interface graphique pour la création des formulaires |

## Installation <a id="installation"> </a>
Pour installer l'application, suivez les étapes ci-dessous :

! Pré-requis ! : L'application ne marchant pas sans base de données, vous devez impérativement vous connecter au réseau du lycée des Chassagnes pour faire marcher l'application.

1. Clonez le dépôt Git.
2. Placez-vous dans la branche master
3. Ouvrez le projet dans Visual Studio.
4. Remplacer le fichier App.config actuel ou créez le s'il n'en existe pas par ce code :
```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
    <startup> 
        <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7.2" />
    </startup>
	<connectionStrings>
		<add name="sqlserver_lyonpalme" connectionString="Data Source=192.168.100.236;Initial Catalog=matteobontemps;User ID=CBMatteo;Password=@pp|iKT1ON!" providerName="System.Data.SqlCLient" />
	</connectionStrings>
  <runtime>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <dependentAssembly>
        <assemblyIdentity name="Microsoft.IdentityModel.Abstractions" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-6.35.0.0" newVersion="6.35.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Runtime.CompilerServices.Unsafe" publicKeyToken="b03f5f7f11d50a3a" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-6.0.0.0" newVersion="6.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Security.Cryptography.ProtectedData" publicKeyToken="b03f5f7f11d50a3a" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-4.0.5.0" newVersion="4.0.5.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Security.AccessControl" publicKeyToken="b03f5f7f11d50a3a" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-6.0.0.0" newVersion="6.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Threading.Tasks.Extensions" publicKeyToken="cc7b13ffcd2ddd51" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-4.2.0.1" newVersion="4.2.0.1" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Text.Encodings.Web" publicKeyToken="cc7b13ffcd2ddd51" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-6.0.0.0" newVersion="6.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.ValueTuple" publicKeyToken="cc7b13ffcd2ddd51" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-4.0.3.0" newVersion="4.0.3.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Buffers" publicKeyToken="cc7b13ffcd2ddd51" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-4.0.3.0" newVersion="4.0.3.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Text.Json" publicKeyToken="cc7b13ffcd2ddd51" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-4.0.1.2" newVersion="4.0.1.2" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Diagnostics.DiagnosticSource" publicKeyToken="cc7b13ffcd2ddd51" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-6.0.0.1" newVersion="6.0.0.1" />
      </dependentAssembly>
    </assemblyBinding>
  </runtime>
</configuration>
```
5. Pour créer un fichier exécutable de l'application, il vous faut aller dans l'onglet "générer" puis cliquez sur "Publier LyonPalme"
6. Connecter vous avec les identifiants suivants :
	login : respmat &
	password : C1Secret!

## Utilisation <a id="utilisation"></a>
- affichage du stock disponible
- ajouter un prêt
- ajouter du stock de matériel
- récupération le matériel d'un prêt
