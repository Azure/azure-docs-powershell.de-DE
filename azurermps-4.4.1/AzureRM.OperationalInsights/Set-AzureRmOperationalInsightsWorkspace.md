---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: e24597d25fffdc1b516c5a18cf011f7222d288c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479002"
---
# <span data-ttu-id="a5c40-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5c40-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="a5c40-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5c40-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c40-103">Aktualisiert einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a5c40-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5c40-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5c40-104">SYNTAX</span></span>

### <span data-ttu-id="a5c40-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5c40-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c40-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a5c40-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tags] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5c40-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5c40-107">DESCRIPTION</span></span>
<span data-ttu-id="a5c40-108">Das Cmdlet " **Satz-AzureRmOperationalInsightsWorkspace** " ändert die Konfiguration eines Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a5c40-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="a5c40-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5c40-109">EXAMPLES</span></span>

### <span data-ttu-id="a5c40-110">Beispiel 1: Ändern eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="a5c40-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="a5c40-111">Mit diesem Befehl werden die SKU und die Tags des Arbeitsbereichs mit dem Namen "myworkspace" in der Ressourcengruppe "ContosoResourceGroup" geändert.</span><span class="sxs-lookup"><span data-stu-id="a5c40-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a5c40-112">Beispiel 2: Aktualisieren eines Arbeitsbereichs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a5c40-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="a5c40-113">Dieser Befehl verwendet das Get-AzureRmOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und übergibt ihn dann mithilfe des Pipelineoperators an das Cmdlet " **Satz-AzureRmOperationalInsightsWorkspace** ", um die SKU auf "Premium" zu setzen.</span><span class="sxs-lookup"><span data-stu-id="a5c40-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="a5c40-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5c40-114">PARAMETERS</span></span>

### <span data-ttu-id="a5c40-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a5c40-115">-Name</span></span>
<span data-ttu-id="a5c40-116">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="a5c40-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="a5c40-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c40-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5c40-118">Gibt den Namen der Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a5c40-118">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="a5c40-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="a5c40-119">-Sku</span></span>
<span data-ttu-id="a5c40-120">Gibt die Dienstebene des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="a5c40-120">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="a5c40-121">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a5c40-121">Valid values are:</span></span> 

- <span data-ttu-id="a5c40-122">kostenlos</span><span class="sxs-lookup"><span data-stu-id="a5c40-122">free</span></span>
- <span data-ttu-id="a5c40-123">Standard</span><span class="sxs-lookup"><span data-stu-id="a5c40-123">standard</span></span>
- <span data-ttu-id="a5c40-124">Premium</span><span class="sxs-lookup"><span data-stu-id="a5c40-124">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c40-125">-Tags</span><span class="sxs-lookup"><span data-stu-id="a5c40-125">-Tags</span></span>
<span data-ttu-id="a5c40-126">Gibt die Ressourcenkategorien für den Arbeitsbereich an.</span><span class="sxs-lookup"><span data-stu-id="a5c40-126">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="a5c40-127">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a5c40-127">-Workspace</span></span>
<span data-ttu-id="a5c40-128">Gibt den Arbeitsbereich an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5c40-128">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="a5c40-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c40-129">-DefaultProfile</span></span>
<span data-ttu-id="a5c40-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5c40-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5c40-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a5c40-131">-RetentionInDays</span></span>
<span data-ttu-id="a5c40-132">Die Aufbewahrung von Arbeitsbereichsdaten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="a5c40-132">The workspace data retention in days.</span></span> <span data-ttu-id="a5c40-133">730 Tage ist der maximal zulässige Wert für alle anderen SKUs.</span><span class="sxs-lookup"><span data-stu-id="a5c40-133">730 days is the maximum allowed for all other Skus.</span></span>

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

### <span data-ttu-id="a5c40-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c40-134">CommonParameters</span></span>
<span data-ttu-id="a5c40-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5c40-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c40-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c40-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c40-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5c40-137">INPUTS</span></span>

### <span data-ttu-id="a5c40-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5c40-138">PSWorkspace</span></span>
<span data-ttu-id="a5c40-139">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5c40-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="a5c40-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5c40-140">OUTPUTS</span></span>

### <span data-ttu-id="a5c40-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5c40-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="a5c40-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5c40-142">NOTES</span></span>

## <span data-ttu-id="a5c40-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5c40-143">RELATED LINKS</span></span>

[<span data-ttu-id="a5c40-144">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="a5c40-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="a5c40-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5c40-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


