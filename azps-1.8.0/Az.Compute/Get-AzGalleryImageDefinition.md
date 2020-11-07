---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: 86da7a6f991bf7eeead14ad3414f9210eb7e175d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820771"
---
# <span data-ttu-id="81bcc-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="81bcc-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="81bcc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="81bcc-103">Abrufen oder Auflisten von Katalogbild Definitionen</span><span class="sxs-lookup"><span data-stu-id="81bcc-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="81bcc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81bcc-104">SYNTAX</span></span>

### <span data-ttu-id="81bcc-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="81bcc-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81bcc-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="81bcc-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81bcc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81bcc-107">DESCRIPTION</span></span>
<span data-ttu-id="81bcc-108">Abrufen oder Auflisten von Katalogbild Definitionen</span><span class="sxs-lookup"><span data-stu-id="81bcc-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="81bcc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81bcc-109">EXAMPLES</span></span>

### <span data-ttu-id="81bcc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81bcc-110">Example 1</span></span>
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

<span data-ttu-id="81bcc-111">Rufen Sie die Katalogbild Definition ab.</span><span class="sxs-lookup"><span data-stu-id="81bcc-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="81bcc-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="81bcc-112">Example 2</span></span>
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

<span data-ttu-id="81bcc-113">Rufen Sie die Katalogbild Definition ab, die mit "Bild" beginnt.</span><span class="sxs-lookup"><span data-stu-id="81bcc-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="81bcc-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="81bcc-114">Example 3</span></span>
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

<span data-ttu-id="81bcc-115">Rufen Sie die Katalogbild Definitionen in Gallery1 ab.</span><span class="sxs-lookup"><span data-stu-id="81bcc-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="81bcc-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="81bcc-116">PARAMETERS</span></span>

### <span data-ttu-id="81bcc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bcc-117">-DefaultProfile</span></span>
<span data-ttu-id="81bcc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81bcc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81bcc-119">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="81bcc-119">-GalleryName</span></span>
<span data-ttu-id="81bcc-120">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="81bcc-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="81bcc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="81bcc-121">-Name</span></span>
<span data-ttu-id="81bcc-122">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="81bcc-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="81bcc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81bcc-123">-ResourceGroupName</span></span>
<span data-ttu-id="81bcc-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81bcc-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="81bcc-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="81bcc-125">-ResourceId</span></span>
<span data-ttu-id="81bcc-126">Die Ressourcen-ID für die Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="81bcc-126">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="81bcc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bcc-127">CommonParameters</span></span>
<span data-ttu-id="81bcc-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81bcc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bcc-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81bcc-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bcc-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81bcc-130">INPUTS</span></span>

### <span data-ttu-id="81bcc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="81bcc-131">System.String</span></span>

## <span data-ttu-id="81bcc-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81bcc-132">OUTPUTS</span></span>

### <span data-ttu-id="81bcc-133">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="81bcc-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="81bcc-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="81bcc-134">NOTES</span></span>

## <span data-ttu-id="81bcc-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81bcc-135">RELATED LINKS</span></span>
