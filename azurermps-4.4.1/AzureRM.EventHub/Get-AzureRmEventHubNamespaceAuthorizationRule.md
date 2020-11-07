---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665062"
---
# Get-AzureRmEventHubNamespaceAuthorizationRule

## Synopsis
Ruft die Details einer Eventubs-Namespace Autorisierungsregel ab oder ruft eine Liste mit Autorisierungsregeln ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## Beschreibung
Das Get-AzureRmEventHubNamespaceAuthorizationRule-Cmdlet ruft entweder die Details einer angegebenen Event Hubs-Namespace Autorisierungsregel oder eine Liste mit Namespace Autorisierungsregeln ab.
Wenn der Name der Autorisierungsregel angegeben ist, werden die Details einer einzelnen Autorisierungsregel zurückgegeben.
Wenn kein Autorisierungsregel Name angegeben wird, wird eine Liste aller Autorisierungsregeln im Namespace zurückgegeben.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

Gibt die Autorisierungsregel \` MyAuthRuleName \` im Namespace \` mynamespacename des Ereignis Hubs \` mit der Ressourcengruppe \` MyResourceGroupName zurück \` .

### Beispiel 2
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

Gibt die standardmäßige Autorisierungsregel \` RootManageSharedAccessKey \` im Namespace \` mynamespacename des Ereignis Hubs \` mit der Ressourcengruppe \` MyResourceGroupName zurück \` .

### Beispiel 3
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

Gibt alle Autorisierungsregeln im Event Hubs \` -Namespace mynamespacename \` mit der Ressourcengruppe \` MyResourceGroupName zurück \` .

## Parameter

### -Authorizationrulename
Der Name der Namespace Autorisierungsregel für Ereignis Hubs

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespacename
Der Namespacename des Event Hubs.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## Eingaben

### System. String

## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]

## Notizen

## Verwandte Links

