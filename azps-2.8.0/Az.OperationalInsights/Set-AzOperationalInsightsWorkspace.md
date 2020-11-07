---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: e339becd21be14d3587252b88dd8069b266b2408
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847815"
---
# <span data-ttu-id="46daf-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="46daf-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="46daf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46daf-102">SYNOPSIS</span></span>
<span data-ttu-id="46daf-103">Aktualisiert einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="46daf-103">Updates a workspace.</span></span>

## <span data-ttu-id="46daf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46daf-104">SYNTAX</span></span>

### <span data-ttu-id="46daf-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="46daf-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46daf-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="46daf-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46daf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46daf-107">DESCRIPTION</span></span>
<span data-ttu-id="46daf-108">Das Cmdlet " **Satz-AzOperationalInsightsWorkspace** " ändert die Konfiguration eines Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="46daf-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="46daf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46daf-109">EXAMPLES</span></span>

### <span data-ttu-id="46daf-110">Beispiel 1: Ändern eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="46daf-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="46daf-111">Mit diesem Befehl werden die SKU und die Tags des Arbeitsbereichs mit dem Namen "myworkspace" in der Ressourcengruppe "ContosoResourceGroup" geändert.</span><span class="sxs-lookup"><span data-stu-id="46daf-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="46daf-112">Beispiel 2: Aktualisieren eines Arbeitsbereichs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="46daf-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="46daf-113">Dieser Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und übergibt ihn dann mithilfe des Pipelineoperators an das Cmdlet " **Satz-AzOperationalInsightsWorkspace** ", um die SKU auf "Premium" zu setzen.</span><span class="sxs-lookup"><span data-stu-id="46daf-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="46daf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="46daf-114">PARAMETERS</span></span>

### <span data-ttu-id="46daf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46daf-115">-DefaultProfile</span></span>
<span data-ttu-id="46daf-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46daf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46daf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="46daf-117">-Name</span></span>
<span data-ttu-id="46daf-118">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="46daf-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="46daf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46daf-119">-ResourceGroupName</span></span>
<span data-ttu-id="46daf-120">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="46daf-120">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="46daf-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="46daf-121">-RetentionInDays</span></span>
<span data-ttu-id="46daf-122">Die Aufbewahrung von Arbeitsbereichsdaten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="46daf-122">The workspace data retention in days.</span></span> <span data-ttu-id="46daf-123">730 Tage ist der maximal zulässige Wert für alle anderen SKUs</span><span class="sxs-lookup"><span data-stu-id="46daf-123">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="46daf-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="46daf-124">-Sku</span></span>
<span data-ttu-id="46daf-125">Gibt die Dienstebene des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="46daf-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="46daf-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="46daf-126">Valid values are:</span></span> 
- <span data-ttu-id="46daf-127">kostenlos</span><span class="sxs-lookup"><span data-stu-id="46daf-127">free</span></span>
- <span data-ttu-id="46daf-128">Standard</span><span class="sxs-lookup"><span data-stu-id="46daf-128">standard</span></span>
- <span data-ttu-id="46daf-129">Premium</span><span class="sxs-lookup"><span data-stu-id="46daf-129">premium</span></span>

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

### <span data-ttu-id="46daf-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="46daf-130">-Tag</span></span>
<span data-ttu-id="46daf-131">Die Ressourcenkategorien für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="46daf-131">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="46daf-132">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="46daf-132">-Workspace</span></span>
<span data-ttu-id="46daf-133">Gibt den Arbeitsbereich an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="46daf-133">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="46daf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46daf-134">CommonParameters</span></span>
<span data-ttu-id="46daf-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46daf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46daf-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46daf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46daf-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46daf-137">INPUTS</span></span>

### <span data-ttu-id="46daf-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="46daf-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="46daf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="46daf-139">System.String</span></span>

### <span data-ttu-id="46daf-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="46daf-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="46daf-141">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="46daf-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="46daf-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46daf-142">OUTPUTS</span></span>

### <span data-ttu-id="46daf-143">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="46daf-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="46daf-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="46daf-144">NOTES</span></span>

## <span data-ttu-id="46daf-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46daf-145">RELATED LINKS</span></span>

[<span data-ttu-id="46daf-146">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="46daf-146">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="46daf-147">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="46daf-147">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


