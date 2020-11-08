---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006753"
---
# Get-AzureVM

## Synopsis
Ruft Informationen von einem oder mehreren Azure Virtual Machines ab.

## Syntax

### ListAllVMs (Standard)
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### GetVMByServiceAndVMName
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureVM** " Ruft Informationen zu virtuellen Computern ab, die in Azure ausgeführt werden.
Sie gibt ein Objekt mit Informationen auf einem bestimmten virtuellen Computer oder, wenn kein virtueller Computer angegeben ist, für alle virtuellen Computer im angegebenen Dienst des aktuellen Abonnements zurück.

## Beispiele

### Beispiel 1: Abrufen von Informationen auf einem angegebenen virtuellen Computer
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

Dieser Befehl gibt ein Objekt mit Informationen auf dem virtuellen VirtualMachine02-Computer zurück, der im ContosoService01-cloudbasierten Dienst ausgeführt wird.

### Beispiel 2: Abrufen von Informationen auf allen virtuellen Computern
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

Dieser Befehl ruft ein Listenobjekt mit Informationen zu allen virtuellen Computern ab, die im ContosoService01-clouddienst ausgeführt werden.

### Beispiel 3: Anzeigen einer Tabelle mit den Status von virtuellen Computern
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

Dieser Befehl zeigt eine Tabelle mit den virtuellen Computern, die im ContosoService01-Dienst ausgeführt werden, ihrer Upgrade-Domäne und dem aktuellen Status der einzelnen virtuellen Computer an.

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
Gibt den Namen des virtuellen Computers an, für den Informationen abgerufen werden sollen.
Wenn dieser Parameter nicht angegeben wird, gibt das Cmdlet ein Listenobjekt mit Informationen zu allen virtuellen Computern im angegebenen Dienst zurück.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
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
Gibt den Namen des Cloud-Diensts an, für den Informationen zu virtuellen Maschinen zurückgegeben werden sollen.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
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

[Neu – AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzureVM](./Remove-AzureVM.md)

[Neustart-AzureVM](./Restart-AzureVM.md)

[Anfang-AzureVM](./Start-AzureVM.md)

[Stopp-AzureVM](./Stop-AzureVM.md)

[Update-AzureVM](./Update-AzureVM.md)


