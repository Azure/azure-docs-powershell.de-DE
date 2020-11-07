---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 7e2a655810c885245d3694fb63caa44c5b4119e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663108"
---
# Get-AzureRmSecurityWorkspaceSetting

## Synopsis
Ruft die konfigurierten Einstellungen des Sicherheits Arbeitsbereichs für ein Abonnement ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SubscriptionScope (Standard)
```
Get-AzureRmSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelResource
```
Get-AzureRmSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Mit diesem Cmdlet können Sie den konfigurierten Arbeitsbereich ermitteln, in dem die Sicherheitsdaten enthalten sind, die vom Sicherheits-Agent erfasst wurden, der in VMs innerhalb dieses Abonnements installiert ist.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzureRmSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

Ruft die Arbeitsbereichseinstellungen für ein Abonnement ab.

## Parameter

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
Ressourcenname

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Ressourcen-ID.

```yaml
Type: String
Parameter Sets: ResourceId
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

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting

## Notizen

## Verwandte Links
