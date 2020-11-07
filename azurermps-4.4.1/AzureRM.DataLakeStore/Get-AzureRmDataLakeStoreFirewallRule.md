---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 8c7d936f8ea64534016286e97b34d36f41a72cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663962"
---
# Get-AzureRmDataLakeStoreFirewallRule

## Synopsis
Ruft die angegebenen Firewallregeln im angegebenen Data Lake Store ab.
Wenn keine Firewall-Regel angegeben ist, werden alle Firewallregeln für das Konto aufgelistet.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Get-AzureRmDataLakeStoreFirewallRule-Cmdlet ruft die angegebenen Firewallregeln im angegebenen Data Lake Store ab.
Wenn keine Firewall-Regel angegeben ist, werden alle Firewallregeln für das Konto aufgelistet.

## Beispiele

### Beispiel 1: Abrufen einer bestimmten Firewall-Regel
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

Gibt die Firewall-Regel mit dem Namen "MyFirewallRule" aus dem Konto "ContosoADL" zurück.

### Beispiel 2: Auflisten aller Firewallregeln in einem Konto
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

Gibt alle Firewall-Regeln im Konto "ContosoADL" zurück.

## Parameter

### -Konto
Das Data Lake Store-Konto, aus dem die Firewall-Regel abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Der Name der Firewall-Regel, die abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe, unter der die angegebene Firewall-Regel des angegebenen Kontos abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### DataLakeStoreFirewallRule
Die angegebene Firewall-Regel zum Abrufen

### IList<DataLakeStoreFirewallRule>
Die Liste der Firewallregeln im angegebenen Konto.

## Notizen

## Verwandte Links

