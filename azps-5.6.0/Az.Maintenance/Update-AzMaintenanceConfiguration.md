---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: d2131d542d845e065e1aae05a272b045ffa882f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935696"
---
# <span data-ttu-id="8da1b-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8da1b-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="8da1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8da1b-102">SYNOPSIS</span></span>
<span data-ttu-id="8da1b-103">Patchkonfigurationsdatensatz</span><span class="sxs-lookup"><span data-stu-id="8da1b-103">Patch configuration record</span></span>

## <span data-ttu-id="8da1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8da1b-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da1b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8da1b-105">DESCRIPTION</span></span>
<span data-ttu-id="8da1b-106">Konfigurationsdatensatz für die Patchwartung</span><span class="sxs-lookup"><span data-stu-id="8da1b-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="8da1b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8da1b-107">EXAMPLES</span></span>

### <span data-ttu-id="8da1b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8da1b-108">Example 1</span></span>
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

<span data-ttu-id="8da1b-109">Konfigurationsdatensatz für die Patchwartung</span><span class="sxs-lookup"><span data-stu-id="8da1b-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="8da1b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8da1b-110">PARAMETERS</span></span>

### <span data-ttu-id="8da1b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8da1b-111">-AsJob</span></span>
<span data-ttu-id="8da1b-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8da1b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8da1b-113">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="8da1b-113">-Configuration</span></span>
<span data-ttu-id="8da1b-114">Die Wartungskonfiguration, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8da1b-114">The maintenance configuration to be updated.</span></span>

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

### <span data-ttu-id="8da1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da1b-115">-DefaultProfile</span></span>
<span data-ttu-id="8da1b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8da1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8da1b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8da1b-117">-Name</span></span>
<span data-ttu-id="8da1b-118">Name der Wartungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="8da1b-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="8da1b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da1b-119">-ResourceGroupName</span></span>
<span data-ttu-id="8da1b-120">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="8da1b-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="8da1b-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8da1b-121">-Confirm</span></span>
<span data-ttu-id="8da1b-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8da1b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da1b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da1b-123">-WhatIf</span></span>
<span data-ttu-id="8da1b-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8da1b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8da1b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8da1b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da1b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da1b-126">CommonParameters</span></span>
<span data-ttu-id="8da1b-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da1b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da1b-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8da1b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da1b-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8da1b-129">INPUTS</span></span>

### <span data-ttu-id="8da1b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8da1b-130">System.String</span></span>

### <span data-ttu-id="8da1b-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8da1b-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="8da1b-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8da1b-132">OUTPUTS</span></span>

### <span data-ttu-id="8da1b-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8da1b-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="8da1b-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8da1b-134">NOTES</span></span>

## <span data-ttu-id="8da1b-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8da1b-135">RELATED LINKS</span></span>
