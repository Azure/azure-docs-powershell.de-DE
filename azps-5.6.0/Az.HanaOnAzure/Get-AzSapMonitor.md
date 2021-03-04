---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 0de9aa6dd623efa379a6123570e766d30c850ab8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949304"
---
# <span data-ttu-id="72d9b-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="72d9b-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="72d9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="72d9b-103">Ruft Eigenschaften eines SAP-Monitors für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="72d9b-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="72d9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72d9b-104">SYNTAX</span></span>

### <span data-ttu-id="72d9b-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="72d9b-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72d9b-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="72d9b-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72d9b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="72d9b-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="72d9b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72d9b-108">DESCRIPTION</span></span>
<span data-ttu-id="72d9b-109">Ruft Eigenschaften eines SAP-Monitors für das angegebene Abonnement, die Ressourcengruppe und den Ressourcennamen ab.</span><span class="sxs-lookup"><span data-stu-id="72d9b-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="72d9b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72d9b-110">EXAMPLES</span></span>

### <span data-ttu-id="72d9b-111">Beispiel 1: Alle SAP-Monitore unter einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="72d9b-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="72d9b-112">Dieser Befehl ruft SAP-Monitore unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="72d9b-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="72d9b-113">Beispiel 2: Benennen eines SAP-Monitors</span><span class="sxs-lookup"><span data-stu-id="72d9b-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="72d9b-114">Dieser Befehl ruft einen SAP-Monitor namens ab.</span><span class="sxs-lookup"><span data-stu-id="72d9b-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="72d9b-115">Beispiel 3: Erstellen eines SAP-Monitors nach Objekt</span><span class="sxs-lookup"><span data-stu-id="72d9b-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="72d9b-116">Dieser Befehl ruft einen SAP-Monitor nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="72d9b-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="72d9b-117">Beispiel 4: Erhalten eines SAP-Monitors per Pipeline</span><span class="sxs-lookup"><span data-stu-id="72d9b-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="72d9b-118">Dieser Befehl ruft einen SAP-Monitor per Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="72d9b-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="72d9b-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="72d9b-119">PARAMETERS</span></span>

### <span data-ttu-id="72d9b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d9b-120">-DefaultProfile</span></span>
<span data-ttu-id="72d9b-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72d9b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72d9b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72d9b-122">-InputObject</span></span>
<span data-ttu-id="72d9b-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="72d9b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="72d9b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="72d9b-124">-Name</span></span>
<span data-ttu-id="72d9b-125">Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="72d9b-125">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="72d9b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d9b-126">-ResourceGroupName</span></span>
<span data-ttu-id="72d9b-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="72d9b-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="72d9b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72d9b-128">-SubscriptionId</span></span>
<span data-ttu-id="72d9b-129">Abonnement-ID, mit der Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="72d9b-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="72d9b-130">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="72d9b-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="72d9b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d9b-131">CommonParameters</span></span>
<span data-ttu-id="72d9b-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d9b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d9b-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72d9b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d9b-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72d9b-134">INPUTS</span></span>

### <span data-ttu-id="72d9b-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="72d9b-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="72d9b-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72d9b-136">OUTPUTS</span></span>

### <span data-ttu-id="72d9b-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="72d9b-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="72d9b-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="72d9b-138">NOTES</span></span>

<span data-ttu-id="72d9b-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="72d9b-139">ALIASES</span></span>

<span data-ttu-id="72d9b-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="72d9b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="72d9b-141">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="72d9b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="72d9b-142">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="72d9b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="72d9b-143">INPUTOBJECT <IHanaOnAzureIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="72d9b-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="72d9b-144">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="72d9b-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="72d9b-145">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="72d9b-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="72d9b-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="72d9b-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="72d9b-147">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="72d9b-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="72d9b-148">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="72d9b-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="72d9b-149">`[ResourceName <String>]`: Der Name der Identitätsressource.</span><span class="sxs-lookup"><span data-stu-id="72d9b-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="72d9b-150">`[SapMonitorName <String>]`: Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="72d9b-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="72d9b-151">`[Scope <String>]`: Der Ressourcenanbieterbereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="72d9b-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="72d9b-152">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="72d9b-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="72d9b-153">`[SubscriptionId <String>]`: Abonnement-ID, mit der Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="72d9b-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="72d9b-154">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="72d9b-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="72d9b-155">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="72d9b-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="72d9b-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="72d9b-156">RELATED LINKS</span></span>

