---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: 12603400c3d1f29eaf77d9a279d7510e08b9fe5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939803"
---
# Get-AzWebAppCertificate

## SYNOPSIS
Ruft ein Azure Web App-Zertifikat ab.

## SYNTAX

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzWebAppCertificate-Cmdlet** ruft Informationen zu Azure Web App-Zertifikaten ab, die einer angegebenen Ressourcengruppe zugeordnet sind.
Wenn Sie den Fingerabdruck des Zertifikats kennen, können Sie dieses Cmdlet auch verwenden, um Informationen zu einem angegebenen Zertifikat zu erhalten.

## BEISPIELE

### Beispiel 1: Herunterladen von Web App-Zertifikaten in einer Ressourcengruppe
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

Dieser Befehl gibt Informationen zu den hochgeladenen Web App-Zertifikaten zurück, die der Ressourcengruppe ContosoResourceGroup zugeordnet sind.

### Beispiel 2: Erhalten eines angegebenen Web App-Zertifikats
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Dieser Befehl ruft das ContosoResourceGroup Web App-Zertifikat mit dem Fingerabdruck E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 ab.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Thumbprint
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

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate

## NOTIZEN

## VERWANDTE LINKS

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)


