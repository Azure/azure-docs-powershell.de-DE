---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364495"
---
# <span data-ttu-id="126c3-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="126c3-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="126c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="126c3-102">SYNOPSIS</span></span>
<span data-ttu-id="126c3-103">Löscht einen vorhandenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="126c3-103">Deletes an existing job.</span></span>
<span data-ttu-id="126c3-104">Nur Aufträge in den Zu Zustände "Erstellen" oder "Abgeschlossen" können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="126c3-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="126c3-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="126c3-105">SYNTAX</span></span>

### <span data-ttu-id="126c3-106">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="126c3-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="126c3-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="126c3-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="126c3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="126c3-108">DESCRIPTION</span></span>
<span data-ttu-id="126c3-109">Löscht einen vorhandenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="126c3-109">Deletes an existing job.</span></span>
<span data-ttu-id="126c3-110">Nur Aufträge in den Zu Zustände "Erstellen" oder "Abgeschlossen" können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="126c3-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="126c3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="126c3-111">EXAMPLES</span></span>

### <span data-ttu-id="126c3-112">Beispiel 1: Entfernen des ImportExport-Auftrags nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="126c3-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="126c3-113">Mit diesem Cmdlet wird der Auftrag "ImportExport" nach "resourceGroup" und "Servername" entfernt.</span><span class="sxs-lookup"><span data-stu-id="126c3-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="126c3-114">Beispiel 2: Entfernen des ImportExport-Auftrags nach Identität</span><span class="sxs-lookup"><span data-stu-id="126c3-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="126c3-115">Mit diesem Cmdlet wird der ImportExport-Auftrag nach Identität entfernt.</span><span class="sxs-lookup"><span data-stu-id="126c3-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="126c3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="126c3-116">PARAMETERS</span></span>

### <span data-ttu-id="126c3-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="126c3-117">-AcceptLanguage</span></span>
<span data-ttu-id="126c3-118">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="126c3-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="126c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126c3-119">-DefaultProfile</span></span>
<span data-ttu-id="126c3-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="126c3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="126c3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="126c3-121">-InputObject</span></span>
<span data-ttu-id="126c3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="126c3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="126c3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="126c3-123">-Name</span></span>
<span data-ttu-id="126c3-124">Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="126c3-124">The name of the import/export job.</span></span>

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

### <span data-ttu-id="126c3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="126c3-125">-PassThru</span></span>
<span data-ttu-id="126c3-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="126c3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="126c3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="126c3-127">-ResourceGroupName</span></span>
<span data-ttu-id="126c3-128">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="126c3-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="126c3-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="126c3-129">-SubscriptionId</span></span>
<span data-ttu-id="126c3-130">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="126c3-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="126c3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="126c3-131">-Confirm</span></span>
<span data-ttu-id="126c3-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="126c3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="126c3-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="126c3-133">-WhatIf</span></span>
<span data-ttu-id="126c3-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="126c3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="126c3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="126c3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="126c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126c3-136">CommonParameters</span></span>
<span data-ttu-id="126c3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="126c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126c3-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="126c3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126c3-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="126c3-139">INPUTS</span></span>

### <span data-ttu-id="126c3-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="126c3-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="126c3-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="126c3-141">OUTPUTS</span></span>

### <span data-ttu-id="126c3-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="126c3-142">System.Boolean</span></span>

## <span data-ttu-id="126c3-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="126c3-143">NOTES</span></span>

<span data-ttu-id="126c3-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="126c3-144">ALIASES</span></span>

<span data-ttu-id="126c3-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="126c3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="126c3-146">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="126c3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="126c3-147">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="126c3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="126c3-148">INPUTOBJECT <IImportExportIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="126c3-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="126c3-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="126c3-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="126c3-150">`[JobName <String>]`: Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="126c3-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="126c3-151">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="126c3-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="126c3-152">Beispielsweise "USA, Westen" oder "Westus".</span><span class="sxs-lookup"><span data-stu-id="126c3-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="126c3-153">`[ResourceGroupName <String>]`: Der Ressourcengruppenname identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="126c3-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="126c3-154">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="126c3-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="126c3-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="126c3-155">RELATED LINKS</span></span>

