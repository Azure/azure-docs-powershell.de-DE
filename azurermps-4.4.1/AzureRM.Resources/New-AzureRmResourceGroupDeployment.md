---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 9512a8ae8e6bbd54704212539ad0650797cf4604
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500742"
---
# New-AzureRmResourceGroupDeployment

## Synopsis
Fügt eine Azure-Bereitstellung zu einer Ressourcengruppe hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Bereitstellung über Vorlagendatei ohne Parameter (Standard)
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Bereitstellung über Vorlagendatei-und Vorlagenparameter Objekt
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Bereitstellung über Vorlagen-URI und Vorlagenparameter-Objekt
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Bereitstellung über Vorlagendatei-und Vorlagenparameter Datei
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Bereitstellung über Vorlagen-URI und Vorlagenparameter-Datei
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Bereitstellung über Vorlagen-Datei Vorlagenparameter-URI
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Bereitstellung über Vorlagen-URI und Vorlagenparameter-URI
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Bereitstellung über Vorlagen-URI ohne Parameter
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureRmResourceGroupDeployment** wird eine Bereitstellung zu einer vorhandenen Ressourcengruppe hinzugefügt.
Dazu gehören die Ressourcen, die für die Bereitstellung erforderlich sind.

Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank, eine Website, einen virtuellen Computer oder ein Speicherkonto.
Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden, beispielsweise die Website, den Datenbankserver und Datenbanken, die für eine Finanzwebsite erforderlich sind.
Eine Ressourcengruppen Bereitstellung verwendet eine Vorlage zum Hinzufügen von Ressourcen zu einer Ressourcengruppe und veröffentlicht diese, damit Sie in Azure verfügbar sind.
Verwenden Sie das New-AzureRmResource-Cmdlet, um einer Ressourcengruppe Ressourcen hinzuzufügen, ohne eine Vorlage zu verwenden.

Wenn Sie eine Ressourcengruppen Bereitstellung hinzufügen möchten, geben Sie den Namen einer vorhandenen Ressourcengruppe und einer Ressourcengruppen Vorlage an.
Eine Ressourcengruppen Vorlage ist eine JSON-Zeichenfolge, die eine Ressourcengruppe für einen komplexen cloudbasierten Dienst, beispielsweise ein Webportal, darstellt.
Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte wie Namen und Größen.
Sie können viele Vorlagen im Azure-Vorlagenkatalog finden, oder Sie können eigene Vorlagen erstellen.
Sie können das Cmdlet **Get-AzureRmResourceGroupGalleryTemplate** verwenden, um eine Vorlage im Katalog zu finden.

Wenn Sie eine benutzerdefinierte Vorlage zum Erstellen einer Ressourcengruppe verwenden möchten, geben Sie den Parameter " *Templatedatei* " oder " *TemplateUri* " an.
Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.
Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *TemplateParameterFile* -Parameter oder den *TemplateParameterObject* -Parameter an.
Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.
Wenn Sie dynamische Parameter verwenden möchten, geben Sie Sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.
Vorlagenparameter Werte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameter Objekt oder einer Datei.

## Beispiele

### Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und einer Parameterdatei zum Erstellen einer Bereitstellung
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

Dieser Befehl erstellt eine neue Bereitstellung mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger.
Der Befehl verwendet den *Templatedatei* -Parameter, um die Vorlage und den *TemplateParameterFile* -Parameter anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.
Die Version der Vorlage wird mithilfe des *TemplateVersion* -Parameters angegeben.

## Parameter

### -ApiVersion
Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.
Sie können eine andere Version als die Standard Version angeben.

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

### -DeploymentDebugLogLevel
Gibt eine Debug-Protokollebene an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- RequestContent 
- ResponseContent 
- Alle 
- Keine

```yaml
Type: System.String
Parameter Sets: (All)
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

### -Modus
Gibt den Bereitstellungsmodus an. Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Komplette 
- Inkrementelle

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der zu erstellende Ressourcengruppen Bereitstellung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die bereitgestellt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vorlagendatei
Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.
Hierbei kann es sich um eine benutzerdefinierte Vorlage oder eine Katalogvorlage handeln, die als JSON-Datei gespeichert wird, beispielsweise eine mit dem Cmdlet **Save-AzureRmResourceGroupGalleryTemplate** erstellte.

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterFile
Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.
Wenn eine Vorlage über Parameter verfügt, müssen Sie die Parameterwerte mit dem *TemplateParameterFile* -Parameter oder dem *TemplateParameterObject* -Parameter angeben.
Vorlagenparameter werden dem Befehl dynamisch hinzugefügt, wenn Sie eine Vorlage angeben.

Wenn Sie die dynamischen Parameter verwenden möchten, geben Sie ein Minuszeichen (-) ein, um einen Parameternamen anzugeben, und verwenden Sie dann die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterObject
Gibt eine Hashtabelle mit Vorlagenparameter Namen und-Werten an.
Wenn Sie Hilfe zu Hashtabellen in Windows PowerShell benötigen, geben Sie `Get-Help about_Hash_Tables` .
Wenn eine Vorlage über Parameter verfügt, müssen Sie Parameterwerte angeben.
Vorlagenparameter werden dem Befehl dynamisch hinzugefügt, wenn Sie eine Vorlage angeben.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateParameterUri
Gibt den URI einer Vorlagenparameter Datei an.

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TemplateUri
Gibt den URI einer JSON-Vorlagendatei an.
Diese Datei kann eine benutzerdefinierte Vorlage oder eine Katalogvorlage sein, die als JSON-Datei gespeichert wird, beispielsweise mithilfe von **Save-AzureRmResourceGroupGalleryTemplate**.

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. ResourceManager. Models. PSResourceGroupDeployment

## Notizen

## Verwandte Links

[Get-AzureRmResourceGroupDeployment](./Get-AzureRmResourceGroupDeployment.md)

[Neu – AzureRmResource](./New-AzureRmResource.md)

[Neu – AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[Stopp-AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


