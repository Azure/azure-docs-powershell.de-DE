---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006076"
---
# Remove-AzureAccount

## Synopsis
Löscht ein Azure-Konto aus Windows PowerShell.

## Syntax

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureAccount** löscht ein Azure-Konto und seine Abonnements aus der Abonnement Datendatei in Ihrem Roaming-Benutzerprofil.
Dadurch wird das Konto nicht aus Microsoft Azure gelöscht oder das tatsächliche Konto in irgendeiner Weise geändert.

Die Verwendung dieses Cmdlets ähnelt viel dem Abmelden von Ihrem Azure-Konto.
Wenn Sie sich erneut bei dem Konto anmelden möchten, verwenden Sie das **Add-AzureAccount** oder **Import-AzurePublishSettingsFile** , um das Konto erneut zu Windows PowerShell hinzuzufügen.

Sie können auch das Cmdlet **Remove-AzureAccount** verwenden, um die Art und Weise zu ändern, wie sich die Azure PowerShell-Cmdlets bei Ihrem Azure-Konto anmelden.
Wenn Ihr Konto über ein Verwaltungszertifikat von **Import-AzurePublishSettingsFile** und ein Zugriffstoken von **Add-AzureAccount** verfügt, verwenden die Azure PowerShell-Cmdlets nur das Zugriffstoken; Das Verwaltungszertifikat wird ignoriert.
Wenn Sie das Verwaltungszertifikat verwenden möchten, führen **Sie Remove-AzureAccount** aus.
Wenn **Remove-AzureAccount** sowohl ein Verwaltungszertifikat als auch ein Zugriffstoken findet, wird nur das Zugriffstoken gelöscht, anstatt das Konto zu löschen.
Da das Verwaltungszertifikat weiterhin vorhanden ist, steht das Konto weiterhin für Windows PowerShell zur Verfügung.

In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

## Beispiele

### Beispiel 1: Entfernen eines Kontos
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

Mit diesem Befehl wird die admin@contoso.com aus der Abonnement Datendatei entfernte Datei entfernt.
Nach Abschluss des Befehls steht das Konto nicht mehr für Windows PowerShell zur Verfügung.

## Parameter

### -Force
Unterdrückt die Bestätigungsaufforderung.
Standardmäßig werden Sie von **Remove-AzureAccount** aufgefordert, bevor Sie das Konto aus Windows PowerShell entfernen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des zu entfernenden Kontos an.
Bei dem Parameterwert wird die Groß-/Kleinschreibung beachtet.
Platzhalterzeichen werden nicht unterstützt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt $true zurück, wenn der Befehl erfolgreich ist, und $false, wenn ein Fehler auftritt.
Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
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
Type: SwitchParameter
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
Type: SwitchParameter
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
Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.

## Ausgaben

### None oder System. Boolean
Wenn Sie den Parameter *passthru* verwenden, gibt dieses Cmdlet einen booleschen Wert zurück.
Andernfalls gibt Sie keine Ausgabe zurück.

## Notizen

## Verwandte Links

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureAccount](./Get-AzureAccount.md)


