---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364761"
---
# <span data-ttu-id="dfe63-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="dfe63-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="dfe63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe63-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe63-103">Ruft Informationen zu Websitewiederherstellungsnetzwerkzuordnungen für den aktuellen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="dfe63-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="dfe63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfe63-104">SYNTAX</span></span>

### <span data-ttu-id="dfe63-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="dfe63-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfe63-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="dfe63-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfe63-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfe63-107">DESCRIPTION</span></span>
<span data-ttu-id="dfe63-108">Das **Cmdlet "Get-AzRecoveryServicesAsrNetworkMapping"** ruft Informationen zu Azure Site Recovery-Netzwerkzuordnungen für den Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="dfe63-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="dfe63-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dfe63-109">EXAMPLES</span></span>

### <span data-ttu-id="dfe63-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dfe63-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="dfe63-111">Ruft alle Netzwerkzuordnungen für das übergebene Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="dfe63-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="dfe63-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dfe63-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="dfe63-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span><span class="sxs-lookup"><span data-stu-id="dfe63-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="dfe63-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfe63-114">PARAMETERS</span></span>

### <span data-ttu-id="dfe63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe63-115">-DefaultProfile</span></span>
<span data-ttu-id="dfe63-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfe63-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dfe63-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dfe63-117">-Name</span></span>
<span data-ttu-id="dfe63-118">Der Name des zu erhaltende ASR-Netzwerkzuordnungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="dfe63-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="dfe63-119">-Network</span><span class="sxs-lookup"><span data-stu-id="dfe63-119">-Network</span></span>
<span data-ttu-id="dfe63-120">Holen Sie sich die ASR-Netzwerkzuordnungen, die dem angegebenen Netzwerk-ASR-Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="dfe63-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="dfe63-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="dfe63-121">-PrimaryFabric</span></span>
<span data-ttu-id="dfe63-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span><span class="sxs-lookup"><span data-stu-id="dfe63-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="dfe63-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe63-123">CommonParameters</span></span>
<span data-ttu-id="dfe63-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe63-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe63-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfe63-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe63-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dfe63-126">INPUTS</span></span>

### <span data-ttu-id="dfe63-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="dfe63-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="dfe63-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="dfe63-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="dfe63-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dfe63-129">OUTPUTS</span></span>

### <span data-ttu-id="dfe63-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="dfe63-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="dfe63-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dfe63-131">NOTES</span></span>

## <span data-ttu-id="dfe63-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dfe63-132">RELATED LINKS</span></span>

[<span data-ttu-id="dfe63-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="dfe63-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="dfe63-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="dfe63-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
