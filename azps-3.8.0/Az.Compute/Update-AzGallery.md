---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846140"
---
# <span data-ttu-id="1dffa-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="1dffa-101">Update-AzGallery</span></span>

## <span data-ttu-id="1dffa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1dffa-102">SYNOPSIS</span></span>
<span data-ttu-id="1dffa-103">Aktualisieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="1dffa-103">Update a gallery.</span></span>

## <span data-ttu-id="1dffa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dffa-104">SYNTAX</span></span>

### <span data-ttu-id="1dffa-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="1dffa-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dffa-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1dffa-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dffa-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1dffa-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dffa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dffa-108">DESCRIPTION</span></span>
<span data-ttu-id="1dffa-109">Aktualisieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="1dffa-109">Update a gallery.</span></span>

## <span data-ttu-id="1dffa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1dffa-110">EXAMPLES</span></span>

### <span data-ttu-id="1dffa-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1dffa-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="1dffa-112">Aktualisieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="1dffa-112">Update a gallery.</span></span>

## <span data-ttu-id="1dffa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dffa-113">PARAMETERS</span></span>

### <span data-ttu-id="1dffa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dffa-114">-AsJob</span></span>
<span data-ttu-id="1dffa-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1dffa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dffa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dffa-116">-DefaultProfile</span></span>
<span data-ttu-id="1dffa-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1dffa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dffa-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dffa-118">-Description</span></span>
<span data-ttu-id="1dffa-119">Die Beschreibung der Katalog Ressource.</span><span class="sxs-lookup"><span data-stu-id="1dffa-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="1dffa-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1dffa-120">-InputObject</span></span>
<span data-ttu-id="1dffa-121">Das PS Gallery-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1dffa-121">The PS Gallery Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dffa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1dffa-122">-Name</span></span>
<span data-ttu-id="1dffa-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="1dffa-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dffa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dffa-124">-ResourceGroupName</span></span>
<span data-ttu-id="1dffa-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1dffa-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1dffa-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1dffa-126">-ResourceId</span></span>
<span data-ttu-id="1dffa-127">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="1dffa-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="1dffa-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="1dffa-128">-Tag</span></span>
<span data-ttu-id="1dffa-129">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="1dffa-129">Resource tags</span></span>

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

### <span data-ttu-id="1dffa-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1dffa-130">-Confirm</span></span>
<span data-ttu-id="1dffa-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1dffa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dffa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dffa-132">-WhatIf</span></span>
<span data-ttu-id="1dffa-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1dffa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dffa-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1dffa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dffa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dffa-135">CommonParameters</span></span>
<span data-ttu-id="1dffa-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dffa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dffa-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dffa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dffa-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1dffa-138">INPUTS</span></span>

### <span data-ttu-id="1dffa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1dffa-139">System.String</span></span>

### <span data-ttu-id="1dffa-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="1dffa-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="1dffa-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1dffa-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1dffa-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1dffa-142">OUTPUTS</span></span>

### <span data-ttu-id="1dffa-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="1dffa-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="1dffa-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="1dffa-144">NOTES</span></span>

## <span data-ttu-id="1dffa-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1dffa-145">RELATED LINKS</span></span>
