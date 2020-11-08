---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003946"
---
# Get-AzServiceBusNetworkRuleSet

## Synopsis
Ruft die Details eines Ereignis Hubs NetworkruleSet des Namespaces im aktuellen Azure-Abonnement ab.

## Syntax

### NetworkRuleSetPropertiesSet (Standard)
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NetworkRuleSetNamespacePropertiesSet
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NetworkRuleSetResourceIdParameterSet
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Ruft die Details eines Ereignis Hubs NetworkruleSet des Namespaces im aktuellen Azure-Abonnement ab.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
Name: standardmäßige Standard-/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.ServiceBus/Namespaces/ServiceBus-Namespace-1122/networkRuleSets/default: Allow ID: Typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/v-ajnavtest/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; falsch}

Abrufen der Details von Ereignis Hubs NetworkruleSet des Namespaces mithilfe von ResourceGroup-und Namespace-Parametern 

### Beispiel 2
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
Name: standardmäßige Standard-/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.ServiceBus/Namespaces/ServiceBus-Namespace-1122/networkRuleSets/default: Allow ID: Typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/v-ajnavtest/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; falsch}

Rufen Sie die Details der Ereignis Hubs NetworkruleSet des Namespaces mit Namespace ab, der im aktuellen Abonnement enthalten ist.

### Beispiel 3
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

Name: standardmäßige Standard-/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.ServiceBus/Namespaces/ServiceBus-Namespace-2389/networkRuleSets/default: Allow ID: Typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/v-ajnavtest/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; falsch}

Abrufen der Details von Ereignis Hubs NetworkruleSet des Namespaces mithilfe der Ressourcen-ID eines anderen Namespaces 

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Namespace
Namespace Name

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Ressourcengruppen Name

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Namespace-Ressourcen-ID

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.
Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes

## Notizen

## Verwandte Links