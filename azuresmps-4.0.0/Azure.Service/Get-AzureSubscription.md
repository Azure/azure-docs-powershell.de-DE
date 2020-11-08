---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005743"
---
# Get-AzureSubscription

## Synopsis
Ruft Azure-Abonnements in Azure-Konto ab.

## Syntax

### ByName (Standard)
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ById
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Standard
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Aktuellen
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureSubscription** " Ruft die Abonnements in Ihrem Azure-Konto ab.
Sie können dieses Cmdlet verwenden, um Informationen zum Abonnement abzurufen und das Abonnement an andere Cmdlets zu übergeben.

Für **Get-AzureSubscription** ist der Zugriff auf Ihre Azure-Konten erforderlich.
Bevor Sie **Get-AzureSubscription** ausführen, müssen Sie das **Add-AzureAccount-** Cmdlet oder die Cmdlets ausführen, die eine Datei für die Veröffentlichungseinstellungen herunterladen und installieren ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.

In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

## Beispiele

### Beispiel 1: Abrufen aller Abonnements
```
C:\PS>Get-AzureSubscription
```

Dieser Befehl ruft alle Abonnements im Konto ab.

### Beispiel 2: Abrufen eines Abonnements nach Name
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

Dieser Befehl ruft nur das "MyProdSubsciption"-Abonnement ab.

### Beispiel 3: Abrufen des Standardabonnements
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

Dieser Befehl ruft nur den Namen des Standardabonnements ab.
Der Befehl ruft zuerst das Abonnement ab und verwendet dann die dot-Methode, um die **subscriptionname** -Eigenschaft des Abonnements abzurufen.

### Beispiel 4: Abrufen ausgewählter Abonnementeigenschaften
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

Dieser Befehl gibt eine Liste mit dem Namen und dem Zertifikat des aktuellen Abonnements zurück.
Es wird ein Befehl " **Get-AzureSubscription** " verwendet, um das aktuelle Abonnement abzurufen.
Anschließend wird das Abonnement an einen Befehl **Format-List** Weiterleitung, in dem die ausgewählten Eigenschaften in einer Liste angezeigt werden.

### Beispiel 5: Verwenden einer alternativen Abonnement Datendatei
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

Dieser Befehl ruft Abonnements aus der Datendatei des C:\Temp\MySubscriptions.xml-Abonnements ab.
Verwenden Sie den **SubscriptionDataFile** -Parameter, wenn Sie beim Ausführen der Cmdlets **Add-AzureAccount** oder **Import-PublishSettingsFile** eine Alternative Abonnementdaten Datei angegeben haben.

## Parameter

### -Current
Ruft nur das aktuelle Abonnement ab, also das Abonnement, das als "aktuell" festgelegt ist. Standardmäßig ruft **Get-AzureSubscription** alle Abonnements in ihren Azure-Konten ab.
Wenn Sie ein Abonnement als "aktuell" festlegen möchten, verwenden Sie den **aktuellen** Parameter des Cmdlets **Select-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Standard
Ruft nur das Standardabonnement ab, also das Abonnement, das als "Standard" festgelegt ist. Standardmäßig ruft **Get-AzureSubscription** alle Abonnements in ihren Azure-Konten ab.
Wenn Sie ein Abonnement als "Standard" festlegen möchten, verwenden Sie den **Standard** Parameter des Cmdlets **Select-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendedDetails
Gibt Kontingentinformationen für das Abonnement zusätzlich zu den Standardeinstellungen zurück.

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
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Abonnementname
Ruft nur das angegebene Abonnement ab.
Geben Sie den Namen des Abonnements ein.
Bei dem Wert wird die Groß-/Kleinschreibung beachtet.
Platzhalterzeichen werden nicht unterstützt.
Standardmäßig ruft **Get-AzureSubscription** alle Abonnements in ihren Azure-Konten ab.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Sie können die Eingabe an die **subscriptionname** -Eigenschaft nach Name, aber nicht nach Wert überleiten.

## Ausgaben

### Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureSubscription

## Notizen
* Get-AzureSubscription ruft Daten aus der Abonnement Datendatei ab, die von den Cmdlets **Add-AzureAccount** und **Import-PublishSettingsFile** erstellt werden.

## Verwandte Links

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Importieren-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Satz-AzureSubscription](./Set-AzureSubscription.md)


