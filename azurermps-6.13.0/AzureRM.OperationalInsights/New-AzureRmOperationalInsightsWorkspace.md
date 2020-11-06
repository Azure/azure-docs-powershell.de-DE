---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 97f8cba0641ed576cb187f3b995d400bc7f521a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498226"
---
# <span data-ttu-id="7cf9c-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="7cf9c-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="7cf9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7cf9c-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf9c-103">Erstellt einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cf9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cf9c-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf9c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7cf9c-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf9c-106">Das Cmdlet **New-AzureRmOperationalInsightsWorkspace** erstellt einen Arbeitsbereich in der angegebenen Ressourcengruppe und dem angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="7cf9c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7cf9c-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf9c-108">Beispiel 1: Erstellen eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="7cf9c-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="7cf9c-109">Mit diesem Befehl wird ein Standard-SKU-Arbeitsbereich mit dem Namen "myworkspace" in der Ressourcengruppe "ContosoResourceGroup" erstellt.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="7cf9c-110">Beispiel 2: Erstellen eines Arbeitsbereichs und Verknüpfen mit einem vorhandenen Konto</span><span class="sxs-lookup"><span data-stu-id="7cf9c-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="7cf9c-111">Der erste Befehl verwendet das Get-AzureRmOperationalInsightsLinkTargets-Cmdlet, um die Zielvorgaben für das Konto "operative Einblicke" abzurufen, und speichert Sie dann in der $OILinkTargets-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="7cf9c-112">Der zweite Befehl übergibt das erste Konto Verknüpfungsziel in $OILinkTargets an das Cmdlet **New-AzureRmOperationalInsightsWorkspace** mithilfe des Pipelineoperators.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7cf9c-113">Mit dem Befehl wird ein Standard-SKU-Arbeitsbereich mit dem Namen myworkspace erstellt, der mit dem ersten Operational Insights-Konto in $OILinkTargets verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="7cf9c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cf9c-114">PARAMETERS</span></span>

### <span data-ttu-id="7cf9c-115">-CustomerID</span><span class="sxs-lookup"><span data-stu-id="7cf9c-115">-CustomerId</span></span>
<span data-ttu-id="7cf9c-116">Gibt das Konto an, mit dem dieser Arbeitsbereich verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="7cf9c-117">Das Get-AzureRmOperationalInsightsLinkTargets-Cmdlet kann auch verwendet werden, um die potenziellen Konten aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

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

### <span data-ttu-id="7cf9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf9c-118">-DefaultProfile</span></span>
<span data-ttu-id="7cf9c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7cf9c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cf9c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7cf9c-120">-Force</span></span>
<span data-ttu-id="7cf9c-121">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7cf9c-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="7cf9c-122">-Location</span></span>
<span data-ttu-id="7cf9c-123">Gibt den Speicherort an, an dem der Arbeitsbereich erstellt werden soll, beispielsweise Ost-oder West Europa.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="7cf9c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7cf9c-124">-Name</span></span>
<span data-ttu-id="7cf9c-125">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="7cf9c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf9c-126">-ResourceGroupName</span></span>
<span data-ttu-id="7cf9c-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7cf9c-128">Der Arbeitsbereich wird in dieser Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="7cf9c-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7cf9c-129">-RetentionInDays</span></span>
<span data-ttu-id="7cf9c-130">Die Aufbewahrung von Arbeitsbereichsdaten in Tagen.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-130">The workspace data retention in days.</span></span> <span data-ttu-id="7cf9c-131">730 Tage ist der maximal zulässige Wert für alle anderen SKUs</span><span class="sxs-lookup"><span data-stu-id="7cf9c-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="7cf9c-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="7cf9c-132">-Sku</span></span>
<span data-ttu-id="7cf9c-133">Gibt die Dienstebene des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="7cf9c-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7cf9c-134">Valid values are:</span></span> 
- <span data-ttu-id="7cf9c-135">kostenlos</span><span class="sxs-lookup"><span data-stu-id="7cf9c-135">free</span></span>
- <span data-ttu-id="7cf9c-136">Standard</span><span class="sxs-lookup"><span data-stu-id="7cf9c-136">standard</span></span>
- <span data-ttu-id="7cf9c-137">Premium</span><span class="sxs-lookup"><span data-stu-id="7cf9c-137">premium</span></span>

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

### <span data-ttu-id="7cf9c-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="7cf9c-138">-Tag</span></span>
<span data-ttu-id="7cf9c-139">Die Ressourcenkategorien für den Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="7cf9c-139">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="7cf9c-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7cf9c-140">-Confirm</span></span>
<span data-ttu-id="7cf9c-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf9c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf9c-142">-WhatIf</span></span>
<span data-ttu-id="7cf9c-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf9c-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf9c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf9c-145">CommonParameters</span></span>
<span data-ttu-id="7cf9c-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf9c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf9c-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf9c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf9c-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7cf9c-148">INPUTS</span></span>

### <span data-ttu-id="7cf9c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf9c-149">System.String</span></span>

### <span data-ttu-id="7cf9c-150">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7cf9c-150">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7cf9c-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7cf9c-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7cf9c-152">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7cf9c-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7cf9c-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7cf9c-153">OUTPUTS</span></span>

### <span data-ttu-id="7cf9c-154">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7cf9c-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="7cf9c-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="7cf9c-155">NOTES</span></span>

## <span data-ttu-id="7cf9c-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7cf9c-156">RELATED LINKS</span></span>

[<span data-ttu-id="7cf9c-157">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="7cf9c-157">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="7cf9c-158">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="7cf9c-158">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


