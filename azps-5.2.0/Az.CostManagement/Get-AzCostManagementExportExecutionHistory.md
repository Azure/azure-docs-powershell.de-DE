---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296092"
---
# <span data-ttu-id="e507b-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="e507b-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="e507b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e507b-102">SYNOPSIS</span></span>
<span data-ttu-id="e507b-103">Der Vorgang zum Erhalten des Ausführungsverlaufs eines Exports für den definierten Bereich und Exportnamen.</span><span class="sxs-lookup"><span data-stu-id="e507b-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="e507b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e507b-104">SYNTAX</span></span>

### <span data-ttu-id="e507b-105">Get (Standard)</span><span class="sxs-lookup"><span data-stu-id="e507b-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e507b-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e507b-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e507b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e507b-107">DESCRIPTION</span></span>
<span data-ttu-id="e507b-108">Der Vorgang zum Erhalten des Ausführungsverlaufs eines Exports für den definierten Bereich und Exportnamen.</span><span class="sxs-lookup"><span data-stu-id="e507b-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="e507b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e507b-109">EXAMPLES</span></span>

### <span data-ttu-id="e507b-110">Beispiel 1: Erhalten Von AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="e507b-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="e507b-111">"AzCostManagementExportExecutionHistory By ExportName and Scope" erhalten</span><span class="sxs-lookup"><span data-stu-id="e507b-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="e507b-112">Beispiel 2: Erhalten von "AzCostManagementExportExecutionHistory" von InputObject</span><span class="sxs-lookup"><span data-stu-id="e507b-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="e507b-113">Holen Sie sich AzCostManagementExportExecutionHistory von InputObject</span><span class="sxs-lookup"><span data-stu-id="e507b-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="e507b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e507b-114">PARAMETERS</span></span>

### <span data-ttu-id="e507b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e507b-115">-DefaultProfile</span></span>
<span data-ttu-id="e507b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e507b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e507b-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="e507b-117">-ExportName</span></span>
<span data-ttu-id="e507b-118">Exportname.</span><span class="sxs-lookup"><span data-stu-id="e507b-118">Export Name.</span></span>

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

### <span data-ttu-id="e507b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e507b-119">-InputObject</span></span>
<span data-ttu-id="e507b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e507b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e507b-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="e507b-121">-Scope</span></span>
<span data-ttu-id="e507b-122">Dieser Parameter definiert den Umfang der Kostenmanagement aus unterschiedlichen Perspektiven wie "Abonnement", "Ressourcengruppe" und "Dienst bereitstellen".</span><span class="sxs-lookup"><span data-stu-id="e507b-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="e507b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e507b-123">CommonParameters</span></span>
<span data-ttu-id="e507b-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e507b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e507b-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e507b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e507b-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e507b-126">INPUTS</span></span>

### <span data-ttu-id="e507b-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="e507b-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="e507b-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e507b-128">OUTPUTS</span></span>

### <span data-ttu-id="e507b-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="e507b-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="e507b-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e507b-130">NOTES</span></span>

<span data-ttu-id="e507b-131">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e507b-131">ALIASES</span></span>

<span data-ttu-id="e507b-132">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e507b-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e507b-133">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e507b-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e507b-134">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e507b-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e507b-135">INPUTOBJECT <ICostManagementIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e507b-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e507b-136">`[AlertId <String>]`: Benachrichtigungs-ID</span><span class="sxs-lookup"><span data-stu-id="e507b-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="e507b-137">`[ExportName <String>]`: Name exportieren.</span><span class="sxs-lookup"><span data-stu-id="e507b-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="e507b-138">`[ExternalCloudProviderId <String>]`: Dies kann "{externalSubscriptionId}" für verknüpftes Konto oder "{externalBillingAccountId}" für konsolidiertes Konto sein, das für Dimensions-/Abfragevorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e507b-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="e507b-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Der externe Cloudanbietertyp, der Dimensions-/Abfragevorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e507b-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="e507b-140">Dies schließt "externalSubscriptions" für verknüpfte Konten und "externalBillingAccounts" für konsolidierte Konten ein.</span><span class="sxs-lookup"><span data-stu-id="e507b-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="e507b-141">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e507b-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e507b-142">`[Scope <String>]`: Der Bereich, der Ansichtsvorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e507b-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="e507b-143">Dies schließt "subscriptions/{subscriptionId}" für den Abonnementbereich ein, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span><span class="sxs-lookup"><span data-stu-id="e507b-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="e507b-144">`[ViewName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="e507b-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="e507b-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e507b-145">RELATED LINKS</span></span>

