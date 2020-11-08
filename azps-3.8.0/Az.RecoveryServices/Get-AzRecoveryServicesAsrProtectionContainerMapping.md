---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7d3b5735cc52ae190cc16c93ad9806a9f47b452d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995315"
---
# <span data-ttu-id="0cc1c-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0cc1c-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="0cc1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0cc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc1c-103">Ruft Azure Site Recovery Protection-Container Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="0cc1c-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="0cc1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cc1c-104">SYNTAX</span></span>

### <span data-ttu-id="0cc1c-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="0cc1c-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cc1c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="0cc1c-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cc1c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cc1c-107">DESCRIPTION</span></span>
<span data-ttu-id="0cc1c-108">Das Cmdlet " **Get-AzRecoveryServicesAsrProtectionContainerMapping** " Ruft Informationen über den Schutzcontainer für Replikationsrichtlinien Zuordnungen (Association) im Tresor für den angegebenen ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="0cc1c-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="0cc1c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cc1c-109">EXAMPLES</span></span>

### <span data-ttu-id="0cc1c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0cc1c-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="0cc1c-111">Liste der Schutzcontainer Zuordnungen für Container.</span><span class="sxs-lookup"><span data-stu-id="0cc1c-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="0cc1c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0cc1c-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="0cc1c-113">Ruft alle Schutzcontainer Zuordnungen für den angegebenen Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="0cc1c-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="0cc1c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cc1c-114">PARAMETERS</span></span>

### <span data-ttu-id="0cc1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc1c-115">-DefaultProfile</span></span>
<span data-ttu-id="0cc1c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0cc1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0cc1c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0cc1c-117">-Name</span></span>
<span data-ttu-id="0cc1c-118">Gibt den Namen der abzurufenden Schutzcontainer Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="0cc1c-118">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc1c-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0cc1c-119">-ProtectionContainer</span></span>
<span data-ttu-id="0cc1c-120">Erhalten Sie Schutzcontainer Zuordnungen, die dem angegebenen ASR-Schutzcontainer Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0cc1c-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cc1c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc1c-121">CommonParameters</span></span>
<span data-ttu-id="0cc1c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc1c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc1c-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cc1c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc1c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0cc1c-124">INPUTS</span></span>

### <span data-ttu-id="0cc1c-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0cc1c-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="0cc1c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0cc1c-126">OUTPUTS</span></span>

### <span data-ttu-id="0cc1c-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0cc1c-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="0cc1c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0cc1c-128">NOTES</span></span>

## <span data-ttu-id="0cc1c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0cc1c-129">RELATED LINKS</span></span>

[<span data-ttu-id="0cc1c-130">Neu – AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0cc1c-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="0cc1c-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0cc1c-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
