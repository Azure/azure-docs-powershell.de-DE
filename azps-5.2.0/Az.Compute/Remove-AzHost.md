---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365167"
---
# <span data-ttu-id="278f5-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="278f5-101">Remove-AzHost</span></span>

## <span data-ttu-id="278f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="278f5-102">SYNOPSIS</span></span>
<span data-ttu-id="278f5-103">Entfernt einen Host.</span><span class="sxs-lookup"><span data-stu-id="278f5-103">Removes a host.</span></span>

## <span data-ttu-id="278f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="278f5-104">SYNTAX</span></span>

### <span data-ttu-id="278f5-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="278f5-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="278f5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="278f5-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="278f5-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="278f5-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="278f5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="278f5-108">DESCRIPTION</span></span>
<span data-ttu-id="278f5-109">Mit diesem Cmdlet wird ein Host gelöscht.</span><span class="sxs-lookup"><span data-stu-id="278f5-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="278f5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="278f5-110">EXAMPLES</span></span>

### <span data-ttu-id="278f5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="278f5-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="278f5-112">Dieser Befehl ruft den angegebenen Host ab und entfernt ihn.</span><span class="sxs-lookup"><span data-stu-id="278f5-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="278f5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="278f5-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="278f5-114">Mit diesem Befehl wird der angegebene Host entfernt.</span><span class="sxs-lookup"><span data-stu-id="278f5-114">This command removes the given host.</span></span>

## <span data-ttu-id="278f5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="278f5-115">PARAMETERS</span></span>

### <span data-ttu-id="278f5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="278f5-116">-AsJob</span></span>
<span data-ttu-id="278f5-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="278f5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="278f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278f5-118">-DefaultProfile</span></span>
<span data-ttu-id="278f5-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="278f5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="278f5-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="278f5-120">-HostGroupName</span></span>
<span data-ttu-id="278f5-121">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="278f5-121">The name of the host group.</span></span>

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

### <span data-ttu-id="278f5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="278f5-122">-InputObject</span></span>
<span data-ttu-id="278f5-123">Das lokale Objekt des Hosts.</span><span class="sxs-lookup"><span data-stu-id="278f5-123">The local object of the host.</span></span>

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

### <span data-ttu-id="278f5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="278f5-124">-Name</span></span>
<span data-ttu-id="278f5-125">Der Name des Hosts.</span><span class="sxs-lookup"><span data-stu-id="278f5-125">The name of the host.</span></span>

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

### <span data-ttu-id="278f5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="278f5-126">-ResourceGroupName</span></span>
<span data-ttu-id="278f5-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="278f5-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="278f5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="278f5-128">-ResourceId</span></span>
<span data-ttu-id="278f5-129">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="278f5-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="278f5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="278f5-130">-Confirm</span></span>
<span data-ttu-id="278f5-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="278f5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="278f5-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="278f5-132">-WhatIf</span></span>
<span data-ttu-id="278f5-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="278f5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="278f5-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="278f5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="278f5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278f5-135">CommonParameters</span></span>
<span data-ttu-id="278f5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="278f5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278f5-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="278f5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278f5-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="278f5-138">INPUTS</span></span>

### <span data-ttu-id="278f5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="278f5-139">System.String</span></span>

### <span data-ttu-id="278f5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="278f5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="278f5-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="278f5-141">OUTPUTS</span></span>

### <span data-ttu-id="278f5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="278f5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="278f5-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="278f5-143">NOTES</span></span>

## <span data-ttu-id="278f5-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="278f5-144">RELATED LINKS</span></span>
