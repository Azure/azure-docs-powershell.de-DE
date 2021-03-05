---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 1aeaba2f4f25abd49f12d087b7390f5e92f19c3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950691"
---
# <span data-ttu-id="361a5-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="361a5-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="361a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="361a5-102">SYNOPSIS</span></span>
<span data-ttu-id="361a5-103">Hier erhalten Sie die Details zu einem Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="361a5-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="361a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="361a5-104">SYNTAX</span></span>

### <span data-ttu-id="361a5-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="361a5-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="361a5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="361a5-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="361a5-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="361a5-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="361a5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="361a5-108">DESCRIPTION</span></span>
<span data-ttu-id="361a5-109">Das **Get-AzRecoveryServicesAsrFabric-Cmdlet** ruft die Eigenschaften eines angegebenen Azure Site Recovery Fabrics oder aller Azure Site Recovery -Fabrics in einem Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="361a5-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="361a5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="361a5-110">EXAMPLES</span></span>

### <span data-ttu-id="361a5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="361a5-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="361a5-112">Gibt alle Azure Site Recovery-Materialien im Tresor zurück.</span><span class="sxs-lookup"><span data-stu-id="361a5-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="361a5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="361a5-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="361a5-114">Geben Sie azure site recovery fabric mit dem Namen xxxx zurück.</span><span class="sxs-lookup"><span data-stu-id="361a5-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="361a5-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="361a5-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="361a5-116">Geben Sie azure site recovery fabric mit dem Anzeigenamen xxxx zurück.</span><span class="sxs-lookup"><span data-stu-id="361a5-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="361a5-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="361a5-117">PARAMETERS</span></span>

### <span data-ttu-id="361a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="361a5-118">-DefaultProfile</span></span>
<span data-ttu-id="361a5-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="361a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="361a5-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="361a5-120">-FriendlyName</span></span>
<span data-ttu-id="361a5-121">Suchen Sie nach dem ASR-Stoff unter dem Anzeigenamen des Fabrics.</span><span class="sxs-lookup"><span data-stu-id="361a5-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="361a5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="361a5-122">-Name</span></span>
<span data-ttu-id="361a5-123">Suchen Sie nach dem ASR-Fabric nach dem Namen des Fabrics.</span><span class="sxs-lookup"><span data-stu-id="361a5-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="361a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="361a5-124">CommonParameters</span></span>
<span data-ttu-id="361a5-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="361a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="361a5-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="361a5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="361a5-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="361a5-127">INPUTS</span></span>

### <span data-ttu-id="361a5-128">Keine</span><span class="sxs-lookup"><span data-stu-id="361a5-128">None</span></span>

## <span data-ttu-id="361a5-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="361a5-129">OUTPUTS</span></span>

### <span data-ttu-id="361a5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="361a5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="361a5-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="361a5-131">NOTES</span></span>

## <span data-ttu-id="361a5-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="361a5-132">RELATED LINKS</span></span>

[<span data-ttu-id="361a5-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="361a5-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="361a5-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="361a5-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
