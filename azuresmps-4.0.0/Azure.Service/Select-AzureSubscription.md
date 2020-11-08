---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005651"
---
# Select-AzureSubscription

## Synopsis
Ändert das aktuelle und das standardmäßige Azure-Abonnement.

## Syntax

### SelectSubscriptionByNameParameterSet (Standard)
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SelectDefaultSubscriptionByNameParameterSet
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SelectSubscriptionByIdParameterSet
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SelectDefaultSubscriptionByIdParameterSet
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### NoCurrentSubscriptionParameterSet
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### NoDefaultSubscriptionParameterSet
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Select-AzureSubscription** werden die aktuellen und die standardmäßigen Azure-Abonnements festgelegt und gelöscht.

Das "aktuelle Abonnement" ist das Abonnement, das standardmäßig in der aktuellen Windows PowerShell-Sitzung verwendet wird.
Das Standardabonnement wird standardmäßig in allen Windows PowerShell-Sitzungen verwendet.
Mit der Bezeichnung "Aktuelles Abonnement" können Sie ein anderes Abonnement angeben, das standardmäßig für die aktuelle Sitzung verwendet werden soll, ohne das "Standardabonnement" für alle anderen Sitzungen zu ändern.

Die Abonnement Bezeichnung "Standard" wird in ihrer Abonnementdaten Datei gespeichert.
Die sitzungsspezifische Bezeichnung "aktuell" wird nicht gespeichert.

In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

## Beispiele

### Beispiel 1: Einrichten des aktuellen Abonnements
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

Mit diesem Befehl wird "ContosoEngineering" zum aktuellen Abonnement.

### Beispiel 2: Festlegen des Standardabonnements
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

Mit diesem Befehl wird das Standardabonnement auf "ContosoFinance" geändert. Die Einstellung wird in der Subscriptions.xml-Abonnement Datendatei anstelle der Standarddaten Datei für das Abonnement gespeichert.

## Parameter

### -Konto
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

### -Current
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Standard
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nocurrent
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NODEFAULT
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt $true zurück, wenn der Befehl erfolgreich ist, und $false, wenn ein Fehler auftritt.
Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.

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

### -Abonnement-Nr
```yaml
Type: String
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Abonnementname
```yaml
Type: String
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Standardmäßig wird keine Ausgabe generiert.

## Notizen

## Verwandte Links

[Get-AzureSubscription](./Get-AzureSubscription.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Satz-AzureSubscription](./Set-AzureSubscription.md)


