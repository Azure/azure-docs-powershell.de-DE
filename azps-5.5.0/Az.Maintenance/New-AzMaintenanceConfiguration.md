---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157513"
---
# <span data-ttu-id="2abc9-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2abc9-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="2abc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2abc9-102">SYNOPSIS</span></span>
<span data-ttu-id="2abc9-103">Erstellen oder Aktualisieren eines Konfigurationsdatensatzs</span><span class="sxs-lookup"><span data-stu-id="2abc9-103">Create or Update configuration record</span></span>

## <span data-ttu-id="2abc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2abc9-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2abc9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2abc9-105">DESCRIPTION</span></span>
<span data-ttu-id="2abc9-106">Erstellen oder Aktualisieren eines Konfigurationsdatensatzs</span><span class="sxs-lookup"><span data-stu-id="2abc9-106">Create or Update configuration record</span></span>

## <span data-ttu-id="2abc9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2abc9-107">EXAMPLES</span></span>

### <span data-ttu-id="2abc9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2abc9-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus -StartDateTime 2020-08-01 00:00 -ExpirationDateTime 2021-08-04 00:00 -TimeZone Pacific Standard Time -Duration 05:00 -RecurEvery Day


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : Host
Visibility          : Custom
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="2abc9-109">Erstellen einer Wartungskonfiguration mit Bereichshost</span><span class="sxs-lookup"><span data-stu-id="2abc9-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="2abc9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2abc9-110">PARAMETERS</span></span>

### <span data-ttu-id="2abc9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2abc9-111">-AsJob</span></span>
<span data-ttu-id="2abc9-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2abc9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2abc9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2abc9-113">-DefaultProfile</span></span>
<span data-ttu-id="2abc9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2abc9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2abc9-115">-Duration</span><span class="sxs-lookup"><span data-stu-id="2abc9-115">-Duration</span></span>
<span data-ttu-id="2abc9-116">Dauer</span><span class="sxs-lookup"><span data-stu-id="2abc9-116">The duration</span></span>


```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abc9-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="2abc9-117">-ExpirationDateTime</span></span>
<span data-ttu-id="2abc9-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span><span class="sxs-lookup"><span data-stu-id="2abc9-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="2abc9-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="2abc9-119">-ExtensionProperty</span></span>
<span data-ttu-id="2abc9-120">Die Erweiterungseigenschaften pro Ressource.</span><span class="sxs-lookup"><span data-stu-id="2abc9-120">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abc9-121">-Location</span><span class="sxs-lookup"><span data-stu-id="2abc9-121">-Location</span></span>
<span data-ttu-id="2abc9-122">Der Speicherort der Wartungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2abc9-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="2abc9-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="2abc9-123">-MaintenanceScope</span></span>
<span data-ttu-id="2abc9-124">Der Wartungsbereich.</span><span class="sxs-lookup"><span data-stu-id="2abc9-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="2abc9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2abc9-125">-Name</span></span>
<span data-ttu-id="2abc9-126">Der Name der Wartungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2abc9-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="2abc9-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="2abc9-127">-RecurEvery</span></span>
<span data-ttu-id="2abc9-128">Terminplanserie</span><span class="sxs-lookup"><span data-stu-id="2abc9-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="2abc9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2abc9-129">-ResourceGroupName</span></span>
<span data-ttu-id="2abc9-130">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="2abc9-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="2abc9-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="2abc9-131">-StartDateTime</span></span>
<span data-ttu-id="2abc9-132">Das Startdatum des Zeitplans im Format JJJJ-MM-TT hh:mm</span><span class="sxs-lookup"><span data-stu-id="2abc9-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="2abc9-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="2abc9-133">-Tag</span></span>
<span data-ttu-id="2abc9-134">Die ARM Tags.</span><span class="sxs-lookup"><span data-stu-id="2abc9-134">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abc9-135">-Zeitzone</span><span class="sxs-lookup"><span data-stu-id="2abc9-135">-Timezone</span></span>
<span data-ttu-id="2abc9-136">Zeitzone</span><span class="sxs-lookup"><span data-stu-id="2abc9-136">The timezone</span></span>

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

### <span data-ttu-id="2abc9-137">-Visibility</span><span class="sxs-lookup"><span data-stu-id="2abc9-137">-Visibility</span></span>
<span data-ttu-id="2abc9-138">Die Sichtbarkeit des Bereichs</span><span class="sxs-lookup"><span data-stu-id="2abc9-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="2abc9-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2abc9-139">-Confirm</span></span>
<span data-ttu-id="2abc9-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2abc9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2abc9-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2abc9-141">-WhatIf</span></span>
<span data-ttu-id="2abc9-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2abc9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2abc9-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2abc9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2abc9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2abc9-144">CommonParameters</span></span>
<span data-ttu-id="2abc9-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2abc9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2abc9-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2abc9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2abc9-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2abc9-147">INPUTS</span></span>

### <span data-ttu-id="2abc9-148">System.String</span><span class="sxs-lookup"><span data-stu-id="2abc9-148">System.String</span></span>

## <span data-ttu-id="2abc9-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2abc9-149">OUTPUTS</span></span>

### <span data-ttu-id="2abc9-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2abc9-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="2abc9-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2abc9-151">NOTES</span></span>

## <span data-ttu-id="2abc9-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2abc9-152">RELATED LINKS</span></span>
