---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172955"
---
# <span data-ttu-id="3accb-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="3accb-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="3accb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3accb-102">SYNOPSIS</span></span>
<span data-ttu-id="3accb-103">Gibt die Details zu einem Speicherort zurück, an den Sie die Datenträger senden können, die einem Import-oder Exportauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3accb-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="3accb-104">Eine Position ist ein Azure-Bereich.</span><span class="sxs-lookup"><span data-stu-id="3accb-104">A location is an Azure region.</span></span>

## <span data-ttu-id="3accb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3accb-105">SYNTAX</span></span>

### <span data-ttu-id="3accb-106">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="3accb-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3accb-107">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3accb-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3accb-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3accb-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3accb-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3accb-109">DESCRIPTION</span></span>
<span data-ttu-id="3accb-110">Gibt die Details zu einem Speicherort zurück, an den Sie die Datenträger senden können, die einem Import-oder Exportauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3accb-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="3accb-111">Eine Position ist ein Azure-Bereich.</span><span class="sxs-lookup"><span data-stu-id="3accb-111">A location is an Azure region.</span></span>

## <span data-ttu-id="3accb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3accb-112">EXAMPLES</span></span>

### <span data-ttu-id="3accb-113">Beispiel 1: Abrufen aller Azure Region-Standortdetails mit dem Standardkontext</span><span class="sxs-lookup"><span data-stu-id="3accb-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="3accb-114">Mit diesem Cmdlet werden alle Standortdetails des Azure-Bereichs mit dem Standardkontext abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3accb-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="3accb-115">Beispiel 2: Abrufen der Standortdetails des Azure-Bereichs nach dem Standortnamen</span><span class="sxs-lookup"><span data-stu-id="3accb-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="3accb-116">Dieses Cmdlet ruft die Details des Azure Region-Standorts nach dem Standortnamen ab.</span><span class="sxs-lookup"><span data-stu-id="3accb-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="3accb-117">Beispiel 3: Abrufen von Details zum Azure Region-Standort nach Identität</span><span class="sxs-lookup"><span data-stu-id="3accb-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="3accb-118">In diesen Cmdlet-Listen werden Standortdetails für Azure-Region nach Identität abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3accb-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="3accb-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="3accb-119">PARAMETERS</span></span>

### <span data-ttu-id="3accb-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="3accb-120">-AcceptLanguage</span></span>
<span data-ttu-id="3accb-121">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="3accb-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="3accb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3accb-122">-DefaultProfile</span></span>
<span data-ttu-id="3accb-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3accb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3accb-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3accb-124">-InputObject</span></span>
<span data-ttu-id="3accb-125">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3accb-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3accb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3accb-126">-Name</span></span>
<span data-ttu-id="3accb-127">Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="3accb-127">The name of the location.</span></span>
<span data-ttu-id="3accb-128">Beispielsweise West-US oder westus.</span><span class="sxs-lookup"><span data-stu-id="3accb-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="3accb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3accb-129">CommonParameters</span></span>
<span data-ttu-id="3accb-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3accb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3accb-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3accb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3accb-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3accb-132">INPUTS</span></span>

### <span data-ttu-id="3accb-133">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="3accb-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="3accb-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3accb-134">OUTPUTS</span></span>

### <span data-ttu-id="3accb-135">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. Api20161101. ILocation</span><span class="sxs-lookup"><span data-stu-id="3accb-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="3accb-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="3accb-136">NOTES</span></span>

<span data-ttu-id="3accb-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="3accb-137">ALIASES</span></span>

<span data-ttu-id="3accb-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3accb-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3accb-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3accb-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3accb-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="3accb-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3accb-141">Inputobject <IImportExportIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="3accb-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3accb-142">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="3accb-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3accb-143">`[JobName <String>]`: Der Name des Import/Export-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="3accb-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="3accb-144">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="3accb-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="3accb-145">Beispielsweise West-US oder westus.</span><span class="sxs-lookup"><span data-stu-id="3accb-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="3accb-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.</span><span class="sxs-lookup"><span data-stu-id="3accb-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="3accb-147">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3accb-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="3accb-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3accb-148">RELATED LINKS</span></span>

