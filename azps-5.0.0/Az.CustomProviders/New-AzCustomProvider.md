---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298947"
---
# New-AzCustomProvider

## Synopsis
Erstellt oder aktualisiert den benutzerdefinierten Ressourcenanbieter.

## Syntax

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Erstellt oder aktualisiert den benutzerdefinierten Ressourcenanbieter.

## Beispiele

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

Erstellen Sie einen benutzerdefinierten Anbieter mit einer Route für benutzerdefinierte Anbieter Zuordnungen.

## Parameter

### – Aktion
Eine Liste der Aktionen, die der benutzerdefinierte Ressourcenanbieter implementiert.
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Aktionseigenschaften und Erstellen einer Hashtabelle.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Standort
Ressourcen Standort

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

### -Nowait
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

### -
Eine Liste der Ressourcentypen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Eigenschaften von "Eigenschaften" und Erstellen einer Hashtabelle.

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

### -Abonnement-Nr
Die Azure-Abonnement-ID.
Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)

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
Ressourcenkategorien

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

### -Validierung
Eine Liste der Validierungen, die für die Anforderungen des benutzerdefinierten Ressourcenanbieters ausgeführt werden sollen.
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Überprüfungseigenschaften und Erstellen einer Hashtabelle.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. Api20180901Preview. ICustomRpManifest

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Action <ICustomRpActionRouteDefinition [] >: eine Liste der Aktionen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.
  - `Endpoint <String>`: Der Endpunkt-URI für die Routendefinition, an den der benutzerdefinierte Ressourcenanbieter Proxyanforderungen stellt. Dies kann in Form eines flachen URIs erfolgen (z.b. ' https://testendpoint/ ') oder es kann angegeben werden, dass es über einen Pfad weitergeleitet werden soll (z.b. ' https://testendpoint/{requestPath} ').
  - `Name <String>`: Der Name der Routendefinition. Dies wird zum Namen für die Erweiterung des Arms (z.b. "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{Name}").
  - `[RoutingType <ActionRouting?>]`: Die Routing Typen, die für Aktionsanforderungen unterstützt werden.

Ressourcen <ICustomRpResourceTypeRouteDefinition [] >: eine Liste der Ressourcentypen, die vom benutzerdefinierten Ressourcenanbieter implementiert werden.
  - `Endpoint <String>`: Der Endpunkt-URI für die Routendefinition, an den der benutzerdefinierte Ressourcenanbieter Proxyanforderungen stellt. Dies kann in Form eines flachen URIs erfolgen (z.b. ' https://testendpoint/ ') oder es kann angegeben werden, dass es über einen Pfad weitergeleitet werden soll (z.b. ' https://testendpoint/{requestPath} ').
  - `Name <String>`: Der Name der Routendefinition. Dies wird zum Namen für die Erweiterung des Arms (z.b. "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{Name}").
  - `[RoutingType <ResourceTypeRouting?>]`: Die Routing Typen, die für Ressourcenanforderungen unterstützt werden.

Validation <ICustomRpValidations [] >: eine Liste der Validierungen, die für die Anforderungen des benutzerdefinierten Ressourcenanbieters ausgeführt werden sollen.
  - `Specification <String>`: Ein Link zur Gültigkeits Prüfungs Spezifikation. Die Spezifikation muss auf RAW.githubusercontent.com gehostet werden.
  - `[ValidationType <ValidationType?>]`: Die Art der Validierung, die für eine übereinstimmende Anforderung ausgeführt werden soll.

## Verwandte Links

