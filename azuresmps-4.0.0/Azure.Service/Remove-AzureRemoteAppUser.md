---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006072"
---
# Remove-AzureRemoteAppUser

## Synopsis
Entfernt einen Benutzer aus einer Azure RemoteApp-Sammlung.

## Syntax

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRemoteAppUser** entfernt einen Benutzer aus einer Azure RemoteApp-Sammlung.

## Beispiele

### Beispiel1: Entfernen eines Benutzers aus einer Sammlung
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

Mit diesem Befehl wird der Azure ActiveDirectory PattiFuller@contoso.com -Benutzer aus der Contoso-Auflistung entfernt.

## Parameter

### -Alias
Gibt einen veröffentlichten Programm-Alias an.
Sie können diesen Parameter nur im pro-App-Veröffentlichungsmodus verwenden.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Gibt den Namen der Azure RemoteApp-Sammlung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### -Typ
Gibt einen Benutzertyp an.
Die zulässigen Werte für diesen Parameter sind: OrgId oder MicrosoftAccount.

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserUpn
Gibt den Benutzerprinzipalnamen (User Principal Name, UPN) eines Benutzers an, beispielsweise user@contoso.com .

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureRemoteAppUser](./Add-AzureRemoteAppUser.md)

[Get-AzureRemoteAppUser](./Get-AzureRemoteAppUser.md)


