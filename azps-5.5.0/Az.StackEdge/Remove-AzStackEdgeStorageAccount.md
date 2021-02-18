---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173764"
---
# <span data-ttu-id="27918-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27918-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="27918-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27918-102">SYNOPSIS</span></span>
<span data-ttu-id="27918-103">Entfernt das Edgespeicherkonto für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="27918-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="27918-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27918-104">SYNTAX</span></span>

### <span data-ttu-id="27918-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="27918-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27918-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27918-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27918-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27918-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27918-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27918-108">DESCRIPTION</span></span>
<span data-ttu-id="27918-109">Das **Cmdlet "Remove-AzStackEdgeStorageAccount"** entfernt ein zugeordnetes Edgespeicherkonto für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="27918-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="27918-110">Sie können den Namen des Edgespeicherkontos angeben, das als Parameter im Cmdlet entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="27918-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="27918-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27918-111">EXAMPLES</span></span>

### <span data-ttu-id="27918-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27918-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="27918-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27918-113">PARAMETERS</span></span>

### <span data-ttu-id="27918-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27918-114">-AsJob</span></span>
<span data-ttu-id="27918-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="27918-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27918-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27918-116">-DefaultProfile</span></span>
<span data-ttu-id="27918-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27918-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27918-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="27918-118">-DeviceName</span></span>
<span data-ttu-id="27918-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="27918-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27918-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27918-120">-InputObject</span></span>
<span data-ttu-id="27918-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="27918-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27918-122">-Name</span><span class="sxs-lookup"><span data-stu-id="27918-122">-Name</span></span>
<span data-ttu-id="27918-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="27918-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27918-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27918-124">-PassThru</span></span>
<span data-ttu-id="27918-125">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="27918-125">returns true if successful</span></span>

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

### <span data-ttu-id="27918-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27918-126">-ResourceGroupName</span></span>
<span data-ttu-id="27918-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="27918-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27918-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27918-128">-ResourceId</span></span>
<span data-ttu-id="27918-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="27918-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27918-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27918-130">-Confirm</span></span>
<span data-ttu-id="27918-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27918-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27918-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="27918-132">-WhatIf</span></span>
<span data-ttu-id="27918-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27918-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27918-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27918-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27918-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27918-135">CommonParameters</span></span>
<span data-ttu-id="27918-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27918-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27918-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27918-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27918-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27918-138">INPUTS</span></span>

### <span data-ttu-id="27918-139">System.String</span><span class="sxs-lookup"><span data-stu-id="27918-139">System.String</span></span>

### <span data-ttu-id="27918-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27918-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="27918-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27918-141">OUTPUTS</span></span>

### <span data-ttu-id="27918-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27918-142">System.Boolean</span></span>

## <span data-ttu-id="27918-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27918-143">NOTES</span></span>

## <span data-ttu-id="27918-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27918-144">RELATED LINKS</span></span>
