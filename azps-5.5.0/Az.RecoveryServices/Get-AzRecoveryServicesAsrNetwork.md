---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169297"
---
# <span data-ttu-id="f4024-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="f4024-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="f4024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4024-102">SYNOPSIS</span></span>
<span data-ttu-id="f4024-103">Ruft Informationen zu den Netzwerken ab, die von der Websitewiederherstellung für den aktuellen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="f4024-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="f4024-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4024-104">SYNTAX</span></span>

### <span data-ttu-id="f4024-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4024-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4024-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f4024-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4024-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f4024-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4024-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4024-108">DESCRIPTION</span></span>
<span data-ttu-id="f4024-109">Das **Cmdlet "Get-AzRecoveryServicesAsrNetwork"** ruft Informationen zu Azure Site Recovery Networks für den aktuellen Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="f4024-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f4024-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4024-110">EXAMPLES</span></span>

### <span data-ttu-id="f4024-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4024-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="f4024-112">Gets all known networks in the specified fabric.</span><span class="sxs-lookup"><span data-stu-id="f4024-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="f4024-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4024-113">PARAMETERS</span></span>

### <span data-ttu-id="f4024-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4024-114">-DefaultProfile</span></span>
<span data-ttu-id="f4024-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4024-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f4024-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="f4024-116">-Fabric</span></span>
<span data-ttu-id="f4024-117">ASR fabric object</span><span class="sxs-lookup"><span data-stu-id="f4024-117">ASR fabric object</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4024-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f4024-118">-FriendlyName</span></span>
<span data-ttu-id="f4024-119">Anzeigename des Netzwerk-ASR-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f4024-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="f4024-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f4024-120">-Name</span></span>
<span data-ttu-id="f4024-121">Name des Netzwerk-ASR-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f4024-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="f4024-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4024-122">CommonParameters</span></span>
<span data-ttu-id="f4024-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4024-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4024-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4024-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4024-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4024-125">INPUTS</span></span>

### <span data-ttu-id="f4024-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f4024-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f4024-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4024-127">OUTPUTS</span></span>

### <span data-ttu-id="f4024-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="f4024-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="f4024-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f4024-129">NOTES</span></span>

## <span data-ttu-id="f4024-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f4024-130">RELATED LINKS</span></span>
