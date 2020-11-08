---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007617"
---
# Remove-WAPackVMRole

## Synopsis
Entfernt Rollen Objekte der virtuellen Maschine.

## Syntax

### FromVMRoleObject (Standard)
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FromCloudService
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Diese Themen sind veraltet und werden in Zukunft entfernt.
In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .

Das Cmdlet **Remove-WAPackVMRole** entfernt Rollen Objekte virtueller Computer.

## Beispiele

### Beispiel 1: Entfernen einer Rolle des virtuellen Computers (die mithilfe des WAP-Portals erstellt wurde)
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

Der erste Befehl ruft die Rolle des virtuellen Computers mit dem Namen ContosoVMRole01 mit dem Cmdlet **Get-WAPackVMRole** ab und speichert dieses Objekt dann in der $VMRole Variablen.

Der zweite Befehl entfernt die Rolle des virtuellen Computers, die in $VMRole gespeichert ist.
Der Befehl fordert Sie zur Bestätigung auf. Vorausgesetzt, dass diese Rolle des virtuellen Computers mithilfe des WAP-Portals erstellt wurde, müssen Sie den Namen des Cloud-Diensts nicht angeben.

### Beispiel 2: Entfernen einer Rolle des virtuellen Computers, die nach dem manuellen Erstellen eines Cloud-Diensts erstellt wurde
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

Der erste Befehl ruft mit dem Cmdlet **Get-WAPackVMRole** die Rolle des virtuellen Computers mit dem Namen "ContosoVMRole02" ab und speichert dieses Objekt dann in der $VMRole Variablen.

Der zweite Befehl entfernt die Rolle des virtuellen Computers, die in $VMRole gespeichert ist.
Der Befehl fordert Sie zur Bestätigung auf.
Vorausgesetzt, dass diese Rolle des virtuellen Computers nicht mithilfe des Portals erstellt wurde, muss der Benutzer den Namen des Cloud-Diensts angeben.
In diesem Fall mit dem Namen "ContosoCloudService02".

### Beispiel 3: Entfernen einer Rolle eines virtuellen Computers ohne Bestätigung
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

Der erste Befehl ruft den clouddienst mit dem Namen ContosoVMRole03 mit dem Cmdlet **Get-WAPackVMRole** ab und speichert dieses Objekt dann in der $VMRole Variablen.

Der zweite Befehl entfernt die Rolle des virtuellen Computers, die in $VMRole gespeichert ist.
Dieser Befehl enthält den Parameter *Force* .
Der Befehl fordert Sie nicht zur Bestätigung auf.

## Parameter

### -CloudServiceName
Gibt den Namen des Cloud-Diensts der Rolle des virtuellen Computers an.

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -PassThru
Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.
Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

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

### -VMRole
Gibt eine Rolle für einen virtuellen Computer an.
Zum Abrufen einer Rolle für einen virtuellen Computer verwenden Sie das Cmdlet **Get-WAPackVMRole** .

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

## Ausgaben

## Notizen

## Verwandte Links

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[Neu – WAPackVMRole](./New-WAPackVMRole.md)

[Satz-WAPackVMRole](./Set-WAPackVMRole.md)


