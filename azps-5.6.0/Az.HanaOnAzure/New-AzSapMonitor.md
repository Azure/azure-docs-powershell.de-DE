---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: a13b0a936eeecd1d7a18b18bb8878b79225da030
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949296"
---
# <span data-ttu-id="03b46-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="03b46-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="03b46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03b46-102">SYNOPSIS</span></span>
<span data-ttu-id="03b46-103">Erstellt einen SAP-Monitor für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="03b46-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="03b46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03b46-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03b46-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03b46-105">DESCRIPTION</span></span>
<span data-ttu-id="03b46-106">Erstellt einen SAP-Monitor für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="03b46-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="03b46-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03b46-107">EXAMPLES</span></span>

### <span data-ttu-id="03b46-108">Beispiel 1: Neuer SAP-Monitor</span><span class="sxs-lookup"><span data-stu-id="03b46-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="03b46-109">Mit diesem Befehl wird ein SAP-Monitor erstellt.</span><span class="sxs-lookup"><span data-stu-id="03b46-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="03b46-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="03b46-110">PARAMETERS</span></span>

### <span data-ttu-id="03b46-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03b46-111">-AsJob</span></span>
<span data-ttu-id="03b46-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="03b46-112">Run the command as a job</span></span>

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

### <span data-ttu-id="03b46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b46-113">-DefaultProfile</span></span>
<span data-ttu-id="03b46-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03b46-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b46-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="03b46-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="03b46-116">Der Wert, der angibt, ob Analysen an Microsoft gesendet werden</span><span class="sxs-lookup"><span data-stu-id="03b46-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="03b46-117">-Location</span><span class="sxs-lookup"><span data-stu-id="03b46-117">-Location</span></span>
<span data-ttu-id="03b46-118">Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="03b46-118">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b46-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="03b46-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="03b46-120">Die Arbeitsbereichs-ID des für die Überwachung zu verwendende Protokollanalysearbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="03b46-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="03b46-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="03b46-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="03b46-122">Die ARM-ID des Log Analytics-Arbeitsbereichs, der für die Überwachung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="03b46-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="03b46-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="03b46-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="03b46-124">Der freigegebene Schlüssel des Für die Überwachung verwendeten Protokollanalysearbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="03b46-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="03b46-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="03b46-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="03b46-126">Das Subnetz, in dem der SAP-Monitor bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="03b46-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="03b46-127">Es sollte dasselbe Subnetz der HANA-Datenbank sein.</span><span class="sxs-lookup"><span data-stu-id="03b46-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="03b46-128">-Name</span><span class="sxs-lookup"><span data-stu-id="03b46-128">-Name</span></span>
<span data-ttu-id="03b46-129">Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="03b46-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b46-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="03b46-130">-NoWait</span></span>
<span data-ttu-id="03b46-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="03b46-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="03b46-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b46-132">-ResourceGroupName</span></span>
<span data-ttu-id="03b46-133">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="03b46-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b46-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03b46-134">-SubscriptionId</span></span>
<span data-ttu-id="03b46-135">Abonnement-ID, mit der Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="03b46-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="03b46-136">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="03b46-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b46-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="03b46-137">-Tag</span></span>
<span data-ttu-id="03b46-138">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="03b46-138">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b46-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03b46-139">-Confirm</span></span>
<span data-ttu-id="03b46-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03b46-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b46-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b46-141">-WhatIf</span></span>
<span data-ttu-id="03b46-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03b46-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03b46-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03b46-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b46-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b46-144">CommonParameters</span></span>
<span data-ttu-id="03b46-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b46-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b46-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03b46-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b46-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03b46-147">INPUTS</span></span>

## <span data-ttu-id="03b46-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03b46-148">OUTPUTS</span></span>

### <span data-ttu-id="03b46-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="03b46-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="03b46-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="03b46-150">NOTES</span></span>

<span data-ttu-id="03b46-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="03b46-151">ALIASES</span></span>

## <span data-ttu-id="03b46-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="03b46-152">RELATED LINKS</span></span>

