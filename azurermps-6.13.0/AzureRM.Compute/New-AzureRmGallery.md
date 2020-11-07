---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGallery.md
ms.openlocfilehash: bb743768654dcaeec9a39e7b590abe71b155cc17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664894"
---
# <span data-ttu-id="bd8f6-101">New-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="bd8f6-101">New-AzureRmGallery</span></span>

## <span data-ttu-id="bd8f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8f6-103">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="bd8f6-103">Create a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd8f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd8f6-104">SYNTAX</span></span>

```
New-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd8f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd8f6-105">DESCRIPTION</span></span>
<span data-ttu-id="bd8f6-106">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="bd8f6-106">Create a gallery.</span></span>

## <span data-ttu-id="bd8f6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd8f6-107">EXAMPLES</span></span>

### <span data-ttu-id="bd8f6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd8f6-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="bd8f6-109">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="bd8f6-109">Create a gallery.</span></span>

## <span data-ttu-id="bd8f6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd8f6-110">PARAMETERS</span></span>

### <span data-ttu-id="bd8f6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd8f6-111">-AsJob</span></span>
<span data-ttu-id="bd8f6-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bd8f6-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd8f6-113">-DefaultProfile</span></span>
<span data-ttu-id="bd8f6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd8f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd8f6-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd8f6-115">-Description</span></span>
<span data-ttu-id="bd8f6-116">Die Beschreibung der Katalog Ressource.</span><span class="sxs-lookup"><span data-stu-id="bd8f6-116">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f6-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="bd8f6-117">-Location</span></span>
<span data-ttu-id="bd8f6-118">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="bd8f6-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bd8f6-119">-Name</span></span>
<span data-ttu-id="bd8f6-120">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="bd8f6-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd8f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="bd8f6-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bd8f6-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f6-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd8f6-123">-Tag</span></span>
<span data-ttu-id="bd8f6-124">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="bd8f6-124">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f6-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd8f6-125">-Confirm</span></span>
<span data-ttu-id="bd8f6-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd8f6-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd8f6-127">-WhatIf</span></span>
<span data-ttu-id="bd8f6-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd8f6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd8f6-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd8f6-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8f6-130">CommonParameters</span></span>
<span data-ttu-id="bd8f6-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd8f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8f6-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd8f6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8f6-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd8f6-133">INPUTS</span></span>

### <span data-ttu-id="bd8f6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bd8f6-134">System.String</span></span>

### <span data-ttu-id="bd8f6-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bd8f6-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bd8f6-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd8f6-136">OUTPUTS</span></span>

### <span data-ttu-id="bd8f6-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="bd8f6-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="bd8f6-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd8f6-138">NOTES</span></span>

## <span data-ttu-id="bd8f6-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd8f6-139">RELATED LINKS</span></span>
