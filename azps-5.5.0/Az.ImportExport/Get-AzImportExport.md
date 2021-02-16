---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175289"
---
# <span data-ttu-id="d8068-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="d8068-101">Get-AzImportExport</span></span>

## <span data-ttu-id="d8068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8068-102">SYNOPSIS</span></span>
<span data-ttu-id="d8068-103">Ruft Informationen zu einem vorhandenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="d8068-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="d8068-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8068-104">SYNTAX</span></span>

### <span data-ttu-id="d8068-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8068-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8068-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d8068-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8068-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8068-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8068-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="d8068-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d8068-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8068-109">DESCRIPTION</span></span>
<span data-ttu-id="d8068-110">Ruft Informationen zu einem vorhandenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="d8068-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="d8068-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8068-111">EXAMPLES</span></span>

### <span data-ttu-id="d8068-112">Beispiel 1: ImportExport-Auftrag mit Standardkontext erhalten</span><span class="sxs-lookup"><span data-stu-id="d8068-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="d8068-113">Dieses Cmdlet ruft den Auftrag "ImportExport" mit dem Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="d8068-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="d8068-114">Beispiel 2: "ImportExport-Auftrag nach Ressourcengruppe und Auftragsname erhalten"</span><span class="sxs-lookup"><span data-stu-id="d8068-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="d8068-115">Dieses Cmdlet ruft "ImportExport"-Auftrag nach Ressourcengruppe und Auftragsname ab.</span><span class="sxs-lookup"><span data-stu-id="d8068-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="d8068-116">Beispiel 3: Listet alle "ImportExport"-Aufträge in der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="d8068-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="d8068-117">Dieses Cmdlet listet alle "ImportExport"-Aufträge in der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="d8068-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="d8068-118">Beispiel 4: ImportExport-Auftrag nach Identität erhalten</span><span class="sxs-lookup"><span data-stu-id="d8068-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="d8068-119">Diese Cmdletlisten erhalten den ImportExport-Auftrag nach Identität.</span><span class="sxs-lookup"><span data-stu-id="d8068-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="d8068-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8068-120">PARAMETERS</span></span>

### <span data-ttu-id="d8068-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="d8068-121">-AcceptLanguage</span></span>
<span data-ttu-id="d8068-122">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="d8068-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="d8068-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8068-123">-DefaultProfile</span></span>
<span data-ttu-id="d8068-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8068-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8068-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="d8068-125">-Filter</span></span>
<span data-ttu-id="d8068-126">Kann verwendet werden, um die Ergebnisse auf bestimmte Bedingungen zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="d8068-126">Can be used to restrict the results to certain conditions.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8068-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8068-127">-InputObject</span></span>
<span data-ttu-id="d8068-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d8068-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8068-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d8068-129">-Name</span></span>
<span data-ttu-id="d8068-130">Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="d8068-130">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8068-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8068-131">-ResourceGroupName</span></span>
<span data-ttu-id="d8068-132">Der Ressourcengruppenname identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="d8068-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8068-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8068-133">-SubscriptionId</span></span>
<span data-ttu-id="d8068-134">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d8068-134">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8068-135">-Top</span><span class="sxs-lookup"><span data-stu-id="d8068-135">-Top</span></span>
<span data-ttu-id="d8068-136">Ein ganzzahliger Wert, der angibt, wie viele Aufträge mindestens zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8068-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="d8068-137">Der Wert darf 100 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="d8068-137">The value cannot exceed 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8068-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8068-138">CommonParameters</span></span>
<span data-ttu-id="d8068-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8068-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8068-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8068-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8068-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8068-141">INPUTS</span></span>

### <span data-ttu-id="d8068-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="d8068-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="d8068-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8068-143">OUTPUTS</span></span>

### <span data-ttu-id="d8068-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="d8068-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="d8068-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d8068-145">NOTES</span></span>

<span data-ttu-id="d8068-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d8068-146">ALIASES</span></span>

<span data-ttu-id="d8068-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d8068-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8068-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d8068-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8068-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8068-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8068-150">INPUTOBJECT <IImportExportIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d8068-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8068-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d8068-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8068-152">`[JobName <String>]`: Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="d8068-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="d8068-153">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="d8068-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="d8068-154">Beispielsweise "USA, Westen" oder "Westus".</span><span class="sxs-lookup"><span data-stu-id="d8068-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="d8068-155">`[ResourceGroupName <String>]`: Der Ressourcengruppenname identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="d8068-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="d8068-156">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d8068-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="d8068-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d8068-157">RELATED LINKS</span></span>

