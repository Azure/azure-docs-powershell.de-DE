---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006025"
---
# Set-AzureServiceProject

## Synopsis
Legt den Standardstandort, das Abonnement, den Steckplatz und das Speicherkonto für den aktuellen Dienst fest.

## Syntax

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureServiceProject** " legt den Bereitstellungsspeicherort, den Steckplatz, das Speicherkonto und das Abonnement für den aktuellen Dienst fest.
Diese Werte werden immer dann verwendet, wenn der Dienst in der Cloud veröffentlicht wird.

## Beispiele

### Beispiel 1: grundlegende Einstellungen
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

Legt den Bereitstellungsspeicherort für den Dienst auf die Nord zentrale US-Region fest.
Legt den Bereitstellungs Steckplatz auf Production fest. Legt das Speicherkonto fest, das zum Bereitstellen der Dienstdefinition für myStorageAccount verwendet wird.
Legt das Abonnement fest, das den Dienst für mysubscription hosten soll.
Wenn der Dienst in der Cloud veröffentlicht wird, wird er in einem Rechenzentrum in der Region Nord-Zentralamerika gehostet, der Bereitstellungs Steckplatz wird aktualisiert, und es wird das angegebene Abonnement-und Speicherkonto verwendet.

## Parameter

### -Standort
Der Bereich, in dem der Dienst gehostet wird.
Dieser Wert wird immer dann verwendet, wenn der Dienst in der Cloud veröffentlicht wird.
Mögliche Werte sind: überall in Asien, überall in Europa, überall in den USA, Ostasien, Ost-und Nordamerika, Nordeuropa, Süd-Zentralamerika, Südostasien, Westeuropa, Westamerika.

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

### -PassThru
Gibt an, dass dieses Cmdlet ein Objekt zurückgibt, das das Element darstellt, auf dem es ausgeführt wird.
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

### -Slot
Der Slot (Production oder Staging), in dem der Dienst gehostet wird.
Dieser Wert wird immer dann verwendet, wenn der Dienst in der Cloud veröffentlicht wird.
Mögliche Werte sind: Production, Staging.

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

### -Speicher
Das Speicherkonto, das beim Hochladen des Dienstpakets in die Cloud verwendet werden soll.
Wenn das Speicherkonto nicht vorhanden ist, wird es erstellt, wenn der Dienst in der Cloud veröffentlicht wird.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen
* Node-dev, php-dev, python-dev

## Verwandte Links

[Neu – AzureServiceProject](./New-AzureServiceProject.md)

[Publish-AzureServiceProject](./Publish-AzureServiceProject.md)

[Satz-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


