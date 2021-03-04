---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: ecc68d6f87728f3bccb2d7fe1947c293e6b670d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937808"
---
# <span data-ttu-id="a3dad-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3dad-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="a3dad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3dad-102">SYNOPSIS</span></span>
<span data-ttu-id="a3dad-103">Aktualisiert einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a3dad-103">Updates a workspace.</span></span>

## <span data-ttu-id="a3dad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3dad-104">SYNTAX</span></span>

### <span data-ttu-id="a3dad-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3dad-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="a3dad-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a3dad-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="a3dad-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3dad-107">DESCRIPTION</span></span>
<span data-ttu-id="a3dad-108">Das **Cmdlet Set-AzOperationalInsightsWorkspace** ändert die Konfiguration eines Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a3dad-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="a3dad-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3dad-109">EXAMPLES</span></span>

### <span data-ttu-id="a3dad-110">Beispiel 1: Ändern eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="a3dad-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="a3dad-111">Mit diesem Befehl werden die SKU und die Tags des Arbeitsbereichs mit dem Namen "MyWorkspace" in der Ressourcengruppe "ContosoResourceGroup" geändert.</span><span class="sxs-lookup"><span data-stu-id="a3dad-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a3dad-112">Beispiel 2: Aktualisieren eines Arbeitsbereichs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a3dad-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="a3dad-113">Dieser Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen MyWorkSpace zu erhalten, und übergibt ihn dann an das **Set-AzOperationalInsightsWorkspace-Cmdlet** mithilfe des Pipelineoperators, um die SKU auf Premium zu setzen.</span><span class="sxs-lookup"><span data-stu-id="a3dad-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="a3dad-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a3dad-114">PARAMETERS</span></span>

### <span data-ttu-id="a3dad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3dad-115">-DefaultProfile</span></span>
<span data-ttu-id="a3dad-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a3dad-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3dad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a3dad-117">-Name</span></span>
<span data-ttu-id="a3dad-118">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="a3dad-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dad-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="a3dad-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="a3dad-120">Der Netzwerkzugriffstyp für den Zugriff auf die Erfassung des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a3dad-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="a3dad-121">Der Wert sollte "Aktiviert" oder "Deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="a3dad-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="a3dad-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="a3dad-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="a3dad-123">Der Netzwerkzugriffstyp für den Zugriff auf Arbeitsbereichsabfragen.</span><span class="sxs-lookup"><span data-stu-id="a3dad-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="a3dad-124">Der Wert sollte "Aktiviert" oder "Deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="a3dad-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="a3dad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3dad-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3dad-126">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a3dad-126">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dad-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a3dad-127">-RetentionInDays</span></span>
<span data-ttu-id="a3dad-128">Die Aufbewahrung von Arbeitsbereichsdaten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="a3dad-128">The workspace data retention in days.</span></span> <span data-ttu-id="a3dad-129">730 Tage ist der maximal zulässige Wert für alle anderen Skus</span><span class="sxs-lookup"><span data-stu-id="a3dad-129">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dad-130">-Sku</span><span class="sxs-lookup"><span data-stu-id="a3dad-130">-Sku</span></span>
<span data-ttu-id="a3dad-131">Gibt die Dienstebene des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="a3dad-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="a3dad-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a3dad-132">Valid values are:</span></span> 
- <span data-ttu-id="a3dad-133">kostenlos</span><span class="sxs-lookup"><span data-stu-id="a3dad-133">free</span></span>
- <span data-ttu-id="a3dad-134">Standard</span><span class="sxs-lookup"><span data-stu-id="a3dad-134">standard</span></span>
- <span data-ttu-id="a3dad-135">Premium</span><span class="sxs-lookup"><span data-stu-id="a3dad-135">premium</span></span>
- <span data-ttu-id="a3dad-136">Pernode</span><span class="sxs-lookup"><span data-stu-id="a3dad-136">pernode</span></span>
- <span data-ttu-id="a3dad-137">Eigenständig</span><span class="sxs-lookup"><span data-stu-id="a3dad-137">standalone</span></span>
- <span data-ttu-id="a3dad-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="a3dad-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dad-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3dad-139">-Tag</span></span>
<span data-ttu-id="a3dad-140">Die Ressourcentags für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a3dad-140">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dad-141">-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a3dad-141">-Workspace</span></span>
<span data-ttu-id="a3dad-142">Gibt den arbeitsbereich an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3dad-142">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dad-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3dad-143">CommonParameters</span></span>
<span data-ttu-id="a3dad-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3dad-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3dad-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3dad-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3dad-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3dad-146">INPUTS</span></span>

### <span data-ttu-id="a3dad-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3dad-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="a3dad-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a3dad-148">System.String</span></span>

### <span data-ttu-id="a3dad-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a3dad-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a3dad-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a3dad-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a3dad-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3dad-151">OUTPUTS</span></span>

### <span data-ttu-id="a3dad-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3dad-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="a3dad-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a3dad-153">NOTES</span></span>

## <span data-ttu-id="a3dad-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a3dad-154">RELATED LINKS</span></span>

[<span data-ttu-id="a3dad-155">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a3dad-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="a3dad-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3dad-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


