---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174713"
---
# <span data-ttu-id="29d3e-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="29d3e-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="29d3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="29d3e-103">Entfernt das Edgespeicherkonto für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="29d3e-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="29d3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29d3e-104">SYNTAX</span></span>

### <span data-ttu-id="29d3e-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="29d3e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29d3e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d3e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29d3e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d3e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29d3e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29d3e-108">DESCRIPTION</span></span>
<span data-ttu-id="29d3e-109">Das **Cmdlet "Remove-AzDataBoxEdgeStorageAccount"** entfernt ein zugeordnetes Edgespeicherkonto für ein Datenfeld-Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="29d3e-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="29d3e-110">Sie können den Namen des Edgespeicherkontos angeben, das als Parameter im Cmdlet entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="29d3e-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="29d3e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29d3e-111">EXAMPLES</span></span>

### <span data-ttu-id="29d3e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29d3e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="29d3e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29d3e-113">PARAMETERS</span></span>

### <span data-ttu-id="29d3e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29d3e-114">-AsJob</span></span>
<span data-ttu-id="29d3e-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29d3e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29d3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d3e-116">-DefaultProfile</span></span>
<span data-ttu-id="29d3e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29d3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29d3e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="29d3e-118">-DeviceName</span></span>
<span data-ttu-id="29d3e-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="29d3e-119">Device Name</span></span>

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

### <span data-ttu-id="29d3e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29d3e-120">-InputObject</span></span>
<span data-ttu-id="29d3e-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="29d3e-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29d3e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="29d3e-122">-Name</span></span>
<span data-ttu-id="29d3e-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="29d3e-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d3e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29d3e-124">-PassThru</span></span>
<span data-ttu-id="29d3e-125">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="29d3e-125">returns true if successful</span></span>

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

### <span data-ttu-id="29d3e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d3e-126">-ResourceGroupName</span></span>
<span data-ttu-id="29d3e-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="29d3e-127">Resource Group Name</span></span>

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

### <span data-ttu-id="29d3e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29d3e-128">-ResourceId</span></span>
<span data-ttu-id="29d3e-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="29d3e-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="29d3e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29d3e-130">-Confirm</span></span>
<span data-ttu-id="29d3e-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29d3e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29d3e-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="29d3e-132">-WhatIf</span></span>
<span data-ttu-id="29d3e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29d3e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29d3e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29d3e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29d3e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d3e-135">CommonParameters</span></span>
<span data-ttu-id="29d3e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d3e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d3e-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29d3e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d3e-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29d3e-138">INPUTS</span></span>

### <span data-ttu-id="29d3e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="29d3e-139">System.String</span></span>

### <span data-ttu-id="29d3e-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="29d3e-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="29d3e-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29d3e-141">OUTPUTS</span></span>

### <span data-ttu-id="29d3e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29d3e-142">System.Boolean</span></span>

## <span data-ttu-id="29d3e-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="29d3e-143">NOTES</span></span>

## <span data-ttu-id="29d3e-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="29d3e-144">RELATED LINKS</span></span>
