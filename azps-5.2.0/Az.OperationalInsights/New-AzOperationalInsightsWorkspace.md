---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 50920451ca96d21875352ff2ef460a5dcc989a20
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295180"
---
# <span data-ttu-id="8d9e2-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8d9e2-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="8d9e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9e2-103">Erstellt einen Arbeitsbereich oder stellt einen weich gelöschten Arbeitsbereich wieder zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-103">Creates a workspace, or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="8d9e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d9e2-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d9e2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="8d9e2-106">Das **Cmdlet "New-AzOperationalInsightsWorkspace"** erstellt einen Arbeitsbereich in der angegebenen Ressourcengruppe und dem angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span> <span data-ttu-id="8d9e2-107">Oder stellen Sie einen soft gelöschten Arbeitsbereich wieder zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-107">Or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="8d9e2-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d9e2-108">EXAMPLES</span></span>

### <span data-ttu-id="8d9e2-109">Beispiel 1: Erstellen eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="8d9e2-109">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="8d9e2-110">Mit diesem Befehl wird ein Standard-SKU-Arbeitsbereich mit dem Namen "MyWorkspace" in der Ressourcengruppe "ContosoResourceGroup" erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-110">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8d9e2-111">Beispiel 2: Erstellen eines Arbeitsbereichs und Verknüpfen mit einem vorhandenen Konto</span><span class="sxs-lookup"><span data-stu-id="8d9e2-111">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="8d9e2-112">Der erste Befehl verwendet das Get-AzOperationalInsightsLinkTargets Cmdlet, um Die Linkziele für das Konto "Operational Insights" zu erhalten, und speichert sie dann in der $OILinkTargets Variable.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-112">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="8d9e2-113">Der zweite Befehl übergibt das erste Kontoverknüpfungsziel in $OILinkTargets mithilfe des Pipelineoperators an das **Cmdlet "New-AzOperationalInsightsWorkspace".**</span><span class="sxs-lookup"><span data-stu-id="8d9e2-113">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8d9e2-114">Der Befehl erstellt einen Standard-SKU-Arbeitsbereich namens "MyWorkspace", der mit dem ersten Konto für betriebliche Einblicke in $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-114">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="8d9e2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d9e2-115">PARAMETERS</span></span>

### <span data-ttu-id="8d9e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9e2-116">-DefaultProfile</span></span>
<span data-ttu-id="8d9e2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8d9e2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d9e2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8d9e2-118">-Force</span></span>
<span data-ttu-id="8d9e2-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d9e2-120">-Location</span><span class="sxs-lookup"><span data-stu-id="8d9e2-120">-Location</span></span>
<span data-ttu-id="8d9e2-121">Gibt den Speicherort an, an dem der Arbeitsbereich erstellt werden soll, z. B. "Ost-USA" oder "Westeuropa".</span><span class="sxs-lookup"><span data-stu-id="8d9e2-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="8d9e2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8d9e2-122">-Name</span></span>
<span data-ttu-id="8d9e2-123">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-123">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="8d9e2-124">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="8d9e2-124">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="8d9e2-125">Der Netzwerkzugriffstyp für den Zugriff auf die Erfassung des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-125">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="8d9e2-126">Der Wert sollte "Enabled" oder "Disabled" sein.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-126">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e2-127">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="8d9e2-127">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="8d9e2-128">Der Netzwerkzugriffstyp für den Zugriff auf Arbeitsbereichsabfragen.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-128">The network access type for accessing workspace query.</span></span> <span data-ttu-id="8d9e2-129">Der Wert sollte "Enabled" oder "Disabled" sein.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-129">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d9e2-130">-ResourceGroupName</span></span>
<span data-ttu-id="8d9e2-131">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8d9e2-132">Der Arbeitsbereich wird in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-132">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="8d9e2-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8d9e2-133">-RetentionInDays</span></span>
<span data-ttu-id="8d9e2-134">Die Aufbewahrung von Arbeitsbereichsdaten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-134">The workspace data retention in days.</span></span> <span data-ttu-id="8d9e2-135">730 Tage sind die maximal zulässigen Für alle anderen SKU</span><span class="sxs-lookup"><span data-stu-id="8d9e2-135">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e2-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="8d9e2-136">-Sku</span></span>
<span data-ttu-id="8d9e2-137">Gibt die Dienstebene des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-137">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="8d9e2-138">Weitere Informationen dazu, welchen Wert Sie verwenden sollten, finden Sie unter https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="8d9e2-138">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="8d9e2-139">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="8d9e2-139">Valid values are:</span></span>
- <span data-ttu-id="8d9e2-140">kostenlos</span><span class="sxs-lookup"><span data-stu-id="8d9e2-140">free</span></span>
- <span data-ttu-id="8d9e2-141">pergb2018</span><span class="sxs-lookup"><span data-stu-id="8d9e2-141">pergb2018</span></span>
- <span data-ttu-id="8d9e2-142">pernode</span><span class="sxs-lookup"><span data-stu-id="8d9e2-142">pernode</span></span>
- <span data-ttu-id="8d9e2-143">Premium</span><span class="sxs-lookup"><span data-stu-id="8d9e2-143">premium</span></span>
- <span data-ttu-id="8d9e2-144">Eigenständig</span><span class="sxs-lookup"><span data-stu-id="8d9e2-144">standalone</span></span>
- <span data-ttu-id="8d9e2-145">Standard</span><span class="sxs-lookup"><span data-stu-id="8d9e2-145">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e2-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="8d9e2-146">-Tag</span></span>
<span data-ttu-id="8d9e2-147">Die Ressourcentags für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-147">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e2-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d9e2-148">-Confirm</span></span>
<span data-ttu-id="8d9e2-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e2-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8d9e2-150">-WhatIf</span></span>
<span data-ttu-id="8d9e2-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d9e2-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9e2-153">CommonParameters</span></span>
<span data-ttu-id="8d9e2-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9e2-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d9e2-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9e2-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d9e2-156">INPUTS</span></span>

### <span data-ttu-id="8d9e2-157">System.String</span><span class="sxs-lookup"><span data-stu-id="8d9e2-157">System.String</span></span>

### <span data-ttu-id="8d9e2-158">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8d9e2-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8d9e2-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8d9e2-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8d9e2-160">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8d9e2-160">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8d9e2-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d9e2-161">OUTPUTS</span></span>

### <span data-ttu-id="8d9e2-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8d9e2-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="8d9e2-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8d9e2-163">NOTES</span></span>

<span data-ttu-id="8d9e2-164">Ein neues Preismodell wurde veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-164">A new pricing model has been released.</span></span> <span data-ttu-id="8d9e2-165">Wenn Sie ein CSP sind, bedeutet dies, dass Sie für die SKU "eigenständig" verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-165">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="8d9e2-166">Hinter den Kulissen wird die SKU in "pergb2018" geändert.</span><span class="sxs-lookup"><span data-stu-id="8d9e2-166">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="8d9e2-167">Weitere Informationen finden Sie in den folgenden Themen: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="8d9e2-167">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="8d9e2-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8d9e2-168">RELATED LINKS</span></span>

[<span data-ttu-id="8d9e2-169">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8d9e2-169">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="8d9e2-170">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="8d9e2-170">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


