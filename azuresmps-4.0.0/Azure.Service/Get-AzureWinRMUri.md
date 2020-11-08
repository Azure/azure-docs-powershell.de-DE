---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006711"
---
# Get-AzureWinRMUri

## Synopsis
Ruft den URI für WinRM-HTTPS-Listener zu einem virtuellen Computer oder eine Liste virtueller Computer in einem gehosteten Dienst ab.

## Syntax

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureWinRMUri** " Ruft den URI des Windows Remote Management (WinRM)-HTTPS-Listener zu einem virtuellen Computer oder eine Liste mit virtuellen Computern in einem gehosteten Dienst ab.

## Beispiele

### Beispiel 1: Abrufen des URIs des WinRM-HTTPS-Listener zu einem virtuellen Computer
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

Dieser Befehl ruft die UIR des WinRM-HTTPS-Listener zu einem virtuellen Computer ab.

### Beispiel 2: Abrufen des URIs des WinRM-HTTPS-Listener zu einem virtuellen Computer eines bestimmten Diensts
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

Dieser Befehl ruft die UIR des WinRM-HTTPS-Listener zu einem virtuellen Computer ab.

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

### -Name
Gibt den Namen des virtuellen Computers an, auf den der WinRM-URI generiert wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### -ServiceName
Gibt den Namen des Microsoft Azure-Diensts an, der den virtuellen Computer hostet.

```yaml
Type: String
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

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzureVM](./New-AzureVM.md)

[Neu – AzureQuickVM](./New-AzureQuickVM.md)


