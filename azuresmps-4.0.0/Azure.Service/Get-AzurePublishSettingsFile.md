---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005839"
---
# Get-AzurePublishSettingsFile

## Synopsis
Lädt die Datei für die Veröffentlichungseinstellungen für ein Azure-Abonnement herunter.

## Syntax

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzurePublishSettingsFile** " downloadet eine Datei für Veröffentlichungseinstellungen für ein Abonnement in Ihrem Konto.
Nach Abschluss des Befehls können Sie das Cmdlet **Import-PublishSettingsFile** verwenden, um die Einstellungen in der Datei für Windows PowerShell zur Verfügung zu stellen.

Wenn Sie Ihr Azure-Konto für Windows PowerShell verfügbar machen möchten, können Sie eine Datei für Veröffentlichungseinstellungen oder das Cmdlet **Add-AzureAccount** verwenden.
Mit den Einstellungen für "Veröffentlichungseinstellungen" können Sie die Sitzung im Voraus vorbereiten, damit Skripts und Hintergrundaufträge unbeaufsichtigt ausgeführt werden können.
Allerdings unterstützen nicht alle Dienste Veröffentlichungs Einstellungsdateien.
Beispielsweise unterstützt das **AzureResourceManager** -Modul keine Veröffentlichungs Einstellungsdateien.

Wenn Sie **Get-AzurePublishSettingsFile** ausführen, wird der Standardbrowser geöffnet, und Sie werden aufgefordert, sich bei Ihrem Azure-Konto anzumelden, ein Abonnement auszuwählen und einen Speicherort für das Dateisystem für die Datei für die Veröffentlichungseinstellungen auszuwählen.
Anschließend wird die Datei für die Veröffentlichungseinstellungen Ihres Abonnements in der von Ihnen ausgewählten Datei heruntergeladen.

Eine "Veröffentlichungs Einstellungsdatei" ist eine XML-Datei mit der Dateinamenerweiterung publishsettings.
Die Datei enthält ein codiertes Zertifikat, das Verwaltungsanmeldeinformationen für Ihre Azure-Abonnements bereitstellt.

**Sicherheitshinweis:** Die Veröffentlichungs Einstellungsdateien enthalten Anmeldeinformationen, die zum Verwalten Ihrer Azure-Abonnements und-Dienste verwendet werden.
Wenn böswillige Benutzer auf Ihre Veröffentlichungs Einstellungsdatei zugreifen, können Sie Ihre Azure-Dienste bearbeiten, erstellen und löschen.
Aus Sicherheitsgründen empfiehlt es sich, die Datei an einem Speicherort im Ordner "Downloads" oder "Dokumente" zu speichern und diese dann nach Verwendung des Cmdlets " **Import-AzurePublishSettingsFile** " zu löschen, um die Einstellungen zu importieren.

In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

## Beispiele

### Beispiel 1: Herunterladen einer Datei für Veröffentlichungseinstellungen
```
PS C:\> Get-AzurePublishSettingsFile
```

Mit diesem Befehl wird der Standardbrowser geöffnet, eine Verbindung mit Ihrem Windows Azure-Konto hergestellt und dann die publishsettings-Datei für Ihr Konto heruntergeladen.

### Beispiel 2: Angeben eines Bereichs
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

Mit diesem Befehl wird die Datei für die Veröffentlichungseinstellungen für ein Konto in der contoso.com-Domäne heruntergeladen.
Verwenden Sie einen Befehl mit dem **Bereich** -Parameter, wenn Sie sich bei Azure mit einem organisationskonto anstatt mit einem Microsoft-Konto anmelden.

## Parameter

### -Umgebung
Gibt eine Azure-Umgebung an.

Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.
Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.
Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

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
Gibt $true zurück, wenn der Befehl erfolgreich ist, und $false, wenn ein Fehler auftritt.
Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Realm
Gibt die Organisation in einer Organisations-ID an.
Wenn Sie sich beispielsweise bei Azure as anmelden admin@contoso.com , lautet der Wert des **Bereichs** Parameters contoso.com.
Verwenden Sie diesen Parameter, wenn Sie eine Organisations-ID verwenden, um sich beim Azure-Portal anzumeldet.
Dieser Parameter ist nicht erforderlich, wenn Sie ein Microsoft-Konto verwenden, beispielsweise ein Outlook.com-oder Live.com-Konto.

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

### Keine
Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.

## Ausgaben

### None oder System. Boolean
Wenn Sie den *passthru* -Parameter verwenden, gibt dieses Cmdlet einen booleschen Wert zurück.
Andernfalls gibt dieses Cmdlet keine Ausgabe zurück.

## Notizen

## Verwandte Links

[Add-AzureAccount](./Add-AzureAccount.md)

[Importieren-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)


