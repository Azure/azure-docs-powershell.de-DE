---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 588c00dc877c4e451a4d8a0c0b44ec001b0787ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824399"
---
# <span data-ttu-id="97d83-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="97d83-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="97d83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97d83-102">SYNOPSIS</span></span>
<span data-ttu-id="97d83-103">Ruft Azure Site Recovery Protection-Container Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="97d83-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="97d83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97d83-104">SYNTAX</span></span>

### <span data-ttu-id="97d83-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="97d83-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97d83-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="97d83-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97d83-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97d83-107">DESCRIPTION</span></span>
<span data-ttu-id="97d83-108">Das Cmdlet " **Get-AzRecoveryServicesAsrProtectionContainerMapping** " Ruft Informationen über den Schutzcontainer für Replikationsrichtlinien Zuordnungen (Association) im Tresor für den angegebenen ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="97d83-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="97d83-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97d83-109">EXAMPLES</span></span>

### <span data-ttu-id="97d83-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97d83-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="97d83-111">Liste der Schutzcontainer Zuordnungen für Container.</span><span class="sxs-lookup"><span data-stu-id="97d83-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="97d83-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="97d83-112">Example 2</span></span>
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

<span data-ttu-id="97d83-113">Ruft alle Schutzcontainer Zuordnungen für den angegebenen Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="97d83-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="97d83-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="97d83-114">PARAMETERS</span></span>

### <span data-ttu-id="97d83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97d83-115">-DefaultProfile</span></span>
<span data-ttu-id="97d83-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97d83-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="97d83-117">-Name</span><span class="sxs-lookup"><span data-stu-id="97d83-117">-Name</span></span>
<span data-ttu-id="97d83-118">Gibt den Namen der abzurufenden Schutzcontainer Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="97d83-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="97d83-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="97d83-119">-ProtectionContainer</span></span>
<span data-ttu-id="97d83-120">Erhalten Sie Schutzcontainer Zuordnungen, die dem angegebenen ASR-Schutzcontainer Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="97d83-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="97d83-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d83-121">CommonParameters</span></span>
<span data-ttu-id="97d83-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97d83-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d83-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97d83-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d83-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97d83-124">INPUTS</span></span>

### <span data-ttu-id="97d83-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="97d83-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="97d83-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97d83-126">OUTPUTS</span></span>

### <span data-ttu-id="97d83-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="97d83-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="97d83-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="97d83-128">NOTES</span></span>

## <span data-ttu-id="97d83-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97d83-129">RELATED LINKS</span></span>

[<span data-ttu-id="97d83-130">Neu – AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="97d83-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="97d83-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="97d83-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
