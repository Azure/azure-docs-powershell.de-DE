---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006158"
---
# Set-AzureServiceProjectRole

## Synopsis
Legt die Anzahl der Instanzen oder die Laufzeitversion einer Rolle fest.

## Syntax

### Instanzen
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Runtime
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### VMSize
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet " **Set-AzureServiceProjectRole** " legt die Anzahl der Rolleninstanzen für die angegebene Rolle fest.

## Beispiele

### Beispiel 1: Einrichten von Instanzen für eine webrolle
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

Legt die Anzahl der Instanzen für die Web-Rolle mit dem Namen MyWebRole1 auf 2 fest.

### Beispiel 2: Einrichten von Instanzen für eine Worker-Rolle
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

Legt die Anzahl der Rolleninstanzen für die Worker-Rolle mit dem Namen WorkerRole1 auf 2 fest.

### Beispiel 3: Einrichten der Laufzeitversion für einen Rollendienst
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

Legt die node.exe-Laufzeitversion für Role MyRole1 auf 0.6.20 fest.

## Parameter

### -Instanzen
Gibt die Anzahl der Rolleninstanzen für die angegebene Web-oder Worker-Rolle an.

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -RoleName
Gibt den Namen der zu ändernden Web-oder Worker-Rolle an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Runtime
Gibt die Laufzeit an, die der angegebenen Rolle hinzugefügt werden soll.

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Gibt die Version der Common Language Runtime an, die der Rolle hinzugefügt werden soll.

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
Gibt die Größe des virtuellen Computers der Rolle an.

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

###  
Gibt die Größe des virtuellen Computers an.

## Ausgaben

## Notizen

## Verwandte Links

[Satz-AzureServiceProject](./Set-AzureServiceProject.md)


