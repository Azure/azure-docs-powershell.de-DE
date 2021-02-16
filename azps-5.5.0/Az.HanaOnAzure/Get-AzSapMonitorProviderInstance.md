---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170543"
---
# <span data-ttu-id="8827e-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="8827e-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="8827e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8827e-102">SYNOPSIS</span></span>
<span data-ttu-id="8827e-103">Ruft eigenschaften einer Anbieterinstanz für das angegebene Abonnement, die angegebene Ressourcengruppe, den Namen von SapMonitor und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="8827e-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="8827e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8827e-104">SYNTAX</span></span>

### <span data-ttu-id="8827e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="8827e-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8827e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="8827e-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8827e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8827e-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8827e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8827e-108">DESCRIPTION</span></span>
<span data-ttu-id="8827e-109">Ruft eigenschaften einer Anbieterinstanz für das angegebene Abonnement, die angegebene Ressourcengruppe, den Namen von SapMonitor und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="8827e-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="8827e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8827e-110">EXAMPLES</span></span>

### <span data-ttu-id="8827e-111">Beispiel 1: Erhalten aller Instanzen unter einem SAP-Monitor</span><span class="sxs-lookup"><span data-stu-id="8827e-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="8827e-112">Dieser Befehl ruft alle Instanzen unter einem SAP Monitor ab.</span><span class="sxs-lookup"><span data-stu-id="8827e-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="8827e-113">Beispiel 2: Erhalten einer Instanz eines SAP-Monitors nach Name</span><span class="sxs-lookup"><span data-stu-id="8827e-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="8827e-114">Dieser Befehl ruft nach Name eine Instanz des SAP-Monitors ab.</span><span class="sxs-lookup"><span data-stu-id="8827e-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="8827e-115">Beispiel 3: Erhalten einer Instanz von "SAP-Monitor nach Objekt"</span><span class="sxs-lookup"><span data-stu-id="8827e-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="8827e-116">Dieser Befehl ruft eine Instanz von "SAP Monitor by Object" ab.</span><span class="sxs-lookup"><span data-stu-id="8827e-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="8827e-117">Beispiel 4: Erhalten einer Instanz eines SAP-Monitors per Pipeline</span><span class="sxs-lookup"><span data-stu-id="8827e-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="8827e-118">Dieser Befehl ruft eine Instanz eines SAP-Monitors per Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="8827e-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="8827e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8827e-119">PARAMETERS</span></span>

### <span data-ttu-id="8827e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8827e-120">-DefaultProfile</span></span>
<span data-ttu-id="8827e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8827e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8827e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8827e-122">-InputObject</span></span>
<span data-ttu-id="8827e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8827e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8827e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8827e-124">-Name</span></span>
<span data-ttu-id="8827e-125">Der Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="8827e-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8827e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8827e-126">-ResourceGroupName</span></span>
<span data-ttu-id="8827e-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8827e-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8827e-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="8827e-128">-SapMonitorName</span></span>
<span data-ttu-id="8827e-129">Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="8827e-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8827e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8827e-130">-SubscriptionId</span></span>
<span data-ttu-id="8827e-131">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8827e-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8827e-132">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="8827e-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8827e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8827e-133">CommonParameters</span></span>
<span data-ttu-id="8827e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8827e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8827e-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8827e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8827e-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8827e-136">INPUTS</span></span>

### <span data-ttu-id="8827e-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="8827e-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="8827e-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8827e-138">OUTPUTS</span></span>

### <span data-ttu-id="8827e-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="8827e-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="8827e-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8827e-140">NOTES</span></span>

<span data-ttu-id="8827e-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8827e-141">ALIASES</span></span>

<span data-ttu-id="8827e-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="8827e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8827e-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8827e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8827e-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8827e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8827e-145">INPUTOBJECT <IHanaOnAzureIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="8827e-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8827e-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="8827e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8827e-147">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="8827e-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="8827e-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="8827e-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="8827e-149">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="8827e-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="8827e-150">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8827e-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8827e-151">`[ResourceName <String>]`: Der Name der Identitätsressource.</span><span class="sxs-lookup"><span data-stu-id="8827e-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="8827e-152">`[SapMonitorName <String>]`: Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="8827e-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="8827e-153">`[Scope <String>]`: Der Umfang des Ressourcenanbieters der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8827e-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="8827e-154">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="8827e-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="8827e-155">`[SubscriptionId <String>]`: Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8827e-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8827e-156">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="8827e-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8827e-157">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="8827e-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="8827e-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8827e-158">RELATED LINKS</span></span>

