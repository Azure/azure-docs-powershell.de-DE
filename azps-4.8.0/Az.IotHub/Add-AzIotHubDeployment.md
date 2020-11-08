---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166676"
---
# Add-AzIotHubDeployment

## Synopsis
Fügen Sie eine viel Edge-Bereitstellung in einem Ziel-viel-Hub hinzu.

## Syntax

### ResourceSet (Standard)
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectSet
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdSet
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Edge-Bereitstellungen können mit benutzerdefinierten Metriken für die bedarfsgesteuerte Auswertung erstellt werden.
Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring .

## Beispiele

### Beispiel 1
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

Erstellen Sie eine Edge-Bereitstellung mit Standardmetadaten.

### Beispiel 2
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

Erstellen Sie eine Edge-Bereitstellung mit einer Priorität von 3, die unter Bedingung gilt, wenn ein Gerät in Gebäude 9 markiert ist und die Umgebung "testen" lautet.

### Beispiel 2
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

Erstellen Sie eine Edge-Bereitstellung mit Benutzer Metriken.

### Beispiel 3
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

Erstellen Sie eine Edge-Bereitstellung mit Beschriftungen.

### Beispiel 4
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

Erstellen Sie eine Edge-Bereitstellung mit Inhalten.

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

### -Inputobject
IotHub-Objekt

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IotHubName
Name des viel-Hubs

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Label
Karte der Beschriftungen, die auf die Ziel Bereitstellung angewendet werden sollen.

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

### -Metric
Querys-Sammlung für die Definition von "viel Edge Deployment Metrics".

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

### -ModulesContent
Bereitstellungs Inhalt von Modulen für viel Edge-Geräte.

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

### -Name
Bezeichner für die Bereitstellung.

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

### -Priorität
Das Gewicht der Bereitstellung bei konkurrierenden Regeln (höchste Gewinne).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
IotHub-Ressourcen-ID

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetCondition
Die zielbedingung, auf die eine Edge-Bereitstellung angewendet werden soll.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub

### System. String

## Ausgaben

### Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment

## Notizen

## Verwandte Links
