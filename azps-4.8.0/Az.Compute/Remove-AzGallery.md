---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010002"
---
# <span data-ttu-id="81e1c-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="81e1c-101">Remove-AzGallery</span></span>

## <span data-ttu-id="81e1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="81e1c-103">Löschen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="81e1c-103">Delete a gallery.</span></span>

## <span data-ttu-id="81e1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81e1c-104">SYNTAX</span></span>

### <span data-ttu-id="81e1c-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="81e1c-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e1c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="81e1c-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e1c-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="81e1c-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81e1c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81e1c-108">DESCRIPTION</span></span>
<span data-ttu-id="81e1c-109">Löschen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="81e1c-109">Delete a gallery.</span></span>

## <span data-ttu-id="81e1c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="81e1c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81e1c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="81e1c-112">Löschen des angegebenen Katalogs</span><span class="sxs-lookup"><span data-stu-id="81e1c-112">Delete the given gallery.</span></span>

## <span data-ttu-id="81e1c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="81e1c-113">PARAMETERS</span></span>

### <span data-ttu-id="81e1c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81e1c-114">-AsJob</span></span>
<span data-ttu-id="81e1c-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="81e1c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81e1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e1c-116">-DefaultProfile</span></span>
<span data-ttu-id="81e1c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81e1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81e1c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="81e1c-118">-Force</span></span>
<span data-ttu-id="81e1c-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="81e1c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81e1c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81e1c-120">-InputObject</span></span>
<span data-ttu-id="81e1c-121">Das PS Gallery-Objekt</span><span class="sxs-lookup"><span data-stu-id="81e1c-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="81e1c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="81e1c-122">-Name</span></span>
<span data-ttu-id="81e1c-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="81e1c-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="81e1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="81e1c-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81e1c-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="81e1c-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="81e1c-126">-ResourceId</span></span>
<span data-ttu-id="81e1c-127">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="81e1c-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="81e1c-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="81e1c-128">-Confirm</span></span>
<span data-ttu-id="81e1c-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="81e1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e1c-130">-WhatIf</span></span>
<span data-ttu-id="81e1c-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81e1c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81e1c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81e1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e1c-133">CommonParameters</span></span>
<span data-ttu-id="81e1c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e1c-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81e1c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e1c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81e1c-136">INPUTS</span></span>

### <span data-ttu-id="81e1c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="81e1c-137">System.String</span></span>

### <span data-ttu-id="81e1c-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="81e1c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="81e1c-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81e1c-139">OUTPUTS</span></span>

### <span data-ttu-id="81e1c-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="81e1c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="81e1c-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="81e1c-141">NOTES</span></span>

## <span data-ttu-id="81e1c-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81e1c-142">RELATED LINKS</span></span>
