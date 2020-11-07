---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: 96c14cd8d8d48b6212ed0e4c7b0d5934754912a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844931"
---
# <span data-ttu-id="fcb7c-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="fcb7c-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="fcb7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcb7c-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb7c-103">Gibt den angeforderten Datenträger Migrationsauftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-103">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="fcb7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcb7c-104">SYNTAX</span></span>

### <span data-ttu-id="fcb7c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcb7c-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] [-SubscriptionId <String[]>] [-Status <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fcb7c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="fcb7c-106">Get</span></span>
```
Get-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fcb7c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fcb7c-107">GetViaIdentity</span></span>
```
Get-AzsDiskMigrationJob -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fcb7c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcb7c-108">DESCRIPTION</span></span>
<span data-ttu-id="fcb7c-109">Gibt den angeforderten Datenträger Migrationsauftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-109">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="fcb7c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcb7c-110">EXAMPLES</span></span>

### <span data-ttu-id="fcb7c-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="fcb7c-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob
```

<span data-ttu-id="fcb7c-112">Gibt eine Liste der verwalteten Datenträger Migrationsaufträge am lokalen Standort zurück.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-112">Returns a list of managed disk migration jobs at the location local.</span></span>

### <span data-ttu-id="fcb7c-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="fcb7c-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob -Name TestNewDiskMigrationJob

CreationTime : 2/26/2020 10:45:41 AM
EndTime      : 2/26/2020 10:46:32 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestNewDiskMigrationJob
Location     : redmond
MigrationId  : TestNewDiskMigrationJob
Name         : redmond/TestNewDiskMigrationJob
StartTime    : 2/26/2020 10:45:41 AM
Status       : Succeeded
Subtask      : {edacd0f6-760a-43f9-a188-8833751f89ce, f1ee38a4-5c27-4728-a12b-36976c565042}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_1
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="fcb7c-114">Abrufen eines bestimmten Migrationsauftrags für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="fcb7c-114">Get a specific managed disk migration job.</span></span>

## <span data-ttu-id="fcb7c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcb7c-115">PARAMETERS</span></span>

### <span data-ttu-id="fcb7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb7c-116">-DefaultProfile</span></span>
<span data-ttu-id="fcb7c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcb7c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fcb7c-118">-InputObject</span></span>
<span data-ttu-id="fcb7c-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fcb7c-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="fcb7c-120">-Location</span></span>
<span data-ttu-id="fcb7c-121">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcb7c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fcb7c-122">-Name</span></span>
<span data-ttu-id="fcb7c-123">Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-123">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcb7c-124">-Status</span><span class="sxs-lookup"><span data-stu-id="fcb7c-124">-Status</span></span>
<span data-ttu-id="fcb7c-125">Die Parameter des Status des Datenträger Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-125">The parameters of disk migration job status.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcb7c-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="fcb7c-126">-SubscriptionId</span></span>
<span data-ttu-id="fcb7c-127">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-127">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fcb7c-128">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fcb7c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb7c-129">CommonParameters</span></span>
<span data-ttu-id="fcb7c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb7c-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcb7c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb7c-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcb7c-132">INPUTS</span></span>

### <span data-ttu-id="fcb7c-133">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="fcb7c-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="fcb7c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcb7c-134">OUTPUTS</span></span>

### <span data-ttu-id="fcb7c-135">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="fcb7c-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="fcb7c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcb7c-136">NOTES</span></span>

<span data-ttu-id="fcb7c-137">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fcb7c-138">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fcb7c-139">Inputobject <IComputeAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="fcb7c-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fcb7c-140">`[DiskId <String>]`: Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="fcb7c-141">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="fcb7c-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fcb7c-142">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="fcb7c-143">`[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="fcb7c-144">`[Offer <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="fcb7c-145">`[Publisher <String>]`: Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="fcb7c-146">`[QuotaName <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="fcb7c-147">`[Sku <String>]`: Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="fcb7c-148">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fcb7c-149">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="fcb7c-150">`[Type <String>]`: Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="fcb7c-151">`[Version <String>]`: Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="fcb7c-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="fcb7c-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcb7c-152">RELATED LINKS</span></span>

