---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: a531ffb8a4fae50b6d352fd1167af9c13cee409c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948707"
---
# <span data-ttu-id="2071e-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="2071e-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="2071e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2071e-102">SYNOPSIS</span></span>
<span data-ttu-id="2071e-103">Aktualisieren Sie den DevSpaces-Controller, um Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2071e-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="2071e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2071e-104">SYNTAX</span></span>

### <span data-ttu-id="2071e-105">DevSpacesControllerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2071e-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2071e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2071e-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2071e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2071e-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2071e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2071e-108">DESCRIPTION</span></span>
<span data-ttu-id="2071e-109">Aktualisieren Sie den DevSpaces-Controller, um Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2071e-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="2071e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2071e-110">EXAMPLES</span></span>

### <span data-ttu-id="2071e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2071e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="2071e-112">Markieren Sie einen DevSpaces-Controller.</span><span class="sxs-lookup"><span data-stu-id="2071e-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="2071e-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2071e-113">PARAMETERS</span></span>

### <span data-ttu-id="2071e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2071e-114">-DefaultProfile</span></span>
<span data-ttu-id="2071e-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2071e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2071e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2071e-116">-InputObject</span></span>
<span data-ttu-id="2071e-117">Ein PSController-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2071e-117">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2071e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2071e-118">-Name</span></span>
<span data-ttu-id="2071e-119">DevSpaces-Controllername.</span><span class="sxs-lookup"><span data-stu-id="2071e-119">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2071e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2071e-120">-ResourceGroupName</span></span>
<span data-ttu-id="2071e-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2071e-121">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2071e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2071e-122">-ResourceId</span></span>
<span data-ttu-id="2071e-123">Die DevSpaces-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2071e-123">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2071e-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="2071e-124">-Tag</span></span>
<span data-ttu-id="2071e-125">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="2071e-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2071e-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2071e-126">-Confirm</span></span>
<span data-ttu-id="2071e-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2071e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2071e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2071e-128">-WhatIf</span></span>
<span data-ttu-id="2071e-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2071e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2071e-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2071e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2071e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2071e-131">CommonParameters</span></span>
<span data-ttu-id="2071e-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2071e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2071e-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2071e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2071e-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2071e-134">INPUTS</span></span>

### <span data-ttu-id="2071e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2071e-135">System.String</span></span>

### <span data-ttu-id="2071e-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="2071e-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="2071e-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2071e-137">OUTPUTS</span></span>

### <span data-ttu-id="2071e-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="2071e-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="2071e-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2071e-139">NOTES</span></span>

## <span data-ttu-id="2071e-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2071e-140">RELATED LINKS</span></span>
