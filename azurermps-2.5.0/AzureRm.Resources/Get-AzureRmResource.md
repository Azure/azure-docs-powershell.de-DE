---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
ms.openlocfilehash: aa9a0c3a1e06c7ef4a66c58f3039bda19d4824ee
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849496"
---
# Get-AzureRmResource

## Synopsis

Ruft Ressourcen ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByTagNameValueParameterSet (Standard)
```
Get-AzureRmResource [[-Name] <String>] [-ResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-TagName <String>] [-TagValue <String>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceId
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTagObjectParameterSet
```
Get-AzureRmResource [[-Name] <String>] [-ResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung

Das Cmdlet " **Get-AzureRmResource** " ruft Azure-Ressourcen ab.

## Beispiele

### Beispiel 1: Abrufen aller Ressourcen im aktuellen Abonnement

```
PS C:\> Get-AzureRmResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

Dieser Befehl ruft alle Ressourcen im aktuellen Abonnement ab.

### Beispiel 2: Abrufen aller Ressourcen in einer Ressourcengruppe

```
PS C:\> Get-AzureRmResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

Dieser Befehl ruft alle Ressourcen in der Ressourcengruppe "testRG" ab.

### Beispiel 3: Abrufen aller Ressourcen, deren Ressourcengruppe mit dem bereitgestellten Platzhalter übereinstimmt

```
PS C:\> Get-AzureRmResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

Dieser Befehl ruft alle Ressourcen ab, deren Ressourcengruppe Sie zu Wesen gehören, mit "Other".

### Beispiel 4: Abrufen aller Ressourcen mit einem angegebenen Namen

```
PS C:\> Get-AzureRmResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

Dieser Befehl ruft alle Ressourcen ab, deren Ressourcenname "testVM" lautet.

### Beispiel 5: Abrufen aller Ressourcen, deren Name mit dem bereitgestellten Platzhalter übereinstimmt

```
PS C:\> Get-AzureRmResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

Dieser Befehl ruft alle Ressourcen ab, deren Ressourcenname mit "Test" beginnt.

### Beispiel 6: Abrufen aller Ressourcen eines angegebenen Ressourcentyps

```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

Dieser Befehl ruft alle Ressourcen in den aktuellen Abonnements ab, die virtuelle Maschinen sind.

### Beispiel 7: Abrufen einer Ressource nach Ressourcen-ID

```
PS C:\> Get-AzureRmResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

Dieser Befehl ruft die Ressource mit der bereitgestellten Ressourcen-ID ab, bei der es sich um einen virtuellen Computer mit dem Namen "testVM" in der Ressourcengruppe "testRG" handelt.

## Parameter

### -ApiVersion

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

### -ExpandProperties
Wenn angegeben, werden die Eigenschaften der Ressource erweitert.

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

### -Name
Der Name der Ressourcen, die abgerufen werden sollen. Dieser Parameter unterstützt Platzhalter am Anfang und/oder Ende der Zeichenfolge.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODataQuery

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre

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
Die Ressourcengruppe, in der die retireved-Ressourcen zugeordnet sind. Dieser Parameter unterstützt Platzhalter am Anfang und/oder Ende der Zeichenfolge.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Gibt die vollqualifizierte Ressourcen-ID an, wie im folgenden Beispiel gezeigt. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`

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

### -
Der Ressourcentyp der Ressourcen, die abgerufen werden sollen. Beispiel: Microsoft. Compute/virtualMachines

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag

Ruft Ressourcen ab, die das angegebene Azure-Tag aufweisen. Geben Sie eine Hashtabelle mit einem Namensschlüssel oder einem Namen-und Wert Schlüssel ein. Platzhalterzeichen werden nicht unterstützt. Ein "Tag" ist ein Name-Wert-Paar, das Sie auf Ressourcen und Ressourcengruppen anwenden können. Verwenden Sie Kategorien, um Ihre Ressourcen zu kategorisieren, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu überwachen. Verwenden Sie zum Hinzufügen einer Kategorie zu einer Ressource den Tag-Parameter der New-AzureRmResource-oder Set-AzureRmResource-Cmdlets. Verwenden Sie das New-AzureRmTag-Cmdlet, um eine vordefinierte Kategorie zu erstellen. Wenn Sie Hilfe zu Hashtabellen in Windows PowerShell benötigen, führen Sie "Get-Help about_Hashtables" aus.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tagname
Der Schlüssel im Tag der Ressourcen, die abgerufen werden sollen.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagValue
Der Wert im Tag der Ressourcen, die abgerufen werden sollen.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
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



[Verschieben-AzureRmResource](./Move-AzureRmResource.md)

[Neu – AzureRmResource](./New-AzureRmResource.md)

[Remove-AzureRmResource](./Remove-AzureRmResource.md)

[Satz-AzureRmResource](./Set-AzureRmResource.md)
