---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175553"
---
# <span data-ttu-id="9d08c-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="9d08c-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="9d08c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d08c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d08c-103">Ruft Eigenschaften eines SAP-Monitors für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="9d08c-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="9d08c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d08c-104">SYNTAX</span></span>

### <span data-ttu-id="9d08c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d08c-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9d08c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9d08c-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9d08c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9d08c-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9d08c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d08c-108">DESCRIPTION</span></span>
<span data-ttu-id="9d08c-109">Ruft Eigenschaften eines SAP-Monitors für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="9d08c-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="9d08c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d08c-110">EXAMPLES</span></span>

### <span data-ttu-id="9d08c-111">Beispiel 1: Abrufen aller SAP-Monitore unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="9d08c-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="9d08c-112">Dieser Befehl ruft SAP-Monitore unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="9d08c-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="9d08c-113">Beispiel 2: Abrufen eines SAP-Monitors nach Name</span><span class="sxs-lookup"><span data-stu-id="9d08c-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="9d08c-114">Dieser Befehl ruft einen SAP-Monitor nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="9d08c-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="9d08c-115">Beispiel 3: Abrufen eines SAP-Monitors nach Objekt</span><span class="sxs-lookup"><span data-stu-id="9d08c-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="9d08c-116">Mit diesem Befehl wird ein SAP-Monitor nach Objekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d08c-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="9d08c-117">Beispiel 4: Abrufen eines SAP-Monitors nach Pipeline</span><span class="sxs-lookup"><span data-stu-id="9d08c-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="9d08c-118">Dieser Befehl ruft einen SAP-Monitor nach Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="9d08c-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="9d08c-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d08c-119">PARAMETERS</span></span>

### <span data-ttu-id="9d08c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d08c-120">-DefaultProfile</span></span>
<span data-ttu-id="9d08c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d08c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d08c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9d08c-122">-InputObject</span></span>
<span data-ttu-id="9d08c-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9d08c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9d08c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9d08c-124">-Name</span></span>
<span data-ttu-id="9d08c-125">Der Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d08c-125">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="9d08c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d08c-126">-ResourceGroupName</span></span>
<span data-ttu-id="9d08c-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d08c-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="9d08c-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9d08c-128">-SubscriptionId</span></span>
<span data-ttu-id="9d08c-129">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9d08c-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9d08c-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9d08c-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9d08c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d08c-131">CommonParameters</span></span>
<span data-ttu-id="9d08c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d08c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d08c-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d08c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d08c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d08c-134">INPUTS</span></span>

### <span data-ttu-id="9d08c-135">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="9d08c-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="9d08c-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d08c-136">OUTPUTS</span></span>

### <span data-ttu-id="9d08c-137">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="9d08c-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="9d08c-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d08c-138">NOTES</span></span>

<span data-ttu-id="9d08c-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="9d08c-139">ALIASES</span></span>

<span data-ttu-id="9d08c-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d08c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9d08c-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9d08c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9d08c-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="9d08c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9d08c-143">Inputobject <IHanaOnAzureIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9d08c-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9d08c-144">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="9d08c-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9d08c-145">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="9d08c-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="9d08c-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="9d08c-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="9d08c-147">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="9d08c-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="9d08c-148">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d08c-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9d08c-149">`[ResourceName <String>]`: Der Name der Identitäts Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d08c-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="9d08c-150">`[SapMonitorName <String>]`: Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d08c-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="9d08c-151">`[Scope <String>]`: Der Ressourcenanbieter Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d08c-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="9d08c-152">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="9d08c-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="9d08c-153">`[SubscriptionId <String>]`: Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9d08c-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9d08c-154">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9d08c-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9d08c-155">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="9d08c-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="9d08c-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d08c-156">RELATED LINKS</span></span>

