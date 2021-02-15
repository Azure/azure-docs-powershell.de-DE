---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175276"
---
# <span data-ttu-id="96755-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="96755-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="96755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96755-102">SYNOPSIS</span></span>
<span data-ttu-id="96755-103">Gibt die Details zu einem Speicherort zurück, an den Sie die einem Import- oder Exportauftrag zugeordneten Datenträger versenden können.</span><span class="sxs-lookup"><span data-stu-id="96755-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="96755-104">Ein Speicherort ist eine Azure-Region.</span><span class="sxs-lookup"><span data-stu-id="96755-104">A location is an Azure region.</span></span>

## <span data-ttu-id="96755-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96755-105">SYNTAX</span></span>

### <span data-ttu-id="96755-106">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="96755-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96755-107">Erhalten</span><span class="sxs-lookup"><span data-stu-id="96755-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="96755-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96755-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="96755-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96755-109">DESCRIPTION</span></span>
<span data-ttu-id="96755-110">Gibt die Details zu einem Speicherort zurück, an den Sie die einem Import- oder Exportauftrag zugeordneten Datenträger versenden können.</span><span class="sxs-lookup"><span data-stu-id="96755-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="96755-111">Ein Speicherort ist eine Azure-Region.</span><span class="sxs-lookup"><span data-stu-id="96755-111">A location is an Azure region.</span></span>

## <span data-ttu-id="96755-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="96755-112">EXAMPLES</span></span>

### <span data-ttu-id="96755-113">Beispiel 1: Alle Details zum Standort der Region Azure mit Standardkontext erhalten</span><span class="sxs-lookup"><span data-stu-id="96755-113">Example 1: Get all Azure region location details with default context</span></span>
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

<span data-ttu-id="96755-114">Dieses Cmdlet ruft alle Details zum Standort der Region Azure mit dem Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="96755-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="96755-115">Beispiel 2: Erhalten von Standortdetails für die Region Azure nach Standortname</span><span class="sxs-lookup"><span data-stu-id="96755-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="96755-116">Dieses Cmdlet ruft Standortdetails für die Region Azure nach Standortname ab.</span><span class="sxs-lookup"><span data-stu-id="96755-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="96755-117">Beispiel 3: Erhalten von Standortdetails für die Region Azure nach Identität</span><span class="sxs-lookup"><span data-stu-id="96755-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="96755-118">Diese Cmdletlisten ruft Standortdetails für die Region Azure nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="96755-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="96755-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96755-119">PARAMETERS</span></span>

### <span data-ttu-id="96755-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="96755-120">-AcceptLanguage</span></span>
<span data-ttu-id="96755-121">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="96755-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="96755-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96755-122">-DefaultProfile</span></span>
<span data-ttu-id="96755-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96755-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96755-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96755-124">-InputObject</span></span>
<span data-ttu-id="96755-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="96755-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96755-126">-Name</span><span class="sxs-lookup"><span data-stu-id="96755-126">-Name</span></span>
<span data-ttu-id="96755-127">Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="96755-127">The name of the location.</span></span>
<span data-ttu-id="96755-128">Beispielsweise "USA, Westen" oder "Westus".</span><span class="sxs-lookup"><span data-stu-id="96755-128">For example, West US or westus.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96755-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96755-129">CommonParameters</span></span>
<span data-ttu-id="96755-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96755-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96755-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96755-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96755-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="96755-132">INPUTS</span></span>

### <span data-ttu-id="96755-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="96755-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="96755-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="96755-134">OUTPUTS</span></span>

### <span data-ttu-id="96755-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span><span class="sxs-lookup"><span data-stu-id="96755-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="96755-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="96755-136">NOTES</span></span>

<span data-ttu-id="96755-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="96755-137">ALIASES</span></span>

<span data-ttu-id="96755-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="96755-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96755-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="96755-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96755-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96755-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96755-141">INPUTOBJECT <IImportExportIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="96755-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96755-142">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="96755-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96755-143">`[JobName <String>]`: Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="96755-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="96755-144">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="96755-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="96755-145">Beispielsweise "USA, Westen" oder "Westus".</span><span class="sxs-lookup"><span data-stu-id="96755-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="96755-146">`[ResourceGroupName <String>]`: Der Ressourcengruppenname identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="96755-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="96755-147">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="96755-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="96755-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="96755-148">RELATED LINKS</span></span>

