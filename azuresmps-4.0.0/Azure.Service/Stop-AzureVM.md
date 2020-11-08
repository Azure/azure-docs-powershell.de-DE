---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005947"
---
# Stop-AzureVM

## Synopsis
Beendet einen virtuellen Azure-Computer.

## Syntax

### ByName (Standard)
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Eingabe
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Stop-AzureVM** " beendet einen virtuellen Computer.

## Beispiele

### Beispiel 1: Herunterfahren eines virtuellen Computers
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

Dieser Befehl beendet einen virtuellen Computer, den der angegebene Dienst enthält.

### Beispiel 2: Herunterfahren eines virtuellen Computers mit einem virtuellen Computerobjekt
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

Dieser Befehl beendet einen virtuellen Computer, den der angegebene Dienst enthält, indem Sie das Objekt des virtuellen Computers verwenden, das von **Get-AzureVM** zurückgegeben wird.

### Beispiel 3: Herunterfahren eines virtuellen Computers und beibehalten der bereitgestellten VM
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

Dieser Befehl beendet einen virtuellen Computer, den der angegebene Dienst enthält, und hält ihn bereitgestellt.

### Beispiel 4: Herunterfahren eines virtuellen Computers und zulassen der Freigabe des letzten virtuellen Computers in der Bereitstellung
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

Dieser Befehl beendet einen virtuellen Computer, den der angegebene Dienst enthält, und ermöglicht die Freigabe des letzten virtuellen Computers in der Bereitstellung.

### Beispiel 5: Herunterfahren mehrerer VMS
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

Mit diesem Befehl werden mehrere virtuelle Computer, die der angegebene Dienst enthält, heruntergefahren.

## Parameter

### -Force
Gibt an, ob die Freigabe des letzten virtuellen Computers in einer Bereitstellung zulässig ist.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Gibt den Namen des virtuellen Computers an, der beendet werden soll.

Verwenden Sie das Platzhalterzeichen, um mehrere virtuelle Computer asynchron zu beenden.
Mit einem Platzhalterzeichen ruft dieses Cmdlet die Operation Shutdown Roles https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) anstelle des Vorgangs für das Herunterfahren der Rolle https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .

```yaml
Type: String[]
Parameter Sets: ByName
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

### -ServiceName
Gibt den Namen des Azure-Diensts an, der den virtuellen Computer enthält, der beendet werden soll.

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

### -StayProvisioned
Gibt an, dass das Cmdlet die Bereitstellung des virtuellen Computers verhindert.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt ein Objekt eines virtuellen Computers an, das den zu beendenden virtuellen Computer identifiziert.

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

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

[Get-AzureVM](./Get-AzureVM.md)

[Neu – AzureVM](./New-AzureVM.md)

[Neustart-AzureVM](./Restart-AzureVM.md)

[Anfang-AzureVM](./Start-AzureVM.md)


