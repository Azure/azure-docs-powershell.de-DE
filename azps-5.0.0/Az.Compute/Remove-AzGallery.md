---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300705"
---
# <span data-ttu-id="66454-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="66454-101">Remove-AzGallery</span></span>

## <span data-ttu-id="66454-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66454-102">SYNOPSIS</span></span>
<span data-ttu-id="66454-103">Löschen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="66454-103">Delete a gallery.</span></span>

## <span data-ttu-id="66454-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66454-104">SYNTAX</span></span>

### <span data-ttu-id="66454-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="66454-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66454-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="66454-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66454-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="66454-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66454-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66454-108">DESCRIPTION</span></span>
<span data-ttu-id="66454-109">Löschen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="66454-109">Delete a gallery.</span></span>

## <span data-ttu-id="66454-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66454-110">EXAMPLES</span></span>

### <span data-ttu-id="66454-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66454-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="66454-112">Löschen des angegebenen Katalogs</span><span class="sxs-lookup"><span data-stu-id="66454-112">Delete the given gallery.</span></span>

## <span data-ttu-id="66454-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="66454-113">PARAMETERS</span></span>

### <span data-ttu-id="66454-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66454-114">-AsJob</span></span>
<span data-ttu-id="66454-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="66454-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66454-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66454-116">-DefaultProfile</span></span>
<span data-ttu-id="66454-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66454-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66454-118">-Force</span><span class="sxs-lookup"><span data-stu-id="66454-118">-Force</span></span>
<span data-ttu-id="66454-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="66454-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66454-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66454-120">-InputObject</span></span>
<span data-ttu-id="66454-121">Das PS Gallery-Objekt</span><span class="sxs-lookup"><span data-stu-id="66454-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="66454-122">-Name</span><span class="sxs-lookup"><span data-stu-id="66454-122">-Name</span></span>
<span data-ttu-id="66454-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="66454-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="66454-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66454-124">-ResourceGroupName</span></span>
<span data-ttu-id="66454-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66454-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="66454-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="66454-126">-ResourceId</span></span>
<span data-ttu-id="66454-127">Die Ressourcen-ID für den Katalog</span><span class="sxs-lookup"><span data-stu-id="66454-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="66454-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66454-128">-Confirm</span></span>
<span data-ttu-id="66454-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66454-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66454-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66454-130">-WhatIf</span></span>
<span data-ttu-id="66454-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66454-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66454-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66454-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66454-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66454-133">CommonParameters</span></span>
<span data-ttu-id="66454-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66454-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66454-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66454-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66454-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66454-136">INPUTS</span></span>

### <span data-ttu-id="66454-137">System. String</span><span class="sxs-lookup"><span data-stu-id="66454-137">System.String</span></span>

### <span data-ttu-id="66454-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="66454-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="66454-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66454-139">OUTPUTS</span></span>

### <span data-ttu-id="66454-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="66454-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="66454-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="66454-141">NOTES</span></span>

## <span data-ttu-id="66454-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66454-142">RELATED LINKS</span></span>
