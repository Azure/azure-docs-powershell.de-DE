---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007606"
---
# New-WAPackQuickVM

## Synopsis
Erstellt einen virtuellen Computer basierend auf einer Vorlage.

## Syntax

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Themen sind veraltet und werden in Zukunft entfernt.
In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .

Das Cmdlet **New-WAPackQuickVM** erstellt einen virtuellen Computer basierend auf einer Vorlage.

## Beispiele

### Beispiel 1: Erstellen eines virtuellen Computers auf Grundlage einer Vorlage
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

Der erste Befehl erstellt ein **PSCredential** -Objekt und speichert es dann in der $Credentials-Variablen.
Das Cmdlet fordert Sie zur Eingabe eines Kontos und eines Kennworts auf.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .

Der zweite Befehl ruft eine Vorlage mit dem Cmdlet **Get-WAPackVMTemplate** ab.
Der Befehl gibt die ID einer Vorlage an.
Der Befehl speichert das Vorlagenobjekt in der $TemplateID Variablen.

Der endgültige Befehl erstellt einen virtuellen Computer mit dem Namen VirtualMachine023.
Der Befehl basiert auf dem virtuellen Computer auf der Vorlage, die in $TemplateId gespeichert ist.

## Parameter

### -Name
Gibt einen Namen für den virtuellen Computer an.

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

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

### -Vorlage
Gibt eine Vorlage an.
Das Cmdlet erstellt einen virtuellen Computer basierend auf der von Ihnen angegebenen Vorlage.
Verwenden Sie zum Abrufen eines Vorlagenobjekts das Cmdlet **Get-WAPackVMTemplate** .

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Gibt die Anmeldeinformationen für das lokale Administrator Konto an.
Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Neu – WAPackVM](./New-WAPackVM.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)


