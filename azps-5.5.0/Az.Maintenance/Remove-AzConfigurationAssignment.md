---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147569"
---
# <span data-ttu-id="70787-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="70787-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="70787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70787-102">SYNOPSIS</span></span>
<span data-ttu-id="70787-103">Aufheben der Registrierung der Konfiguration für die Ressource</span><span class="sxs-lookup"><span data-stu-id="70787-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="70787-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70787-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70787-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70787-105">DESCRIPTION</span></span>
<span data-ttu-id="70787-106">Aufheben der Registrierung der Konfiguration für die Ressource</span><span class="sxs-lookup"><span data-stu-id="70787-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="70787-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70787-107">EXAMPLES</span></span>

### <span data-ttu-id="70787-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70787-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="70787-109">Aufheben der Registrierung der Konfiguration für die Ressource</span><span class="sxs-lookup"><span data-stu-id="70787-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="70787-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70787-110">PARAMETERS</span></span>

### <span data-ttu-id="70787-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70787-111">-AsJob</span></span>
<span data-ttu-id="70787-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="70787-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70787-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="70787-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="70787-114">Der Name der Konfigurationszuweisung.</span><span class="sxs-lookup"><span data-stu-id="70787-114">The configuration assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70787-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70787-115">-DefaultProfile</span></span>
<span data-ttu-id="70787-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70787-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70787-117">-Force</span><span class="sxs-lookup"><span data-stu-id="70787-117">-Force</span></span>
<span data-ttu-id="70787-118">Erzwingen Sie das Entfernen ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="70787-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="70787-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70787-119">-PassThru</span></span>
<span data-ttu-id="70787-120">Gibt den Status des Vorgangs "Entfernen" zurück.</span><span class="sxs-lookup"><span data-stu-id="70787-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="70787-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="70787-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="70787-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="70787-122">-ProviderName</span></span>
<span data-ttu-id="70787-123">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="70787-123">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70787-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70787-124">-ResourceGroupName</span></span>
<span data-ttu-id="70787-125">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="70787-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70787-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="70787-126">-ResourceName</span></span>
<span data-ttu-id="70787-127">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="70787-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70787-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="70787-128">-ResourceParentName</span></span>
<span data-ttu-id="70787-129">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="70787-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70787-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="70787-130">-ResourceParentType</span></span>
<span data-ttu-id="70787-131">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="70787-131">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70787-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="70787-132">-ResourceType</span></span>
<span data-ttu-id="70787-133">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="70787-133">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70787-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70787-134">-Confirm</span></span>
<span data-ttu-id="70787-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70787-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70787-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="70787-136">-WhatIf</span></span>
<span data-ttu-id="70787-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70787-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70787-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70787-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70787-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70787-139">CommonParameters</span></span>
<span data-ttu-id="70787-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70787-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70787-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70787-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70787-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70787-142">INPUTS</span></span>

### <span data-ttu-id="70787-143">System.String</span><span class="sxs-lookup"><span data-stu-id="70787-143">System.String</span></span>

## <span data-ttu-id="70787-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70787-144">OUTPUTS</span></span>

### <span data-ttu-id="70787-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70787-145">System.Boolean</span></span>

## <span data-ttu-id="70787-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70787-146">NOTES</span></span>

## <span data-ttu-id="70787-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70787-147">RELATED LINKS</span></span>
