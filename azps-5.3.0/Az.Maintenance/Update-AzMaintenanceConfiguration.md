---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470439"
---
# <span data-ttu-id="d3c4f-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3c4f-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="d3c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c4f-103">Patchkonfigurationsdatensatz</span><span class="sxs-lookup"><span data-stu-id="d3c4f-103">Patch configuration record</span></span>

## <span data-ttu-id="d3c4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3c4f-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3c4f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="d3c4f-106">Konfigurationsdatensatz für die Patchwartung</span><span class="sxs-lookup"><span data-stu-id="d3c4f-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="d3c4f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="d3c4f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d3c4f-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="d3c4f-109">Konfigurationsdatensatz für die Patchwartung</span><span class="sxs-lookup"><span data-stu-id="d3c4f-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="d3c4f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3c4f-110">PARAMETERS</span></span>

### <span data-ttu-id="d3c4f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3c4f-111">-AsJob</span></span>
<span data-ttu-id="d3c4f-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d3c4f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3c4f-113">-Configuration</span><span class="sxs-lookup"><span data-stu-id="d3c4f-113">-Configuration</span></span>
<span data-ttu-id="d3c4f-114">Die zu aktualisierende Wartungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d3c4f-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c4f-115">-DefaultProfile</span></span>
<span data-ttu-id="d3c4f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3c4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3c4f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d3c4f-117">-Name</span></span>
<span data-ttu-id="d3c4f-118">Der Name der Wartungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d3c4f-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="d3c4f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3c4f-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3c4f-120">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d3c4f-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="d3c4f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3c4f-121">-Confirm</span></span>
<span data-ttu-id="d3c4f-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3c4f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3c4f-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d3c4f-123">-WhatIf</span></span>
<span data-ttu-id="d3c4f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3c4f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3c4f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3c4f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3c4f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c4f-126">CommonParameters</span></span>
<span data-ttu-id="d3c4f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3c4f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c4f-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3c4f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c4f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3c4f-129">INPUTS</span></span>

### <span data-ttu-id="d3c4f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d3c4f-130">System.String</span></span>

### <span data-ttu-id="d3c4f-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3c4f-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="d3c4f-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3c4f-132">OUTPUTS</span></span>

### <span data-ttu-id="d3c4f-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3c4f-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="d3c4f-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d3c4f-134">NOTES</span></span>

## <span data-ttu-id="d3c4f-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d3c4f-135">RELATED LINKS</span></span>
