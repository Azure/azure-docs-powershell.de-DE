---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: 75c1f01730d4dfe3e9769a430f874887fd2d2090
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148396"
---
# <span data-ttu-id="257d5-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="257d5-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="257d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="257d5-102">SYNOPSIS</span></span>
<span data-ttu-id="257d5-103">Der Vorgang zum Löschen eines Exports.</span><span class="sxs-lookup"><span data-stu-id="257d5-103">The operation to delete a export.</span></span>

## <span data-ttu-id="257d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="257d5-104">SYNTAX</span></span>

### <span data-ttu-id="257d5-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="257d5-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="257d5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="257d5-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="257d5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="257d5-107">DESCRIPTION</span></span>
<span data-ttu-id="257d5-108">Der Vorgang zum Löschen eines Exports.</span><span class="sxs-lookup"><span data-stu-id="257d5-108">The operation to delete a export.</span></span>

## <span data-ttu-id="257d5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="257d5-109">EXAMPLES</span></span>

### <span data-ttu-id="257d5-110">Beispiel 1: Löschen des AzCostManagementExport nach Bereich und Name</span><span class="sxs-lookup"><span data-stu-id="257d5-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="257d5-111">Löschen von "AzCostManagementExport by Scope" und "ExportName"</span><span class="sxs-lookup"><span data-stu-id="257d5-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="257d5-112">Beispiel 2: Löschen des Objekts "AzCostManagementExport by Export"</span><span class="sxs-lookup"><span data-stu-id="257d5-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="257d5-113">Löschen von "AzCostManagementExport by InputObject"</span><span class="sxs-lookup"><span data-stu-id="257d5-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="257d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="257d5-114">PARAMETERS</span></span>

### <span data-ttu-id="257d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257d5-115">-DefaultProfile</span></span>
<span data-ttu-id="257d5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="257d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="257d5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="257d5-117">-InputObject</span></span>
<span data-ttu-id="257d5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="257d5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="257d5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="257d5-119">-Name</span></span>
<span data-ttu-id="257d5-120">Exportname.</span><span class="sxs-lookup"><span data-stu-id="257d5-120">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257d5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="257d5-121">-PassThru</span></span>
<span data-ttu-id="257d5-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="257d5-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="257d5-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="257d5-123">-Scope</span></span>
<span data-ttu-id="257d5-124">Dieser Parameter definiert den Umfang der Kostenmanagement aus unterschiedlichen Perspektiven wie "Abonnement", "Ressourcengruppe" und "Dienst bereitstellen".</span><span class="sxs-lookup"><span data-stu-id="257d5-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257d5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="257d5-125">-Confirm</span></span>
<span data-ttu-id="257d5-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="257d5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="257d5-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="257d5-127">-WhatIf</span></span>
<span data-ttu-id="257d5-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="257d5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="257d5-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="257d5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="257d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257d5-130">CommonParameters</span></span>
<span data-ttu-id="257d5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257d5-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="257d5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257d5-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="257d5-133">INPUTS</span></span>

### <span data-ttu-id="257d5-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="257d5-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="257d5-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="257d5-135">OUTPUTS</span></span>

### <span data-ttu-id="257d5-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="257d5-136">System.Boolean</span></span>

## <span data-ttu-id="257d5-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="257d5-137">NOTES</span></span>

<span data-ttu-id="257d5-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="257d5-138">ALIASES</span></span>

<span data-ttu-id="257d5-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="257d5-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="257d5-140">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="257d5-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="257d5-141">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="257d5-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="257d5-142">INPUTOBJECT <ICostManagementIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="257d5-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="257d5-143">`[AlertId <String>]`: Benachrichtigungs-ID</span><span class="sxs-lookup"><span data-stu-id="257d5-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="257d5-144">`[ExportName <String>]`: Name exportieren.</span><span class="sxs-lookup"><span data-stu-id="257d5-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="257d5-145">`[ExternalCloudProviderId <String>]`: Dies kann "{externalSubscriptionId}" für verknüpftes Konto oder "{externalBillingAccountId}" für konsolidiertes Konto sein, das für Dimensions-/Abfragevorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="257d5-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="257d5-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Der externe Cloudanbietertyp, der Dimensions-/Abfragevorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="257d5-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="257d5-147">Dies schließt "externalSubscriptions" für verknüpfte Konten und "externalBillingAccounts" für konsolidierte Konten ein.</span><span class="sxs-lookup"><span data-stu-id="257d5-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="257d5-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="257d5-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="257d5-149">`[Scope <String>]`: Der Bereich, der Ansichtsvorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="257d5-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="257d5-150">Dies schließt "subscriptions/{subscriptionId}" für den Abonnementbereich ein, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span><span class="sxs-lookup"><span data-stu-id="257d5-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="257d5-151">`[ViewName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="257d5-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="257d5-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="257d5-152">RELATED LINKS</span></span>

