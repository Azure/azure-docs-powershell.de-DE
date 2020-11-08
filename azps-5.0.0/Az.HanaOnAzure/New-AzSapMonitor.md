---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175549"
---
# <span data-ttu-id="3f901-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="3f901-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="3f901-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f901-102">SYNOPSIS</span></span>
<span data-ttu-id="3f901-103">Erstellt einen SAP-Monitor für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="3f901-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="3f901-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f901-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f901-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f901-105">DESCRIPTION</span></span>
<span data-ttu-id="3f901-106">Erstellt einen SAP-Monitor für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="3f901-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="3f901-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f901-107">EXAMPLES</span></span>

### <span data-ttu-id="3f901-108">Beispiel 1: neuer SAP-Monitor</span><span class="sxs-lookup"><span data-stu-id="3f901-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="3f901-109">Dieser Befehl erstellt einen SAP-Monitor.</span><span class="sxs-lookup"><span data-stu-id="3f901-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="3f901-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f901-110">PARAMETERS</span></span>

### <span data-ttu-id="3f901-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f901-111">-AsJob</span></span>
<span data-ttu-id="3f901-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3f901-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3f901-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f901-113">-DefaultProfile</span></span>
<span data-ttu-id="3f901-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f901-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f901-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="3f901-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="3f901-116">Der Wert, der angibt, ob Analysen an Microsoft gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3f901-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="3f901-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="3f901-117">-Location</span></span>
<span data-ttu-id="3f901-118">Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="3f901-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="3f901-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="3f901-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="3f901-120">Die Arbeitsbereichs-ID des für die Überwachung zu verwendenden Protokollanalyse Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="3f901-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="3f901-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="3f901-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="3f901-122">Die Arm-ID des für die Überwachung verwendeten Protokollanalyse Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="3f901-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="3f901-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="3f901-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="3f901-124">Der freigegebene Schlüssel des für die Überwachung verwendeten Protokollanalyse Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="3f901-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="3f901-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="3f901-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="3f901-126">Das Subnetz, in dem der SAP-Monitor bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3f901-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="3f901-127">Es sollte sich um dasselbe Subnetz der Hana-Datenbank handeln.</span><span class="sxs-lookup"><span data-stu-id="3f901-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="3f901-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3f901-128">-Name</span></span>
<span data-ttu-id="3f901-129">Der Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="3f901-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="3f901-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3f901-130">-NoWait</span></span>
<span data-ttu-id="3f901-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3f901-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3f901-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f901-132">-ResourceGroupName</span></span>
<span data-ttu-id="3f901-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3f901-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="3f901-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="3f901-134">-SubscriptionId</span></span>
<span data-ttu-id="3f901-135">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3f901-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3f901-136">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="3f901-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3f901-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f901-137">-Tag</span></span>
<span data-ttu-id="3f901-138">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="3f901-138">Resource tags.</span></span>

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

### <span data-ttu-id="3f901-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f901-139">-Confirm</span></span>
<span data-ttu-id="3f901-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f901-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f901-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f901-141">-WhatIf</span></span>
<span data-ttu-id="3f901-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f901-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f901-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f901-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f901-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f901-144">CommonParameters</span></span>
<span data-ttu-id="3f901-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f901-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f901-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f901-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f901-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f901-147">INPUTS</span></span>

## <span data-ttu-id="3f901-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f901-148">OUTPUTS</span></span>

### <span data-ttu-id="3f901-149">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="3f901-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="3f901-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f901-150">NOTES</span></span>

<span data-ttu-id="3f901-151">Aliase</span><span class="sxs-lookup"><span data-stu-id="3f901-151">ALIASES</span></span>

## <span data-ttu-id="3f901-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f901-152">RELATED LINKS</span></span>

