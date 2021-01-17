---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473036"
---
# <span data-ttu-id="453cf-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="453cf-101">Remove-AzHost</span></span>

## <span data-ttu-id="453cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="453cf-102">SYNOPSIS</span></span>
<span data-ttu-id="453cf-103">Entfernt einen Host.</span><span class="sxs-lookup"><span data-stu-id="453cf-103">Removes a host.</span></span>

## <span data-ttu-id="453cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="453cf-104">SYNTAX</span></span>

### <span data-ttu-id="453cf-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="453cf-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="453cf-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="453cf-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="453cf-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="453cf-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="453cf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="453cf-108">DESCRIPTION</span></span>
<span data-ttu-id="453cf-109">Mit diesem Cmdlet wird ein Host gelöscht.</span><span class="sxs-lookup"><span data-stu-id="453cf-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="453cf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="453cf-110">EXAMPLES</span></span>

### <span data-ttu-id="453cf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="453cf-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="453cf-112">Dieser Befehl ruft den angegebenen Host ab und entfernt ihn.</span><span class="sxs-lookup"><span data-stu-id="453cf-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="453cf-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="453cf-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="453cf-114">Mit diesem Befehl wird der angegebene Host entfernt.</span><span class="sxs-lookup"><span data-stu-id="453cf-114">This command removes the given host.</span></span>

## <span data-ttu-id="453cf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="453cf-115">PARAMETERS</span></span>

### <span data-ttu-id="453cf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="453cf-116">-AsJob</span></span>
<span data-ttu-id="453cf-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="453cf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="453cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="453cf-118">-DefaultProfile</span></span>
<span data-ttu-id="453cf-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="453cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="453cf-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="453cf-120">-HostGroupName</span></span>
<span data-ttu-id="453cf-121">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="453cf-121">The name of the host group.</span></span>

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

### <span data-ttu-id="453cf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="453cf-122">-InputObject</span></span>
<span data-ttu-id="453cf-123">Das lokale Objekt des Hosts.</span><span class="sxs-lookup"><span data-stu-id="453cf-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="453cf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="453cf-124">-Name</span></span>
<span data-ttu-id="453cf-125">Der Name des Hosts.</span><span class="sxs-lookup"><span data-stu-id="453cf-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="453cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="453cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="453cf-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="453cf-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="453cf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="453cf-128">-ResourceId</span></span>
<span data-ttu-id="453cf-129">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="453cf-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="453cf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="453cf-130">-Confirm</span></span>
<span data-ttu-id="453cf-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="453cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="453cf-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="453cf-132">-WhatIf</span></span>
<span data-ttu-id="453cf-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="453cf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="453cf-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="453cf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="453cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453cf-135">CommonParameters</span></span>
<span data-ttu-id="453cf-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="453cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453cf-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="453cf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453cf-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="453cf-138">INPUTS</span></span>

### <span data-ttu-id="453cf-139">System.String</span><span class="sxs-lookup"><span data-stu-id="453cf-139">System.String</span></span>

### <span data-ttu-id="453cf-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="453cf-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="453cf-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="453cf-141">OUTPUTS</span></span>

### <span data-ttu-id="453cf-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="453cf-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="453cf-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="453cf-143">NOTES</span></span>

## <span data-ttu-id="453cf-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="453cf-144">RELATED LINKS</span></span>
