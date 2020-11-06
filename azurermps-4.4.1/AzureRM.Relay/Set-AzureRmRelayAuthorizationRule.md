---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 64c839140907b10d62b4f71025afab985d5ba736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500777"
---
# Set-AzureRmRelayAuthorizationRule

## Synopsis
Aktualisiert die angegebene Autorisierungsregel Beschreibung für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### NamespaceAuthorizationRuleSet (Standard)
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### WcfRelayAuthorizationRuleSet
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HybridConnectionAuthorizationRuleSet
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-InputObject <AuthorizationRuleAttributes>]
 [-Rights <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AuthoRuleInputObjectSet
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 -InputObject <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AuthoRulePropertiesSet
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> -Rights <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmRelayAuthorizationRule** " aktualisiert die Beschreibung für die angegebene Autorisierungsregel der angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).

## Beispiele

### Example 1,1-Namespace mit Inputobject
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

Fügt **Send** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in Namespace hinzu `TestNameSpace-Relay1` .

### Beispiel für 1,2-Namespace mit rights-Parameter
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

Fügt **Send** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in Namespace hinzu `TestNameSpace-Relay1` .

### Beispiel 2,1-WcfRelay mit Inputobject
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des WcfRelay `TestWCFRelay1` .

### Beispiel 2,2-WcfRelay mit rights-Parameter
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des WcfRelay `TestWCFRelay1` .

### Beispiel 3,1-HybridConnection mit Inputobject
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des HybridConnection `TestHybridConnection` .

### Beispiel 3,2-HybridConnection mit rights-Parameter
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des HybridConnection `TestHybridConnection` .

## Parameter

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HybridConnection
HybridConnection-Name.

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
AuthorizationRule-Name.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Namespace Name.

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rechte
Rechte, z.b. @ ("Abhören"; "Senden"; "verwalten")

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WcfRelay
WcfRelay-Name.

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Inputobject
{{Fill Inputobject Description}}

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### -ResourceGroupName
 System. String 

### -Namespace
 System. String 
 

### -WcfRelay
 System. String 

### -HybridConnection
 System. String 
 

### -Name
 System. String

### -Inputobject
 Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes
 

### -Rechte
 System. String []

## Ausgaben

### Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes

### Beispiel 1 – Namespace
Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1

### Beispiel 2: WcfRelay
Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1

### Beispiel 3: HybridConnection
Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1

## Notizen

## Verwandte Links

