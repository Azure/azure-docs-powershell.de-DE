---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174723"
---
# <span data-ttu-id="bfb6e-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="bfb6e-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="bfb6e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bfb6e-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb6e-103">Erstellt einen SAP-Monitor für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="bfb6e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfb6e-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bfb6e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb6e-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb6e-106">Erstellt einen SAP-Monitor für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="bfb6e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bfb6e-107">EXAMPLES</span></span>

### <span data-ttu-id="bfb6e-108">Beispiel 1: neuer SAP-Monitor</span><span class="sxs-lookup"><span data-stu-id="bfb6e-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="bfb6e-109">Dieser Befehl erstellt einen SAP-Monitor.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="bfb6e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfb6e-110">PARAMETERS</span></span>

### <span data-ttu-id="bfb6e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfb6e-111">-AsJob</span></span>
<span data-ttu-id="bfb6e-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="bfb6e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="bfb6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb6e-113">-DefaultProfile</span></span>
<span data-ttu-id="bfb6e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfb6e-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="bfb6e-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="bfb6e-116">Der Wert, der angibt, ob Analysen an Microsoft gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="bfb6e-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="bfb6e-117">-Location</span></span>
<span data-ttu-id="bfb6e-118">Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="bfb6e-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="bfb6e-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="bfb6e-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="bfb6e-120">Die Arbeitsbereichs-ID des für die Überwachung zu verwendenden Protokollanalyse Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="bfb6e-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="bfb6e-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="bfb6e-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="bfb6e-122">Die Arm-ID des für die Überwachung verwendeten Protokollanalyse Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="bfb6e-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="bfb6e-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="bfb6e-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="bfb6e-124">Der freigegebene Schlüssel des für die Überwachung verwendeten Protokollanalyse Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="bfb6e-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="bfb6e-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="bfb6e-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="bfb6e-126">Das Subnetz, in dem der SAP-Monitor bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="bfb6e-127">Es sollte sich um dasselbe Subnetz der Hana-Datenbank handeln.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="bfb6e-128">-Name</span><span class="sxs-lookup"><span data-stu-id="bfb6e-128">-Name</span></span>
<span data-ttu-id="bfb6e-129">Der Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="bfb6e-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bfb6e-130">-NoWait</span></span>
<span data-ttu-id="bfb6e-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="bfb6e-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bfb6e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb6e-132">-ResourceGroupName</span></span>
<span data-ttu-id="bfb6e-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="bfb6e-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="bfb6e-134">-SubscriptionId</span></span>
<span data-ttu-id="bfb6e-135">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bfb6e-136">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bfb6e-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="bfb6e-137">-Tag</span></span>
<span data-ttu-id="bfb6e-138">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-138">Resource tags.</span></span>

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

### <span data-ttu-id="bfb6e-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bfb6e-139">-Confirm</span></span>
<span data-ttu-id="bfb6e-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfb6e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb6e-141">-WhatIf</span></span>
<span data-ttu-id="bfb6e-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfb6e-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfb6e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb6e-144">CommonParameters</span></span>
<span data-ttu-id="bfb6e-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb6e-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfb6e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb6e-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bfb6e-147">INPUTS</span></span>

## <span data-ttu-id="bfb6e-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bfb6e-148">OUTPUTS</span></span>

### <span data-ttu-id="bfb6e-149">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="bfb6e-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="bfb6e-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="bfb6e-150">NOTES</span></span>

<span data-ttu-id="bfb6e-151">Aliase</span><span class="sxs-lookup"><span data-stu-id="bfb6e-151">ALIASES</span></span>

## <span data-ttu-id="bfb6e-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bfb6e-152">RELATED LINKS</span></span>

