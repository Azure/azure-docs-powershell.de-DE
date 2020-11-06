---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 75d30165c5dc5d69eabd08e89ad2577df82f7ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480490"
---
# <span data-ttu-id="96491-101">Get-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="96491-101">Get-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="96491-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96491-102">SYNOPSIS</span></span>
<span data-ttu-id="96491-103">Abrufen oder Auflisten von Katalogbild Definitionen</span><span class="sxs-lookup"><span data-stu-id="96491-103">Get or list gallery image definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96491-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96491-104">SYNTAX</span></span>

### <span data-ttu-id="96491-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="96491-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96491-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="96491-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96491-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96491-107">DESCRIPTION</span></span>
<span data-ttu-id="96491-108">Abrufen oder Auflisten von Katalogbild Definitionen</span><span class="sxs-lookup"><span data-stu-id="96491-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="96491-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96491-109">EXAMPLES</span></span>

### <span data-ttu-id="96491-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="96491-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image
```

<span data-ttu-id="96491-111">Rufen Sie die Katalogbild Definition ab.</span><span class="sxs-lookup"><span data-stu-id="96491-111">Get the gallery image definition.</span></span>

## <span data-ttu-id="96491-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="96491-112">PARAMETERS</span></span>

### <span data-ttu-id="96491-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96491-113">-DefaultProfile</span></span>
<span data-ttu-id="96491-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96491-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96491-115">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="96491-115">-GalleryName</span></span>
<span data-ttu-id="96491-116">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="96491-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="96491-117">-Name</span><span class="sxs-lookup"><span data-stu-id="96491-117">-Name</span></span>
<span data-ttu-id="96491-118">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="96491-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96491-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96491-119">-ResourceGroupName</span></span>
<span data-ttu-id="96491-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="96491-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="96491-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="96491-121">-ResourceId</span></span>
<span data-ttu-id="96491-122">Die Ressourcen-ID für die Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="96491-122">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="96491-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96491-123">CommonParameters</span></span>
<span data-ttu-id="96491-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96491-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96491-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96491-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96491-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96491-126">INPUTS</span></span>

### <span data-ttu-id="96491-127">System. String</span><span class="sxs-lookup"><span data-stu-id="96491-127">System.String</span></span>

## <span data-ttu-id="96491-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96491-128">OUTPUTS</span></span>

### <span data-ttu-id="96491-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="96491-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="96491-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="96491-130">NOTES</span></span>

## <span data-ttu-id="96491-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96491-131">RELATED LINKS</span></span>
