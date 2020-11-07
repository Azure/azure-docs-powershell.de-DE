---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
ms.openlocfilehash: 5d8ed5a26e141d0ae8d6eb7494a76d8c53590d29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664084"
---
# <span data-ttu-id="0ab57-101">Update-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="0ab57-101">Update-AzureRmGallery</span></span>

## <span data-ttu-id="0ab57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ab57-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab57-103">Aktualisieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="0ab57-103">Update a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ab57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ab57-104">SYNTAX</span></span>

### <span data-ttu-id="0ab57-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ab57-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ab57-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0ab57-106">ResourceIdParameter</span></span>
```
Update-AzureRmGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ab57-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="0ab57-107">ObjectParameter</span></span>
```
Update-AzureRmGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ab57-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ab57-108">DESCRIPTION</span></span>
<span data-ttu-id="0ab57-109">Aktualisieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="0ab57-109">Update a gallery.</span></span>

## <span data-ttu-id="0ab57-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ab57-110">EXAMPLES</span></span>

### <span data-ttu-id="0ab57-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ab57-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="0ab57-112">Aktualisieren eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="0ab57-112">Update a gallery.</span></span>

## <span data-ttu-id="0ab57-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ab57-113">PARAMETERS</span></span>

### <span data-ttu-id="0ab57-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ab57-114">-AsJob</span></span>
<span data-ttu-id="0ab57-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0ab57-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ab57-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab57-116">-DefaultProfile</span></span>
<span data-ttu-id="0ab57-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ab57-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ab57-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ab57-118">-Description</span></span>
<span data-ttu-id="0ab57-119">Die Beschreibung der Katalog Ressource.</span><span class="sxs-lookup"><span data-stu-id="0ab57-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="0ab57-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0ab57-120">-InputObject</span></span>
<span data-ttu-id="0ab57-121">Das PS Gallery-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0ab57-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="0ab57-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0ab57-122">-Name</span></span>
<span data-ttu-id="0ab57-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="0ab57-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="0ab57-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab57-124">-ResourceGroupName</span></span>
<span data-ttu-id="0ab57-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0ab57-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="0ab57-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0ab57-126">-ResourceId</span></span>
<span data-ttu-id="0ab57-127">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="0ab57-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="0ab57-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ab57-128">-Tag</span></span>
<span data-ttu-id="0ab57-129">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="0ab57-129">Resource tags</span></span>

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

### <span data-ttu-id="0ab57-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ab57-130">-Confirm</span></span>
<span data-ttu-id="0ab57-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ab57-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ab57-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ab57-132">-WhatIf</span></span>
<span data-ttu-id="0ab57-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ab57-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ab57-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ab57-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ab57-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab57-135">CommonParameters</span></span>
<span data-ttu-id="0ab57-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab57-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab57-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab57-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab57-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ab57-138">INPUTS</span></span>

### <span data-ttu-id="0ab57-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0ab57-139">System.String</span></span>

### <span data-ttu-id="0ab57-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="0ab57-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="0ab57-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0ab57-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0ab57-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ab57-142">OUTPUTS</span></span>

### <span data-ttu-id="0ab57-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="0ab57-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="0ab57-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ab57-144">NOTES</span></span>

## <span data-ttu-id="0ab57-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ab57-145">RELATED LINKS</span></span>
