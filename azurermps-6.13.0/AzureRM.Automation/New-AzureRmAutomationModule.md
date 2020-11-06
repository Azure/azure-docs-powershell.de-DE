---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 0ddfbd8aceeb26a4f40fcf104919fa9b67b39aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476273"
---
# New-AzureRmAutomationModule

## Synopsis
Importiert ein Modul in die Automatisierung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureRmAutomationModule** wird ein Modul in die Azure-Automatisierung importiert.
Dieser Befehl akzeptiert eine komprimierte Datei, die eine ZIP-Dateinamenerweiterung aufweist.
Die Datei enthält einen Ordner, der eine Datei mit einem der folgenden Typen enthält: 
- wps_2 Modul mit der Dateinamenerweiterung psm1 oder dll 
- wps_2 Modul Manifest mit einer psd1-Dateinamenerweiterung der Name der ZIP-Datei, der Name des Ordners und der Name der Datei im Ordner müssen identisch sein.
Geben Sie die ZIP-Datei als URL an, auf die der Automatisierungs Dienst zugreifen kann.
Wenn Sie ein wps_2 Modul mithilfe dieses Cmdlets oder des Set-AzureRmAutomationModule-Cmdlets in die Automatisierung importieren, ist der Vorgang asynchron.
Der Befehl beendet, ob der Import erfolgreich ist oder fehlschlägt.
Führen Sie den folgenden Befehl aus, um zu überprüfen, ob er erfolgreich war: `PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name ` Modulname überprüfen Sie die **ProvisioningState** -Eigenschaft auf den Wert erfolgreich.

## Beispiele

### Beispiel 1: Importieren eines Moduls
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

Dieser Befehl importiert ein Modul mit dem Namen ContosoModule in das Automatisierungs Konto mit dem Namen Contoso17.
Das Modul wird in einem Azure-BLOB in einem Speicherkonto mit dem Namen contosostorage und einem Container mit dem Namen Module gespeichert.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Modul importiert.

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
Die URL zu einem Modul-ZIP-Paket

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name
Gibt den Namen des Moduls an, das dieses Cmdlet importiert.

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
Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Modul importiert.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. Uri

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. Module

## Notizen

## Verwandte Links

[Get-AzureRmAutomationModule](./Get-AzureRmAutomationModule.md)

[Remove-AzureRmAutomationModule](./Remove-AzureRmAutomationModule.md)

[Satz-AzureRmAutomationModule](./Set-AzureRmAutomationModule.md)


