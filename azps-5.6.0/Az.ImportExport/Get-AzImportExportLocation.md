---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: 928ac0254619a2924421a0b52bf20212b8ba19a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924107"
---
# <span data-ttu-id="1acfc-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="1acfc-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="1acfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1acfc-102">SYNOPSIS</span></span>
<span data-ttu-id="1acfc-103">Gibt die Details zu einem Speicherort zurück, an den Sie die Datenträger versenden können, die einem Import- oder Exportauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1acfc-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="1acfc-104">Ein Speicherort ist eine Azure-Region.</span><span class="sxs-lookup"><span data-stu-id="1acfc-104">A location is an Azure region.</span></span>

## <span data-ttu-id="1acfc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1acfc-105">SYNTAX</span></span>

### <span data-ttu-id="1acfc-106">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="1acfc-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1acfc-107">Erhalten</span><span class="sxs-lookup"><span data-stu-id="1acfc-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1acfc-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1acfc-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1acfc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1acfc-109">DESCRIPTION</span></span>
<span data-ttu-id="1acfc-110">Gibt die Details zu einem Speicherort zurück, an den Sie die Datenträger versenden können, die einem Import- oder Exportauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1acfc-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="1acfc-111">Ein Speicherort ist eine Azure-Region.</span><span class="sxs-lookup"><span data-stu-id="1acfc-111">A location is an Azure region.</span></span>

## <span data-ttu-id="1acfc-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1acfc-112">EXAMPLES</span></span>

### <span data-ttu-id="1acfc-113">Beispiel 1: Alle Details zum Standort der Azure-Region mit Standardkontext</span><span class="sxs-lookup"><span data-stu-id="1acfc-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="1acfc-114">Dieses Cmdlet ruft alle Details zum Standort der Azure-Region mit dem Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="1acfc-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="1acfc-115">Beispiel 2: Informationen zum Standort der Azure-Region nach Standortname</span><span class="sxs-lookup"><span data-stu-id="1acfc-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="1acfc-116">Dieses Cmdlet ruft Die Standortdetails der Azure-Region nach Standortname ab.</span><span class="sxs-lookup"><span data-stu-id="1acfc-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="1acfc-117">Beispiel 3: Informationen zum Standort der Azure-Region nach Identität</span><span class="sxs-lookup"><span data-stu-id="1acfc-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="1acfc-118">Diese Cmdletlisten ruft Die Standortdetails der Azure-Region nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="1acfc-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="1acfc-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1acfc-119">PARAMETERS</span></span>

### <span data-ttu-id="1acfc-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="1acfc-120">-AcceptLanguage</span></span>
<span data-ttu-id="1acfc-121">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="1acfc-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="1acfc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1acfc-122">-DefaultProfile</span></span>
<span data-ttu-id="1acfc-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1acfc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1acfc-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1acfc-124">-InputObject</span></span>
<span data-ttu-id="1acfc-125">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1acfc-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1acfc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1acfc-126">-Name</span></span>
<span data-ttu-id="1acfc-127">Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="1acfc-127">The name of the location.</span></span>
<span data-ttu-id="1acfc-128">Beispiel: West US oder westus.</span><span class="sxs-lookup"><span data-stu-id="1acfc-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="1acfc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1acfc-129">CommonParameters</span></span>
<span data-ttu-id="1acfc-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1acfc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1acfc-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1acfc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1acfc-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1acfc-132">INPUTS</span></span>

### <span data-ttu-id="1acfc-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="1acfc-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="1acfc-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1acfc-134">OUTPUTS</span></span>

### <span data-ttu-id="1acfc-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span><span class="sxs-lookup"><span data-stu-id="1acfc-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="1acfc-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1acfc-136">NOTES</span></span>

<span data-ttu-id="1acfc-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1acfc-137">ALIASES</span></span>

<span data-ttu-id="1acfc-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1acfc-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1acfc-139">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="1acfc-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1acfc-140">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1acfc-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1acfc-141">INPUTOBJECT <IImportExportIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="1acfc-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1acfc-142">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="1acfc-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1acfc-143">`[JobName <String>]`: Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="1acfc-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="1acfc-144">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="1acfc-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="1acfc-145">Beispiel: West US oder westus.</span><span class="sxs-lookup"><span data-stu-id="1acfc-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="1acfc-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1acfc-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="1acfc-147">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="1acfc-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="1acfc-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1acfc-148">RELATED LINKS</span></span>

