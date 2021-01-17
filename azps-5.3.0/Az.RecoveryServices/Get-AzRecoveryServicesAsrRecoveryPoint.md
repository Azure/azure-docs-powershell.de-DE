---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470374"
---
# <span data-ttu-id="116c3-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="116c3-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="116c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="116c3-102">SYNOPSIS</span></span>
<span data-ttu-id="116c3-103">Ruft die verfügbaren Wiederherstellungspunkte für ein replikationsgeschütztes Element ab.</span><span class="sxs-lookup"><span data-stu-id="116c3-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="116c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="116c3-104">SYNTAX</span></span>

### <span data-ttu-id="116c3-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="116c3-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="116c3-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="116c3-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="116c3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="116c3-107">DESCRIPTION</span></span>
<span data-ttu-id="116c3-108">Das **Cmdlet "Get-AzRecoveryServicesAsrRecoveryPoint"** ruft die Liste der verfügbaren Wiederherstellungspunkte für ein replikationsgeschütztes Element ab.</span><span class="sxs-lookup"><span data-stu-id="116c3-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="116c3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="116c3-109">EXAMPLES</span></span>

### <span data-ttu-id="116c3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="116c3-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="116c3-111">Ruft Wiederherstellungspunkte für das angegebene asR-replikationsgeschützte Element ab.</span><span class="sxs-lookup"><span data-stu-id="116c3-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="116c3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="116c3-112">PARAMETERS</span></span>

### <span data-ttu-id="116c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116c3-113">-DefaultProfile</span></span>
<span data-ttu-id="116c3-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="116c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="116c3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="116c3-115">-Name</span></span>
<span data-ttu-id="116c3-116">Gibt den Namen des wiederherstellungspunkts an, den Sie erhalten müssen.</span><span class="sxs-lookup"><span data-stu-id="116c3-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="116c3-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="116c3-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="116c3-118">Gibt das Geschützte Elementobjekt für die Azure-Websitewiederherstellungsreplikation an, für das die Liste der verfügbaren Wiederherstellungspunkte angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="116c3-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="116c3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116c3-119">CommonParameters</span></span>
<span data-ttu-id="116c3-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="116c3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116c3-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="116c3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116c3-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="116c3-122">INPUTS</span></span>

### <span data-ttu-id="116c3-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="116c3-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="116c3-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="116c3-124">OUTPUTS</span></span>

### <span data-ttu-id="116c3-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="116c3-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="116c3-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="116c3-126">NOTES</span></span>

## <span data-ttu-id="116c3-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="116c3-127">RELATED LINKS</span></span>

[<span data-ttu-id="116c3-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="116c3-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="116c3-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="116c3-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="116c3-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="116c3-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="116c3-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="116c3-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="116c3-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="116c3-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
