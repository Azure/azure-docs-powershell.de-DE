---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: f0c5c52773d5750b86ce82d696e9130df76f4700
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004428"
---
# <span data-ttu-id="f68db-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f68db-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="f68db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f68db-102">SYNOPSIS</span></span>
<span data-ttu-id="f68db-103">Registrieren Sie die Konfiguration für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="f68db-103">Register configuration for resource.</span></span>

## <span data-ttu-id="f68db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f68db-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f68db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f68db-105">DESCRIPTION</span></span>
<span data-ttu-id="f68db-106">Registrieren der Wartungs Konfiguration für die Ressource</span><span class="sxs-lookup"><span data-stu-id="f68db-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="f68db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f68db-107">EXAMPLES</span></span>

### <span data-ttu-id="f68db-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f68db-108">Example 1</span></span>
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

<span data-ttu-id="f68db-109">Registrieren der Wartungs Konfiguration für den didicated-Host</span><span class="sxs-lookup"><span data-stu-id="f68db-109">Register maintenance configuration for didicated host.</span></span>

## <span data-ttu-id="f68db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f68db-110">PARAMETERS</span></span>

### <span data-ttu-id="f68db-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f68db-111">-AsJob</span></span>
<span data-ttu-id="f68db-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f68db-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f68db-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f68db-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="f68db-114">Der Name der Konfigurationsaufgabe sollte mit dem MaintenanceConfigurationName übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f68db-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="f68db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f68db-115">-DefaultProfile</span></span>
<span data-ttu-id="f68db-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f68db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f68db-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="f68db-117">-Location</span></span>
<span data-ttu-id="f68db-118">Die Position ohne Leerzeichen für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="f68db-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="f68db-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f68db-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="f68db-120">Das vollqualifizierte MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f68db-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="f68db-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="f68db-121">-ProviderName</span></span>
<span data-ttu-id="f68db-122">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="f68db-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="f68db-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f68db-123">-ResourceGroupName</span></span>
<span data-ttu-id="f68db-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f68db-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="f68db-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f68db-125">-ResourceId</span></span>
<span data-ttu-id="f68db-126">Der Name der Konfigurationsaufgabe sollte mit dem MaintenanceConfigurationName übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f68db-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="f68db-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f68db-127">-ResourceName</span></span>
<span data-ttu-id="f68db-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f68db-128">The resource name.</span></span>

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

### <span data-ttu-id="f68db-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="f68db-129">-ResourceParentName</span></span>
<span data-ttu-id="f68db-130">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="f68db-130">The parent resource name.</span></span>

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

### <span data-ttu-id="f68db-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="f68db-131">-ResourceParentType</span></span>
<span data-ttu-id="f68db-132">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="f68db-132">The parent resource type.</span></span>

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

### <span data-ttu-id="f68db-133">-</span><span class="sxs-lookup"><span data-stu-id="f68db-133">-ResourceType</span></span>
<span data-ttu-id="f68db-134">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="f68db-134">The resource type.</span></span>

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

### <span data-ttu-id="f68db-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f68db-135">-Confirm</span></span>
<span data-ttu-id="f68db-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f68db-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f68db-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f68db-137">-WhatIf</span></span>
<span data-ttu-id="f68db-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f68db-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f68db-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f68db-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f68db-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f68db-140">CommonParameters</span></span>
<span data-ttu-id="f68db-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f68db-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f68db-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f68db-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f68db-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f68db-143">INPUTS</span></span>

### <span data-ttu-id="f68db-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f68db-144">System.String</span></span>

## <span data-ttu-id="f68db-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f68db-145">OUTPUTS</span></span>

### <span data-ttu-id="f68db-146">Microsoft. Azure. Commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f68db-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="f68db-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="f68db-147">NOTES</span></span>

## <span data-ttu-id="f68db-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f68db-148">RELATED LINKS</span></span>
