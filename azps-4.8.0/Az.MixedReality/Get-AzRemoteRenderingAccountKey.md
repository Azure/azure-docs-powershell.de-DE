---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010152"
---
# Get-AzRemoteRenderingAccountKey

## Synopsis
Abrufen von Schlüsseln des Remote Rendering-Kontos

## Syntax

### DefaultParameterSet (Standard)
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PipelineParameterSet
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Abrufen von Entwickler Schlüsseln des Remote Rendering-Kontos

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

Holen Sie sich die Entwickler Schlüssel des Remote Rendering-Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1".

### Beispiel 2
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

Holen Sie sich die Entwickler Schlüssel des Remote Rendering-Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1" mit Piping.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Das benutzerdefinierte Domänenobjekt.

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Name des Remote Rendering-Kontos

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Ressourcen-ID des Remote Rendering-Kontos.

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.
Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount

## Ausgaben

### Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys

## Notizen

## Verwandte Links
