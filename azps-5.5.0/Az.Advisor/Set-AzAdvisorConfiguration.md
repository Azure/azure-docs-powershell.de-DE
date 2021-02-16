---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: bfd1677fa46a749b73206b02bb6585c4a529637f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157644"
---
# <span data-ttu-id="76a29-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="76a29-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="76a29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76a29-102">SYNOPSIS</span></span>
<span data-ttu-id="76a29-103">Aktualisiert oder erstellt die Azure Advisor-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="76a29-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="76a29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76a29-104">SYNTAX</span></span>

### <span data-ttu-id="76a29-105">InputObjectRgExcludeParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="76a29-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76a29-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="76a29-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a29-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76a29-107">DESCRIPTION</span></span>
<span data-ttu-id="76a29-108">Wird verwendet, um die Konfiguration des Azure Advisors zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="76a29-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="76a29-109">Es gibt zwei Konfigurationstypen: Konfiguration auf Abonnementebene und Konfiguration auf Ressourcengruppenebene.</span><span class="sxs-lookup"><span data-stu-id="76a29-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="76a29-110">Konfiguration auf Abonnementebene: Für dieses Abonnement kann es nur eine Konfiguration für diesen Typ geben.</span><span class="sxs-lookup"><span data-stu-id="76a29-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="76a29-111">Die Eigenschaften "LowCpuThreshold" und "Exclude" können mit diesem Cmdlet aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="76a29-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="76a29-112">Konfiguration auf Ressourcengruppenebene: Für jede Ressourcengruppe kann es nur eine Konfiguration gibt.</span><span class="sxs-lookup"><span data-stu-id="76a29-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="76a29-113">Mit diesem Cmdlet kann nur die Eigenschaft "Exclude" aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="76a29-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="76a29-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76a29-114">EXAMPLES</span></span>

###  <span data-ttu-id="76a29-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76a29-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="76a29-116">Aktualisiert die Konfiguration (lowCpuThreshold) für die Konfiguration auf Abonnementebene.</span><span class="sxs-lookup"><span data-stu-id="76a29-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="76a29-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="76a29-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="76a29-118">Aktualisiert die Konfiguration (lowCpuThreshold, exclude) für die Konfiguration auf Abonnementebene und schließt die Empfehlungsgenerierung aus.</span><span class="sxs-lookup"><span data-stu-id="76a29-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="76a29-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="76a29-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="76a29-120">Aktualisiert die Konfiguration(ausschluss) für "resourceGroupName1", die in der Empfehlungsgenerierung ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="76a29-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="76a29-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="76a29-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="76a29-122">Aktualisiert die Konfiguration für die von der Pipeline übergebene Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="76a29-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="76a29-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76a29-123">PARAMETERS</span></span>

### <span data-ttu-id="76a29-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76a29-124">-Confirm</span></span>
<span data-ttu-id="76a29-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76a29-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a29-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a29-126">-DefaultProfile</span></span>
<span data-ttu-id="76a29-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76a29-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a29-128">-Exclude</span><span class="sxs-lookup"><span data-stu-id="76a29-128">-Exclude</span></span>
<span data-ttu-id="76a29-129">Aus der Empfehlungsgenerierung ausschließen.</span><span class="sxs-lookup"><span data-stu-id="76a29-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="76a29-130">Wenn nicht angegeben, wird die "exclude"-Eigenschaft auf "false" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76a29-130">If not specified exclude property will be set to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a29-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76a29-131">-InputObject</span></span>
<span data-ttu-id="76a29-132">Der von einem Aufruf zurückgegebene PsAzureAdvisorConfigurationData-Get-AzAdvisorConfiguration Powershell-Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="76a29-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

```yaml
Type: PsAzureAdvisorConfigurationData
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76a29-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="76a29-133">-LowCpuThreshold</span></span>
<span data-ttu-id="76a29-134">Wert für niedrigen Cpu-Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="76a29-134">Value for Low Cpu threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: InputObjectLowCpuExcludeParameterSet
Aliases:
Accepted values: 0, 5, 10, 15, 20

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a29-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a29-135">-ResourceGroupName</span></span>
<span data-ttu-id="76a29-136">Ressourcengruppenname für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="76a29-136">Resource Group name for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: InputObjectRgExcludeParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a29-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76a29-137">-WhatIf</span></span>
<span data-ttu-id="76a29-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76a29-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a29-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76a29-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a29-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a29-140">CommonParameters</span></span>
<span data-ttu-id="76a29-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a29-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="76a29-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76a29-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a29-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76a29-143">INPUTS</span></span>

### <span data-ttu-id="76a29-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="76a29-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="76a29-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76a29-145">OUTPUTS</span></span>

### <span data-ttu-id="76a29-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="76a29-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="76a29-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76a29-147">NOTES</span></span>

## <span data-ttu-id="76a29-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76a29-148">RELATED LINKS</span></span>
