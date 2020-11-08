---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: a9e9f5fdc71250acb2496c8eaaf1677461e9cd07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003080"
---
# Remove-AzDataShare

## Synopsis
Entfernt eine Datenfreigabe.

## Syntax

### ByFieldsParameterSet (Standard)
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Remove-AzDataShare** " entfernt eine Datenfreigabe.

## Beispiele

### Beispiel 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Dieser Befehl entfernt die Datenfreigabe mit dem Namen AdsShare aus dem Azure Data Share-Konto WikiAds. 

## Parameter

### -Kontoname
Name des Azure-Datenfreigabe Kontos

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
{{Fill AsJob Description}}

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
Azure Data Share-Objekt ' ' ' YAML-Typ: PSDataShare-Parameter Sätze: ByObjectParameterSet-Aliase: 

Erforderlich: true-Position: benannter Standardwert: keine Pipelineeingabe akzeptieren: wahr (ByValue) akzeptiert Platzhalterzeichen: falsch


### -Name
Name der Azure-Datenfreigabe

YAML Type: String-Parameter Sätze: ByFieldsParameterSet-Aliase: 

Erforderlich: true-Position: benannter Standardwert: None akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch


### -PassThru
Objekt zurückgeben (sofern angegeben).

YAML-Typ: Switchparameter-Parameter Sätze: (alle) Aliase: 

Erforderlich: falsche Position: benannter Standardwert: keiner akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch


### -ResourceGroupName
Der Name der Ressourcengruppe des Azure Data Share-Kontos

YAML Type: String-Parameter Sätze: ByFieldsParameterSet-Aliase: 

Erforderlich: true-Position: benannter Standardwert: None akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch


### -Resourcen-Nr
Die Ressourcen-ID der Azure-Datenfreigabe

YAML Type: String-Parameter Sätze: ByResourceIdParameterSet-Aliase: 

Erforderlich: true-Position: benannter Standardwert: keine Pipelineeingabe akzeptieren: wahr (ByPropertyName) akzeptiert Platzhalterzeichen: falsch


### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

YAML Type: Switchparameter-Parameter Sätze: (alle) Aliase: CF

Erforderlich: falsche Position: benannter Standardwert: keiner akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch


### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

YAML Type: Switchparameter-Parameter Sätze: (alle) Aliase: Wi

Erforderlich: falsche Position: benannter Standardwert: keiner akzeptiert Pipelineeingabe: false akzeptieren Platzhalterzeichen: falsch
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Name der Azure-Datenfreigabe

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Objekt zurückgeben (sofern angegeben).

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
Der Name der Ressourcengruppe des Azure Data Share-Kontos

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Die Ressourcen-ID der Azure-Datenfreigabe

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### System. String

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links
