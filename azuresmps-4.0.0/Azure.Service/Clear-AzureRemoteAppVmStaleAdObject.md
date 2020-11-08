---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005909"
---
# Clear-AzureRemoteAppVmStaleAdObject

## Synopsis
Entfernt Objekte in Azure Active Directory, die Azure RemoteApp-virtuellen Computern zugeordnet sind, die nicht mehr vorhanden sind.

## Syntax

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Clear-AzureRemoteAppVmStaleAdObject** " werden Objekte in Azure Active Directory entfernt, die Azure RemoteApp-virtuellen Computern zugeordnet sind, die nicht mehr vorhanden sind.
Sie müssen Anmeldeinformationen verwenden, die Rechte zum Entfernen von Azure Active Directory-Objekten aufweisen.
Wenn Sie den allgemeinen Parameter *verbose* angeben, zeigt dieses Cmdlet den Namen jedes gelöschten Objekts an.

## Beispiele

### Beispiel 1: Löschen veralteter Objekte für eine Sammlung
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

Der erste Befehl fordert Sie auf, einen Benutzernamen und ein Kennwort einzugeben, indem Sie **Get-Credential** verwenden.
Der Befehl speichert die Ergebnisse in der $AdminCredentials-Variablen.

Mit dem zweiten Befehl werden die veralteten Objekte für die Sammlung mit dem Namen "Contoso" gelöscht.
Der Befehl verwendet die in $AdminCredentials Variablen gespeicherten Anmeldeinformationen.
Damit der Befehl erfolgreich ausgeführt werden kann, müssen diese Anmeldeinformationen über die entsprechenden Berechtigungen verfügen.

## Parameter

### -CollectionName
Gibt den Namen der Azure RemoteApp-Sammlung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Anmeldeinformationen
Gibt eine Anmeldeinformation an, die Rechte zum Ausführen dieser Aktion aufweist.
Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.
Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet die aktuellen Anmeldeinformationen des Benutzers.

```yaml
Type: PSCredential
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

[Get-AzureRemoteAppVmStaleAdObject](./Get-AzureRemoteAppVmStaleAdObject.md)


