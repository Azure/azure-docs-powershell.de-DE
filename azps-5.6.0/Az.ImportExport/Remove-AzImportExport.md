---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: c4ba805ca2f8f89fcc3ed23747f71c9efff01d47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931168"
---
# <span data-ttu-id="e8fa1-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e8fa1-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="e8fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="e8fa1-103">Löscht einen vorhandenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-103">Deletes an existing job.</span></span>
<span data-ttu-id="e8fa1-104">Nur Aufträge im Zustände Erstellen oder Abgeschlossen können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="e8fa1-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8fa1-105">SYNTAX</span></span>

### <span data-ttu-id="e8fa1-106">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8fa1-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e8fa1-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e8fa1-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e8fa1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8fa1-108">DESCRIPTION</span></span>
<span data-ttu-id="e8fa1-109">Löscht einen vorhandenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-109">Deletes an existing job.</span></span>
<span data-ttu-id="e8fa1-110">Nur Aufträge im Zustände Erstellen oder Abgeschlossen können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="e8fa1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8fa1-111">EXAMPLES</span></span>

### <span data-ttu-id="e8fa1-112">Beispiel 1: Entfernen des ImportExportauftrags nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="e8fa1-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="e8fa1-113">Dieses Cmdlet entfernt ImportExportauftrag nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="e8fa1-114">Beispiel 2: Entfernen des ImportExportauftrags nach Identität</span><span class="sxs-lookup"><span data-stu-id="e8fa1-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="e8fa1-115">Dieses Cmdlet entfernt ImportExportauftrag nach Identität.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="e8fa1-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e8fa1-116">PARAMETERS</span></span>

### <span data-ttu-id="e8fa1-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e8fa1-117">-AcceptLanguage</span></span>
<span data-ttu-id="e8fa1-118">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="e8fa1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8fa1-119">-DefaultProfile</span></span>
<span data-ttu-id="e8fa1-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8fa1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8fa1-121">-InputObject</span></span>
<span data-ttu-id="e8fa1-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fa1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e8fa1-123">-Name</span></span>
<span data-ttu-id="e8fa1-124">Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-124">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fa1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8fa1-125">-PassThru</span></span>
<span data-ttu-id="e8fa1-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e8fa1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8fa1-127">-ResourceGroupName</span></span>
<span data-ttu-id="e8fa1-128">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="e8fa1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8fa1-129">-SubscriptionId</span></span>
<span data-ttu-id="e8fa1-130">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-130">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fa1-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8fa1-131">-Confirm</span></span>
<span data-ttu-id="e8fa1-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8fa1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8fa1-133">-WhatIf</span></span>
<span data-ttu-id="e8fa1-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8fa1-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8fa1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8fa1-136">CommonParameters</span></span>
<span data-ttu-id="e8fa1-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8fa1-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8fa1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8fa1-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8fa1-139">INPUTS</span></span>

### <span data-ttu-id="e8fa1-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="e8fa1-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="e8fa1-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8fa1-141">OUTPUTS</span></span>

### <span data-ttu-id="e8fa1-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e8fa1-142">System.Boolean</span></span>

## <span data-ttu-id="e8fa1-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e8fa1-143">NOTES</span></span>

<span data-ttu-id="e8fa1-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e8fa1-144">ALIASES</span></span>

<span data-ttu-id="e8fa1-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e8fa1-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e8fa1-146">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e8fa1-147">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e8fa1-148">INPUTOBJECT <IImportExportIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="e8fa1-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e8fa1-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e8fa1-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e8fa1-150">`[JobName <String>]`: Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="e8fa1-151">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="e8fa1-152">Beispiel: West US oder westus.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="e8fa1-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="e8fa1-154">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e8fa1-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="e8fa1-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e8fa1-155">RELATED LINKS</span></span>

