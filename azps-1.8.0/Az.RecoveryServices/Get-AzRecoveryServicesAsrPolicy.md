---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a25375a565db8d2c69a423aa95033033de3f0f8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659943"
---
# <span data-ttu-id="8f6da-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="8f6da-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="8f6da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f6da-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6da-103">Ruft ASR-Replikationsrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="8f6da-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="8f6da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f6da-104">SYNTAX</span></span>

### <span data-ttu-id="8f6da-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f6da-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f6da-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8f6da-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f6da-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8f6da-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f6da-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f6da-108">DESCRIPTION</span></span>
<span data-ttu-id="8f6da-109">Das Cmdlet " **Get-AzRecoveryServicesAsrPolicy** " Ruft die Liste der konfigurierten Azure Site Recovery-Replikationsrichtlinien oder einer bestimmten Replikationsrichtlinie nach Namen ab.</span><span class="sxs-lookup"><span data-stu-id="8f6da-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="8f6da-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f6da-110">EXAMPLES</span></span>

### <span data-ttu-id="8f6da-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f6da-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="8f6da-112">Gibt der Liste der Replikationsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="8f6da-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="8f6da-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8f6da-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="8f6da-114">Gibt-Replikationsrichtlinie mit Namen.</span><span class="sxs-lookup"><span data-stu-id="8f6da-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="8f6da-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8f6da-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="8f6da-116">Gibt die Replikationsrichtlinie mit dem angegebenen Anzeigenamen zurück.</span><span class="sxs-lookup"><span data-stu-id="8f6da-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="8f6da-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f6da-117">PARAMETERS</span></span>

### <span data-ttu-id="8f6da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6da-118">-DefaultProfile</span></span>
<span data-ttu-id="8f6da-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f6da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8f6da-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8f6da-120">-FriendlyName</span></span>
<span data-ttu-id="8f6da-121">Gibt den Anzeigenamen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="8f6da-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="8f6da-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8f6da-122">-Name</span></span>
<span data-ttu-id="8f6da-123">Gibt den Namen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="8f6da-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="8f6da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6da-124">CommonParameters</span></span>
<span data-ttu-id="8f6da-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f6da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6da-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f6da-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6da-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f6da-127">INPUTS</span></span>

### <span data-ttu-id="8f6da-128">Keine</span><span class="sxs-lookup"><span data-stu-id="8f6da-128">None</span></span>

## <span data-ttu-id="8f6da-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f6da-129">OUTPUTS</span></span>

### <span data-ttu-id="8f6da-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="8f6da-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="8f6da-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f6da-131">NOTES</span></span>

## <span data-ttu-id="8f6da-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f6da-132">RELATED LINKS</span></span>

[<span data-ttu-id="8f6da-133">Neu – AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="8f6da-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="8f6da-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="8f6da-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
