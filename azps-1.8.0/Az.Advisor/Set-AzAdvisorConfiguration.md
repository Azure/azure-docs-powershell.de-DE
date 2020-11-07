---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 4c3a3fd8f80bf1f8a18f65a8dc5c9d0bf26b6d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650459"
---
# <span data-ttu-id="7de2e-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="7de2e-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="7de2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7de2e-102">SYNOPSIS</span></span>
<span data-ttu-id="7de2e-103">Aktualisiert oder erstellt die Azure Advisor-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7de2e-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="7de2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7de2e-104">SYNTAX</span></span>

### <span data-ttu-id="7de2e-105">InputObjectRgExcludeParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7de2e-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de2e-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="7de2e-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de2e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7de2e-107">DESCRIPTION</span></span>
<span data-ttu-id="7de2e-108">Wird verwendet, um die Konfiguration des Azure Advisor zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7de2e-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="7de2e-109">Es sind zwei Konfigurationsarten vorhanden: Konfiguration auf Abonnementebene und Konfiguration auf der Ebene der Quell Codegruppen.</span><span class="sxs-lookup"><span data-stu-id="7de2e-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="7de2e-110">Konfiguration auf Abonnementebene: für ein Abonnement kann nur eine Konfiguration für diesen Typ vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7de2e-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="7de2e-111">LowCpuThreshold-und Exclude-Eigenschaften können mit diesem Cmdlet aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7de2e-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="7de2e-112">Konfiguration auf der Ebene "ResourceGroup": Es kann nur eine Konfiguration für jede ResourceGroup geben.</span><span class="sxs-lookup"><span data-stu-id="7de2e-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="7de2e-113">Nur Exclude-Eigenschaft kann mit diesem Cmdlet aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7de2e-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="7de2e-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7de2e-114">EXAMPLES</span></span>

###  <span data-ttu-id="7de2e-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7de2e-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="7de2e-116">Aktualisiert die Konfiguration (lowCpuThreshold) für die Konfiguration auf Abonnementebene.</span><span class="sxs-lookup"><span data-stu-id="7de2e-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="7de2e-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7de2e-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="7de2e-118">Aktualisiert die Konfiguration (lowCpuThreshold, Exclude) für die Konfiguration auf Abonnementebene und schließt aus der Empfehlungs Generierung aus.</span><span class="sxs-lookup"><span data-stu-id="7de2e-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="7de2e-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7de2e-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="7de2e-120">Aktualisiert die Konfiguration (Exclude) für resourceGroupName1, die in der Empfehlungs Generierung ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7de2e-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="7de2e-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="7de2e-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="7de2e-122">Aktualisiert die Konfiguration für die angegebene Empfehlung, die von der Pipeline weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7de2e-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="7de2e-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="7de2e-123">PARAMETERS</span></span>

### <span data-ttu-id="7de2e-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7de2e-124">-Confirm</span></span>
<span data-ttu-id="7de2e-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7de2e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7de2e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de2e-126">-DefaultProfile</span></span>
<span data-ttu-id="7de2e-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7de2e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7de2e-128">-Ausschließen</span><span class="sxs-lookup"><span data-stu-id="7de2e-128">-Exclude</span></span>
<span data-ttu-id="7de2e-129">Aus der Empfehlungs Generierung ausschließen.</span><span class="sxs-lookup"><span data-stu-id="7de2e-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="7de2e-130">Wenn nicht angegeben, wird Exclude-Eigenschaft auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7de2e-130">If not specified exclude property will be set to false.</span></span>

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

### <span data-ttu-id="7de2e-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7de2e-131">-InputObject</span></span>
<span data-ttu-id="7de2e-132">Der von Get-AzAdvisorConfiguration Aufruf zurückgegebene PowerShell-Objekttyp PsAzureAdvisorConfigurationData.</span><span class="sxs-lookup"><span data-stu-id="7de2e-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

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

### <span data-ttu-id="7de2e-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="7de2e-133">-LowCpuThreshold</span></span>
<span data-ttu-id="7de2e-134">Wert für niedrige CPU-Schwelle.</span><span class="sxs-lookup"><span data-stu-id="7de2e-134">Value for Low Cpu threshold.</span></span>

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

### <span data-ttu-id="7de2e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de2e-135">-ResourceGroupName</span></span>
<span data-ttu-id="7de2e-136">Ressourcengruppenname für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7de2e-136">Resource Group name for the configuration.</span></span>

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

### <span data-ttu-id="7de2e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de2e-137">-WhatIf</span></span>
<span data-ttu-id="7de2e-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7de2e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de2e-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7de2e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7de2e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de2e-140">CommonParameters</span></span>
<span data-ttu-id="7de2e-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7de2e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7de2e-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de2e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de2e-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7de2e-143">INPUTS</span></span>

### <span data-ttu-id="7de2e-144">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="7de2e-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="7de2e-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7de2e-145">OUTPUTS</span></span>

### <span data-ttu-id="7de2e-146">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="7de2e-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="7de2e-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="7de2e-147">NOTES</span></span>

## <span data-ttu-id="7de2e-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7de2e-148">RELATED LINKS</span></span>
