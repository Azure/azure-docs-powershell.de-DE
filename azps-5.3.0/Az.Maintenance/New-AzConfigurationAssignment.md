---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472305"
---
# <span data-ttu-id="caf1c-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="caf1c-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="caf1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caf1c-102">SYNOPSIS</span></span>
<span data-ttu-id="caf1c-103">Registrieren sie die Konfiguration für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="caf1c-103">Register configuration for resource.</span></span>

## <span data-ttu-id="caf1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="caf1c-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="caf1c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="caf1c-105">DESCRIPTION</span></span>
<span data-ttu-id="caf1c-106">Registrieren sie die Wartungskonfiguration für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="caf1c-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="caf1c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="caf1c-107">EXAMPLES</span></span>

### <span data-ttu-id="caf1c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="caf1c-108">Example 1</span></span>
```powershell
PS C:\> New-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName -MaintenanceConfigurationId $maintenanceConfigurationCreated.Id -Location $location


Location                   : westus2
MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
ResourceId                 : 7b32ed22-dc7b-4a17-9c42-36c024f4c9f9
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="caf1c-109">Registrieren Sie die Wartungskonfiguration für einen dedizierten Host.</span><span class="sxs-lookup"><span data-stu-id="caf1c-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="caf1c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="caf1c-110">PARAMETERS</span></span>

### <span data-ttu-id="caf1c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="caf1c-111">-AsJob</span></span>
<span data-ttu-id="caf1c-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="caf1c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="caf1c-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="caf1c-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="caf1c-114">Der Name der Konfigurationszuweisung sollte mit "MaintenanceConfigurationName" übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="caf1c-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="caf1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf1c-115">-DefaultProfile</span></span>
<span data-ttu-id="caf1c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="caf1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caf1c-117">-Location</span><span class="sxs-lookup"><span data-stu-id="caf1c-117">-Location</span></span>
<span data-ttu-id="caf1c-118">Der Ort ohne Leerzeichen für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="caf1c-118">The location without spaces for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf1c-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="caf1c-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="caf1c-120">Die vollqualifizierte MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="caf1c-120">The fully qualified MaintenanceConfiguration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf1c-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="caf1c-121">-ProviderName</span></span>
<span data-ttu-id="caf1c-122">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="caf1c-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="caf1c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caf1c-123">-ResourceGroupName</span></span>
<span data-ttu-id="caf1c-124">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="caf1c-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="caf1c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caf1c-125">-ResourceId</span></span>
<span data-ttu-id="caf1c-126">Der Name der Konfigurationszuweisung sollte mit "MaintenanceConfigurationName" übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="caf1c-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf1c-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="caf1c-127">-ResourceName</span></span>
<span data-ttu-id="caf1c-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="caf1c-128">The resource name.</span></span>

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

### <span data-ttu-id="caf1c-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="caf1c-129">-ResourceParentName</span></span>
<span data-ttu-id="caf1c-130">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="caf1c-130">The parent resource name.</span></span>

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

### <span data-ttu-id="caf1c-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="caf1c-131">-ResourceParentType</span></span>
<span data-ttu-id="caf1c-132">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="caf1c-132">The parent resource type.</span></span>

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

### <span data-ttu-id="caf1c-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="caf1c-133">-ResourceType</span></span>
<span data-ttu-id="caf1c-134">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="caf1c-134">The resource type.</span></span>

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

### <span data-ttu-id="caf1c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caf1c-135">-Confirm</span></span>
<span data-ttu-id="caf1c-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="caf1c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caf1c-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="caf1c-137">-WhatIf</span></span>
<span data-ttu-id="caf1c-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="caf1c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caf1c-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="caf1c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caf1c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf1c-140">CommonParameters</span></span>
<span data-ttu-id="caf1c-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caf1c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf1c-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="caf1c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf1c-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="caf1c-143">INPUTS</span></span>

### <span data-ttu-id="caf1c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="caf1c-144">System.String</span></span>

## <span data-ttu-id="caf1c-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="caf1c-145">OUTPUTS</span></span>

### <span data-ttu-id="caf1c-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="caf1c-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="caf1c-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="caf1c-147">NOTES</span></span>

## <span data-ttu-id="caf1c-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="caf1c-148">RELATED LINKS</span></span>
