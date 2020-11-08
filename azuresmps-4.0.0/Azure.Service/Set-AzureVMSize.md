---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005997"
---
# Set-AzureVMSize

## Synopsis
Legt die Größe eines Azure Virtual Machine fest.

## Syntax

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureVMSize** " aktualisiert die Größe eines virtuellen Computers.
Es hat zwei Parameter: *Instanzen* , also die neue Größe des virtuellen Computers, und *VM* , bei der es sich um ein virtuelles Computerobjekt handelt, das mit dem Cmdlet **Get-AzureVM** abgerufen wurde.
Das Ergebnis von **AzureVMSize** kann an das **Update-AzureVM-** Cmdlet weitergeleitet oder zur späteren Verwendung in einer Variablen gespeichert werden.
Eine tatsächliche Änderung wird erst vorgenommen, wenn **Update-AzureVM** ausgeführt wird.

Hinweis: für dieses Cmdlet muss die virtuelle Maschine erneut bereitgestellt werden, und es wird möglicherweise eine neue IP-Adresse abgerufen.

## Beispiele

### Beispiel 1: Bestimmen der Größe eines virtuellen Computers
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

Dieser Befehl aktualisiert einen virtuellen Computer, um die Größe "klein" zu ändern.

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

### -Instanzen
Gibt die Größe des virtuellen Computers an.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

--ExtraSmall--klein--mittel--groß--extra large--A5--A6--A7

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -VM
Gibt das Objekt des beständigen virtuellen Computers an, dessen Größe von diesem Cmdlet festgelegt wird.

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

[Get-AzureVM](./Get-AzureVM.md)

[Update-AzureVM](./Update-AzureVM.md)


