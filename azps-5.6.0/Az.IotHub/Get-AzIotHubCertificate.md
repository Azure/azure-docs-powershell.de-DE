---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 06a6f2ea8ffbd0d90689a24d3fcec5ca8222f9ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936968"
---
# Get-AzIotHubCertificate

## SYNOPSIS
Listet alle Zertifikate oder ein bestimmtes Zertifikat auf, die in einem Azure IoT Hub enthalten sind. 

## SYNTAX

### ResourceSet (Standard)
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObjectSet
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdSet
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Eine detaillierte Erläuterung der Zertifizierungsstellenzertifikate in Azure IoT Hub finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview

## BEISPIELE

### Beispiel 1
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

Auflisten aller Zertifikate in MyIotHub

### Beispiel 2
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

Anzeigen von Details zu MyCertificate

## PARAMETER

### -CertificateName
Name des Zertifikats

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -InputObject
IotHub-Objekt

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Name des Iot-Hubs

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
IotHub-Ressourcen-ID

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription

## NOTIZEN

## VERWANDTE LINKS
