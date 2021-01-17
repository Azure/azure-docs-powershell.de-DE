---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 602ad3506f4a4fc0f8aa22128ca223e6a90f6ab5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458471"
---
# <span data-ttu-id="0e52d-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0e52d-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="0e52d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e52d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e52d-103">Löscht eine Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="0e52d-103">Deletes a service instance.</span></span>

## <span data-ttu-id="0e52d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e52d-104">SYNTAX</span></span>

### <span data-ttu-id="0e52d-105">ServiceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e52d-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e52d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e52d-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e52d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e52d-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e52d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e52d-108">DESCRIPTION</span></span>
<span data-ttu-id="0e52d-109">Löscht eine Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="0e52d-109">Deletes a service instance.</span></span>

## <span data-ttu-id="0e52d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0e52d-110">EXAMPLES</span></span>

### <span data-ttu-id="0e52d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e52d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="0e52d-112">Löscht den vorhandenen Dienst "HealthcareApis" mit dem bereitgestellten Namen innerhalb einer bereitgestellten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0e52d-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="0e52d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0e52d-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="0e52d-114">Löscht den vorhandenen Dienst "HealthcareApis" mit der bereitgestellten ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0e52d-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="0e52d-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0e52d-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="0e52d-116">Löscht das bereitgestellte Dienstobjekt "HealthcareApis".</span><span class="sxs-lookup"><span data-stu-id="0e52d-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="0e52d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e52d-117">PARAMETERS</span></span>

### <span data-ttu-id="0e52d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e52d-118">-AsJob</span></span>
<span data-ttu-id="0e52d-119">Führen Sie das Cmdlet als Aufgabe im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="0e52d-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="0e52d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e52d-120">-DefaultProfile</span></span>
<span data-ttu-id="0e52d-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e52d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e52d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e52d-122">-InputObject</span></span>
<span data-ttu-id="0e52d-123">Dienstobjekt "HealthcareApis"</span><span class="sxs-lookup"><span data-stu-id="0e52d-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e52d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0e52d-124">-Name</span></span>
<span data-ttu-id="0e52d-125">Dienstname von HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="0e52d-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e52d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e52d-126">-PassThru</span></span>
<span data-ttu-id="0e52d-127">Wenn angegeben, wird "true" zurückgegeben, wenn der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0e52d-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="0e52d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e52d-128">-ResourceGroupName</span></span>
<span data-ttu-id="0e52d-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0e52d-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e52d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e52d-130">-ResourceId</span></span>
<span data-ttu-id="0e52d-131">DienstressourceId des Gesundheitswesens.</span><span class="sxs-lookup"><span data-stu-id="0e52d-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e52d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e52d-132">-Confirm</span></span>
<span data-ttu-id="0e52d-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e52d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e52d-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0e52d-134">-WhatIf</span></span>
<span data-ttu-id="0e52d-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e52d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e52d-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e52d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e52d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e52d-137">CommonParameters</span></span>
<span data-ttu-id="0e52d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e52d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e52d-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e52d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e52d-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0e52d-140">INPUTS</span></span>

### <span data-ttu-id="0e52d-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0e52d-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="0e52d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0e52d-142">System.String</span></span>

## <span data-ttu-id="0e52d-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0e52d-143">OUTPUTS</span></span>

### <span data-ttu-id="0e52d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e52d-144">System.Boolean</span></span>

## <span data-ttu-id="0e52d-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0e52d-145">NOTES</span></span>

## <span data-ttu-id="0e52d-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0e52d-146">RELATED LINKS</span></span>
