---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: eb358a0caf2b1ea5ccba8d92c39562d2c39706c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941043"
---
# <span data-ttu-id="0305a-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="0305a-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="0305a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0305a-102">SYNOPSIS</span></span>
<span data-ttu-id="0305a-103">Ruft Details der vCenter-Server ab, die für die Ermittlung auf dem vom ASR-Fabric angegebenen Konfigurationsserver registriert sind.</span><span class="sxs-lookup"><span data-stu-id="0305a-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="0305a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0305a-104">SYNTAX</span></span>

### <span data-ttu-id="0305a-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="0305a-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0305a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0305a-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0305a-107">ByName</span><span class="sxs-lookup"><span data-stu-id="0305a-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0305a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0305a-108">DESCRIPTION</span></span>
<span data-ttu-id="0305a-109">Das **Get-AzRecoveryServicesAsrvCenter-Cmdlet** ruft Details der vCenter-Server ab, die für die Ermittlung auf dem von der ASR-Fabric angegebenen Konfigurationsserver registriert sind.</span><span class="sxs-lookup"><span data-stu-id="0305a-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="0305a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0305a-110">EXAMPLES</span></span>

### <span data-ttu-id="0305a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0305a-111">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="0305a-112">Holen Sie sich azure site recovery vCenter nach Fabricname und Name von vCenter.</span><span class="sxs-lookup"><span data-stu-id="0305a-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="0305a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0305a-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="0305a-114">Holen Sie sich die vCenter-Liste der Azure-Websitewiederherstellung nach Fabricname.</span><span class="sxs-lookup"><span data-stu-id="0305a-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="0305a-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0305a-115">PARAMETERS</span></span>

### <span data-ttu-id="0305a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0305a-116">-DefaultProfile</span></span>
<span data-ttu-id="0305a-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0305a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0305a-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="0305a-118">-Fabric</span></span>
<span data-ttu-id="0305a-119">ASR-Fabricobjekt, das den Konfigurationsserver darstellt.</span><span class="sxs-lookup"><span data-stu-id="0305a-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0305a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0305a-120">-Name</span></span>
<span data-ttu-id="0305a-121">Name des vCenter-Servers.</span><span class="sxs-lookup"><span data-stu-id="0305a-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="0305a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0305a-122">-ResourceId</span></span>
<span data-ttu-id="0305a-123">Gibt die resourceId von vCenter an.</span><span class="sxs-lookup"><span data-stu-id="0305a-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0305a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0305a-124">CommonParameters</span></span>
<span data-ttu-id="0305a-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0305a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0305a-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0305a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0305a-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0305a-127">INPUTS</span></span>

### <span data-ttu-id="0305a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0305a-128">System.String</span></span>

### <span data-ttu-id="0305a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="0305a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="0305a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0305a-130">OUTPUTS</span></span>

### <span data-ttu-id="0305a-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="0305a-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="0305a-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0305a-132">NOTES</span></span>

## <span data-ttu-id="0305a-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0305a-133">RELATED LINKS</span></span>
