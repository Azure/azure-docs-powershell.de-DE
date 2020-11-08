---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175548"
---
# <span data-ttu-id="f0cf4-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="f0cf4-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="f0cf4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="f0cf4-103">Ruft Eigenschaften einer Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="f0cf4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0cf4-104">SYNTAX</span></span>

### <span data-ttu-id="f0cf4-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0cf4-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f0cf4-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f0cf4-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f0cf4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f0cf4-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0cf4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0cf4-108">DESCRIPTION</span></span>
<span data-ttu-id="f0cf4-109">Ruft Eigenschaften einer Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="f0cf4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0cf4-110">EXAMPLES</span></span>

### <span data-ttu-id="f0cf4-111">Beispiel 1: Abrufen aller Instanzen unter einem SAP-Monitor</span><span class="sxs-lookup"><span data-stu-id="f0cf4-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f0cf4-112">Dieser Befehl ruft alle Instanzen unter einem SAP-Monitor ab.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="f0cf4-113">Beispiel 2: Abrufen einer Instanz des SAP-Monitors nach Name</span><span class="sxs-lookup"><span data-stu-id="f0cf4-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f0cf4-114">Dieser Befehl ruft eine Instanz des SAP-Monitors nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="f0cf4-115">Beispiel 3: Abrufen einer Instanz des SAP-Monitors nach Objekt</span><span class="sxs-lookup"><span data-stu-id="f0cf4-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f0cf4-116">Dieser Befehl ruft eine Instanz des SAP-Monitors nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="f0cf4-117">Beispiel 4: Abrufen einer Instanz des SAP-Monitors nach Pipeline</span><span class="sxs-lookup"><span data-stu-id="f0cf4-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f0cf4-118">Dieser Befehl ruft eine Instanz des SAP-Monitors nach Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="f0cf4-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0cf4-119">PARAMETERS</span></span>

### <span data-ttu-id="f0cf4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0cf4-120">-DefaultProfile</span></span>
<span data-ttu-id="f0cf4-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0cf4-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f0cf4-122">-InputObject</span></span>
<span data-ttu-id="f0cf4-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f0cf4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f0cf4-124">-Name</span></span>
<span data-ttu-id="f0cf4-125">Der Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-125">Name of the provider instance.</span></span>

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

### <span data-ttu-id="f0cf4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0cf4-126">-ResourceGroupName</span></span>
<span data-ttu-id="f0cf4-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="f0cf4-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="f0cf4-128">-SapMonitorName</span></span>
<span data-ttu-id="f0cf4-129">Der Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="f0cf4-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f0cf4-130">-SubscriptionId</span></span>
<span data-ttu-id="f0cf4-131">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f0cf4-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f0cf4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0cf4-133">CommonParameters</span></span>
<span data-ttu-id="f0cf4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0cf4-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0cf4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0cf4-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0cf4-136">INPUTS</span></span>

### <span data-ttu-id="f0cf4-137">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="f0cf4-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="f0cf4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0cf4-138">OUTPUTS</span></span>

### <span data-ttu-id="f0cf4-139">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="f0cf4-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="f0cf4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0cf4-140">NOTES</span></span>

<span data-ttu-id="f0cf4-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="f0cf4-141">ALIASES</span></span>

<span data-ttu-id="f0cf4-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0cf4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0cf4-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0cf4-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0cf4-145">Inputobject <IHanaOnAzureIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f0cf4-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0cf4-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f0cf4-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0cf4-147">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="f0cf4-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f0cf4-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="f0cf4-149">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="f0cf4-150">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f0cf4-151">`[ResourceName <String>]`: Der Name der Identitäts Ressource.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="f0cf4-152">`[SapMonitorName <String>]`: Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="f0cf4-153">`[Scope <String>]`: Der Ressourcenanbieter Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="f0cf4-154">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="f0cf4-155">`[SubscriptionId <String>]`: Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f0cf4-156">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f0cf4-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f0cf4-157">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="f0cf4-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="f0cf4-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0cf4-158">RELATED LINKS</span></span>

