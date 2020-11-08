---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006683"
---
# Remove-AzureEnvironment

## Synopsis
Löscht eine Azure-Umgebung aus Windows PowerShell.

## Syntax

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureEnvironment** löscht eine Azure-Umgebung aus Ihrem Roaming-Profil, damit Sie von Windows PowerShell nicht gefunden werden kann.
Mit diesem Cmdlet wird die Umgebung nicht aus Microsoft Azure gelöscht, oder die tatsächliche Umgebung wird in keiner Weise geändert.

Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.
Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.
Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

## Beispiele

### Beispiel 1: Löschen einer Umgebung
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

Dieser Befehl löscht die ContosoEnv-Umgebung aus Windows PowerShell.

### Beispiel 2: Löschen mehrerer Umgebungen
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

Dieser Befehl löscht Umgebungen, deren Namen mit "Contoso" von Windows PowerShell beginnen.

## Parameter

### -Force
Unterdrückt die Bestätigungsaufforderung.

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
Gibt den Namen der zu entfernenden Umgebung an.
Dieser Parameter ist erforderlich.
Bei diesem Parameterwert wird die Groß-/Kleinschreibung beachtet.
Platzhalterzeichen sind nicht zulässig.

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

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Satz-AzureEnvironment](./Set-AzureEnvironment.md)


