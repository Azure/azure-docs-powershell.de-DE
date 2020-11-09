---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296242"
---
# <span data-ttu-id="60dee-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="60dee-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="60dee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60dee-102">SYNOPSIS</span></span>
<span data-ttu-id="60dee-103">Gibt die Details zu einem Speicherort zurück, an den Sie die Datenträger senden können, die einem Import-oder Exportauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="60dee-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="60dee-104">Eine Position ist ein Azure-Bereich.</span><span class="sxs-lookup"><span data-stu-id="60dee-104">A location is an Azure region.</span></span>

## <span data-ttu-id="60dee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60dee-105">SYNTAX</span></span>

### <span data-ttu-id="60dee-106">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="60dee-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="60dee-107">Erhalten</span><span class="sxs-lookup"><span data-stu-id="60dee-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="60dee-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="60dee-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="60dee-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60dee-109">DESCRIPTION</span></span>
<span data-ttu-id="60dee-110">Gibt die Details zu einem Speicherort zurück, an den Sie die Datenträger senden können, die einem Import-oder Exportauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="60dee-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="60dee-111">Eine Position ist ein Azure-Bereich.</span><span class="sxs-lookup"><span data-stu-id="60dee-111">A location is an Azure region.</span></span>

## <span data-ttu-id="60dee-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60dee-112">EXAMPLES</span></span>

### <span data-ttu-id="60dee-113">Beispiel 1: Abrufen aller Azure Region-Standortdetails mit dem Standardkontext</span><span class="sxs-lookup"><span data-stu-id="60dee-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="60dee-114">Mit diesem Cmdlet werden alle Standortdetails des Azure-Bereichs mit dem Standardkontext abgerufen.</span><span class="sxs-lookup"><span data-stu-id="60dee-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="60dee-115">Beispiel 2: Abrufen der Standortdetails des Azure-Bereichs nach dem Standortnamen</span><span class="sxs-lookup"><span data-stu-id="60dee-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="60dee-116">Dieses Cmdlet ruft die Details des Azure Region-Standorts nach dem Standortnamen ab.</span><span class="sxs-lookup"><span data-stu-id="60dee-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="60dee-117">Beispiel 3: Abrufen von Details zum Azure Region-Standort nach Identität</span><span class="sxs-lookup"><span data-stu-id="60dee-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="60dee-118">In diesen Cmdlet-Listen werden Standortdetails für Azure-Region nach Identität abgerufen.</span><span class="sxs-lookup"><span data-stu-id="60dee-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="60dee-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="60dee-119">PARAMETERS</span></span>

### <span data-ttu-id="60dee-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="60dee-120">-AcceptLanguage</span></span>
<span data-ttu-id="60dee-121">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="60dee-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="60dee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60dee-122">-DefaultProfile</span></span>
<span data-ttu-id="60dee-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60dee-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60dee-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="60dee-124">-InputObject</span></span>
<span data-ttu-id="60dee-125">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="60dee-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="60dee-126">-Name</span><span class="sxs-lookup"><span data-stu-id="60dee-126">-Name</span></span>
<span data-ttu-id="60dee-127">Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="60dee-127">The name of the location.</span></span>
<span data-ttu-id="60dee-128">Beispielsweise West-US oder westus.</span><span class="sxs-lookup"><span data-stu-id="60dee-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="60dee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60dee-129">CommonParameters</span></span>
<span data-ttu-id="60dee-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60dee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60dee-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60dee-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60dee-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60dee-132">INPUTS</span></span>

### <span data-ttu-id="60dee-133">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="60dee-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="60dee-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60dee-134">OUTPUTS</span></span>

### <span data-ttu-id="60dee-135">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. Api20161101. ILocation</span><span class="sxs-lookup"><span data-stu-id="60dee-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="60dee-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="60dee-136">NOTES</span></span>

<span data-ttu-id="60dee-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="60dee-137">ALIASES</span></span>

<span data-ttu-id="60dee-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60dee-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60dee-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60dee-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60dee-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="60dee-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60dee-141">Inputobject <IImportExportIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="60dee-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60dee-142">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="60dee-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60dee-143">`[JobName <String>]`: Der Name des Import/Export-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="60dee-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="60dee-144">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="60dee-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="60dee-145">Beispielsweise West-US oder westus.</span><span class="sxs-lookup"><span data-stu-id="60dee-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="60dee-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.</span><span class="sxs-lookup"><span data-stu-id="60dee-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="60dee-147">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="60dee-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="60dee-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60dee-148">RELATED LINKS</span></span>

