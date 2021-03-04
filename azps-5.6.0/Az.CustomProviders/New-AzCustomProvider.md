---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: a3180cd693ae4c234656ba5d0812900ce8c308b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942664"
---
# New-AzCustomProvider

## SYNOPSIS
Erstellt oder aktualisiert den benutzerdefinierten Ressourcenanbieter.

## SYNTAX

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Erstellt oder aktualisiert den benutzerdefinierten Ressourcenanbieter.

## BEISPIELE

### Beispiel 1: Erstellen eines benutzerdefinierten Anbieters
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

Erstellen eines benutzerdefinierten Ressourcenanbieters

### Beispiel 2: Erstellen eines benutzerdefinierten Anbieters mit Zuordnungen
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

Erstellen Sie einen benutzerdefinierten Anbieter mit einer Route für benutzerdefinierte Anbieterzuordnungen.

## PARAMETER

### -Aktion
Eine Liste der Aktionen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu ACTION-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Ausführen des Befehls als Auftrag

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Ressourcenspeicherort

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name des Ressourcenanbieters.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Asynchrones Ausführen des Befehls

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Eine Liste der Ressourcentypen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für RESSOURCENTYP-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Die Azure-Abonnement-ID.
Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Ressourcentags

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Überprüfung
Eine Liste der Überprüfungen, die für die Anforderungen des benutzerdefinierten Ressourcenanbieters ausgeführt werden.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für GÜLTIGKEITSPRÜFUNGseigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


ACTION <ICustomRpActionRouteDefinition[]>: Eine Liste der Aktionen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.
  - `Endpoint <String>`: Der Routendefinitionsendpunkt-URI, an den vom benutzerdefinierten Ressourcenanbieter Proxyanforderungen gesendet werden. Dies kann in Form eines flachen URI (z. B. ' ') oder als Route über einen Pfad https://testendpoint/ angegeben werden (z. B. ' https://testendpoint/{requestPath} ')
  - `Name <String>`: Der Name der Routendefinition. Dies wird der Name der ARM-Erweiterung (z. B. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')
  - `[RoutingType <ActionRouting?>]`: Die Routingtypen, die für Aktionsanforderungen unterstützt werden.

RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: Eine Liste der Ressourcentypen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.
  - `Endpoint <String>`: Der Routendefinitionsendpunkt-URI, an den vom benutzerdefinierten Ressourcenanbieter Proxyanforderungen gesendet werden. Dies kann in Form eines flachen URI (z. B. ' ') oder als Route über einen Pfad https://testendpoint/ angegeben werden (z. B. ' https://testendpoint/{requestPath} ')
  - `Name <String>`: Der Name der Routendefinition. Dies wird der Name der ARM-Erweiterung (z. B. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')
  - `[RoutingType <ResourceTypeRouting?>]`: Die Routingtypen, die für Ressourcenanforderungen unterstützt werden.

VALIDATION <ICustomRpValidations[]>: Eine Liste der Überprüfungen, die für die Anforderungen des benutzerdefinierten Ressourcenanbieters ausgeführt werden müssen.
  - `Specification <String>`: Ein Link zur Gültigkeitsprüfungsspezifikation. Die Spezifikation muss auf einer raw.githubusercontent.com.
  - `[ValidationType <ValidationType?>]`: Der Typ der Überprüfung, die für eine übereinstimmende Anforderung ausgeführt werden soll.

## VERWANDTE LINKS

