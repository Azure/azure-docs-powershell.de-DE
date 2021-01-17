---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470613"
---
# <span data-ttu-id="61f4d-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61f4d-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="61f4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="61f4d-103">Entfernt das Edgespeicherkonto für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="61f4d-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="61f4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61f4d-104">SYNTAX</span></span>

### <span data-ttu-id="61f4d-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="61f4d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f4d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61f4d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f4d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61f4d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f4d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61f4d-108">DESCRIPTION</span></span>
<span data-ttu-id="61f4d-109">Das **Cmdlet "Remove-AzDataBoxEdgeStorageAccount"** entfernt ein zugeordnetes Edgespeicherkonto für ein Datenfeld-Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="61f4d-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="61f4d-110">Sie können den Namen des Edgespeicherkontos angeben, das als Parameter im Cmdlet entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="61f4d-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="61f4d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61f4d-111">EXAMPLES</span></span>

### <span data-ttu-id="61f4d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61f4d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="61f4d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61f4d-113">PARAMETERS</span></span>

### <span data-ttu-id="61f4d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61f4d-114">-AsJob</span></span>
<span data-ttu-id="61f4d-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="61f4d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61f4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f4d-116">-DefaultProfile</span></span>
<span data-ttu-id="61f4d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61f4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61f4d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="61f4d-118">-DeviceName</span></span>
<span data-ttu-id="61f4d-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="61f4d-119">Device Name</span></span>

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

### <span data-ttu-id="61f4d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61f4d-120">-InputObject</span></span>
<span data-ttu-id="61f4d-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="61f4d-121">Input Object</span></span>

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

### <span data-ttu-id="61f4d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="61f4d-122">-Name</span></span>
<span data-ttu-id="61f4d-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="61f4d-123">Resource Name</span></span>

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

### <span data-ttu-id="61f4d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61f4d-124">-PassThru</span></span>
<span data-ttu-id="61f4d-125">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="61f4d-125">returns true if successful</span></span>

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

### <span data-ttu-id="61f4d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f4d-126">-ResourceGroupName</span></span>
<span data-ttu-id="61f4d-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="61f4d-127">Resource Group Name</span></span>

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

### <span data-ttu-id="61f4d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61f4d-128">-ResourceId</span></span>
<span data-ttu-id="61f4d-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="61f4d-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="61f4d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61f4d-130">-Confirm</span></span>
<span data-ttu-id="61f4d-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61f4d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f4d-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="61f4d-132">-WhatIf</span></span>
<span data-ttu-id="61f4d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61f4d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61f4d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61f4d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f4d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f4d-135">CommonParameters</span></span>
<span data-ttu-id="61f4d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f4d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f4d-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61f4d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f4d-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61f4d-138">INPUTS</span></span>

### <span data-ttu-id="61f4d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="61f4d-139">System.String</span></span>

### <span data-ttu-id="61f4d-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61f4d-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="61f4d-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61f4d-141">OUTPUTS</span></span>

### <span data-ttu-id="61f4d-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61f4d-142">System.Boolean</span></span>

## <span data-ttu-id="61f4d-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="61f4d-143">NOTES</span></span>

## <span data-ttu-id="61f4d-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="61f4d-144">RELATED LINKS</span></span>
