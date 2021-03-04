---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: e3c464ee8a2ae038a9e6d8d7578c3e4862c16460
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923819"
---
# <span data-ttu-id="1f07f-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1f07f-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="1f07f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f07f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f07f-103">Der Vorgang zum Löschen eines Exports.</span><span class="sxs-lookup"><span data-stu-id="1f07f-103">The operation to delete a export.</span></span>

## <span data-ttu-id="1f07f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f07f-104">SYNTAX</span></span>

### <span data-ttu-id="1f07f-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f07f-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f07f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f07f-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f07f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f07f-107">DESCRIPTION</span></span>
<span data-ttu-id="1f07f-108">Der Vorgang zum Löschen eines Exports.</span><span class="sxs-lookup"><span data-stu-id="1f07f-108">The operation to delete a export.</span></span>

## <span data-ttu-id="1f07f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1f07f-109">EXAMPLES</span></span>

### <span data-ttu-id="1f07f-110">Beispiel 1: Löschen des AzCostManagementExports nach Bereich und Name</span><span class="sxs-lookup"><span data-stu-id="1f07f-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="1f07f-111">Löschen des AzCostManagementExport by Scope und ExportName</span><span class="sxs-lookup"><span data-stu-id="1f07f-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="1f07f-112">Beispiel 2: Löschen des AzCostManagementExport by Export-Objekts</span><span class="sxs-lookup"><span data-stu-id="1f07f-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="1f07f-113">Löschen des AzCostManagementExport By InputObject</span><span class="sxs-lookup"><span data-stu-id="1f07f-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="1f07f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1f07f-114">PARAMETERS</span></span>

### <span data-ttu-id="1f07f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f07f-115">-DefaultProfile</span></span>
<span data-ttu-id="1f07f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f07f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f07f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f07f-117">-InputObject</span></span>
<span data-ttu-id="1f07f-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1f07f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1f07f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1f07f-119">-Name</span></span>
<span data-ttu-id="1f07f-120">Exportname.</span><span class="sxs-lookup"><span data-stu-id="1f07f-120">Export Name.</span></span>

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

### <span data-ttu-id="1f07f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f07f-121">-PassThru</span></span>
<span data-ttu-id="1f07f-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f07f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1f07f-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="1f07f-123">-Scope</span></span>
<span data-ttu-id="1f07f-124">Dieser Parameter definiert den Umfang des Kostenmanagements aus verschiedenen Perspektiven : "Abonnement", "Ressourcengruppe" und "Dienst bereitstellen".</span><span class="sxs-lookup"><span data-stu-id="1f07f-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="1f07f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f07f-125">-Confirm</span></span>
<span data-ttu-id="1f07f-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f07f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f07f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f07f-127">-WhatIf</span></span>
<span data-ttu-id="1f07f-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f07f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f07f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f07f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f07f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f07f-130">CommonParameters</span></span>
<span data-ttu-id="1f07f-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f07f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f07f-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f07f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f07f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1f07f-133">INPUTS</span></span>

### <span data-ttu-id="1f07f-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="1f07f-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="1f07f-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1f07f-135">OUTPUTS</span></span>

### <span data-ttu-id="1f07f-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f07f-136">System.Boolean</span></span>

## <span data-ttu-id="1f07f-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1f07f-137">NOTES</span></span>

<span data-ttu-id="1f07f-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1f07f-138">ALIASES</span></span>

<span data-ttu-id="1f07f-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1f07f-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f07f-140">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="1f07f-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f07f-141">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f07f-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f07f-142">INPUTOBJECT <ICostManagementIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="1f07f-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f07f-143">`[AlertId <String>]`: Warnungs-ID</span><span class="sxs-lookup"><span data-stu-id="1f07f-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="1f07f-144">`[ExportName <String>]`: Name exportieren.</span><span class="sxs-lookup"><span data-stu-id="1f07f-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="1f07f-145">`[ExternalCloudProviderId <String>]`: Dies kann "{externalSubscriptionId}" für verknüpftes Konto oder "{externalBillingAccountId}" für konsolidiertes Konto sein, das mit Dimensions-/Abfragevorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f07f-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="1f07f-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Der externe Cloudanbietertyp, der mit Dimensions-/Abfragevorgängen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="1f07f-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="1f07f-147">Dies umfasst "externalSubscriptions" für verknüpfte Konten und "externalBillingAccounts" für konsolidierte Konten.</span><span class="sxs-lookup"><span data-stu-id="1f07f-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="1f07f-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="1f07f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f07f-149">`[Scope <String>]`: Der Bereich, der Ansichtsvorgängen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1f07f-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="1f07f-150">Dies umfasst "Abonnements/{subscriptionId}" für den Abonnementbereich, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" für resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}" für den Bereich "Management Group", "providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" für den Bereich "Externe Abrechnungskonten", "providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" für den Bereich "Externes Abonnement".</span><span class="sxs-lookup"><span data-stu-id="1f07f-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="1f07f-151">`[ViewName <String>]`: Anzeigename</span><span class="sxs-lookup"><span data-stu-id="1f07f-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="1f07f-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1f07f-152">RELATED LINKS</span></span>

