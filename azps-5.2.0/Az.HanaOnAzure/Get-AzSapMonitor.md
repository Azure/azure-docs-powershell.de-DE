---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357257"
---
# <span data-ttu-id="5e232-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="5e232-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="5e232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e232-102">SYNOPSIS</span></span>
<span data-ttu-id="5e232-103">Ruft die Eigenschaften eines SAP-Monitors für das angegebene Abonnement, die angegebene Ressourcengruppe und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="5e232-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="5e232-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e232-104">SYNTAX</span></span>

### <span data-ttu-id="5e232-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e232-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e232-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="5e232-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e232-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e232-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5e232-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e232-108">DESCRIPTION</span></span>
<span data-ttu-id="5e232-109">Ruft die Eigenschaften eines SAP-Monitors für das angegebene Abonnement, die angegebene Ressourcengruppe und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="5e232-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="5e232-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e232-110">EXAMPLES</span></span>

### <span data-ttu-id="5e232-111">Beispiel 1: Alle Monitore für SAP unter einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="5e232-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="5e232-112">Mit diesem Befehl werden die MONITORE von SAP unter einem Abonnement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e232-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="5e232-113">Beispiel 2: Benennen eines SAP-Monitors nach Name</span><span class="sxs-lookup"><span data-stu-id="5e232-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="5e232-114">Dieser Befehl ruft einen SAP Monitor nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="5e232-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="5e232-115">Beispiel 3: Objekt zum Erstellen eines SAP-Monitors</span><span class="sxs-lookup"><span data-stu-id="5e232-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="5e232-116">Dieser Befehl ruft einen SAP Monitor nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="5e232-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="5e232-117">Beispiel 4: Erhalten eines SAP-Monitors per Pipeline</span><span class="sxs-lookup"><span data-stu-id="5e232-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="5e232-118">Dieser Befehl ruft einen SAP-Monitor per Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="5e232-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="5e232-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e232-119">PARAMETERS</span></span>

### <span data-ttu-id="5e232-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e232-120">-DefaultProfile</span></span>
<span data-ttu-id="5e232-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e232-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e232-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e232-122">-InputObject</span></span>
<span data-ttu-id="5e232-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5e232-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e232-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5e232-124">-Name</span></span>
<span data-ttu-id="5e232-125">Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="5e232-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e232-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e232-126">-ResourceGroupName</span></span>
<span data-ttu-id="5e232-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e232-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e232-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e232-128">-SubscriptionId</span></span>
<span data-ttu-id="5e232-129">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5e232-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5e232-130">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="5e232-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5e232-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e232-131">CommonParameters</span></span>
<span data-ttu-id="5e232-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e232-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e232-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e232-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e232-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e232-134">INPUTS</span></span>

### <span data-ttu-id="5e232-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="5e232-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="5e232-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e232-136">OUTPUTS</span></span>

### <span data-ttu-id="5e232-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="5e232-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="5e232-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5e232-138">NOTES</span></span>

<span data-ttu-id="5e232-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5e232-139">ALIASES</span></span>

<span data-ttu-id="5e232-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="5e232-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e232-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5e232-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e232-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e232-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e232-143">INPUTOBJECT <IHanaOnAzureIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="5e232-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e232-144">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="5e232-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e232-145">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="5e232-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="5e232-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="5e232-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="5e232-147">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="5e232-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="5e232-148">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e232-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5e232-149">`[ResourceName <String>]`: Der Name der Identitätsressource.</span><span class="sxs-lookup"><span data-stu-id="5e232-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="5e232-150">`[SapMonitorName <String>]`: Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="5e232-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="5e232-151">`[Scope <String>]`: Der Umfang des Ressourcenanbieters der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5e232-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="5e232-152">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="5e232-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="5e232-153">`[SubscriptionId <String>]`: Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5e232-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5e232-154">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="5e232-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5e232-155">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="5e232-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="5e232-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5e232-156">RELATED LINKS</span></span>

