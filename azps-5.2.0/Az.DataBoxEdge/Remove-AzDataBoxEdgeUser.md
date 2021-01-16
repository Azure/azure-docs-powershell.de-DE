---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306067"
---
# <span data-ttu-id="3735b-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="3735b-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="3735b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3735b-102">SYNOPSIS</span></span>
<span data-ttu-id="3735b-103">Entfernt einen Benutzer auf einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="3735b-103">Removes a user on a device.</span></span>

## <span data-ttu-id="3735b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3735b-104">SYNTAX</span></span>

### <span data-ttu-id="3735b-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3735b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3735b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3735b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3735b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3735b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3735b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3735b-108">DESCRIPTION</span></span>
<span data-ttu-id="3735b-109">Das **Cmdlet "Remove-AzDataBoxEdgeUser"** entfernt einen Benutzer auf dem Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="3735b-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="3735b-110">Die Erstellung nur von Typbenutzern `Share` wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3735b-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="3735b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3735b-111">EXAMPLES</span></span>

### <span data-ttu-id="3735b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3735b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="3735b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3735b-113">PARAMETERS</span></span>

### <span data-ttu-id="3735b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3735b-114">-AsJob</span></span>
<span data-ttu-id="3735b-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3735b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3735b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3735b-116">-DefaultProfile</span></span>
<span data-ttu-id="3735b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3735b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3735b-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3735b-118">-DeviceName</span></span>
<span data-ttu-id="3735b-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="3735b-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3735b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3735b-120">-InputObject</span></span>
<span data-ttu-id="3735b-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="3735b-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3735b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3735b-122">-Name</span></span>
<span data-ttu-id="3735b-123">Benutzername</span><span class="sxs-lookup"><span data-stu-id="3735b-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3735b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3735b-124">-PassThru</span></span>
<span data-ttu-id="3735b-125">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3735b-125">returns true if successful</span></span>

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

### <span data-ttu-id="3735b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3735b-126">-ResourceGroupName</span></span>
<span data-ttu-id="3735b-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3735b-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3735b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3735b-128">-ResourceId</span></span>
<span data-ttu-id="3735b-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3735b-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="3735b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3735b-130">-Confirm</span></span>
<span data-ttu-id="3735b-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3735b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3735b-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3735b-132">-WhatIf</span></span>
<span data-ttu-id="3735b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3735b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3735b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3735b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3735b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3735b-135">CommonParameters</span></span>
<span data-ttu-id="3735b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3735b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3735b-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3735b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3735b-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3735b-138">INPUTS</span></span>

### <span data-ttu-id="3735b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3735b-139">System.String</span></span>

### <span data-ttu-id="3735b-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="3735b-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="3735b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3735b-141">OUTPUTS</span></span>

### <span data-ttu-id="3735b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3735b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3735b-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3735b-143">NOTES</span></span>

## <span data-ttu-id="3735b-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3735b-144">RELATED LINKS</span></span>
