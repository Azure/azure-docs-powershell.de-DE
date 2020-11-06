---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
ms.openlocfilehash: bff748b8c867b272208469d34229cc2724bc8610
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480489"
---
# <span data-ttu-id="3d9b9-101">Get-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3d9b9-101">Get-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="3d9b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9b9-103">Abrufen oder Auflisten von Katalogbild Versionen</span><span class="sxs-lookup"><span data-stu-id="3d9b9-103">Get or list gallery image versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d9b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d9b9-104">SYNTAX</span></span>

### <span data-ttu-id="3d9b9-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d9b9-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d9b9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3d9b9-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d9b9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d9b9-107">DESCRIPTION</span></span>
<span data-ttu-id="3d9b9-108">Abrufen oder Auflisten von Katalogbild Versionen</span><span class="sxs-lookup"><span data-stu-id="3d9b9-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="3d9b9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d9b9-109">EXAMPLES</span></span>

### <span data-ttu-id="3d9b9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d9b9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="3d9b9-111">Holen Sie sich die Version des katalogbilds.</span><span class="sxs-lookup"><span data-stu-id="3d9b9-111">Get the gallery image version.</span></span>

## <span data-ttu-id="3d9b9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d9b9-112">PARAMETERS</span></span>

### <span data-ttu-id="3d9b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9b9-113">-DefaultProfile</span></span>
<span data-ttu-id="3d9b9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d9b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d9b9-115">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="3d9b9-115">-ExpandReplicationStatus</span></span>
<span data-ttu-id="3d9b9-116">Replikationsstatus anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d9b9-116">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9b9-117">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3d9b9-117">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="3d9b9-118">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="3d9b9-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9b9-119">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="3d9b9-119">-GalleryName</span></span>
<span data-ttu-id="3d9b9-120">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="3d9b9-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="3d9b9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3d9b9-121">-Name</span></span>
<span data-ttu-id="3d9b9-122">Der Name der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3d9b9-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d9b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d9b9-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3d9b9-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="3d9b9-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3d9b9-125">-ResourceId</span></span>
<span data-ttu-id="3d9b9-126">Die Ressourcen-ID für die Version des katalogbilds</span><span class="sxs-lookup"><span data-stu-id="3d9b9-126">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="3d9b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9b9-127">CommonParameters</span></span>
<span data-ttu-id="3d9b9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d9b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9b9-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d9b9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9b9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d9b9-130">INPUTS</span></span>

### <span data-ttu-id="3d9b9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3d9b9-131">System.String</span></span>

### <span data-ttu-id="3d9b9-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3d9b9-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="3d9b9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d9b9-133">OUTPUTS</span></span>

### <span data-ttu-id="3d9b9-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3d9b9-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="3d9b9-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d9b9-135">NOTES</span></span>

## <span data-ttu-id="3d9b9-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d9b9-136">RELATED LINKS</span></span>
