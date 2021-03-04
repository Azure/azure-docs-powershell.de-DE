---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 0a573f8fa293d2c3e4c84eced54c88eb77032970
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945508"
---
# <span data-ttu-id="548d3-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="548d3-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="548d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="548d3-102">SYNOPSIS</span></span>
<span data-ttu-id="548d3-103">Entfernt das Edgespeicherkonto für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="548d3-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="548d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="548d3-104">SYNTAX</span></span>

### <span data-ttu-id="548d3-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="548d3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="548d3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="548d3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="548d3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="548d3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548d3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="548d3-108">DESCRIPTION</span></span>
<span data-ttu-id="548d3-109">Das **Cmdlet Remove-AzStackEdgeStorageAccount** entfernt ein zugeordnetes Edgespeicherkonto für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="548d3-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="548d3-110">Sie können den Namen des Edgespeicherkontos angeben, das als Parameter im Cmdlet entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="548d3-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="548d3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="548d3-111">EXAMPLES</span></span>

### <span data-ttu-id="548d3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="548d3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="548d3-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="548d3-113">PARAMETERS</span></span>

### <span data-ttu-id="548d3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="548d3-114">-AsJob</span></span>
<span data-ttu-id="548d3-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="548d3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="548d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548d3-116">-DefaultProfile</span></span>
<span data-ttu-id="548d3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="548d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="548d3-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="548d3-118">-DeviceName</span></span>
<span data-ttu-id="548d3-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="548d3-119">Device Name</span></span>

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

### <span data-ttu-id="548d3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="548d3-120">-InputObject</span></span>
<span data-ttu-id="548d3-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="548d3-121">Input Object</span></span>

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

### <span data-ttu-id="548d3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="548d3-122">-Name</span></span>
<span data-ttu-id="548d3-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="548d3-123">Resource Name</span></span>

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

### <span data-ttu-id="548d3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="548d3-124">-PassThru</span></span>
<span data-ttu-id="548d3-125">gibt "true" zurück, wenn dies erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="548d3-125">returns true if successful</span></span>

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

### <span data-ttu-id="548d3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548d3-126">-ResourceGroupName</span></span>
<span data-ttu-id="548d3-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="548d3-127">Resource Group Name</span></span>

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

### <span data-ttu-id="548d3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="548d3-128">-ResourceId</span></span>
<span data-ttu-id="548d3-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="548d3-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="548d3-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="548d3-130">-Confirm</span></span>
<span data-ttu-id="548d3-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="548d3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="548d3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548d3-132">-WhatIf</span></span>
<span data-ttu-id="548d3-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="548d3-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="548d3-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="548d3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="548d3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548d3-135">CommonParameters</span></span>
<span data-ttu-id="548d3-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548d3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548d3-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="548d3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548d3-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="548d3-138">INPUTS</span></span>

### <span data-ttu-id="548d3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="548d3-139">System.String</span></span>

### <span data-ttu-id="548d3-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="548d3-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="548d3-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="548d3-141">OUTPUTS</span></span>

### <span data-ttu-id="548d3-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="548d3-142">System.Boolean</span></span>

## <span data-ttu-id="548d3-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="548d3-143">NOTES</span></span>

## <span data-ttu-id="548d3-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="548d3-144">RELATED LINKS</span></span>
