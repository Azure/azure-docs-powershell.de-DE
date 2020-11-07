---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: 57e4bd86ad3f5205749579e190960ea4f8e70588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662299"
---
# New-AzureRmResource

## Synopsis
Erstellt eine Ressource.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByResourceId (Standard)
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### BySubscriptionLevel
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTenantLevel
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmResource** erstellt eine Azure-Ressource, beispielsweise eine Website, einen Azure SQL-Datenbankserver oder eine Azure SQL-Datenbank, in einer Ressourcengruppe.

## Beispiele

### Beispiel 1: Erstellen einer Ressource
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.

### Beispiel 2: Erstellen einer Ressource mithilfe von splatting
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

Mit diesem Befehl wird eine Ressource erstellt, bei der es sich um eine Website in ResourceGroup11 handelt.

## Parameter

### -ApiVersion
Gibt die Version der zu verwendenden Ressourcenanbieter-API an. Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Ausführen eines Cmdlets im Hintergrund

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -ExtensionResourceName
Gibt den Namen einer Erweiterungs Ressource für die Ressource an. Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Servername- `/` Datenbankname

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionResourceType
Gibt den Ressourcentyp für eine Erweiterungs Ressource an.
Wenn es sich bei der Erweiterungs Ressource beispielsweise um eine Datenbank handelt, geben Sie den folgenden Typ an: `Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -Isfullobject
Gibt an, dass das Objekt, das der *Properties* -Parameter angibt, das vollständige Objekt ist.

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

### -Art
Gibt die Art der Ressource für die Ressource an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Gibt den Speicherort der Ressource an.
Geben Sie den Speicherort des Datencenters an, beispielsweise Zentralamerika oder Südostasien.
Sie können eine Ressource an einem beliebigen Speicherort platzieren, der Ressourcen dieses Typs unterstützt. Ressourcengruppen können Ressourcen aus unterschiedlichen Speicherorten enthalten. Verwenden Sie das Get-AzureLocation-Cmdlet, um zu ermitteln, welche Speicherorte die einzelnen Ressourcentypen unterstützen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODataQuery
Gibt einen Open Data Protocol (OData)-stilfilter an. Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plan
Eine Hashtabelle, die Ressourcenplan Eigenschaften darstellt.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.

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

### -Eigenschaften
Gibt Ressourceneigenschaften für die Ressource an. Verwenden Sie diesen Parameter, um die Werte von Eigenschaften anzugeben, die für einen Ressourcentyp spezifisch sind.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet die Ressource erstellt.

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Gibt den Namen der Ressource an. Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -
Gibt den Typ der Ressource an.
Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Eine Hashtabelle, die SKU-Eigenschaften darstellt.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantLevel
Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. ResourceManagement. Models. PSResource

## Notizen

## Verwandte Links

[Finden-AzureRmResource](./Find-AzureRmResource.md)

[Get-AzureRmResource](./Get-AzureRmResource.md)

[Verschieben-AzureRmResource](./Move-AzureRmResource.md)

[Remove-AzureRmResource](./Remove-AzureRmResource.md)

[Satz-AzureRmResource](./Set-AzureRmResource.md)
