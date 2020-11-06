---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
ms.openlocfilehash: d7fbd87a436b9d0ea2fd0d311e19dc3df5bb8dda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499902"
---
# Get-AzureRmWebAppCertificate

## Synopsis
Ruft ein Azure Web App-Zertifikat ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmWebAppCertificate** " Ruft Informationen zu Azure Web App-Zertifikaten ab, die einer angegebenen Ressourcengruppe zugeordnet sind.
Wenn Sie den Fingerabdruck des Zertifikats kennen, können Sie dieses Cmdlet auch verwenden, um Informationen zu einem angegebenen Zertifikat abzurufen.

## Beispiele

### Beispiel 1: Abrufen von Web App-Zertifikaten in einer Ressourcengruppe
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

Dieser Befehl gibt Informationen zu den geuploadeten Web App-Zertifikaten zurück, die der Ressourcengruppe ContosoResourceGroup zugeordnet sind.

### Beispiel 2: Abrufen eines angegebenen Web App-Zertifikats
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Dieser Befehl ruft das ContosoResourceGroup Web App-Zertifikat mit dem Fingerabdruck-E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.

## Parameter

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fingerabdruck
Gibt den eindeutigen Bezeichner für das Zertifikat an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
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

## Notizen

## Verwandte Links

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)


