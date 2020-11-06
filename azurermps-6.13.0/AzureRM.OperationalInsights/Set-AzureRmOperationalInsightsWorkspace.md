---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 8c884e69dd13b96925940f467633baf515d88eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482165"
---
# <span data-ttu-id="ce3b5-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce3b5-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="ce3b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce3b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ce3b5-103">Aktualisiert einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="ce3b5-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce3b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce3b5-104">SYNTAX</span></span>

### <span data-ttu-id="ce3b5-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce3b5-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce3b5-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="ce3b5-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce3b5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce3b5-107">DESCRIPTION</span></span>
<span data-ttu-id="ce3b5-108">Das Cmdlet " **Satz-AzureRmOperationalInsightsWorkspace** " ändert die Konfiguration eines Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ce3b5-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="ce3b5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce3b5-109">EXAMPLES</span></span>

### <span data-ttu-id="ce3b5-110">Beispiel 1: Ändern eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="ce3b5-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="ce3b5-111">Mit diesem Befehl werden die SKU und die Tags des Arbeitsbereichs mit dem Namen "myworkspace" in der Ressourcengruppe "ContosoResourceGroup" geändert.</span><span class="sxs-lookup"><span data-stu-id="ce3b5-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="ce3b5-112">Beispiel 2: Aktualisieren eines Arbeitsbereichs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="ce3b5-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="ce3b5-113">Dieser Befehl verwendet das Get-AzureRmOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und übergibt ihn dann mithilfe des Pipelineoperators an das Cmdlet " **Satz-AzureRmOperationalInsightsWorkspace** ", um die SKU auf "Premium" zu setzen.</span><span class="sxs-lookup"><span data-stu-id="ce3b5-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="ce3b5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce3b5-114">PARAMETERS</span></span>

### <span data-ttu-id="ce3b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce3b5-115">-DefaultProfile</span></span>
<span data-ttu-id="ce3b5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ce3b5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3b5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ce3b5-117">-Name</span></span>
<span data-ttu-id="ce3b5-118">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="ce3b5-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ce3b5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce3b5-119">-ResourceGroupName</span></span>
<span data-ttu-id="ce3b5-120">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ce3b5-120">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="ce3b5-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ce3b5-121">-RetentionInDays</span></span>
<span data-ttu-id="ce3b5-122">Die Aufbewahrung von Arbeitsbereichsdaten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="ce3b5-122">The workspace data retention in days.</span></span> <span data-ttu-id="ce3b5-123">730 Tage ist der maximal zulässige Wert für alle anderen SKUs</span><span class="sxs-lookup"><span data-stu-id="ce3b5-123">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="ce3b5-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="ce3b5-124">-Sku</span></span>
<span data-ttu-id="ce3b5-125">Gibt die Dienstebene des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="ce3b5-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="ce3b5-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ce3b5-126">Valid values are:</span></span> 
- <span data-ttu-id="ce3b5-127">kostenlos</span><span class="sxs-lookup"><span data-stu-id="ce3b5-127">free</span></span>
- <span data-ttu-id="ce3b5-128">Standard</span><span class="sxs-lookup"><span data-stu-id="ce3b5-128">standard</span></span>
- <span data-ttu-id="ce3b5-129">Premium</span><span class="sxs-lookup"><span data-stu-id="ce3b5-129">premium</span></span>

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

### <span data-ttu-id="ce3b5-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce3b5-130">-Tag</span></span>
<span data-ttu-id="ce3b5-131">Die Ressourcenkategorien für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="ce3b5-131">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="ce3b5-132">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="ce3b5-132">-Workspace</span></span>
<span data-ttu-id="ce3b5-133">Gibt den Arbeitsbereich an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce3b5-133">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="ce3b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce3b5-134">CommonParameters</span></span>
<span data-ttu-id="ce3b5-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce3b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce3b5-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce3b5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce3b5-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce3b5-137">INPUTS</span></span>

### <span data-ttu-id="ce3b5-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce3b5-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="ce3b5-139">Parameter: Arbeitsbereich (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ce3b5-139">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="ce3b5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ce3b5-140">System.String</span></span>

### <span data-ttu-id="ce3b5-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ce3b5-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ce3b5-142">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ce3b5-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ce3b5-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce3b5-143">OUTPUTS</span></span>

### <span data-ttu-id="ce3b5-144">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce3b5-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="ce3b5-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce3b5-145">NOTES</span></span>

## <span data-ttu-id="ce3b5-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce3b5-146">RELATED LINKS</span></span>

[<span data-ttu-id="ce3b5-147">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="ce3b5-147">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="ce3b5-148">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce3b5-148">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


