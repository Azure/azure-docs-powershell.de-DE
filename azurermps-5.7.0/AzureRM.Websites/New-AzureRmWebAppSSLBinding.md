---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: d3971c2838b3fed04e1aa38d96e2cd27b2e8276e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501286"
---
# New-AzureRmWebAppSSLBinding

## Synopsis
Erstellt eine SSL-Zertifikat Bindung für eine Azure Web App.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### S1
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmWebAppSSLBinding** erstellt eine SSL-Zertifikat Bindung (Secure Socket Layer) für eine Azure Web App.
Das Cmdlet erstellt eine SSL-Bindung auf zwei Arten: 

- Sie können eine Web-App an ein vorhandenes Zertifikat binden.
- Sie können ein neues Zertifikat hochladen und dann die Web-App an dieses neue Zertifikat binden.

Unabhängig davon, welche Methode Sie verwenden, muss das Zertifikat und die Web-App derselben Azure-Ressourcengruppe zugeordnet sein.
Wenn Sie eine Web-App in der Ressourcengruppe a haben und diese Web-App an ein Zertifikat in der Ressourcengruppe B binden möchten, besteht die einzige Möglichkeit darin, eine Kopie des Zertifikats in die Ressourcengruppe a hochzuladen.

Wenn Sie ein neues Zertifikat hochladen, sollten Sie die folgenden Anforderungen für ein Azure SSL-Zertifikat berücksichtigen: 

- Das Zertifikat muss einen privaten Schlüssel enthalten. 
- Das Zertifikat muss das PFX-Format (Personal Information Exchange) verwenden. 
- Der Antragstellername des Zertifikats muss mit der Domäne übereinstimmen, die für den Zugriff auf die Web-App verwendet wird. 
- Das Zertifikat muss mindestens eine 2048-Bit-Verschlüsselung verwenden.

## Beispiele

### Beispiel 1: Binden eines Zertifikats an eine Web-App
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

Dieser Befehl bindet ein vorhandenes Azure-Zertifikat (ein Zertifikat mit dem Fingerabdruck E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) an die Web-App mit dem Namen ContosoWebApp.

## Parameter

### -CertificateFilePath
Gibt den Dateipfad für das Zertifikat an, das hochgeladen werden soll.

Der *CertificateFilePath* -Parameter ist nur erforderlich, wenn das Zertifikat noch nicht in Azure hochgeladen wurde.

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Gibt das Entschlüsselungskennwort für das Zertifikat an.

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Web-App an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.

Im gleichen Befehl können *ResourceGroupName* Sie den Parameter ResourceGroupName *und den Parameter* "Webanwendung" nicht verwenden.

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Gibt den Namen des Web App-Bereitstellungs Steckplatzes an.
Sie können das Get-AzureRMWebAppSlot-Cmdlet verwenden, um einen Steckplatz abzurufen.

Bereitstellungs Steckplätze bieten Ihnen die Möglichkeit, Web-Apps zu inszenieren und zu überprüfen, ohne dass diese apps über das Internet zugänglich sind.
In der Regel werden Sie Ihre Änderungen auf einer Staging-Website bereitstellen, diese Änderungen überprüfen und dann auf der Produktionswebsite (Internet-barrierefrei) bereitstellen.

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslState
Gibt an, ob das Zertifikat aktiviert ist.
Setzen Sie den *SSLState* -Parameter auf 1, um das Zertifikat zu aktivieren, oder setzen Sie *SSLState* auf 0, um das Zertifikat zu deaktivieren.

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fingerabdruck
Gibt den eindeutigen Bezeichner für das Zertifikat an.

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Webbasierte
Gibt eine Web-App an.
Verwenden Sie das Get-AzureRmWebApp-Cmdlet, um eine Web-App abzurufen.

Sie können den Webanwendungs Parameter nicht im gleichen Befehl *wie der* *ResourceGroupName* -Parameter und/oder den Webanwendungs *-Parameter verwenden* .

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Webbasierter
Gibt den Namen der Web-App an, für die die neue SSL-Bindung erstellt wird.

Im gleichen Befehl können *Sie den Parameter "* Webanwendungs" und *den "Webanwendungs Parameter"* nicht verwenden.

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Website
Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[Remove-AzureRmWebAppSSLBinding](./Remove-AzureRmWebAppSSLBinding.md)

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


