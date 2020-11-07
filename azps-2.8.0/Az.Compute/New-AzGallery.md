---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: 2ea4bc3d1e3e6c88ec615feda97c12891030c9c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652085"
---
# <span data-ttu-id="7b95a-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="7b95a-101">New-AzGallery</span></span>

## <span data-ttu-id="7b95a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b95a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b95a-103">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="7b95a-103">Create a gallery.</span></span>

## <span data-ttu-id="7b95a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b95a-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b95a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b95a-105">DESCRIPTION</span></span>
<span data-ttu-id="7b95a-106">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="7b95a-106">Create a gallery.</span></span>

## <span data-ttu-id="7b95a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b95a-107">EXAMPLES</span></span>

### <span data-ttu-id="7b95a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7b95a-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="7b95a-109">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="7b95a-109">Create a gallery.</span></span>

## <span data-ttu-id="7b95a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b95a-110">PARAMETERS</span></span>

### <span data-ttu-id="7b95a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b95a-111">-AsJob</span></span>
<span data-ttu-id="7b95a-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7b95a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b95a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b95a-113">-DefaultProfile</span></span>
<span data-ttu-id="7b95a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b95a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b95a-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b95a-115">-Description</span></span>
<span data-ttu-id="7b95a-116">Die Beschreibung der Katalog Ressource.</span><span class="sxs-lookup"><span data-stu-id="7b95a-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="7b95a-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="7b95a-117">-Location</span></span>
<span data-ttu-id="7b95a-118">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="7b95a-118">Resource location</span></span>

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

### <span data-ttu-id="7b95a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7b95a-119">-Name</span></span>
<span data-ttu-id="7b95a-120">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="7b95a-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="7b95a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b95a-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b95a-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7b95a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="7b95a-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b95a-123">-Tag</span></span>
<span data-ttu-id="7b95a-124">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="7b95a-124">Resource tags</span></span>

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

### <span data-ttu-id="7b95a-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b95a-125">-Confirm</span></span>
<span data-ttu-id="7b95a-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b95a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b95a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b95a-127">-WhatIf</span></span>
<span data-ttu-id="7b95a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b95a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b95a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b95a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b95a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b95a-130">CommonParameters</span></span>
<span data-ttu-id="7b95a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b95a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b95a-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b95a-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b95a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b95a-133">INPUTS</span></span>

### <span data-ttu-id="7b95a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7b95a-134">System.String</span></span>

### <span data-ttu-id="7b95a-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7b95a-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7b95a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b95a-136">OUTPUTS</span></span>

### <span data-ttu-id="7b95a-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="7b95a-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="7b95a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b95a-138">NOTES</span></span>

## <span data-ttu-id="7b95a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b95a-139">RELATED LINKS</span></span>
