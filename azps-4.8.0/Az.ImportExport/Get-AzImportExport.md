---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167449"
---
# <span data-ttu-id="3a73b-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="3a73b-101">Get-AzImportExport</span></span>

## <span data-ttu-id="3a73b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a73b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a73b-103">Ruft Informationen zu einem vorhandenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="3a73b-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="3a73b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a73b-104">SYNTAX</span></span>

### <span data-ttu-id="3a73b-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a73b-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a73b-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3a73b-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a73b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a73b-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a73b-108">List1</span><span class="sxs-lookup"><span data-stu-id="3a73b-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3a73b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a73b-109">DESCRIPTION</span></span>
<span data-ttu-id="3a73b-110">Ruft Informationen zu einem vorhandenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="3a73b-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="3a73b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a73b-111">EXAMPLES</span></span>

### <span data-ttu-id="3a73b-112">Beispiel 1: Abrufen des DataObjects-Auftrags mit dem Standardkontext</span><span class="sxs-lookup"><span data-stu-id="3a73b-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="3a73b-113">Dieses Cmdlet ruft DataObjects-Auftrag mit dem Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="3a73b-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="3a73b-114">Beispiel 2: Abrufen des DataObjects-Auftrags nach Ressourcengruppe und Auftragsname</span><span class="sxs-lookup"><span data-stu-id="3a73b-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="3a73b-115">Dieses Cmdlet ruft DataObjects Job nach Ressourcengruppe und Auftragsname ab.</span><span class="sxs-lookup"><span data-stu-id="3a73b-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="3a73b-116">Beispiel 3: Listet alle DataObjects-Aufträge in der angegebenen Ressourcengruppe auf</span><span class="sxs-lookup"><span data-stu-id="3a73b-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="3a73b-117">Dieses Cmdlet listet alle DataObjects-Aufträge in der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="3a73b-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="3a73b-118">Beispiel 4: Abrufen des DataObjects-Auftrags nach Identität</span><span class="sxs-lookup"><span data-stu-id="3a73b-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="3a73b-119">Diese Cmdlet-Listen ruft DataObjects Job nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="3a73b-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="3a73b-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a73b-120">PARAMETERS</span></span>

### <span data-ttu-id="3a73b-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="3a73b-121">-AcceptLanguage</span></span>
<span data-ttu-id="3a73b-122">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="3a73b-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="3a73b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a73b-123">-DefaultProfile</span></span>
<span data-ttu-id="3a73b-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a73b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a73b-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="3a73b-125">-Filter</span></span>
<span data-ttu-id="3a73b-126">Kann verwendet werden, um die Ergebnisse auf bestimmte Bedingungen zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="3a73b-126">Can be used to restrict the results to certain conditions.</span></span>

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

### <span data-ttu-id="3a73b-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a73b-127">-InputObject</span></span>
<span data-ttu-id="3a73b-128">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3a73b-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a73b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3a73b-129">-Name</span></span>
<span data-ttu-id="3a73b-130">Der Name des Import/Export-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="3a73b-130">The name of the import/export job.</span></span>

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

### <span data-ttu-id="3a73b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a73b-131">-ResourceGroupName</span></span>
<span data-ttu-id="3a73b-132">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.</span><span class="sxs-lookup"><span data-stu-id="3a73b-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="3a73b-133">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="3a73b-133">-SubscriptionId</span></span>
<span data-ttu-id="3a73b-134">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3a73b-134">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="3a73b-135">-Top</span><span class="sxs-lookup"><span data-stu-id="3a73b-135">-Top</span></span>
<span data-ttu-id="3a73b-136">Ein ganzzahliger Wert, der angibt, wie viele Aufträge höchstens zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3a73b-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="3a73b-137">Der Wert darf 100 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="3a73b-137">The value cannot exceed 100.</span></span>

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

### <span data-ttu-id="3a73b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a73b-138">CommonParameters</span></span>
<span data-ttu-id="3a73b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a73b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a73b-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a73b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a73b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a73b-141">INPUTS</span></span>

### <span data-ttu-id="3a73b-142">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="3a73b-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="3a73b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a73b-143">OUTPUTS</span></span>

### <span data-ttu-id="3a73b-144">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="3a73b-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="3a73b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a73b-145">NOTES</span></span>

<span data-ttu-id="3a73b-146">Aliase</span><span class="sxs-lookup"><span data-stu-id="3a73b-146">ALIASES</span></span>

<span data-ttu-id="3a73b-147">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a73b-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a73b-148">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a73b-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a73b-149">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="3a73b-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a73b-150">Inputobject <IImportExportIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="3a73b-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a73b-151">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="3a73b-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a73b-152">`[JobName <String>]`: Der Name des Import/Export-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="3a73b-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="3a73b-153">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="3a73b-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="3a73b-154">Beispielsweise West-US oder westus.</span><span class="sxs-lookup"><span data-stu-id="3a73b-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="3a73b-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.</span><span class="sxs-lookup"><span data-stu-id="3a73b-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="3a73b-156">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3a73b-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="3a73b-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a73b-157">RELATED LINKS</span></span>

