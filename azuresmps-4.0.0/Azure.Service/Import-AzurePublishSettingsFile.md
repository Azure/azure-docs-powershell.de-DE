---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006467"
---
# Import-AzurePublishSettingsFile

## Synopsis
Importiert eine Datei für Veröffentlichungseinstellungen, in der Sie Ihre Azure-Konten in Windows PowerShell verwalten können.

## Syntax

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Import-AzurePublishSettingsFile** " importiert eine Datei für Veröffentlichungseinstellungen (*. publishsettings), die Informationen zu ihren Azure-Konten enthält, und speichert eine Abonnement Datendatei auf Ihrem Computer.
Nach Abschluss des Cmdlets können Sie Ihre Azure-Konten in Windows PowerShell verwalten.

Führen Sie vor dem Ausführen von **Import-AzurePublishSettingsFile** den Eintrag **Get-AzurePublishSettingsFile** aus, der die Datei für die Veröffentlichungseinstellungen downloadet und speichert, sodass Sie Sie importieren können.

Wenn Sie Ihr Azure-Konto für Windows PowerShell verfügbar machen möchten, können Sie eine Datei für Veröffentlichungseinstellungen oder das Cmdlet **Add-AzureAccount** verwenden.
Mit den Einstellungen für "Veröffentlichungseinstellungen" können Sie die Sitzung im Voraus vorbereiten, damit Skripts und Hintergrundaufträge unbeaufsichtigt ausgeführt werden können.
Allerdings unterstützen nicht alle Dienste Veröffentlichungs Einstellungsdateien.
Beispielsweise unterstützt das **AzureResourceManager** -Modul keine Veröffentlichungs Einstellungsdateien.

**Sicherheitshinweis:** Dateien für Veröffentlichungseinstellungen enthalten ein Verwaltungszertifikat, das verschlüsselt, aber nicht verschlüsselt ist.
Wenn böswillige Benutzer auf Ihre Veröffentlichungs Einstellungsdatei zugreifen, können Sie Ihre Azure-Dienste möglicherweise bearbeiten, erstellen und löschen.
Aus Sicherheitsgründen empfiehlt es sich, die Datei an einem Speicherort im Ordner "Downloads" oder "Dokumente" zu speichern und diese dann nach Verwendung des Cmdlets " **Import-AzurePublishSettingsFile** " zu löschen, um die Einstellungen zu importieren.

## Beispiele

### Beispiel 1: Importieren einer Datei
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

Dieser Befehl importiert die "C:\Temp\MyAccount.publishsettings"-Datei.

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

### -PublishSettingsFile
```yaml
Type: String
Parameter Sets: (All)
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

### Keine
Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.

## Ausgaben

### Keine
Dieses Cmdlet generiert keine Ausgabe.

## Notizen
* Eine "Veröffentlichungs Einstellungsdatei" ist eine XML-Datei mit der Dateinamenerweiterung publishsettings. Die Datei enthält ein codiertes Zertifikat, das Verwaltungsanmeldeinformationen für Ihre Azure-Abonnements bereitstellt. Nachdem Sie diese Datei importiert haben, löschen Sie Sie, um Sicherheitsrisiken zu vermeiden.
* Eine "Abonnement Datendatei" ist eine XML-Datei, die auf Ihrem Computer sicher gespeichert werden kann. Standardmäßig wird es in Ihrem Roaming-Benutzerprofil ($Home/AppData/Roaming) gespeichert.

## Verwandte Links

[Installieren und Konfigurieren von Azure PowerShell](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)


