---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: c309b855b6ae8491e8b4a97301a902367a5377e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931504"
---
# <span data-ttu-id="bc1c7-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bc1c7-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="bc1c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc1c7-102">SYNOPSIS</span></span>
<span data-ttu-id="bc1c7-103">Ruft Informationen zu Websitewiederherstellungsnetzwerkzuordnungen für den aktuellen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="bc1c7-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="bc1c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc1c7-104">SYNTAX</span></span>

### <span data-ttu-id="bc1c7-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc1c7-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc1c7-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="bc1c7-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc1c7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc1c7-107">DESCRIPTION</span></span>
<span data-ttu-id="bc1c7-108">Das **Get-AzRecoveryServicesAsrNetworkMapping-Cmdlet** ruft Informationen zu Azure Site Recovery-Netzwerkzuordnungen für den Recovery Services-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="bc1c7-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="bc1c7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bc1c7-109">EXAMPLES</span></span>

### <span data-ttu-id="bc1c7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc1c7-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="bc1c7-111">Ruft alle Netzwerkzuordnungen für das übergebene Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="bc1c7-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="bc1c7-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bc1c7-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="bc1c7-113">Ruft die Netzwerkzuordnung mit dem angegebenen Namen in der angegebenen Azure-Websitewiederherstellungsstruktur ab.</span><span class="sxs-lookup"><span data-stu-id="bc1c7-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="bc1c7-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bc1c7-114">PARAMETERS</span></span>

### <span data-ttu-id="bc1c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc1c7-115">-DefaultProfile</span></span>
<span data-ttu-id="bc1c7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc1c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bc1c7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bc1c7-117">-Name</span></span>
<span data-ttu-id="bc1c7-118">Der Name des zu erhaltende ASR-Netzwerkzuordnungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="bc1c7-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="bc1c7-119">-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="bc1c7-119">-Network</span></span>
<span data-ttu-id="bc1c7-120">Holen Sie sich die ASR-Netzwerkzuordnungen, die dem angegebenen Netzwerk-ASR-Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bc1c7-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc1c7-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="bc1c7-121">-PrimaryFabric</span></span>
<span data-ttu-id="bc1c7-122">Holen Sie sich die ASR-Netzwerkzuordnungen, die dem angegebenen primären Fabricobjekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bc1c7-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc1c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc1c7-123">CommonParameters</span></span>
<span data-ttu-id="bc1c7-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc1c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc1c7-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc1c7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc1c7-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bc1c7-126">INPUTS</span></span>

### <span data-ttu-id="bc1c7-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="bc1c7-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="bc1c7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="bc1c7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="bc1c7-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bc1c7-129">OUTPUTS</span></span>

### <span data-ttu-id="bc1c7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bc1c7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="bc1c7-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bc1c7-131">NOTES</span></span>

## <span data-ttu-id="bc1c7-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bc1c7-132">RELATED LINKS</span></span>

[<span data-ttu-id="bc1c7-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bc1c7-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="bc1c7-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bc1c7-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
