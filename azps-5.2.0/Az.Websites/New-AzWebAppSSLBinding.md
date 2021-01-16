---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367099"
---
# New-AzWebAppSSLBinding

## SYNOPSIS
Erstellt eine SSL-Zertifikatbindung für eine Azure Web App.

## SYNTAX

### S1
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzWebAppSSLBinding"** erstellt eine SECURE Socket Layer (SSL)-Zertifikatbindung für eine Azure Web App.
Das Cmdlet erstellt auf zwei Arten eine SSL-Bindung: 
- Sie können eine Web App an ein vorhandenes Zertifikat binden.
- Sie können ein neues Zertifikat hochladen und dann die Web App an dieses neue Zertifikat binden.
Unabhängig davon, welchen Ansatz Sie verwenden, müssen das Zertifikat und die Web App derselben Azure-Ressourcengruppe zugeordnet sein.
Wenn Sie über eine Web App in der Ressourcengruppe A verfügen und diese Web App an ein Zertifikat in der Ressourcengruppe B binden möchten, besteht die einzige Möglichkeit hierin, eine Kopie des Zertifikats in die Ressourcengruppe A hochzuladen. Wenn Sie ein neues Zertifikat hochladen, beachten Sie die folgenden Anforderungen für ein Azure SSL-Zertifikat: 
- Das Zertifikat muss einen privaten Schlüssel enthalten. 
- Für das Zertifikat muss das Format PFX (Personal Information Exchange) verwendet werden. 
- Der Betreffname des Zertifikats muss mit der Domäne übereinstimmen, die für den Zugriff auf die Web App verwendet wird. 
- Für das Zertifikat muss mindestens eine 2048-Bit-Verschlüsselung verwendet werden.

## BEISPIELE

### Beispiel 1: Binden eines Zertifikats an eine Web App
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

Mit diesem Befehl wird ein vorhandenes Azure-Zertifikat (ein Zertifikat mit Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) an die Web App namens ContosoWebApp gebunden.

### Beispiel 2

Erstellt eine SSL-Zertifikatbindung für eine Azure Web App. (automatisch generiert)

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## PARAMETERS

### -CertificateFilePath
Gibt den Dateipfad für das hoch zuladende Zertifikat an.
Der *Parameter "CertificateFilePath"* ist nur erforderlich, wenn das Zertifikat noch nicht in Azure hochgeladen wurde.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Web App an.

```yaml
Type: System.String
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
Sie können den Parameter *"ResourceGroupName"* und den Parameter *"WebApp" nicht* in demselben Befehl verwenden.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Gibt den Namen des Bereitstellungsplatzes für Web App an.
Sie können das cmdlet Get-AzWebAppSlot verwenden, um einen Slot zu erhalten.
Bereitstellungsplätze bieten Ihnen die Möglichkeit, Web Apps inszenieren und überprüfen zu können, ohne dass sie über das Internet zugänglich sind.
Normalerweise stellen Sie Ihre Änderungen auf einer Stagingwebsite zur Verfügung, überprüfen diese Änderungen und stellen sie dann auf der Produktionswebsite (internetbarrierefrei) zur Verfügung.

```yaml
Type: System.String
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
Legen Sie *den Parameter "SSLState"* auf "1" zum Aktivieren des Zertifikats oder *"SSLState"* auf "0" zum Deaktivieren des Zertifikats festgelegt.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Thumbprint
Gibt den eindeutigen Bezeichner für das Zertifikat an.

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Gibt eine Web App an.
Um eine Web App zu erhalten, verwenden Sie das Get-AzWebApp-Cmdlet.
Sie können den Parameter *"WebApp"* nicht in demselben Befehl wie den *Parameter "ResourceGroupName"* und/oder *"WebAppName" verwenden.*

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Gibt den Namen der Web App an, für die die neue SSL-Bindung erstellt wird.
Sie können den Parameter *"WebAppName"* und den Parameter *"WebApp"* nicht im gleichen Befehl verwenden.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## AUSGABEN

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


