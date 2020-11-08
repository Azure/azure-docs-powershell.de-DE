---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006602"
---
# Add-AzureAccount

## Synopsis
Fügt Windows PowerShell das Azure-Konto hinzu.

## Syntax

### Benutzer (Standard)
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServicePrincipal
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureAccount** können Sie Ihr Azure-Konto und seine Abonnements in Windows PowerShell zur Verfügung stellen.
Es ist wie bei der Anmeldung bei Ihrem Azure-Konto in Windows PowerShell.
Zum Abmelden des Kontos verwenden Sie das Cmdlet **Remove-AzureAccount** .

**Add-AzureAccount** downloadet Informationen zu Ihrem Azure-Konto und speichert Sie in einer Abonnement Datendatei in Ihrem Roaming-Benutzerprofil.
Außerdem wird ein Zugriffstoken abgerufen, mit dem Windows PowerShell in Ihrem Auftrag auf Ihr Azure-Konto zugreifen kann.
Nach Abschluss des Befehls können Sie Ihr Azure-Konto in Windows PowerShell verwalten.

Es gibt zwei verschiedene Möglichkeiten, Ihr Azure-Konto für Windows PowerShell verfügbar zu machen.
Sie können das **Add-AzureAccount-** Cmdlet verwenden, das Azure Active Directory-Authentifizierungs Zugriffstoken (Azure AD) oder **Import-AzurePublishSettingsFile** verwendet, das ein Verwaltungszertifikat verwendet.
Anleitungen zu den zu verwendenden Methoden finden Sie unter [so wird es gemacht: Herstellen einer Verbindung mit Ihrem Abonnement](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .

Wenn Sie **Add-AzureAccount** ausführen, wird ein interaktives Fenster angezeigt, in dem Sie aufgefordert werden, sich bei Ihrem Azure-Konto anzumeldet.
Diese Anmeldung ist gültig, bis das Zugriffstoken abläuft.
Wenn es abläuft, werden Cmdlets, die Zugriff auf Ihr Konto benötigen, aufgefordert, **Add-AzureAccount** erneut auszuführen.

In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

## Beispiele

### Beispiel 1: Hinzufügen eines Kontos
```
PS C:\> Add-AzureAccount
```

Mit diesem Befehl wird Windows PowerShell ein Azure-Konto hinzugefügt.
Wenn Sie den Befehl ausführen, wird ein Windows-Fenster eingeblendet, in dem Sie den Benutzernamen und das Kennwort des Kontos anfordern können.

### Beispiel 2: Verwenden einer alternativen Abonnement Datendatei
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

Dieser Befehl verwendet den **SubscriptionDataFile** -Parameter, um **Add-AzureAccount** zu verweisen, um die Kontodaten anstelle der Standarddatei in der C:\Testing\SDF.xml Datei zu speichern.

## Parameter

### – Anmeldeinformationen
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ServicePrincipal
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mandant
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Sie können keine Eingabe an dieses Cmdlet übergeben

## Ausgaben

### Keine
Dieses Cmdlet gibt keine Ausgabe zurück.

## Notizen
* **Add-AzureAccount** (und die Azure AD-Authentifizierungsmethode) hat Vorrang vor der **Import-AzurePublishSettings** (und der Management Certificate-Methode). Wenn Sie **Add-AzureAccount** auch einmal für Ihr Konto verwenden, wird die Azure AD-Authentifizierungsmethode verwendet, und das Verwaltungszertifikat wird ignoriert. Wenn Sie das Azure AD-Token entfernen und die Verwaltungszertifikat Methode wiederherstellen möchten, verwenden Sie das Cmdlet **Remove-AzureAccount** . Wenn Sie weitere Informationen benötigen, geben Sie Folgendes ein: **get-help Remove-AzureAccount**.
* Der Fehler "Ihre Anmeldeinformationen sind abgelaufen. Bitte verwenden Sie Add-AzureAccount, um sich erneut anzumelden. " Gibt an, dass das Zugriffstoken abgelaufen ist und Windows PowerShell nicht auf Ihr Azure-Konto zugreifen kann. Wenn Sie den Zugriff auf Ihr Konto wiederherstellen möchten, führen **Sie Add-AzureAccount** erneut aus.
* Die Azure PowerShell-Konto-und Abonnement-Cmdlets erhalten Ihre Daten aus der Abonnement Datendatei, nicht aus dem Live Azure-Konto. Wenn Sie Ihr Konto oder Ihre Abonnements außerhalb von Windows PowerShell ändern, beispielsweise mithilfe des Azure-Verwaltungsportals, führen Sie **Add-AzureAccount** erneut aus, um die Abonnement Datendatei zu aktualisieren.

## Verwandte Links

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Importieren-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Get-AzureAccount](./Get-AzureAccount.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


