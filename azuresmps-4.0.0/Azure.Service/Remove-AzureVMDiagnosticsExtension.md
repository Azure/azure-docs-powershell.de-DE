---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005710"
---
# Remove-AzureVMDiagnosticsExtension

## Synopsis
Entfernt die Azure Diagnostics-Erweiterung von einem virtuellen Computer.

## Syntax

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureVMDiagnosticsExtension** entfernt eine Microsoft Azure Diagnostics-Erweiterung von einem virtuellen Computer.
Sie müssen die Ausgabe dieses Cmdlets an das Cmdlet **Update-AzureVM** übergeben.

## Beispiele

### Beispiel 1: Entfernen der Azure Diagnostics-Erweiterung von einem virtuellen Computer
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

Mit diesem Befehl wird die Azure Diagnostics-Erweiterung von einem virtuellen Computer entfernt.

## Parameter

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -VM
Gibt das Objekt des beständigen virtuellen Computers an.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureVMDiagnosticsExtension](./Get-AzureVMDiagnosticsExtension.md)

[Satz-AzureVMDiagnosticsExtension](./Set-AzureVMDiagnosticsExtension.md)

[Update-AzureVM](./Update-AzureVM.md)


