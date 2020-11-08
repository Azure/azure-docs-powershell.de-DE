---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003646"
---
# <span data-ttu-id="add66-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="add66-101">Get-AzGallery</span></span>

## <span data-ttu-id="add66-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="add66-102">SYNOPSIS</span></span>
<span data-ttu-id="add66-103">Abrufen oder Auflisten von Katalogen</span><span class="sxs-lookup"><span data-stu-id="add66-103">Get or list galleries.</span></span>

## <span data-ttu-id="add66-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="add66-104">SYNTAX</span></span>

### <span data-ttu-id="add66-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="add66-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="add66-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="add66-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="add66-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="add66-107">DESCRIPTION</span></span>
<span data-ttu-id="add66-108">Abrufen oder Auflisten von Katalogen</span><span class="sxs-lookup"><span data-stu-id="add66-108">Get or list galleries.</span></span>

## <span data-ttu-id="add66-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="add66-109">EXAMPLES</span></span>

### <span data-ttu-id="add66-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="add66-110">Example 1</span></span>
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

<span data-ttu-id="add66-111">Holen Sie sich die Galerie "Gallery1"</span><span class="sxs-lookup"><span data-stu-id="add66-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="add66-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="add66-112">Example 2</span></span>
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

<span data-ttu-id="add66-113">Abrufen aller Kataloge in RG1</span><span class="sxs-lookup"><span data-stu-id="add66-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="add66-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="add66-114">Example 3</span></span>
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

<span data-ttu-id="add66-115">Alle Kataloge im Abonnement abrufen.</span><span class="sxs-lookup"><span data-stu-id="add66-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="add66-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="add66-116">Example 4</span></span>
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

<span data-ttu-id="add66-117">Rufen Sie alle Kataloge im Abonnement ab, die mit "Gallery" beginnen.</span><span class="sxs-lookup"><span data-stu-id="add66-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="add66-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="add66-118">PARAMETERS</span></span>

### <span data-ttu-id="add66-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add66-119">-DefaultProfile</span></span>
<span data-ttu-id="add66-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="add66-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="add66-121">-Name</span><span class="sxs-lookup"><span data-stu-id="add66-121">-Name</span></span>
<span data-ttu-id="add66-122">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="add66-122">The name of the gallery.</span></span>

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

### <span data-ttu-id="add66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add66-123">-ResourceGroupName</span></span>
<span data-ttu-id="add66-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="add66-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="add66-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="add66-125">-ResourceId</span></span>
<span data-ttu-id="add66-126">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="add66-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="add66-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add66-127">CommonParameters</span></span>
<span data-ttu-id="add66-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add66-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add66-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="add66-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add66-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="add66-130">INPUTS</span></span>

### <span data-ttu-id="add66-131">System. String</span><span class="sxs-lookup"><span data-stu-id="add66-131">System.String</span></span>

## <span data-ttu-id="add66-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="add66-132">OUTPUTS</span></span>

### <span data-ttu-id="add66-133">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="add66-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="add66-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="add66-134">NOTES</span></span>

## <span data-ttu-id="add66-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="add66-135">RELATED LINKS</span></span>
