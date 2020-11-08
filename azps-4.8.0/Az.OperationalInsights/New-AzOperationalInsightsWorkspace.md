---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: feac2aa9c5dd92c0d76090c6fc28353d56f9647c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174239"
---
# <span data-ttu-id="05c8d-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="05c8d-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="05c8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="05c8d-103">Erstellt einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="05c8d-103">Creates a workspace.</span></span>

## <span data-ttu-id="05c8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05c8d-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05c8d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05c8d-105">DESCRIPTION</span></span>
<span data-ttu-id="05c8d-106">Das Cmdlet **New-AzOperationalInsightsWorkspace** erstellt einen Arbeitsbereich in der angegebenen Ressourcengruppe und dem angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="05c8d-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="05c8d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05c8d-107">EXAMPLES</span></span>

### <span data-ttu-id="05c8d-108">Beispiel 1: Erstellen eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="05c8d-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="05c8d-109">Mit diesem Befehl wird ein Standard-SKU-Arbeitsbereich mit dem Namen "myworkspace" in der Ressourcengruppe "ContosoResourceGroup" erstellt.</span><span class="sxs-lookup"><span data-stu-id="05c8d-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="05c8d-110">Beispiel 2: Erstellen eines Arbeitsbereichs und Verknüpfen mit einem vorhandenen Konto</span><span class="sxs-lookup"><span data-stu-id="05c8d-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="05c8d-111">Der erste Befehl verwendet das Get-AzOperationalInsightsLinkTargets-Cmdlet, um die Zielvorgaben für das Konto "operative Einblicke" abzurufen, und speichert Sie dann in der $OILinkTargets-Variablen.</span><span class="sxs-lookup"><span data-stu-id="05c8d-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="05c8d-112">Der zweite Befehl übergibt das erste Konto Verknüpfungsziel in $OILinkTargets an das Cmdlet **New-AzOperationalInsightsWorkspace** mithilfe des Pipelineoperators.</span><span class="sxs-lookup"><span data-stu-id="05c8d-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="05c8d-113">Mit dem Befehl wird ein Standard-SKU-Arbeitsbereich mit dem Namen myworkspace erstellt, der mit dem ersten Operational Insights-Konto in $OILinkTargets verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="05c8d-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="05c8d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="05c8d-114">PARAMETERS</span></span>

### <span data-ttu-id="05c8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c8d-115">-DefaultProfile</span></span>
<span data-ttu-id="05c8d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="05c8d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05c8d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="05c8d-117">-Force</span></span>
<span data-ttu-id="05c8d-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="05c8d-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="05c8d-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="05c8d-119">-Location</span></span>
<span data-ttu-id="05c8d-120">Gibt den Speicherort an, an dem der Arbeitsbereich erstellt werden soll, beispielsweise Ost-oder West Europa.</span><span class="sxs-lookup"><span data-stu-id="05c8d-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="05c8d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="05c8d-121">-Name</span></span>
<span data-ttu-id="05c8d-122">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="05c8d-122">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="05c8d-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="05c8d-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="05c8d-124">Der Netzwerkzugriffstyp für den Zugriff auf die Arbeitsbereichs Aufnahme.</span><span class="sxs-lookup"><span data-stu-id="05c8d-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="05c8d-125">Der Wert sollte "aktiviert" oder "deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="05c8d-125">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="05c8d-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="05c8d-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="05c8d-127">Der Netzwerkzugriffstyp für den Zugriff auf die Arbeitsbereichs Abfrage.</span><span class="sxs-lookup"><span data-stu-id="05c8d-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="05c8d-128">Der Wert sollte "aktiviert" oder "deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="05c8d-128">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="05c8d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c8d-129">-ResourceGroupName</span></span>
<span data-ttu-id="05c8d-130">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="05c8d-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="05c8d-131">Der Arbeitsbereich wird in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="05c8d-131">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="05c8d-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="05c8d-132">-RetentionInDays</span></span>
<span data-ttu-id="05c8d-133">Die Aufbewahrung von Arbeitsbereichsdaten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="05c8d-133">The workspace data retention in days.</span></span> <span data-ttu-id="05c8d-134">730 Tage ist der maximal zulässige Wert für alle anderen SKUs</span><span class="sxs-lookup"><span data-stu-id="05c8d-134">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="05c8d-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="05c8d-135">-Sku</span></span>
<span data-ttu-id="05c8d-136">Gibt die Dienstebene des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="05c8d-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="05c8d-137">Weitere Informationen zu dem zu verwendenden Wert finden Sie unter https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="05c8d-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="05c8d-138">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="05c8d-138">Valid values are:</span></span>
- <span data-ttu-id="05c8d-139">kostenlos</span><span class="sxs-lookup"><span data-stu-id="05c8d-139">free</span></span>
- <span data-ttu-id="05c8d-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="05c8d-140">pergb2018</span></span>
- <span data-ttu-id="05c8d-141">pernode</span><span class="sxs-lookup"><span data-stu-id="05c8d-141">pernode</span></span>
- <span data-ttu-id="05c8d-142">Premium</span><span class="sxs-lookup"><span data-stu-id="05c8d-142">premium</span></span>
- <span data-ttu-id="05c8d-143">Standalone</span><span class="sxs-lookup"><span data-stu-id="05c8d-143">standalone</span></span>
- <span data-ttu-id="05c8d-144">Standard</span><span class="sxs-lookup"><span data-stu-id="05c8d-144">standard</span></span>

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

### <span data-ttu-id="05c8d-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="05c8d-145">-Tag</span></span>
<span data-ttu-id="05c8d-146">Die Ressourcenkategorien für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="05c8d-146">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="05c8d-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05c8d-147">-Confirm</span></span>
<span data-ttu-id="05c8d-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05c8d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05c8d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05c8d-149">-WhatIf</span></span>
<span data-ttu-id="05c8d-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05c8d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05c8d-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05c8d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05c8d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c8d-152">CommonParameters</span></span>
<span data-ttu-id="05c8d-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05c8d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c8d-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05c8d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c8d-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05c8d-155">INPUTS</span></span>

### <span data-ttu-id="05c8d-156">System. String</span><span class="sxs-lookup"><span data-stu-id="05c8d-156">System.String</span></span>

### <span data-ttu-id="05c8d-157">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="05c8d-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="05c8d-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="05c8d-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="05c8d-159">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="05c8d-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="05c8d-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05c8d-160">OUTPUTS</span></span>

### <span data-ttu-id="05c8d-161">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="05c8d-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="05c8d-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="05c8d-162">NOTES</span></span>

<span data-ttu-id="05c8d-163">Es wurde ein neues Preismodell veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="05c8d-163">A new pricing model has been released.</span></span> <span data-ttu-id="05c8d-164">Wenn Sie ein CSP sind, bedeutet dies, dass Sie "Standalone" für die SKU verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="05c8d-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="05c8d-165">Hinter den Kulissen wird die SKU in pergb2018 geändert.</span><span class="sxs-lookup"><span data-stu-id="05c8d-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="05c8d-166">Weitere Informationen finden Sie in den folgenden Themen: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="05c8d-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="05c8d-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05c8d-167">RELATED LINKS</span></span>

[<span data-ttu-id="05c8d-168">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="05c8d-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="05c8d-169">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="05c8d-169">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


