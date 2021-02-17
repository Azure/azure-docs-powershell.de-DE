---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: c6c689ce2c9ccda71150f221bdea4ae5dd2a20fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176017"
---
# <span data-ttu-id="df023-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="df023-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="df023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df023-102">SYNOPSIS</span></span>
<span data-ttu-id="df023-103">Bilddefinitionen für "Get" oder "List Gallery"</span><span class="sxs-lookup"><span data-stu-id="df023-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="df023-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df023-104">SYNTAX</span></span>

### <span data-ttu-id="df023-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="df023-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df023-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="df023-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df023-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df023-107">DESCRIPTION</span></span>
<span data-ttu-id="df023-108">Bilddefinitionen für "Get" oder "List Gallery"</span><span class="sxs-lookup"><span data-stu-id="df023-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="df023-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="df023-109">EXAMPLES</span></span>

### <span data-ttu-id="df023-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df023-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="df023-111">Hier erhalten Sie die Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="df023-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="df023-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="df023-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image*

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="df023-113">Erhalten Sie die Katalogbilddefinition, die mit "image" beginnt.</span><span class="sxs-lookup"><span data-stu-id="df023-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="df023-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="df023-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="df023-115">Holen Sie sich die Katalogbilddefinitionen in "gallery1".</span><span class="sxs-lookup"><span data-stu-id="df023-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="df023-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df023-116">PARAMETERS</span></span>

### <span data-ttu-id="df023-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df023-117">-DefaultProfile</span></span>
<span data-ttu-id="df023-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df023-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df023-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="df023-119">-GalleryName</span></span>
<span data-ttu-id="df023-120">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="df023-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df023-121">-Name</span><span class="sxs-lookup"><span data-stu-id="df023-121">-Name</span></span>
<span data-ttu-id="df023-122">Der Name der Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="df023-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="df023-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df023-123">-ResourceGroupName</span></span>
<span data-ttu-id="df023-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="df023-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df023-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df023-125">-ResourceId</span></span>
<span data-ttu-id="df023-126">Die Ressourcen-ID für die Bilddefinition des Katalogs</span><span class="sxs-lookup"><span data-stu-id="df023-126">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="df023-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df023-127">CommonParameters</span></span>
<span data-ttu-id="df023-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df023-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df023-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df023-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df023-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="df023-130">INPUTS</span></span>

### <span data-ttu-id="df023-131">System.String</span><span class="sxs-lookup"><span data-stu-id="df023-131">System.String</span></span>

## <span data-ttu-id="df023-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="df023-132">OUTPUTS</span></span>

### <span data-ttu-id="df023-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="df023-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="df023-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="df023-134">NOTES</span></span>

## <span data-ttu-id="df023-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="df023-135">RELATED LINKS</span></span>
