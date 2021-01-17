---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458074"
---
# Get-AzDataLakeStoreTrustedIdProvider

## SYNOPSIS
Ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.
Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgeführt.

## SYNTAX

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzDataLakeStoreTrustedIdProvider"** ruft den angegebenen vertrauenswürdigen Identitätsanbieter im angegebenen Data Lake Store ab.
Wenn kein Anbieter angegeben ist, werden alle Anbieter für das Konto aufgeführt.

## BEISPIELE

### Beispiel 1: Einen bestimmten vertrauenswürdigen Identitätsanbieter erhalten
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

Gibt den Anbieter namens "MyProvider" aus dem Konto "ContosoADL" zurück.

### Beispiel 2: Auflisten aller Anbieter in einem Konto
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

Listet alle Anbieter unter dem Konto "ContosoADL" auf.

## PARAMETERS

### -Konto
Das Data Lake Store-Konto, von dem der vertrauenswürdige Identitätsanbieter abgerufen werden soll

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

### -Name
Der Name des vertrauenswürdigen Identitätsanbieters, der abgerufen werden soll

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
Name der Ressourcengruppe, unter der der angegebene vertrauenswürdige Identitätsanbieter des angegebenen Kontos abgerufen werden soll.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
