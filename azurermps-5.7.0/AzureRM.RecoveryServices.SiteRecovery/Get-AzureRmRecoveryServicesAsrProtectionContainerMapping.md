---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 5d0d6bc894cd252ac36b4ceee312040a998b3857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481034"
---
# <span data-ttu-id="f6a15-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f6a15-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="f6a15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6a15-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a15-103">Ruft Azure Site Recovery Protection-Container Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="f6a15-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6a15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6a15-104">SYNTAX</span></span>

### <span data-ttu-id="f6a15-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6a15-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6a15-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f6a15-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a15-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6a15-107">DESCRIPTION</span></span>
<span data-ttu-id="f6a15-108">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** " Ruft Informationen über den Schutzcontainer für Replikationsrichtlinien Zuordnungen (Association) im Tresor für den angegebenen ASR-Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="f6a15-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="f6a15-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6a15-109">EXAMPLES</span></span>

### <span data-ttu-id="f6a15-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6a15-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="f6a15-111">Liste der Schutzcontainer Zuordnungen für Container.</span><span class="sxs-lookup"><span data-stu-id="f6a15-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="f6a15-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f6a15-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

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

<span data-ttu-id="f6a15-113">Ruft alle Schutzcontainer Zuordnungen für den angegebenen Schutzcontainer ab.</span><span class="sxs-lookup"><span data-stu-id="f6a15-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="f6a15-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6a15-114">PARAMETERS</span></span>

### <span data-ttu-id="f6a15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a15-115">-DefaultProfile</span></span>
<span data-ttu-id="f6a15-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6a15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="f6a15-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f6a15-117">-Name</span></span>
<span data-ttu-id="f6a15-118">Gibt den Namen der abzurufenden Schutzcontainer Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="f6a15-118">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a15-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f6a15-119">-ProtectionContainer</span></span>
<span data-ttu-id="f6a15-120">Erhalten Sie Schutzcontainer Zuordnungen, die dem angegebenen ASR-Schutzcontainer Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f6a15-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a15-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a15-121">CommonParameters</span></span>
<span data-ttu-id="f6a15-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6a15-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a15-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a15-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a15-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6a15-124">INPUTS</span></span>

### <span data-ttu-id="f6a15-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f6a15-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="f6a15-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6a15-126">OUTPUTS</span></span>

### <span data-ttu-id="f6a15-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f6a15-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f6a15-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6a15-128">NOTES</span></span>

## <span data-ttu-id="f6a15-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6a15-129">RELATED LINKS</span></span>

[<span data-ttu-id="f6a15-130">Neu – AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f6a15-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="f6a15-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f6a15-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
