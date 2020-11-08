---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006718"
---
# Get-AzureWebHostingPlan

## Synopsis
Ruft Azure Web Hosting-Pläne im aktuellen Abonnement ab.

## Syntax

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet " **Get-AzureWebHostingPlan** " Ruft die Azure Web Hosting-Pläne im aktuellen Abonnement ab.

Standardmäßig ruft **Get-AzureWebHostingPlan** alle Azure-hostpläne im aktuellen Abonnement ab und gibt ein Objekt zurück, das grundlegende Informationen zu den Plänen bereitstellt.
Wenn Sie die Parameter *Webspace* und *Name* verwenden, gibt **Get-AzureWebHostingPlan** ein bestimmtes Host Planobjekt zurück.

Um das aktuelle Abonnement zu finden, verwenden Sie den *aktuellen* Parameter des Cmdlets **Get-AzureSubscription** .
Wenn Sie das aktuelle Abonnement ändern möchten, verwenden Sie das Cmdlet **Select-AzureSubscription** .

## Beispiele

### Beispiel 1: Abrufen aller Webhosting-Pläne in einem Abonnement
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

Dieser Befehl ruft alle Azure Web Hosting-Pläne im aktuellen Abonnement ab.

### Beispiel 2: Abrufen eines bestimmten Webhosting-Plans in einem Abonnement
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

Dieser Befehl ruft den Webhosting-Plan mit dem Namen Default0 im Webspace mit dem Namen westeuropewebspace im aktuellen Abonnement ab.

## Parameter

### -Name
Gibt den Namen eines Plans im Abonnement an.
Standardmäßig ruft dieses Cmdlet alle Pläne im aktuellen Abonnement ab.
Dieser Parameter unterstützt keine Platzhalterzeichen.

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

### -Webspacename
Gibt den Namen eines Webspaces im Abonnement an.
Standardmäßig ruft dieses Cmdlet alle Websites im angegebenen Webspace ab.
Dieser Parameter unterstützt keine Platzhalterzeichen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

###  
Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.

## Ausgaben

### Microsoft. WindowsAzure. Commands. Utilities. Websites. Services. webentities. WebHostingPlan
Standardmäßig gibt **Get-AzureWebHostingPlan** ein Array von **WebHostingPlan** -Objekten zurück.

## Notizen

## Verwandte Links

