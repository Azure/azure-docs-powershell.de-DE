---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166342"
---
# <span data-ttu-id="4629a-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4629a-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="4629a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4629a-102">SYNOPSIS</span></span>
<span data-ttu-id="4629a-103">Erstellen oder Aktualisieren eines Konfigurationseintrags</span><span class="sxs-lookup"><span data-stu-id="4629a-103">Create or Update configuration record</span></span>

## <span data-ttu-id="4629a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4629a-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4629a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4629a-105">DESCRIPTION</span></span>
<span data-ttu-id="4629a-106">Erstellen oder Aktualisieren eines Konfigurationseintrags</span><span class="sxs-lookup"><span data-stu-id="4629a-106">Create or Update configuration record</span></span>

## <span data-ttu-id="4629a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4629a-107">EXAMPLES</span></span>

### <span data-ttu-id="4629a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4629a-108">Example 1</span></span>
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

<span data-ttu-id="4629a-109">Erstellen einer Wartungs Konfiguration mit Scope-Host</span><span class="sxs-lookup"><span data-stu-id="4629a-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="4629a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4629a-110">PARAMETERS</span></span>

### <span data-ttu-id="4629a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4629a-111">-AsJob</span></span>
<span data-ttu-id="4629a-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4629a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4629a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4629a-113">-DefaultProfile</span></span>
<span data-ttu-id="4629a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4629a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4629a-115">-Dauer</span><span class="sxs-lookup"><span data-stu-id="4629a-115">-Duration</span></span>
<span data-ttu-id="4629a-116">Die Dauer</span><span class="sxs-lookup"><span data-stu-id="4629a-116">The duration</span></span>


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

### <span data-ttu-id="4629a-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="4629a-117">-ExpirationDateTime</span></span>
<span data-ttu-id="4629a-118">Die expirationDateTime des Zeitplans im Format yyyy-mm-tt hh: mm</span><span class="sxs-lookup"><span data-stu-id="4629a-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="4629a-119">-Extensionproperty</span><span class="sxs-lookup"><span data-stu-id="4629a-119">-ExtensionProperty</span></span>
<span data-ttu-id="4629a-120">Die Erweiterungseigenschaften pro Ressource.</span><span class="sxs-lookup"><span data-stu-id="4629a-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="4629a-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="4629a-121">-Location</span></span>
<span data-ttu-id="4629a-122">Der Speicherort der Wartungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4629a-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="4629a-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="4629a-123">-MaintenanceScope</span></span>
<span data-ttu-id="4629a-124">Der Wartungsbereich.</span><span class="sxs-lookup"><span data-stu-id="4629a-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="4629a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4629a-125">-Name</span></span>
<span data-ttu-id="4629a-126">Der Name der Wartungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4629a-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="4629a-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="4629a-127">-RecurEvery</span></span>
<span data-ttu-id="4629a-128">Die Terminplan Serie</span><span class="sxs-lookup"><span data-stu-id="4629a-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="4629a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4629a-129">-ResourceGroupName</span></span>
<span data-ttu-id="4629a-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4629a-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="4629a-131">-Startdatum</span><span class="sxs-lookup"><span data-stu-id="4629a-131">-StartDateTime</span></span>
<span data-ttu-id="4629a-132">Das Startdatum des Terminplans im Format yyyy-mm-tt hh: mm</span><span class="sxs-lookup"><span data-stu-id="4629a-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="4629a-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="4629a-133">-Tag</span></span>
<span data-ttu-id="4629a-134">Die Arm-Tags.</span><span class="sxs-lookup"><span data-stu-id="4629a-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="4629a-135">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="4629a-135">-Timezone</span></span>
<span data-ttu-id="4629a-136">Zeitzone</span><span class="sxs-lookup"><span data-stu-id="4629a-136">The timezone</span></span>

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

### <span data-ttu-id="4629a-137">– Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="4629a-137">-Visibility</span></span>
<span data-ttu-id="4629a-138">Die Sichtbarkeit des Bereichs</span><span class="sxs-lookup"><span data-stu-id="4629a-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="4629a-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4629a-139">-Confirm</span></span>
<span data-ttu-id="4629a-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4629a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4629a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4629a-141">-WhatIf</span></span>
<span data-ttu-id="4629a-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4629a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4629a-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4629a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4629a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4629a-144">CommonParameters</span></span>
<span data-ttu-id="4629a-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4629a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4629a-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4629a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4629a-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4629a-147">INPUTS</span></span>

### <span data-ttu-id="4629a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4629a-148">System.String</span></span>

## <span data-ttu-id="4629a-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4629a-149">OUTPUTS</span></span>

### <span data-ttu-id="4629a-150">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4629a-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="4629a-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="4629a-151">NOTES</span></span>

## <span data-ttu-id="4629a-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4629a-152">RELATED LINKS</span></span>
