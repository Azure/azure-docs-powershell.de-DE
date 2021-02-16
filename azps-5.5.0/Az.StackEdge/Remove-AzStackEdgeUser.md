---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163068"
---
# <span data-ttu-id="c9a1b-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c9a1b-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="c9a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a1b-103">Entfernt einen Benutzer auf einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="c9a1b-103">Removes a user on a device.</span></span>

## <span data-ttu-id="c9a1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9a1b-104">SYNTAX</span></span>

### <span data-ttu-id="c9a1b-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9a1b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9a1b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9a1b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9a1b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9a1b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9a1b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9a1b-108">DESCRIPTION</span></span>
<span data-ttu-id="c9a1b-109">Das **Cmdlet "Remove-AzStackEdgeUser"** entfernt einen Benutzer auf dem Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="c9a1b-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="c9a1b-110">Die Erstellung nur von Typbenutzern `Share` wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9a1b-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="c9a1b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c9a1b-111">EXAMPLES</span></span>

### <span data-ttu-id="c9a1b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c9a1b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="c9a1b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9a1b-113">PARAMETERS</span></span>

### <span data-ttu-id="c9a1b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9a1b-114">-AsJob</span></span>
<span data-ttu-id="c9a1b-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c9a1b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9a1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a1b-116">-DefaultProfile</span></span>
<span data-ttu-id="c9a1b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9a1b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9a1b-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c9a1b-118">-DeviceName</span></span>
<span data-ttu-id="c9a1b-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="c9a1b-119">Device Name</span></span>

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

### <span data-ttu-id="c9a1b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9a1b-120">-InputObject</span></span>
<span data-ttu-id="c9a1b-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="c9a1b-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9a1b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c9a1b-122">-Name</span></span>
<span data-ttu-id="c9a1b-123">Benutzername</span><span class="sxs-lookup"><span data-stu-id="c9a1b-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9a1b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9a1b-124">-PassThru</span></span>
<span data-ttu-id="c9a1b-125">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c9a1b-125">returns true if successful</span></span>

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

### <span data-ttu-id="c9a1b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a1b-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9a1b-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c9a1b-127">Resource Group Name</span></span>

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

### <span data-ttu-id="c9a1b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9a1b-128">-ResourceId</span></span>
<span data-ttu-id="c9a1b-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9a1b-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="c9a1b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9a1b-130">-Confirm</span></span>
<span data-ttu-id="c9a1b-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9a1b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9a1b-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c9a1b-132">-WhatIf</span></span>
<span data-ttu-id="c9a1b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9a1b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9a1b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9a1b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9a1b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a1b-135">CommonParameters</span></span>
<span data-ttu-id="c9a1b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9a1b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a1b-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9a1b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a1b-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c9a1b-138">INPUTS</span></span>

### <span data-ttu-id="c9a1b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c9a1b-139">System.String</span></span>

### <span data-ttu-id="c9a1b-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="c9a1b-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="c9a1b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c9a1b-141">OUTPUTS</span></span>

### <span data-ttu-id="c9a1b-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c9a1b-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c9a1b-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c9a1b-143">NOTES</span></span>

## <span data-ttu-id="c9a1b-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c9a1b-144">RELATED LINKS</span></span>
