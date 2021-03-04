---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 21c623187e72406d1120e225bf567a48bb2e6f30
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934272"
---
# <span data-ttu-id="da379-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="da379-101">Remove-AzHost</span></span>

## <span data-ttu-id="da379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da379-102">SYNOPSIS</span></span>
<span data-ttu-id="da379-103">Entfernt einen Host.</span><span class="sxs-lookup"><span data-stu-id="da379-103">Removes a host.</span></span>

## <span data-ttu-id="da379-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da379-104">SYNTAX</span></span>

### <span data-ttu-id="da379-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="da379-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da379-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="da379-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da379-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="da379-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da379-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da379-108">DESCRIPTION</span></span>
<span data-ttu-id="da379-109">Dieses Cmdlet löscht einen Host</span><span class="sxs-lookup"><span data-stu-id="da379-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="da379-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da379-110">EXAMPLES</span></span>

### <span data-ttu-id="da379-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="da379-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="da379-112">Dieser Befehl ruft den angegebenen Host ab und entfernt ihn.</span><span class="sxs-lookup"><span data-stu-id="da379-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="da379-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="da379-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="da379-114">Mit diesem Befehl wird der angegebene Host entfernt.</span><span class="sxs-lookup"><span data-stu-id="da379-114">This command removes the given host.</span></span>

## <span data-ttu-id="da379-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="da379-115">PARAMETERS</span></span>

### <span data-ttu-id="da379-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da379-116">-AsJob</span></span>
<span data-ttu-id="da379-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="da379-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da379-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da379-118">-DefaultProfile</span></span>
<span data-ttu-id="da379-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da379-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da379-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="da379-120">-HostGroupName</span></span>
<span data-ttu-id="da379-121">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="da379-121">The name of the host group.</span></span>

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

### <span data-ttu-id="da379-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da379-122">-InputObject</span></span>
<span data-ttu-id="da379-123">Das lokale Objekt des Hosts.</span><span class="sxs-lookup"><span data-stu-id="da379-123">The local object of the host.</span></span>

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

### <span data-ttu-id="da379-124">-Name</span><span class="sxs-lookup"><span data-stu-id="da379-124">-Name</span></span>
<span data-ttu-id="da379-125">Der Name des Hosts.</span><span class="sxs-lookup"><span data-stu-id="da379-125">The name of the host.</span></span>

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

### <span data-ttu-id="da379-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da379-126">-ResourceGroupName</span></span>
<span data-ttu-id="da379-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="da379-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="da379-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da379-128">-ResourceId</span></span>
<span data-ttu-id="da379-129">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="da379-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="da379-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da379-130">-Confirm</span></span>
<span data-ttu-id="da379-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da379-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da379-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da379-132">-WhatIf</span></span>
<span data-ttu-id="da379-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da379-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da379-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da379-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da379-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da379-135">CommonParameters</span></span>
<span data-ttu-id="da379-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da379-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da379-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da379-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da379-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da379-138">INPUTS</span></span>

### <span data-ttu-id="da379-139">System.String</span><span class="sxs-lookup"><span data-stu-id="da379-139">System.String</span></span>

### <span data-ttu-id="da379-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="da379-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="da379-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da379-141">OUTPUTS</span></span>

### <span data-ttu-id="da379-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="da379-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="da379-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="da379-143">NOTES</span></span>

## <span data-ttu-id="da379-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="da379-144">RELATED LINKS</span></span>
