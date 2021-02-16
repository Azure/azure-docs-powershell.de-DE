---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170718"
---
# <span data-ttu-id="73465-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="73465-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="73465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73465-102">SYNOPSIS</span></span>
<span data-ttu-id="73465-103">Aktualisieren Sie den DevSpaces-Controller, um Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="73465-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="73465-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73465-104">SYNTAX</span></span>

### <span data-ttu-id="73465-105">DevSpacesControllerNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="73465-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73465-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73465-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73465-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73465-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73465-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73465-108">DESCRIPTION</span></span>
<span data-ttu-id="73465-109">Aktualisieren Sie den DevSpaces-Controller, um Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="73465-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="73465-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73465-110">EXAMPLES</span></span>

### <span data-ttu-id="73465-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73465-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="73465-112">Markieren Sie einen DevSpaces-Controller.</span><span class="sxs-lookup"><span data-stu-id="73465-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="73465-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73465-113">PARAMETERS</span></span>

### <span data-ttu-id="73465-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73465-114">-DefaultProfile</span></span>
<span data-ttu-id="73465-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73465-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73465-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73465-116">-InputObject</span></span>
<span data-ttu-id="73465-117">Ein PSController-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="73465-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="73465-118">-Name</span><span class="sxs-lookup"><span data-stu-id="73465-118">-Name</span></span>
<span data-ttu-id="73465-119">DevSpaces-Controllername.</span><span class="sxs-lookup"><span data-stu-id="73465-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="73465-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73465-120">-ResourceGroupName</span></span>
<span data-ttu-id="73465-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="73465-121">Resource group name</span></span>

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

### <span data-ttu-id="73465-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73465-122">-ResourceId</span></span>
<span data-ttu-id="73465-123">Die DevSpaces-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="73465-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="73465-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="73465-124">-Tag</span></span>
<span data-ttu-id="73465-125">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="73465-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="73465-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73465-126">-Confirm</span></span>
<span data-ttu-id="73465-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73465-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73465-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="73465-128">-WhatIf</span></span>
<span data-ttu-id="73465-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73465-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73465-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73465-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73465-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73465-131">CommonParameters</span></span>
<span data-ttu-id="73465-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73465-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73465-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73465-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73465-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73465-134">INPUTS</span></span>

### <span data-ttu-id="73465-135">System.String</span><span class="sxs-lookup"><span data-stu-id="73465-135">System.String</span></span>

### <span data-ttu-id="73465-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="73465-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="73465-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73465-137">OUTPUTS</span></span>

### <span data-ttu-id="73465-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="73465-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="73465-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="73465-139">NOTES</span></span>

## <span data-ttu-id="73465-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="73465-140">RELATED LINKS</span></span>
