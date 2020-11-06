---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 55b95cec3e699872688fad5daeb0d2f7e89059c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498057"
---
# New-AzureRmApiManagementCertificate

## Synopsis
Erstellt ein API-Verwaltungszertifikat, das während der Authentifizierung mit Back-End verwendet werden soll.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Aus Datei laden (Standard)
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Unformatierte
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmApiManagementCertificate** erstellt ein Azure API-Verwaltungszertifikat.

## Beispiele

### Beispiel 1: Erstellen und Hochladen eines Zertifikats
```
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

Mit diesem Befehl wird ein API-Verwaltungszertifikat erstellt und hochgeladen.

## Parameter

### -Certificate-Nr
Gibt die ID des zu erstellenden Zertifikats an.
Wenn Sie diesen Parameter nicht angeben, wird eine ID für Sie erstellt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
Gibt ein **PsApiManagementContext** -Objekt an.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxBytes
Gibt ein Bytearray der Zertifikatsdatei im PFX-Format an.
Dieser Parameter ist erforderlich, wenn Sie den *PfxFilePath* -Parameter nicht angeben.

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxFilePath
Gibt den Pfad zur Zertifikatsdatei im PFX-Format zum Erstellen und Hochladen an.
Dieser Parameter ist erforderlich, wenn Sie den *PfxBytes* -Parameter nicht angeben.

```yaml
Type: System.String
Parameter Sets: Load from file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxPassword
Gibt das Kennwort für das Zertifikat an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCertificate

## Notizen

## Verwandte Links

[Get-AzureRmApiManagementCertificate](./Get-AzureRmApiManagementCertificate.md)

[Remove-AzureRmApiManagementCertificate](./Remove-AzureRmApiManagementCertificate.md)

[Satz-AzureRmApiManagementCertificate](./Set-AzureRmApiManagementCertificate.md)


