---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: a4584e4c0fc64920fbffb7e3d685a9be3ac04ad1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482854"
---
# <span data-ttu-id="033dd-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="033dd-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="033dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="033dd-102">SYNOPSIS</span></span>
<span data-ttu-id="033dd-103">Aktualisiert einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="033dd-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="033dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="033dd-104">SYNTAX</span></span>

### <span data-ttu-id="033dd-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="033dd-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="033dd-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="033dd-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="033dd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="033dd-107">DESCRIPTION</span></span>
<span data-ttu-id="033dd-108">Das Cmdlet " **Satz-AzureRmOperationalInsightsWorkspace** " ändert die Konfiguration eines Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="033dd-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="033dd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="033dd-109">EXAMPLES</span></span>

### <span data-ttu-id="033dd-110">Beispiel 1: Ändern eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="033dd-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="033dd-111">Mit diesem Befehl werden die SKU und die Tags des Arbeitsbereichs mit dem Namen "myworkspace" in der Ressourcengruppe "ContosoResourceGroup" geändert.</span><span class="sxs-lookup"><span data-stu-id="033dd-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="033dd-112">Beispiel 2: Aktualisieren eines Arbeitsbereichs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="033dd-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="033dd-113">Dieser Befehl verwendet das Get-AzureRmOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und übergibt ihn dann mithilfe des Pipelineoperators an das Cmdlet " **Satz-AzureRmOperationalInsightsWorkspace** ", um die SKU auf "Premium" zu setzen.</span><span class="sxs-lookup"><span data-stu-id="033dd-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="033dd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="033dd-114">PARAMETERS</span></span>

### <span data-ttu-id="033dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="033dd-115">-DefaultProfile</span></span>
<span data-ttu-id="033dd-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="033dd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="033dd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="033dd-117">-Name</span></span>
<span data-ttu-id="033dd-118">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="033dd-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="033dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="033dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="033dd-120">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="033dd-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="033dd-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="033dd-121">-RetentionInDays</span></span>
<span data-ttu-id="033dd-122">Die Aufbewahrung von Arbeitsbereichsdaten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="033dd-122">The workspace data retention in days.</span></span> <span data-ttu-id="033dd-123">730 Tage ist der maximal zulässige Wert für alle anderen SKUs</span><span class="sxs-lookup"><span data-stu-id="033dd-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="033dd-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="033dd-124">-Sku</span></span>
<span data-ttu-id="033dd-125">Gibt die Dienstebene des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="033dd-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="033dd-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="033dd-126">Valid values are:</span></span> 

- <span data-ttu-id="033dd-127">kostenlos</span><span class="sxs-lookup"><span data-stu-id="033dd-127">free</span></span>
- <span data-ttu-id="033dd-128">Standard</span><span class="sxs-lookup"><span data-stu-id="033dd-128">standard</span></span>
- <span data-ttu-id="033dd-129">Premium</span><span class="sxs-lookup"><span data-stu-id="033dd-129">premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="033dd-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="033dd-130">-Tag</span></span>
<span data-ttu-id="033dd-131">Die Ressourcenkategorien für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="033dd-131">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="033dd-132">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="033dd-132">-Workspace</span></span>
<span data-ttu-id="033dd-133">Gibt den Arbeitsbereich an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="033dd-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="033dd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033dd-134">CommonParameters</span></span>
<span data-ttu-id="033dd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="033dd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033dd-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="033dd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033dd-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="033dd-137">INPUTS</span></span>

### <span data-ttu-id="033dd-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="033dd-138">PSWorkspace</span></span>
<span data-ttu-id="033dd-139">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="033dd-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="033dd-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="033dd-140">OUTPUTS</span></span>

### <span data-ttu-id="033dd-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="033dd-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="033dd-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="033dd-142">NOTES</span></span>

## <span data-ttu-id="033dd-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="033dd-143">RELATED LINKS</span></span>

[<span data-ttu-id="033dd-144">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="033dd-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="033dd-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="033dd-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


