---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169308"
---
# <span data-ttu-id="a27a2-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="a27a2-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="a27a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a27a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a27a2-103">Erhalten Sie die Details eines Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="a27a2-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="a27a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a27a2-104">SYNTAX</span></span>

### <span data-ttu-id="a27a2-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="a27a2-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a27a2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a27a2-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a27a2-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a27a2-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a27a2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a27a2-108">DESCRIPTION</span></span>
<span data-ttu-id="a27a2-109">Das **Get-AzRecoveryServicesAsrFabric-Cmdlet** ruft die Eigenschaften eines angegebenen Azure Site Recovery Fabric oder aller Azure Site Recovery Recovery In a Recovery Service Vault ab.</span><span class="sxs-lookup"><span data-stu-id="a27a2-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="a27a2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a27a2-110">EXAMPLES</span></span>

### <span data-ttu-id="a27a2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a27a2-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="a27a2-112">Gibt alle Azure Site Recovery-Dienste im Tresor zurück.</span><span class="sxs-lookup"><span data-stu-id="a27a2-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="a27a2-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a27a2-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="a27a2-114">Return azure site recovery fabric with name xxxx.</span><span class="sxs-lookup"><span data-stu-id="a27a2-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="a27a2-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a27a2-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="a27a2-116">Return azure site recovery fabric with friendly name xxxx.</span><span class="sxs-lookup"><span data-stu-id="a27a2-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="a27a2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a27a2-117">PARAMETERS</span></span>

### <span data-ttu-id="a27a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27a2-118">-DefaultProfile</span></span>
<span data-ttu-id="a27a2-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a27a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a27a2-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a27a2-120">-FriendlyName</span></span>
<span data-ttu-id="a27a2-121">Suchen Sie nach dem ASR-Fabric unter dem Anzeigenamen des Fabriks.</span><span class="sxs-lookup"><span data-stu-id="a27a2-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="a27a2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a27a2-122">-Name</span></span>
<span data-ttu-id="a27a2-123">Search for the ASR fabric by the name of the fabric.</span><span class="sxs-lookup"><span data-stu-id="a27a2-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="a27a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27a2-124">CommonParameters</span></span>
<span data-ttu-id="a27a2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a27a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27a2-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a27a2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27a2-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a27a2-127">INPUTS</span></span>

### <span data-ttu-id="a27a2-128">Keine</span><span class="sxs-lookup"><span data-stu-id="a27a2-128">None</span></span>

## <span data-ttu-id="a27a2-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a27a2-129">OUTPUTS</span></span>

### <span data-ttu-id="a27a2-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a27a2-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="a27a2-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a27a2-131">NOTES</span></span>

## <span data-ttu-id="a27a2-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a27a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="a27a2-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="a27a2-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="a27a2-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="a27a2-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
