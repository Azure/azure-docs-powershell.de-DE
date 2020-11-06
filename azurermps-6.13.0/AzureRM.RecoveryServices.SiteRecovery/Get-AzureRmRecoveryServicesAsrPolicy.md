---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: aeceb76fe2f1faf6e7e1f2ddf09ee9262370e8ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499430"
---
# <span data-ttu-id="81ead-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="81ead-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="81ead-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81ead-102">SYNOPSIS</span></span>
<span data-ttu-id="81ead-103">Ruft ASR-Replikationsrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="81ead-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81ead-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81ead-104">SYNTAX</span></span>

### <span data-ttu-id="81ead-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="81ead-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81ead-106">ByName</span><span class="sxs-lookup"><span data-stu-id="81ead-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81ead-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="81ead-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81ead-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81ead-108">DESCRIPTION</span></span>
<span data-ttu-id="81ead-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrPolicy** " Ruft die Liste der konfigurierten Azure Site Recovery-Replikationsrichtlinien oder einer bestimmten Replikationsrichtlinie nach Namen ab.</span><span class="sxs-lookup"><span data-stu-id="81ead-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="81ead-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81ead-110">EXAMPLES</span></span>

### <span data-ttu-id="81ead-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81ead-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy
```

<span data-ttu-id="81ead-112">Gibt der Liste der Replikationsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="81ead-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="81ead-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="81ead-113">Example 2</span></span>
```
PS C:\>  Get-AzureRmRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="81ead-114">Gibt-Replikationsrichtlinie mit Namen.</span><span class="sxs-lookup"><span data-stu-id="81ead-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="81ead-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="81ead-115">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="81ead-116">Gibt die Replikationsrichtlinie mit dem angegebenen Anzeigenamen zurück.</span><span class="sxs-lookup"><span data-stu-id="81ead-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="81ead-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="81ead-117">PARAMETERS</span></span>

### <span data-ttu-id="81ead-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ead-118">-DefaultProfile</span></span>
<span data-ttu-id="81ead-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81ead-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="81ead-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="81ead-120">-FriendlyName</span></span>
<span data-ttu-id="81ead-121">Gibt den Anzeigenamen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="81ead-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ead-122">-Name</span><span class="sxs-lookup"><span data-stu-id="81ead-122">-Name</span></span>
<span data-ttu-id="81ead-123">Gibt den Namen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="81ead-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ead-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ead-124">CommonParameters</span></span>
<span data-ttu-id="81ead-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81ead-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ead-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81ead-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ead-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81ead-127">INPUTS</span></span>

### <span data-ttu-id="81ead-128">Keine</span><span class="sxs-lookup"><span data-stu-id="81ead-128">None</span></span>

## <span data-ttu-id="81ead-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81ead-129">OUTPUTS</span></span>

### <span data-ttu-id="81ead-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="81ead-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="81ead-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="81ead-131">NOTES</span></span>

## <span data-ttu-id="81ead-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81ead-132">RELATED LINKS</span></span>

[<span data-ttu-id="81ead-133">Neu – AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="81ead-133">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="81ead-134">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="81ead-134">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
