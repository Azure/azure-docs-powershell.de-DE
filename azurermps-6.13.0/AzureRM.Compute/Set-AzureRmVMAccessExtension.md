---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0a2d3ce354a5039db21fdd336f6f2d64efdb56fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504453"
---
# Set-AzureRmVMAccessExtension

## Synopsis
Fügt die VMAccess-Erweiterung zu einem virtuellen Computer hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **AzureRmVMAccessExtension** " wird der Virtual Machine Access-VMAccess-VMAccess-Erweiterung zu einem virtuellen Computer hinzugefügt. VMAccess Extension kann verwendet werden, um ein temporäres Kennwort festzulegen, das nach der Anmeldung am Computer sofort geändert werden sollte. Auf Windows-Domänencontrollern wird dies nicht unterstützt.

## Beispiele

### Beispiel 1: Hinzufügen einer VMAccess-Erweiterung
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

Mit diesem Befehl wird eine VMAccess-Erweiterung für den virtuellen Computer mit dem Namen VirtualMachine07 in ResrouceGroup11 hinzugefügt.
Der Befehl gibt die Version für Name und Typ des Handlers für VMAccess an.

## Parameter

### – Anmeldeinformationen
Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential** -Objekt an.
Wenn Sie einen anderen Namen als das aktuelle lokale Administratorkonto auf dem virtuellen Computer eingeben, fügt die VMAccess-Erweiterung ein lokales Administratorkonto mit diesem Namen hinzu und weist diesem Konto das angegebene Kennwort zu. Wenn das lokale Administratorkonto auf dem virtuellen Computer vorhanden ist, wird das Kennwort zurückgesetzt, und wenn das Konto deaktiviert ist, wird es durch die VMAccess-Erweiterung aktiviert.
Verwenden Sie zum Abrufen von Anmeldeinformationen das Get-Credential-Cmdlet.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DisableAutoUpgradeMinorVersion
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceRerun
Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.
Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.
Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.

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

### -Standort
Gibt den Speicherort der virtuellen Maschine an.

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

### -Name
Gibt den Namen der Erweiterung an, die von diesem Cmdlet hinzugefügt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des virtuellen Computers an.

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

### -TypeHandlerVersion
Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.
Führen Sie zum Abrufen der Version das Get-AzureRmVMExtensionImage-Cmdlet mit dem Wert Microsoft. Compute für den *PublisherName* -Parameter und VMAccessAgent für den *Type* -Parameter aus. Die typeHandlerVersion muss 2,0 oder größer sein, da Version 1 veraltet ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Gibt den Namen einer virtuellen Maschine an.
Dieses Cmdlet fügt dem virtuellen Computer, den dieser Parameter angibt, VMAccess hinzu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. Management. Automation. PSCredential

### System. String

### System. Management. Automation. Switchparameter

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse

## Notizen

## Verwandte Links

[Get-AzureRmVMAccessExtension](./Get-AzureRmVMAccessExtension.md)

[Remove-AzureRmVMAccessExtension](./Remove-AzureRmVMAccessExtension.md)

[Satz-AzureRmVMExtension](./Set-AzureRmVMExtension.md)

[Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md)


