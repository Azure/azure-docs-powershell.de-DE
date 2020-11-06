---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
ms.openlocfilehash: cdb703144daa6f9abd62aee41eaad94b2cfa50e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480505"
---
# <span data-ttu-id="97f0c-101">Get-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="97f0c-101">Get-AzureRmGallery</span></span>

## <span data-ttu-id="97f0c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="97f0c-103">Abrufen oder Auflisten von Katalogen</span><span class="sxs-lookup"><span data-stu-id="97f0c-103">Get or list galleries.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97f0c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97f0c-104">SYNTAX</span></span>

### <span data-ttu-id="97f0c-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="97f0c-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGallery [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97f0c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="97f0c-106">ResourceIdParameter</span></span>
```
Get-AzureRmGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97f0c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97f0c-107">DESCRIPTION</span></span>
<span data-ttu-id="97f0c-108">Abrufen oder Auflisten von Katalogen</span><span class="sxs-lookup"><span data-stu-id="97f0c-108">Get or list galleries.</span></span>

## <span data-ttu-id="97f0c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97f0c-109">EXAMPLES</span></span>

### <span data-ttu-id="97f0c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97f0c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName

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

<span data-ttu-id="97f0c-111">Abrufen des Katalogs</span><span class="sxs-lookup"><span data-stu-id="97f0c-111">Get the gallery.</span></span>

## <span data-ttu-id="97f0c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="97f0c-112">PARAMETERS</span></span>

### <span data-ttu-id="97f0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f0c-113">-DefaultProfile</span></span>
<span data-ttu-id="97f0c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97f0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97f0c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="97f0c-115">-Name</span></span>
<span data-ttu-id="97f0c-116">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="97f0c-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f0c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97f0c-117">-ResourceGroupName</span></span>
<span data-ttu-id="97f0c-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="97f0c-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97f0c-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="97f0c-119">-ResourceId</span></span>
<span data-ttu-id="97f0c-120">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="97f0c-120">The resource id for Gallery</span></span>

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

### <span data-ttu-id="97f0c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f0c-121">CommonParameters</span></span>
<span data-ttu-id="97f0c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f0c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f0c-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f0c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f0c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97f0c-124">INPUTS</span></span>

### <span data-ttu-id="97f0c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="97f0c-125">System.String</span></span>

### <span data-ttu-id="97f0c-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="97f0c-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="97f0c-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97f0c-127">OUTPUTS</span></span>

### <span data-ttu-id="97f0c-128">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="97f0c-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="97f0c-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="97f0c-129">NOTES</span></span>

## <span data-ttu-id="97f0c-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97f0c-130">RELATED LINKS</span></span>
