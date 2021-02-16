---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145009"
---
# <span data-ttu-id="b3d01-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="b3d01-101">Get-AzGallery</span></span>

## <span data-ttu-id="b3d01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3d01-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d01-103">Sie können Kataloge von "Get" oder "List" erstellen.</span><span class="sxs-lookup"><span data-stu-id="b3d01-103">Get or list galleries.</span></span>

## <span data-ttu-id="b3d01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3d01-104">SYNTAX</span></span>

### <span data-ttu-id="b3d01-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3d01-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3d01-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b3d01-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3d01-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3d01-107">DESCRIPTION</span></span>
<span data-ttu-id="b3d01-108">Sie können Kataloge von "Get" oder "List" erstellen.</span><span class="sxs-lookup"><span data-stu-id="b3d01-108">Get or list galleries.</span></span>

## <span data-ttu-id="b3d01-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3d01-109">EXAMPLES</span></span>

### <span data-ttu-id="b3d01-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3d01-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="b3d01-111">Katalog "Gallery1" erhalten</span><span class="sxs-lookup"><span data-stu-id="b3d01-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="b3d01-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b3d01-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="b3d01-113">Alle Kataloge in rg1 erhalten.</span><span class="sxs-lookup"><span data-stu-id="b3d01-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="b3d01-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b3d01-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="b3d01-115">Holen Sie sich alle Kataloge im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3d01-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="b3d01-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="b3d01-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="b3d01-117">Erhalten Sie alle Kataloge im Abonnement, die mit "Gallery" beginnen.</span><span class="sxs-lookup"><span data-stu-id="b3d01-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="b3d01-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3d01-118">PARAMETERS</span></span>

### <span data-ttu-id="b3d01-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d01-119">-DefaultProfile</span></span>
<span data-ttu-id="b3d01-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3d01-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d01-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b3d01-121">-Name</span></span>
<span data-ttu-id="b3d01-122">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="b3d01-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b3d01-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d01-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3d01-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3d01-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b3d01-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3d01-125">-ResourceId</span></span>
<span data-ttu-id="b3d01-126">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="b3d01-126">The resource id for Gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d01-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d01-127">CommonParameters</span></span>
<span data-ttu-id="b3d01-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d01-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d01-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3d01-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d01-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3d01-130">INPUTS</span></span>

### <span data-ttu-id="b3d01-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b3d01-131">System.String</span></span>

## <span data-ttu-id="b3d01-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3d01-132">OUTPUTS</span></span>

### <span data-ttu-id="b3d01-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="b3d01-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="b3d01-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3d01-134">NOTES</span></span>

## <span data-ttu-id="b3d01-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3d01-135">RELATED LINKS</span></span>
