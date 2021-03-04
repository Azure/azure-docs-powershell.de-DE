---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 66f5a875f05b9c5d2fcdcc8a63eba9d149a9ba7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949299"
---
# <span data-ttu-id="eb01c-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="eb01c-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="eb01c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb01c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb01c-103">Ruft Eigenschaften einer Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="eb01c-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="eb01c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb01c-104">SYNTAX</span></span>

### <span data-ttu-id="eb01c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb01c-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb01c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="eb01c-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb01c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eb01c-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb01c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb01c-108">DESCRIPTION</span></span>
<span data-ttu-id="eb01c-109">Ruft Eigenschaften einer Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="eb01c-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="eb01c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb01c-110">EXAMPLES</span></span>

### <span data-ttu-id="eb01c-111">Beispiel 1: Alle Instanzen unter einem SAP-Monitor erhalten</span><span class="sxs-lookup"><span data-stu-id="eb01c-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="eb01c-112">Dieser Befehl ruft alle Instanzen unter einem SAP-Monitor ab.</span><span class="sxs-lookup"><span data-stu-id="eb01c-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="eb01c-113">Beispiel 2: Erhalten einer Instanz des SAP-Monitors nach Name</span><span class="sxs-lookup"><span data-stu-id="eb01c-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="eb01c-114">Dieser Befehl ruft eine Instanz des SAP-Monitors nach Namen ab.</span><span class="sxs-lookup"><span data-stu-id="eb01c-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="eb01c-115">Beispiel 3: Erhalten einer Instanz des SAP-Monitors nach Objekt</span><span class="sxs-lookup"><span data-stu-id="eb01c-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="eb01c-116">Dieser Befehl ruft eine Instanz des SAP-Monitors nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="eb01c-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="eb01c-117">Beispiel 4: Erhalten einer Instanz eines SAP-Monitors per Pipeline</span><span class="sxs-lookup"><span data-stu-id="eb01c-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="eb01c-118">Dieser Befehl ruft eine Instanz des SAP-Monitors per Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="eb01c-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="eb01c-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eb01c-119">PARAMETERS</span></span>

### <span data-ttu-id="eb01c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb01c-120">-DefaultProfile</span></span>
<span data-ttu-id="eb01c-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb01c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb01c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb01c-122">-InputObject</span></span>
<span data-ttu-id="eb01c-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="eb01c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eb01c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="eb01c-124">-Name</span></span>
<span data-ttu-id="eb01c-125">Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="eb01c-125">Name of the provider instance.</span></span>

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

### <span data-ttu-id="eb01c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb01c-126">-ResourceGroupName</span></span>
<span data-ttu-id="eb01c-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eb01c-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="eb01c-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="eb01c-128">-SapMonitorName</span></span>
<span data-ttu-id="eb01c-129">Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="eb01c-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="eb01c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb01c-130">-SubscriptionId</span></span>
<span data-ttu-id="eb01c-131">Abonnement-ID, mit der Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="eb01c-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eb01c-132">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="eb01c-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eb01c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb01c-133">CommonParameters</span></span>
<span data-ttu-id="eb01c-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb01c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb01c-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb01c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb01c-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb01c-136">INPUTS</span></span>

### <span data-ttu-id="eb01c-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="eb01c-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="eb01c-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb01c-138">OUTPUTS</span></span>

### <span data-ttu-id="eb01c-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="eb01c-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="eb01c-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eb01c-140">NOTES</span></span>

<span data-ttu-id="eb01c-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="eb01c-141">ALIASES</span></span>

<span data-ttu-id="eb01c-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="eb01c-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb01c-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="eb01c-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb01c-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eb01c-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb01c-145">INPUTOBJECT <IHanaOnAzureIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="eb01c-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eb01c-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="eb01c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eb01c-147">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="eb01c-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="eb01c-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="eb01c-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="eb01c-149">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="eb01c-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="eb01c-150">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eb01c-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="eb01c-151">`[ResourceName <String>]`: Der Name der Identitätsressource.</span><span class="sxs-lookup"><span data-stu-id="eb01c-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="eb01c-152">`[SapMonitorName <String>]`: Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="eb01c-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="eb01c-153">`[Scope <String>]`: Der Ressourcenanbieterbereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="eb01c-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="eb01c-154">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="eb01c-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="eb01c-155">`[SubscriptionId <String>]`: Abonnement-ID, mit der Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="eb01c-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eb01c-156">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="eb01c-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="eb01c-157">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="eb01c-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="eb01c-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eb01c-158">RELATED LINKS</span></span>

