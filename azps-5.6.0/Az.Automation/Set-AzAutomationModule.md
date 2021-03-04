---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 475c4ab3105aa8ae01543c0f3674d5d119604a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947528"
---
# Set-AzAutomationModule

## SYNOPSIS
Aktualisiert ein Modul in der Automatisierung.

## SYNTAX

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzAutomationModule** aktualisiert ein Modul in Azure Automation.
Dieser Befehl akzeptiert eine komprimierte Datei mit einer ZIP-Dateinamenerweiterung.
Die Datei enthält einen Ordner, der eine Datei enthält, die einen der folgenden Typen enthält: 
- wps_2-Modul mit der Dateinamenerweiterung PSM1 oder DLL 
- wps_2-Modulmanifest mit der Dateinamenerweiterung PSD1 Der Name der ZIP-Datei, der Name des Ordners und der Name der Datei im Ordner müssen identisch sein.
Geben Sie die ZIP-Datei als URL an, auf die der Automatisierungsdienst zugreifen kann.
Wenn Sie ein wps_2-Modul mithilfe dieses Cmdlets oder des New-AzAutomationModule-Cmdlets in die Automatisierung importieren, ist der Vorgang asynchron.
Der Befehl endet, ob der Import erfolgreich ist oder fehlschlägt.
Um zu überprüfen, ob dies erfolgreich war, führen Sie den folgenden Befehl aus: ModuleName Überprüfen Sie die `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` **ProvisioningState-Eigenschaft** auf den Wert "Succeeded".

## BEISPIELE

### Beispiel 1: Aktualisieren eines Moduls
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

Mit diesem Befehl wird eine aktualisierte Version eines vorhandenen Moduls namens ContosoModule in das Automatisierungskonto namens Contoso17 importiert.  Das Modul wird in einem Azure-Blob in einem Speicherkonto namens contosostorage und einem Container namens Module gespeichert.

## PARAMETER

### -AutomationAccountName
Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet ein Modul aktualisiert.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkUri
Gibt die URL der ZIP-Datei an, die die neue Version eines Moduls enthält, das von diesem Cmdlet importiert wird.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
Gibt die Version des Moduls an, auf das dieses Cmdlet die Automatisierung aktualisiert.

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

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -Name
Gibt den Namen des Moduls an, das von diesem Cmdlet importiert wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Modul aktualisiert.

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

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### System.Uri

## AUSGABEN

### Microsoft.Azure.Commands.Automation.Model.Module

## NOTIZEN

## VERWANDTE LINKS

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[New-AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)


