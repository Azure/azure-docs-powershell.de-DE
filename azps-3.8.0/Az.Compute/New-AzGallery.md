---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996167"
---
# <span data-ttu-id="01156-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="01156-101">New-AzGallery</span></span>

## <span data-ttu-id="01156-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01156-102">SYNOPSIS</span></span>
<span data-ttu-id="01156-103">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="01156-103">Create a gallery.</span></span>

## <span data-ttu-id="01156-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01156-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01156-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01156-105">DESCRIPTION</span></span>
<span data-ttu-id="01156-106">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="01156-106">Create a gallery.</span></span>

## <span data-ttu-id="01156-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01156-107">EXAMPLES</span></span>

### <span data-ttu-id="01156-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01156-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="01156-109">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="01156-109">Create a gallery.</span></span>

## <span data-ttu-id="01156-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="01156-110">PARAMETERS</span></span>

### <span data-ttu-id="01156-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01156-111">-AsJob</span></span>
<span data-ttu-id="01156-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="01156-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01156-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01156-113">-DefaultProfile</span></span>
<span data-ttu-id="01156-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01156-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01156-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01156-115">-Description</span></span>
<span data-ttu-id="01156-116">Die Beschreibung der Katalog Ressource.</span><span class="sxs-lookup"><span data-stu-id="01156-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="01156-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="01156-117">-Location</span></span>
<span data-ttu-id="01156-118">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="01156-118">Resource location</span></span>

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

### <span data-ttu-id="01156-119">-Name</span><span class="sxs-lookup"><span data-stu-id="01156-119">-Name</span></span>
<span data-ttu-id="01156-120">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="01156-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="01156-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01156-121">-ResourceGroupName</span></span>
<span data-ttu-id="01156-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01156-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="01156-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="01156-123">-Tag</span></span>
<span data-ttu-id="01156-124">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="01156-124">Resource tags</span></span>

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

### <span data-ttu-id="01156-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01156-125">-Confirm</span></span>
<span data-ttu-id="01156-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01156-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01156-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01156-127">-WhatIf</span></span>
<span data-ttu-id="01156-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01156-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01156-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01156-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01156-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01156-130">CommonParameters</span></span>
<span data-ttu-id="01156-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01156-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01156-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01156-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01156-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01156-133">INPUTS</span></span>

### <span data-ttu-id="01156-134">System. String</span><span class="sxs-lookup"><span data-stu-id="01156-134">System.String</span></span>

### <span data-ttu-id="01156-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="01156-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="01156-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01156-136">OUTPUTS</span></span>

### <span data-ttu-id="01156-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="01156-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="01156-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="01156-138">NOTES</span></span>

## <span data-ttu-id="01156-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01156-139">RELATED LINKS</span></span>
