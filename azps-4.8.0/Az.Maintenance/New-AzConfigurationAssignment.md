---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166350"
---
# <span data-ttu-id="c6c1a-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="c6c1a-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="c6c1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c1a-103">Registrieren Sie die Konfiguration für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-103">Register configuration for resource.</span></span>

## <span data-ttu-id="c6c1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6c1a-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6c1a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6c1a-105">DESCRIPTION</span></span>
<span data-ttu-id="c6c1a-106">Registrieren der Wartungs Konfiguration für die Ressource</span><span class="sxs-lookup"><span data-stu-id="c6c1a-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="c6c1a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6c1a-107">EXAMPLES</span></span>

### <span data-ttu-id="c6c1a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6c1a-108">Example 1</span></span>
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

<span data-ttu-id="c6c1a-109">Registrieren der Wartungs Konfiguration für dedizierten Host.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="c6c1a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6c1a-110">PARAMETERS</span></span>

### <span data-ttu-id="c6c1a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6c1a-111">-AsJob</span></span>
<span data-ttu-id="c6c1a-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c6c1a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6c1a-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="c6c1a-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="c6c1a-114">Der Name der Konfigurationsaufgabe sollte mit dem MaintenanceConfigurationName übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="c6c1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c1a-115">-DefaultProfile</span></span>
<span data-ttu-id="c6c1a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c1a-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="c6c1a-117">-Location</span></span>
<span data-ttu-id="c6c1a-118">Die Position ohne Leerzeichen für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="c6c1a-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c6c1a-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="c6c1a-120">Das vollqualifizierte MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="c6c1a-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="c6c1a-121">-ProviderName</span></span>
<span data-ttu-id="c6c1a-122">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="c6c1a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c1a-123">-ResourceGroupName</span></span>
<span data-ttu-id="c6c1a-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="c6c1a-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c6c1a-125">-ResourceId</span></span>
<span data-ttu-id="c6c1a-126">Der Name der Konfigurationsaufgabe sollte mit dem MaintenanceConfigurationName übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="c6c1a-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c6c1a-127">-ResourceName</span></span>
<span data-ttu-id="c6c1a-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-128">The resource name.</span></span>

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

### <span data-ttu-id="c6c1a-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="c6c1a-129">-ResourceParentName</span></span>
<span data-ttu-id="c6c1a-130">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-130">The parent resource name.</span></span>

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

### <span data-ttu-id="c6c1a-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="c6c1a-131">-ResourceParentType</span></span>
<span data-ttu-id="c6c1a-132">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-132">The parent resource type.</span></span>

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

### <span data-ttu-id="c6c1a-133">-</span><span class="sxs-lookup"><span data-stu-id="c6c1a-133">-ResourceType</span></span>
<span data-ttu-id="c6c1a-134">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-134">The resource type.</span></span>

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

### <span data-ttu-id="c6c1a-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6c1a-135">-Confirm</span></span>
<span data-ttu-id="c6c1a-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6c1a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6c1a-137">-WhatIf</span></span>
<span data-ttu-id="c6c1a-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6c1a-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6c1a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c1a-140">CommonParameters</span></span>
<span data-ttu-id="c6c1a-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c1a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c1a-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6c1a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c1a-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6c1a-143">INPUTS</span></span>

### <span data-ttu-id="c6c1a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c6c1a-144">System.String</span></span>

## <span data-ttu-id="c6c1a-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6c1a-145">OUTPUTS</span></span>

### <span data-ttu-id="c6c1a-146">Microsoft. Azure. Commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="c6c1a-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="c6c1a-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6c1a-147">NOTES</span></span>

## <span data-ttu-id="c6c1a-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6c1a-148">RELATED LINKS</span></span>
