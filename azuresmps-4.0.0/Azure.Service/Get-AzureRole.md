---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006520"
---
# Get-AzureRole

## Synopsis
Gibt eine Liste der Rollen in Ihrem Microsoft Azure-Dienst zurück.

## Syntax

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRole** " gibt ein Listenobjekt mit Details zu den Rollen in Ihrem Microsoft Azure-Dienst zurück.
Wenn Sie den *roleName* -Parameter angeben, gibt **Get-AzureRole** nur Details zu dieser Rolle zurück.
Wenn Sie den *InstanceDetails* -Parameter angeben, werden zusätzliche, instanzenspezifische Details zurückgegeben.

## Beispiele

### Beispiel 1: Abrufen einer Liste der Rollen für einen Dienst
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

Dieser Befehl gibt ein Objekt mit Details zu allen Produktions Rollen zurück, die im MySvc01-Dienst ausgeführt werden.

### Beispiel 2: Abrufen von Details zu einer Rolle, die in einem Dienst ausgeführt wird
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

Dieser Befehl gibt ein Objekt mit Details zur MyTestVM3-Rolle zurück, die in der Staging-Umgebung des MySvc01-Diensts ausgeführt werden.

### Beispiel 3: Abrufen von Instanzen Informationen zu Instanzen einer Rolle, die in einem Dienst ausgeführt wird
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

Dieser Befehl gibt ein Objekt mit Details zu den Instanzen der MyTestVM02-Rolle zurück, die in der Produktionsumgebung des MySvc01-Diensts ausgeführt werden.

### Beispiel 4: Abrufen einer Tabelle mit den Rolleninstanzen, die einem Dienst zugeordnet sind
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

Dieser Befehl gibt eine Tabelle des Instanznamens, der Größe und des Status aller Rolleninstanzen zurück, die in der Produktionsumgebung des MySvc01-Diensts ausgeführt werden.

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

### -InstanceDetails
Gibt an, dass dieses Cmdlet Details zu den Instanzen für jede Rolle zurückgibt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -RoleName
Gibt den Namen der abzurufenden Rolle an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Gibt den Namen des Azure-Diensts an.

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

### -Slot
Gibt die Azure-Bereitstellungsumgebung an.
Die akzeptablen Werte für diesen Parameter sind: Production oder Staging.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Satz-AzureRole](./Set-AzureRole.md)


