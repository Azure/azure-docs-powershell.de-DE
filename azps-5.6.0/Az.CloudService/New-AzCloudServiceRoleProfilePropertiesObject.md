---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: 6eec8f849d555fd2bf71f564c2e5c3ed9c699d80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932016"
---
# <span data-ttu-id="d6864-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="d6864-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="d6864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6864-102">SYNOPSIS</span></span>
<span data-ttu-id="d6864-103">Erstellen eines Speicherobjekts für CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="d6864-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="d6864-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6864-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="d6864-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6864-105">DESCRIPTION</span></span>
<span data-ttu-id="d6864-106">Erstellen eines Speicherobjekts für CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="d6864-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="d6864-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d6864-107">EXAMPLES</span></span>

### <span data-ttu-id="d6864-108">Beispiel 1: Erstellen eines Rollenprofileigenschaftenobjekts</span><span class="sxs-lookup"><span data-stu-id="d6864-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="d6864-109">Mit diesem Befehl wird ein Rollenprofileigenschaftenobjekt erstellt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6864-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="d6864-110">Weitere Informationen finden Sie unter New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="d6864-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="d6864-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d6864-111">PARAMETERS</span></span>

### <span data-ttu-id="d6864-112">-Name</span><span class="sxs-lookup"><span data-stu-id="d6864-112">-Name</span></span>
<span data-ttu-id="d6864-113">Name des Rollenprofils.</span><span class="sxs-lookup"><span data-stu-id="d6864-113">Name of role profile.</span></span>

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

### <span data-ttu-id="d6864-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d6864-114">-SkuCapacity</span></span>
<span data-ttu-id="d6864-115">Gibt die Anzahl der Rolleninstanzen im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="d6864-115">Specifies the number of role instances in the cloud service.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6864-116">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d6864-116">-SkuName</span></span>
<span data-ttu-id="d6864-117">Der Name der Sku.</span><span class="sxs-lookup"><span data-stu-id="d6864-117">The sku name.</span></span>

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

### <span data-ttu-id="d6864-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d6864-118">-SkuTier</span></span>
<span data-ttu-id="d6864-119">SkuTier.</span><span class="sxs-lookup"><span data-stu-id="d6864-119">SkuTier.</span></span>

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

### <span data-ttu-id="d6864-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6864-120">CommonParameters</span></span>
<span data-ttu-id="d6864-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6864-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6864-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6864-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6864-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d6864-123">INPUTS</span></span>

## <span data-ttu-id="d6864-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d6864-124">OUTPUTS</span></span>

### <span data-ttu-id="d6864-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="d6864-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="d6864-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d6864-126">NOTES</span></span>

<span data-ttu-id="d6864-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d6864-127">ALIASES</span></span>

## <span data-ttu-id="d6864-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d6864-128">RELATED LINKS</span></span>

