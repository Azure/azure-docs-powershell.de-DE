---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 602797e32e5d29e3dd4ff2b6ade75ff8055efd0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947451"
---
# <span data-ttu-id="066d7-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="066d7-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="066d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="066d7-102">SYNOPSIS</span></span>
<span data-ttu-id="066d7-103">Der Vorgang, um den Ausführungsverlauf eines Exports für den definierten Bereich und Exportnamen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="066d7-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="066d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="066d7-104">SYNTAX</span></span>

### <span data-ttu-id="066d7-105">Get (Standard)</span><span class="sxs-lookup"><span data-stu-id="066d7-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="066d7-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="066d7-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="066d7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="066d7-107">DESCRIPTION</span></span>
<span data-ttu-id="066d7-108">Der Vorgang, um den Ausführungsverlauf eines Exports für den definierten Bereich und Exportnamen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="066d7-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="066d7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="066d7-109">EXAMPLES</span></span>

### <span data-ttu-id="066d7-110">Beispiel 1: AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="066d7-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="066d7-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span><span class="sxs-lookup"><span data-stu-id="066d7-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="066d7-112">Beispiel 2: "AzCostManagementExportExecutionHistory by InputObject"</span><span class="sxs-lookup"><span data-stu-id="066d7-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="066d7-113">Get AzCostManagementExportExecutionHistory By InputObject</span><span class="sxs-lookup"><span data-stu-id="066d7-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="066d7-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="066d7-114">PARAMETERS</span></span>

### <span data-ttu-id="066d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066d7-115">-DefaultProfile</span></span>
<span data-ttu-id="066d7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="066d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="066d7-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="066d7-117">-ExportName</span></span>
<span data-ttu-id="066d7-118">Exportname.</span><span class="sxs-lookup"><span data-stu-id="066d7-118">Export Name.</span></span>

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

### <span data-ttu-id="066d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="066d7-119">-InputObject</span></span>
<span data-ttu-id="066d7-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="066d7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="066d7-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="066d7-121">-Scope</span></span>
<span data-ttu-id="066d7-122">Dieser Parameter definiert den Umfang des Kostenmanagements aus verschiedenen Perspektiven : "Abonnement", "Ressourcengruppe" und "Dienst bereitstellen".</span><span class="sxs-lookup"><span data-stu-id="066d7-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="066d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066d7-123">CommonParameters</span></span>
<span data-ttu-id="066d7-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="066d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066d7-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="066d7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066d7-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="066d7-126">INPUTS</span></span>

### <span data-ttu-id="066d7-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="066d7-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="066d7-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="066d7-128">OUTPUTS</span></span>

### <span data-ttu-id="066d7-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="066d7-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="066d7-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="066d7-130">NOTES</span></span>

<span data-ttu-id="066d7-131">ALIASE</span><span class="sxs-lookup"><span data-stu-id="066d7-131">ALIASES</span></span>

<span data-ttu-id="066d7-132">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="066d7-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="066d7-133">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="066d7-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="066d7-134">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="066d7-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="066d7-135">INPUTOBJECT <ICostManagementIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="066d7-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="066d7-136">`[AlertId <String>]`: Warnungs-ID</span><span class="sxs-lookup"><span data-stu-id="066d7-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="066d7-137">`[ExportName <String>]`: Name exportieren.</span><span class="sxs-lookup"><span data-stu-id="066d7-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="066d7-138">`[ExternalCloudProviderId <String>]`: Dies kann "{externalSubscriptionId}" für verknüpftes Konto oder "{externalBillingAccountId}" für konsolidiertes Konto sein, das mit Dimensions-/Abfragevorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="066d7-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="066d7-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Der externe Cloudanbietertyp, der mit Dimensions-/Abfragevorgängen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="066d7-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="066d7-140">Dies umfasst "externalSubscriptions" für verknüpfte Konten und "externalBillingAccounts" für konsolidierte Konten.</span><span class="sxs-lookup"><span data-stu-id="066d7-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="066d7-141">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="066d7-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="066d7-142">`[Scope <String>]`: Der Bereich, der Ansichtsvorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="066d7-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="066d7-143">Dies umfasst "Abonnements/{subscriptionId}" für den Abonnementbereich, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" für resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}" für den Bereich "Management Group", "providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" für den Bereich "Externe Abrechnungskonten", "providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" für den Bereich "Externes Abonnement".</span><span class="sxs-lookup"><span data-stu-id="066d7-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="066d7-144">`[ViewName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="066d7-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="066d7-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="066d7-145">RELATED LINKS</span></span>

