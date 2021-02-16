---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163929"
---
# <span data-ttu-id="45aea-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="45aea-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="45aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45aea-102">SYNOPSIS</span></span>
<span data-ttu-id="45aea-103">Der Vorgang zum Exportieren für den definierten Bereich nach Exportname.</span><span class="sxs-lookup"><span data-stu-id="45aea-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="45aea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45aea-104">SYNTAX</span></span>

### <span data-ttu-id="45aea-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="45aea-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="45aea-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="45aea-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="45aea-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45aea-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="45aea-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45aea-108">DESCRIPTION</span></span>
<span data-ttu-id="45aea-109">Der Vorgang zum Exportieren für den definierten Bereich nach Exportname.</span><span class="sxs-lookup"><span data-stu-id="45aea-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="45aea-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45aea-110">EXAMPLES</span></span>

### <span data-ttu-id="45aea-111">Beispiel 1: Alle "AzCostManagementExports" nach Bereich erhalten</span><span class="sxs-lookup"><span data-stu-id="45aea-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="45aea-112">Alle AzCostManagementExports nach Bereich erhalten</span><span class="sxs-lookup"><span data-stu-id="45aea-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="45aea-113">Beispiel 2: "AzCostManagementExport nach Name und Bereich erhalten"</span><span class="sxs-lookup"><span data-stu-id="45aea-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="45aea-114">AzCostManagementExport nach Name und Bereich erhalten</span><span class="sxs-lookup"><span data-stu-id="45aea-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="45aea-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45aea-115">PARAMETERS</span></span>

### <span data-ttu-id="45aea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45aea-116">-DefaultProfile</span></span>
<span data-ttu-id="45aea-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45aea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45aea-118">-Expand</span><span class="sxs-lookup"><span data-stu-id="45aea-118">-Expand</span></span>
<span data-ttu-id="45aea-119">Kann verwendet werden, um die Eigenschaften in einem Export zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="45aea-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="45aea-120">Derzeit wird nur "runHistory" unterstützt und gibt Informationen für die letzten 10 Exportausführungen zurück.</span><span class="sxs-lookup"><span data-stu-id="45aea-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="45aea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45aea-121">-InputObject</span></span>
<span data-ttu-id="45aea-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="45aea-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45aea-123">-Name</span><span class="sxs-lookup"><span data-stu-id="45aea-123">-Name</span></span>
<span data-ttu-id="45aea-124">Exportname.</span><span class="sxs-lookup"><span data-stu-id="45aea-124">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45aea-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="45aea-125">-Scope</span></span>
<span data-ttu-id="45aea-126">Dieser Parameter definiert den Umfang der Kostenmanagement aus unterschiedlichen Perspektiven wie "Abonnement", "Ressourcengruppe" und "Dienst bereitstellen".</span><span class="sxs-lookup"><span data-stu-id="45aea-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="45aea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45aea-127">CommonParameters</span></span>
<span data-ttu-id="45aea-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45aea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45aea-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45aea-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45aea-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45aea-130">INPUTS</span></span>

### <span data-ttu-id="45aea-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="45aea-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="45aea-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45aea-132">OUTPUTS</span></span>

### <span data-ttu-id="45aea-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="45aea-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="45aea-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45aea-134">NOTES</span></span>

<span data-ttu-id="45aea-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="45aea-135">ALIASES</span></span>

<span data-ttu-id="45aea-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="45aea-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45aea-137">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45aea-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45aea-138">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45aea-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45aea-139">INPUTOBJECT <ICostManagementIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="45aea-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45aea-140">`[AlertId <String>]`: Benachrichtigungs-ID</span><span class="sxs-lookup"><span data-stu-id="45aea-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="45aea-141">`[ExportName <String>]`: Name exportieren.</span><span class="sxs-lookup"><span data-stu-id="45aea-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="45aea-142">`[ExternalCloudProviderId <String>]`: Dies kann "{externalSubscriptionId}" für verknüpftes Konto oder "{externalBillingAccountId}" für konsolidiertes Konto sein, das für Dimensions-/Abfragevorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="45aea-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="45aea-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Der externe Cloudanbietertyp, der Dimensions-/Abfragevorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="45aea-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="45aea-144">Dies schließt "externalSubscriptions" für verknüpfte Konten und "externalBillingAccounts" für konsolidierte Konten ein.</span><span class="sxs-lookup"><span data-stu-id="45aea-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="45aea-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="45aea-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45aea-146">`[Scope <String>]`: Der Bereich, der Ansichtsvorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="45aea-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="45aea-147">Dies schließt "subscriptions/{subscriptionId}" für den Abonnementbereich ein, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span><span class="sxs-lookup"><span data-stu-id="45aea-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="45aea-148">`[ViewName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="45aea-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="45aea-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45aea-149">RELATED LINKS</span></span>

