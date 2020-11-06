---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 83f9ec56f5d33b65810da96364ab11dd4eb7c52a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481726"
---
# <span data-ttu-id="1c7ba-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1c7ba-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1c7ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1c7ba-103">Erstellt einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c7ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c7ba-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c7ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c7ba-105">DESCRIPTION</span></span>
<span data-ttu-id="1c7ba-106">Das Cmdlet **New-AzureRmOperationalInsightsWorkspace** erstellt einen Arbeitsbereich in der angegebenen Ressourcengruppe und dem angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="1c7ba-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c7ba-107">EXAMPLES</span></span>

### <span data-ttu-id="1c7ba-108">Beispiel 1: Erstellen eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="1c7ba-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="1c7ba-109">Mit diesem Befehl wird ein Standard-SKU-Arbeitsbereich mit dem Namen "myworkspace" in der Ressourcengruppe "ContosoResourceGroup" erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1c7ba-110">Beispiel 2: Erstellen eines Arbeitsbereichs und Verknüpfen mit einem vorhandenen Konto</span><span class="sxs-lookup"><span data-stu-id="1c7ba-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="1c7ba-111">Der erste Befehl verwendet das Get-AzureRmOperationalInsightsLinkTargets-Cmdlet, um die Zielvorgaben für das Konto "operative Einblicke" abzurufen, und speichert Sie dann in der $OILinkTargets-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>

<span data-ttu-id="1c7ba-112">Der zweite Befehl übergibt das erste Konto Verknüpfungsziel in $OILinkTargets an das Cmdlet **New-AzureRmOperationalInsightsWorkspace** mithilfe des Pipelineoperators.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1c7ba-113">Mit dem Befehl wird ein Standard-SKU-Arbeitsbereich mit dem Namen myworkspace erstellt, der mit dem ersten Operational Insights-Konto in $OILinkTargets verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="1c7ba-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c7ba-114">PARAMETERS</span></span>

### <span data-ttu-id="1c7ba-115">-CustomerID</span><span class="sxs-lookup"><span data-stu-id="1c7ba-115">-CustomerId</span></span>
<span data-ttu-id="1c7ba-116">Gibt das Konto an, mit dem dieser Arbeitsbereich verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="1c7ba-117">Das Get-AzureRmOperationalInsightsLinkTargets-Cmdlet kann auch verwendet werden, um die potenziellen Konten aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

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

### <span data-ttu-id="1c7ba-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1c7ba-118">-Force</span></span>
<span data-ttu-id="1c7ba-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c7ba-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="1c7ba-120">-Location</span></span>
<span data-ttu-id="1c7ba-121">Gibt den Speicherort an, an dem der Arbeitsbereich erstellt werden soll, beispielsweise Ost-oder West Europa.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="1c7ba-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1c7ba-122">-Name</span></span>
<span data-ttu-id="1c7ba-123">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-123">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="1c7ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c7ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c7ba-125">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1c7ba-126">Der Arbeitsbereich wird in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-126">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="1c7ba-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="1c7ba-127">-Sku</span></span>
<span data-ttu-id="1c7ba-128">Gibt die Dienstebene des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-128">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="1c7ba-129">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1c7ba-129">Valid values are:</span></span> 

- <span data-ttu-id="1c7ba-130">kostenlos</span><span class="sxs-lookup"><span data-stu-id="1c7ba-130">free</span></span>
- <span data-ttu-id="1c7ba-131">Standard</span><span class="sxs-lookup"><span data-stu-id="1c7ba-131">standard</span></span>
- <span data-ttu-id="1c7ba-132">Premium</span><span class="sxs-lookup"><span data-stu-id="1c7ba-132">premium</span></span>

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

### <span data-ttu-id="1c7ba-133">-Tags</span><span class="sxs-lookup"><span data-stu-id="1c7ba-133">-Tags</span></span>
<span data-ttu-id="1c7ba-134">Gibt die Ressourcenkategorien für den Arbeitsbereich an.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-134">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="1c7ba-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c7ba-135">-Confirm</span></span>
<span data-ttu-id="1c7ba-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c7ba-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c7ba-137">-WhatIf</span></span>
<span data-ttu-id="1c7ba-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c7ba-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c7ba-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c7ba-140">-DefaultProfile</span></span>
<span data-ttu-id="1c7ba-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c7ba-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1c7ba-142">-RetentionInDays</span></span>
<span data-ttu-id="1c7ba-143">Die Aufbewahrung von Arbeitsbereichsdaten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-143">The workspace data retention in days.</span></span> <span data-ttu-id="1c7ba-144">730 Tage ist der maximal zulässige Wert für alle anderen SKUs.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-144">730 days is the maximum allowed for all other Skus.</span></span>

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

### <span data-ttu-id="1c7ba-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c7ba-145">CommonParameters</span></span>
<span data-ttu-id="1c7ba-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c7ba-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c7ba-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c7ba-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c7ba-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c7ba-148">INPUTS</span></span>

## <span data-ttu-id="1c7ba-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c7ba-149">OUTPUTS</span></span>

### <span data-ttu-id="1c7ba-150">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1c7ba-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="1c7ba-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c7ba-151">NOTES</span></span>

## <span data-ttu-id="1c7ba-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c7ba-152">RELATED LINKS</span></span>

[<span data-ttu-id="1c7ba-153">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="1c7ba-153">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="1c7ba-154">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="1c7ba-154">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


