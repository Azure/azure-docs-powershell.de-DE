---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: c9e41a6a4fa7a89db31304dc343da466e8632a74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149020"
---
# <span data-ttu-id="36282-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="36282-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="36282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36282-102">SYNOPSIS</span></span>
<span data-ttu-id="36282-103">Erstellen eines Speicherobjekts für CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="36282-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="36282-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36282-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="36282-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36282-105">DESCRIPTION</span></span>
<span data-ttu-id="36282-106">Erstellen eines Speicherobjekts für CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="36282-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="36282-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36282-107">EXAMPLES</span></span>

### <span data-ttu-id="36282-108">Beispiel 1: Erstellen eines Rollenprofileigenschaftenobjekts</span><span class="sxs-lookup"><span data-stu-id="36282-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="36282-109">Dieser Befehl erstellt ein Rollenprofileigenschaftenobjekt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36282-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="36282-110">Weitere Details finden Sie unter "New-AzCloudService".</span><span class="sxs-lookup"><span data-stu-id="36282-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="36282-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36282-111">PARAMETERS</span></span>

### <span data-ttu-id="36282-112">-Name</span><span class="sxs-lookup"><span data-stu-id="36282-112">-Name</span></span>
<span data-ttu-id="36282-113">Name des Rollenprofils.</span><span class="sxs-lookup"><span data-stu-id="36282-113">Name of role profile.</span></span>

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

### <span data-ttu-id="36282-114">-Sku1</span><span class="sxs-lookup"><span data-stu-id="36282-114">-SkuCapacity</span></span>
<span data-ttu-id="36282-115">Gibt die Anzahl der Rolleninstanzen im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="36282-115">Specifies the number of role instances in the cloud service.</span></span>

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

### <span data-ttu-id="36282-116">-SkuName</span><span class="sxs-lookup"><span data-stu-id="36282-116">-SkuName</span></span>
<span data-ttu-id="36282-117">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="36282-117">The sku name.</span></span>

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

### <span data-ttu-id="36282-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="36282-118">-SkuTier</span></span>
<span data-ttu-id="36282-119">SkuTier.</span><span class="sxs-lookup"><span data-stu-id="36282-119">SkuTier.</span></span>

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

### <span data-ttu-id="36282-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36282-120">CommonParameters</span></span>
<span data-ttu-id="36282-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36282-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36282-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36282-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36282-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36282-123">INPUTS</span></span>

## <span data-ttu-id="36282-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36282-124">OUTPUTS</span></span>

### <span data-ttu-id="36282-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="36282-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="36282-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36282-126">NOTES</span></span>

<span data-ttu-id="36282-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="36282-127">ALIASES</span></span>

## <span data-ttu-id="36282-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36282-128">RELATED LINKS</span></span>

