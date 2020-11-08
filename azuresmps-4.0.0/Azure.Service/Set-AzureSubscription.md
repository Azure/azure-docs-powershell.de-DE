---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006156"
---
# Set-AzureSubscription

## Synopsis
Ändert ein Azure-Abonnement.

## Syntax

### UpdateSubscriptionByIdParameterSetName (Standard)
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### UpdateSubscriptionByNameParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AddSubscriptionParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureSubscription** " erstellt und ändert die Eigenschaften eines Azure-Abonnementobjekts.
Sie können dieses Cmdlet verwenden, um in einem Azure-Abonnement zu arbeiten, bei dem es sich nicht um Ihr Standardabonnement handelt, oder um Ihr aktuelles Speicherkonto zu ändern.
Informationen zu aktuellen und Standardabonnements finden Sie unter dem Cmdlet **Select-AzureSubscription** .

Dieses Cmdlet arbeitet für ein Azure-Abonnementobjekt und nicht für das tatsächliche Azure-Abonnement.
Besuchen Sie zum Erstellen und Bereitstellen eines Azure-Abonnements das [Azure-Portal](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .

Mit diesem Cmdlet werden die Daten in der Abonnementdaten Datei geändert, die Sie erstellen, wenn Sie Windows PowerShell mithilfe des Cmdlets **Add-AzureAccount** oder **Import-AzurePublishSettingsFile** ein Azure-Konto hinzufügen.

In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

## Beispiele

### Beispiel 1: Ändern einer vorhandenen abonnement1
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

In diesem Beispiel wird das Zertifikat für das Abonnement mit dem Namen ContosoEngineering geändert.

### Beispiel 2: Ändern des Dienstendpunkts
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

Mit diesem Befehl wird ein benutzerdefinierter Dienstendpunkt für das ContosoEngineering-Abonnement hinzugefügt oder geändert.

### Beispiel 3: Löschen von Eigenschaftswerten
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

Mit diesem Befehl werden die Werte der Eigenschaften Certificate und ResourceManagerEndpoint auf NULL ($null) festgelegt.
Dadurch werden die Werte dieser Eigenschaften gelöscht, ohne dass andere Einstellungen geändert werden.

### Beispiel 4: Verwenden einer alternativen Abonnement Datendatei
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

Mit diesem Befehl wird das aktuelle Speicherkonto des ContosoFinance-Abonnements in ContosoStorage01 geändert.
Der Befehl verwendet den **SubscriptionDataFile** -Parameter, um die Daten in der C:\Azure\SubscriptionData.xml-Abonnement Datendatei zu ändern.
Standardmäßig verwendet " **Satz-AzureSubscription** " die standardmäßige Abonnement Datendatei in Ihrem Roaming-Benutzerprofil.

## Parameter

### -Zertifikat
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CurrentStorageAccountName
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

### -ResourceManagerEndpoint
Gibt den Endpunkt für Azure Resource Manager-Daten an, einschließlich Daten zu Ressourcengruppen, die dem Konto zugeordnet sind.
Weitere Informationen zum Azure Resource Manager finden Sie unter [Azure Resource Manager-Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) und [Verwenden von Windows PowerShell mit Ressourcen-Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  ( https://go.microsoft.com/fwlink/?LinkID=394767) .

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

### -ServiceEndpoint
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

### -Abonnement-Nr
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Abonnementname
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
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

### None oder System. Boolean
Wenn Sie den *passthru* -Parameter verwenden, gibt dieses Cmdlet einen booleschen Wert zurück.
Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.

## Notizen

## Verwandte Links

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureSubscription](./Get-AzureSubscription.md)

[Importieren-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[SELECT-AzureSubscription](./Select-AzureSubscription.md)


