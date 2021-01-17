---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470570"
---
# New-AzDataFactoryEncryptValue

## SYNOPSIS
Verschlüsselt vertrauliche Daten.

## SYNTAX

### ByFactoryName (Standard)
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzDataFactoryEncryptValue"** verschlüsselt vertrauliche Daten, z. B. ein Kennwort oder eine Microsoft SQL Server-Verbindungszeichenfolge, und gibt einen verschlüsselten Wert zurück.

## BEISPIELE

### Beispiel 1: Verschlüsseln einer Nicht-ODBC-Verbindungszeichenfolge
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

Der erste Befehl verwendet das ConvertTo-SecureString-Cmdlet, um die angegebene Verbindungszeichenfolge in ein **SecureString-Objekt** zu konvertieren, und speichert dieses Objekt dann in der $Value Variable.
Weitere Informationen erhalten Sie, wenn Sie " `Get-Help ConvertTo-SecureString` eingeben" aus.
Zulässige Werte: SQL Server oder Oracle-Verbindungszeichenfolge.
Der zweite Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value für die angegebene Daten factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.

### Beispiel 2: Verschlüsseln einer Nicht-ODBC-Verbindungszeichenfolge, die die Windows-Authentifizierung verwendet.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

Der erste Befehl verwendet **ConvertTo-SecureString,** um die angegebene Verbindungszeichenfolge in ein sicheres Zeichenfolgenobjekt zu konvertieren, und speichert dieses Objekt dann in der $Value Variable.
Der zweite Befehl verwendet das cmdlet Get-Credential zum Erfassen der Windows-Authentifizierung (Benutzername und Kennwort) und speichert dieses **"PSCredential"-Objekt** dann in der $Credential Variable.
Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Credential` eingeben" aus.
Der dritte Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value und $Credential für die angegebene Daten factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.

### Beispiel 3: Verschlüsseln des Servernamens und der Anmeldeinformationen für den verknüpften Dateisystemdienst
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

Der erste Befehl verwendet **ConvertTo-SecureString,** um die angegebene Zeichenfolge in eine sichere Zeichenfolge zu konvertieren, und speichert dieses Objekt dann in der $Value Variable.
Der zweite Befehl verwendet **"Get-Credential"** zum Sammeln der Windows-Authentifizierung (Benutzername und Kennwort) und speichert dieses **"PSCredential"-Objekt** dann in der $Credential Variable.
Der dritte Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value und $Credential für die angegebene Daten factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.

### Beispiel 4: Verschlüsseln der Anmeldeinformationen für den verknüpften HDFS-Dienst
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

Der **Befehl "ConvertTo-SecureString"** konvertiert die angegebene Zeichenfolge in eine sichere Zeichenfolge.
Der **Befehl "Neues Objekt"** erstellt ein "PSCredential"-Objekt mit dem sicheren Benutzernamen und den Kennwortzeichenfolgen.
Stattdessen könnten Sie den Befehl **"Get-Credential"** verwenden, um die Windows-Authentifizierung (Benutzername und Kennwort) zu sammeln, und dann das zurückgegebene **"PSCredential"-Objekt** wie in den vorherigen Beispielen gezeigt in der $credential-Variable speichern.
Der **Befehl "New-AzDataFactoryEncryptValue"** erstellt einen verschlüsselten Wert für das Objekt, das in $Credential für die angegebene Datenfactory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.

### Beispiel 5: Verschlüsseln der Anmeldeinformationen für den verknüpften ODBC-Dienst
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

Der **Befehl "ConvertTo-SecureString"** konvertiert die angegebene Zeichenfolge in eine sichere Zeichenfolge.
Der **Befehl "New-AzDataFactoryEncryptValue"** erstellt einen verschlüsselten Wert für das Objekt, das in $Value für die angegebene Datenfactory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.

## PARAMETERS

### -AuthenticationType
Gibt den Authentifizierungstyp an, der zum Herstellen einer Verbindung mit der Datenquelle verwendet werden soll.
Die zulässigen Werte für diesen Parameter sind:
- Windows
- Standard
- Anonym.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Gibt die zu verwendenden Anmeldeinformationen für die Windows-Authentifizierung (Benutzername und Kennwort) an.
Dieses Cmdlet verschlüsselt die hier angegebenen Anmeldeinformationen.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
Gibt den Datenbanknamen des verknüpften Diensts an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactory
Gibt ein **"PSDataFactory"-Objekt** an.
Dieses Cmdlet verschlüsselt Daten für die Daten factory, die dieser Parameter angibt.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Gibt den Namen einer Daten factory an.
Dieses Cmdlet verschlüsselt Daten für die Daten factory, die dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewayName
Gibt den Namen des Gateways an.
Dieses Cmdlet verschlüsselt die Daten für das Gateway, das dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCredentialValue
Gibt den Teil der OdBC-Verbindungszeichenfolge (Open Database Connectivity) ohne Anmeldeinformationen an.
Dieser Parameter gilt nur für den verknüpften ODBC-Dienst.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.
Dieses Cmdlet verschlüsselt Daten für die Gruppe, die dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Server
Gibt den Servernamen des verknüpften Diensts an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Gibt den verknüpften Diensttyp an.
Dieses Cmdlet verschlüsselt Daten für den verknüpften Diensttyp, den dieser Parameter angibt.
Die zulässigen Werte für diesen Parameter sind:
- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
Gibt den zu verschlüsselnden Wert an.
Verwenden Sie für einen lokalen SQL Server verknüpften Dienst und einen lokalen verknüpften Oracle-Dienst eine Verbindungszeichenfolge.
Verwenden Sie für einen lokalen ODBC-verknüpften Dienst den Anmeldeinformationsteil der Verbindungszeichenfolge.
Verwenden Sie für einen lokalen, mit dem Dateisystem verknüpften Dienst den lokalen Dateisystemnamen des Gatewaycomputers, verwenden Sie "Local" oder "localhost". Wenn sich das Dateisystem auf einem anderen Server als dem Gatewaycomputer befindet, verwenden Sie den \\ \\ Servernamen.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## AUSGABEN

### System.String

## HINWEISE
* Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys

## LINKS ZU VERWANDTEN THEMEN

[New-AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


