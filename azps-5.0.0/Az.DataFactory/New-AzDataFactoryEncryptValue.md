---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298426"
---
# New-AzDataFactoryEncryptValue

## Synopsis
Verschlüsselt vertrauliche Daten.

## Syntax

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

## Beschreibung
Das Cmdlet **New-AzDataFactoryEncryptValue** verschlüsselt vertrauliche Daten wie ein Kennwort oder eine Microsoft SQL Server-Verbindungszeichenfolge und gibt einen verschlüsselten Wert zurück.

## Beispiele

### Beispiel 1: Verschlüsseln einer nicht-ODBC-Verbindungszeichenfolge
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

Der erste Befehl verwendet das ConvertTo-SecureString-Cmdlet, um die angegebene Verbindungszeichenfolge in ein **SecureString** -Objekt zu konvertieren, und speichert dieses Objekt dann in der Variablen $value.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` .
Zulässige Werte: SQL Server-oder Oracle-Verbindungszeichenfolge.
Der zweite Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.

### Beispiel 2: Verschlüsseln einer nicht-ODBC-Verbindungszeichenfolge, die die Windows-Authentifizierung verwendet
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

Der erste Befehl verwendet **ConvertTo-SecureString** , um die angegebene Verbindungszeichenfolge in ein sicheres Zeichenfolgenobjekt zu konvertieren, und speichert dieses Objekt dann in der $Value Variablen.
Der zweite Befehl verwendet das Get-Credential-Cmdlet, um die Windows-Authentifizierung (Benutzername und Kennwort) zu erfassen, und speichert dann das **PSCredential** -Objekt in der $Credential-Variablen.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .
Der dritte Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value und $Credential für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.

### Beispiel 3: Verschlüsseln des Server namens und der Anmeldeinformationen für den Dateisystem-verknüpften Dienst
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

Der erste Befehl verwendet **ConvertTo-SecureString** , um die angegebene Zeichenfolge in eine sichere Zeichenfolge zu konvertieren, und speichert dieses Objekt dann in der $Value Variablen.
Der zweite Befehl verwendet **Get-Credential** , um die Windows-Authentifizierung (Benutzername und Kennwort) zu erfassen, und speichert dann das **PSCredential** -Objekt in der $Credential-Variablen.
Der dritte Befehl erstellt einen verschlüsselten Wert für das Objekt, das in $Value und $Credential für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.

### Beispiel 4: Verschlüsseln von Anmeldeinformationen für HDFS-verknüpften Dienst
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

Der Befehl **ConvertTo-SecureString** wandelt die angegebene Zeichenfolge in eine sichere Zeichenfolge um.
Mit dem Befehl " **New-Object** " wird ein PSCredential-Objekt mithilfe der Zeichenfolgen für sicheres Benutzernamen und Kennwort erstellt.
Stattdessen können Sie den Befehl **Get-Credential** verwenden, um die Windows-Authentifizierung (Benutzername und Kennwort) zu erfassen und dann das zurückgegebene **PSCredential** -Objekt in der $Credential-Variable zu speichern, wie in den vorherigen Beispielen dargestellt.
Der Befehl **New-AzDataFactoryEncryptValue** erstellt einen verschlüsselten Wert für das Objekt, das in $Credential für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.

### Beispiel 5: Verschlüsseln von Anmeldeinformationen für ODBC-verknüpften Dienst
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

Der Befehl **ConvertTo-SecureString** wandelt die angegebene Zeichenfolge in eine sichere Zeichenfolge um.
Der Befehl **New-AzDataFactoryEncryptValue** erstellt einen verschlüsselten Wert für das Objekt, das in $Value für die angegebene Daten Factory, das Gateway, die Ressourcengruppe und den verknüpften Diensttyp gespeichert ist.

## Parameter

### -AuthenticationType
Gibt den Authentifizierungstyp an, der für die Verbindung mit der Datenquelle verwendet werden soll.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Windows
- Grundlegende
- Anonyme.

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

### – Anmeldeinformationen
Gibt die Windows-Authentifizierungsanmeldeinformationen (Benutzername und Kennwort) an, die verwendet werden sollen.
Mit diesem Cmdlet werden die hier angegebenen Anmeldeinformationsdaten verschlüsselt.

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

### -Datenbank
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
Gibt ein **PSDataFactory** -Objekt an.
Dieses Cmdlet verschlüsselt Daten für die Data Factory, die dieser Parameter angibt.

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

### -Datafactoryname
Gibt den Namen einer Data Factory an.
Dieses Cmdlet verschlüsselt Daten für die Data Factory, die dieser Parameter angibt.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Gatewayname
Gibt den Namen des Gateways an.
Dieses Cmdlet verschlüsselt Daten für das Gateway, das dieser Parameter angibt.

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

### -Nicht credentialvalue
Gibt den Teil der nicht-Anmeldeinformationen der ODBC-Verbindungszeichenfolge (Open Database Connectivity) an.
Dieser Parameter ist nur für den ODBC-verknüpften Dienst anwendbar.

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

### -Typ
Gibt den verknüpften Diensttyp an.
Mit diesem Cmdlet werden Daten für den Typ des verknüpften Diensts verschlüsselt, den dieser Parameter angibt.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
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

### -Wert
Gibt den zu verschlüsselenden Wert an.
Verwenden Sie für einen lokalen SQL Server-verknüpften Dienst und einen lokalen Oracle-verknüpften Dienst eine Verbindungszeichenfolge.
Verwenden Sie für einen lokalen ODBC-verknüpften Dienst den Anmelde Informationsteil der Verbindungszeichenfolge.
Verwenden Sie für den verknüpften Dienst im lokalen Dateisystem, wenn das Dateisystem lokal auf dem Gatewaycomputer vorhanden ist, local oder localhost, und wenn sich das Dateisystem auf einem anderen Server als dem Gatewaycomputer befindet, verwenden Sie \\ \\ Servername.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## Ausgaben

### System. String

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys

## Verwandte Links

[Neu – AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


