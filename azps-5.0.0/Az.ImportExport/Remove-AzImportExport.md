---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177572"
---
# <span data-ttu-id="9405b-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="9405b-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="9405b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9405b-102">SYNOPSIS</span></span>
<span data-ttu-id="9405b-103">Löscht einen vorhandenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="9405b-103">Deletes an existing job.</span></span>
<span data-ttu-id="9405b-104">Nur Aufträge im Status "erstellen" oder "abgeschlossen" können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9405b-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="9405b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9405b-105">SYNTAX</span></span>

### <span data-ttu-id="9405b-106">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="9405b-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9405b-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9405b-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9405b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9405b-108">DESCRIPTION</span></span>
<span data-ttu-id="9405b-109">Löscht einen vorhandenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="9405b-109">Deletes an existing job.</span></span>
<span data-ttu-id="9405b-110">Nur Aufträge im Status "erstellen" oder "abgeschlossen" können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9405b-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="9405b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9405b-111">EXAMPLES</span></span>

### <span data-ttu-id="9405b-112">Beispiel 1: Entfernen des DataObjects-Auftrags nach ResourceGroup und Servername</span><span class="sxs-lookup"><span data-stu-id="9405b-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="9405b-113">Mit diesem Cmdlet wird der DataObjects-Auftrag nach ResourceGroup und Servername entfernt.</span><span class="sxs-lookup"><span data-stu-id="9405b-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="9405b-114">Beispiel 2: Entfernen des DataObjects-Auftrags nach Identität</span><span class="sxs-lookup"><span data-stu-id="9405b-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="9405b-115">Mit diesem Cmdlet wird DataObjects Job nach Identität entfernt.</span><span class="sxs-lookup"><span data-stu-id="9405b-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="9405b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9405b-116">PARAMETERS</span></span>

### <span data-ttu-id="9405b-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="9405b-117">-AcceptLanguage</span></span>
<span data-ttu-id="9405b-118">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="9405b-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="9405b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9405b-119">-DefaultProfile</span></span>
<span data-ttu-id="9405b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9405b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9405b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9405b-121">-InputObject</span></span>
<span data-ttu-id="9405b-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9405b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9405b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9405b-123">-Name</span></span>
<span data-ttu-id="9405b-124">Der Name des Import/Export-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="9405b-124">The name of the import/export job.</span></span>

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

### <span data-ttu-id="9405b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9405b-125">-PassThru</span></span>
<span data-ttu-id="9405b-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="9405b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9405b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9405b-127">-ResourceGroupName</span></span>
<span data-ttu-id="9405b-128">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.</span><span class="sxs-lookup"><span data-stu-id="9405b-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="9405b-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9405b-129">-SubscriptionId</span></span>
<span data-ttu-id="9405b-130">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9405b-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="9405b-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9405b-131">-Confirm</span></span>
<span data-ttu-id="9405b-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9405b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9405b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9405b-133">-WhatIf</span></span>
<span data-ttu-id="9405b-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9405b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9405b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9405b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9405b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9405b-136">CommonParameters</span></span>
<span data-ttu-id="9405b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9405b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9405b-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9405b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9405b-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9405b-139">INPUTS</span></span>

### <span data-ttu-id="9405b-140">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="9405b-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="9405b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9405b-141">OUTPUTS</span></span>

### <span data-ttu-id="9405b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9405b-142">System.Boolean</span></span>

## <span data-ttu-id="9405b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="9405b-143">NOTES</span></span>

<span data-ttu-id="9405b-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="9405b-144">ALIASES</span></span>

<span data-ttu-id="9405b-145">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9405b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9405b-146">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9405b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9405b-147">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="9405b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9405b-148">Inputobject <IImportExportIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9405b-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9405b-149">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="9405b-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9405b-150">`[JobName <String>]`: Der Name des Import/Export-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="9405b-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="9405b-151">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="9405b-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="9405b-152">Beispielsweise West-US oder westus.</span><span class="sxs-lookup"><span data-stu-id="9405b-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="9405b-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.</span><span class="sxs-lookup"><span data-stu-id="9405b-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="9405b-154">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9405b-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="9405b-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9405b-155">RELATED LINKS</span></span>

