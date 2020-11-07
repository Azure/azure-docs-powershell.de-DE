---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 863b83cbab64d791e55f8cfc2719d66be64fcac6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847940"
---
# <span data-ttu-id="09022-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="09022-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="09022-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09022-102">SYNOPSIS</span></span>
<span data-ttu-id="09022-103">Erstellt einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="09022-103">Creates a workspace.</span></span>

## <span data-ttu-id="09022-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09022-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09022-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09022-105">DESCRIPTION</span></span>
<span data-ttu-id="09022-106">Das Cmdlet **New-AzOperationalInsightsWorkspace** erstellt einen Arbeitsbereich in der angegebenen Ressourcengruppe und dem angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="09022-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="09022-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09022-107">EXAMPLES</span></span>

### <span data-ttu-id="09022-108">Beispiel 1: Erstellen eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="09022-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="09022-109">Mit diesem Befehl wird ein Standard-SKU-Arbeitsbereich mit dem Namen "myworkspace" in der Ressourcengruppe "ContosoResourceGroup" erstellt.</span><span class="sxs-lookup"><span data-stu-id="09022-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="09022-110">Beispiel 2: Erstellen eines Arbeitsbereichs und Verknüpfen mit einem vorhandenen Konto</span><span class="sxs-lookup"><span data-stu-id="09022-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="09022-111">Der erste Befehl verwendet das Get-AzOperationalInsightsLinkTargets-Cmdlet, um die Zielvorgaben für das Konto "operative Einblicke" abzurufen, und speichert Sie dann in der $OILinkTargets-Variablen.</span><span class="sxs-lookup"><span data-stu-id="09022-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="09022-112">Der zweite Befehl übergibt das erste Konto Verknüpfungsziel in $OILinkTargets an das Cmdlet **New-AzOperationalInsightsWorkspace** mithilfe des Pipelineoperators.</span><span class="sxs-lookup"><span data-stu-id="09022-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="09022-113">Mit dem Befehl wird ein Standard-SKU-Arbeitsbereich mit dem Namen myworkspace erstellt, der mit dem ersten Operational Insights-Konto in $OILinkTargets verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="09022-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="09022-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="09022-114">PARAMETERS</span></span>

### <span data-ttu-id="09022-115">-CustomerID</span><span class="sxs-lookup"><span data-stu-id="09022-115">-CustomerId</span></span>
<span data-ttu-id="09022-116">Gibt das Konto an, mit dem dieser Arbeitsbereich verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="09022-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="09022-117">Das Get-AzOperationalInsightsLinkTargets-Cmdlet kann auch verwendet werden, um die potenziellen Konten aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="09022-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09022-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09022-118">-DefaultProfile</span></span>
<span data-ttu-id="09022-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="09022-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09022-120">-Force</span><span class="sxs-lookup"><span data-stu-id="09022-120">-Force</span></span>
<span data-ttu-id="09022-121">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="09022-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09022-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="09022-122">-Location</span></span>
<span data-ttu-id="09022-123">Gibt den Speicherort an, an dem der Arbeitsbereich erstellt werden soll, beispielsweise Ost-oder West Europa.</span><span class="sxs-lookup"><span data-stu-id="09022-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="09022-124">-Name</span><span class="sxs-lookup"><span data-stu-id="09022-124">-Name</span></span>
<span data-ttu-id="09022-125">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="09022-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="09022-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09022-126">-ResourceGroupName</span></span>
<span data-ttu-id="09022-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="09022-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="09022-128">Der Arbeitsbereich wird in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="09022-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="09022-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="09022-129">-RetentionInDays</span></span>
<span data-ttu-id="09022-130">Die Aufbewahrung von Arbeitsbereichsdaten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="09022-130">The workspace data retention in days.</span></span> <span data-ttu-id="09022-131">730 Tage ist der maximal zulässige Wert für alle anderen SKUs</span><span class="sxs-lookup"><span data-stu-id="09022-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="09022-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="09022-132">-Sku</span></span>
<span data-ttu-id="09022-133">Gibt die Dienstebene des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="09022-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="09022-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="09022-134">Valid values are:</span></span>
- <span data-ttu-id="09022-135">kostenlos</span><span class="sxs-lookup"><span data-stu-id="09022-135">free</span></span>
- <span data-ttu-id="09022-136">Standard</span><span class="sxs-lookup"><span data-stu-id="09022-136">standard</span></span>
- <span data-ttu-id="09022-137">Standalone</span><span class="sxs-lookup"><span data-stu-id="09022-137">standalone</span></span>
- <span data-ttu-id="09022-138">Premium</span><span class="sxs-lookup"><span data-stu-id="09022-138">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09022-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="09022-139">-Tag</span></span>
<span data-ttu-id="09022-140">Die Ressourcenkategorien für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="09022-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="09022-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09022-141">-Confirm</span></span>
<span data-ttu-id="09022-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09022-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09022-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09022-143">-WhatIf</span></span>
<span data-ttu-id="09022-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09022-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09022-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09022-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09022-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09022-146">CommonParameters</span></span>
<span data-ttu-id="09022-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09022-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09022-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09022-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09022-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09022-149">INPUTS</span></span>

### <span data-ttu-id="09022-150">System. String</span><span class="sxs-lookup"><span data-stu-id="09022-150">System.String</span></span>

### <span data-ttu-id="09022-151">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09022-151">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="09022-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="09022-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="09022-153">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09022-153">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="09022-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09022-154">OUTPUTS</span></span>

### <span data-ttu-id="09022-155">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="09022-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="09022-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="09022-156">NOTES</span></span>

<span data-ttu-id="09022-157">Es wurde ein neues Preismodell veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="09022-157">A new pricing model has been released.</span></span> <span data-ttu-id="09022-158">Wenn Sie ein CSP sind, bedeutet dies, dass Sie "Standalone" für die SKU verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="09022-158">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="09022-159">Hinter den Kulissen wird die SKU in pergb2018 geändert.</span><span class="sxs-lookup"><span data-stu-id="09022-159">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="09022-160">Weitere Informationen finden Sie in den folgenden Themen: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="09022-160">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="09022-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09022-161">RELATED LINKS</span></span>

[<span data-ttu-id="09022-162">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="09022-162">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
