---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 21e1af2a36478f2e0b8e470660d0fbe2539a396e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843428"
---
# Get-AzProviderOperation

## Synopsis
Ruft die Vorgänge für einen Azure-Ressourcenanbieter ab, die mithilfe von Azure RBAC Sicherungs fähig sind.

## Syntax

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Die Get-AzProviderOperation ruft die von Azure-Ressourcen Anbietern verfügbar gemachten Vorgänge ab.
Vorgänge können zum Erstellen benutzerdefinierter Rollen in Azure RBAC zusammengestellt werden.
Der Befehl nimmt als Eingabe eine Vorgangs Suchzeichenfolge (mit möglichen Platzhalter *Zeichen ()) an, die die anzuzeigenden Vorgangsdetails bestimmt. Verwenden Sie Get-AzProviderOperation *, um alle Vorgänge für alle Azure-Ressourcenanbieter abzurufen. Verwenden Sie Get-AzProviderOperation Microsoft. Compute/* , um alle Vorgänge des Microsoft. Compute-Ressourcenanbieters zu erhalten.

## Beispiele

### Abrufen aller Aktionen für alle Anbieter
```
PS C:\> Get-AzProviderOperation *
```

### Abrufen von Aktionen für einen bestimmten Ressourcenanbieter
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Abrufen aller Aktionen, die auf virtuellen Computern ausgeführt werden können
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
Die Suchzeichenfolge des Vorgangs (mit möglichen Platzhalterzeichen (*))

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String
Parameter: OperationSearchString (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation

## Notizen
Schlüsselwörter: Azure, AZ, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung

## Verwandte Links
