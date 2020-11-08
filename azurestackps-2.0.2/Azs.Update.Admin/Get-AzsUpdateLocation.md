---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006948"
---
# <span data-ttu-id="d4a18-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="d4a18-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="d4a18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4a18-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a18-103">Abrufen eines Update Speicherorts basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="d4a18-103">Get an update location based on name.</span></span>

## <span data-ttu-id="d4a18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4a18-104">SYNTAX</span></span>

### <span data-ttu-id="d4a18-105">Abrufen (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4a18-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4a18-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d4a18-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4a18-107">Liste</span><span class="sxs-lookup"><span data-stu-id="d4a18-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4a18-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4a18-108">DESCRIPTION</span></span>
<span data-ttu-id="d4a18-109">Abrufen eines Update Speicherorts basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="d4a18-109">Get an update location based on name.</span></span>

## <span data-ttu-id="d4a18-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4a18-110">EXAMPLES</span></span>

### <span data-ttu-id="d4a18-111">Beispiel 1: Abrufen aller Aktualisierungsspeicherorte</span><span class="sxs-lookup"><span data-stu-id="d4a18-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="d4a18-112">Ohne Parameter ruft dieser Unifiedgroup alle Update Speicherorte ab.</span><span class="sxs-lookup"><span data-stu-id="d4a18-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="d4a18-113">Beispiel 2: Abrufen der Speicherorte für alle Updates nach Namen</span><span class="sxs-lookup"><span data-stu-id="d4a18-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="d4a18-114">Ruft alle Update Speicherorte ab, die dem angegebenen Name-Parameter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d4a18-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="d4a18-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4a18-115">PARAMETERS</span></span>

### <span data-ttu-id="d4a18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a18-116">-DefaultProfile</span></span>
<span data-ttu-id="d4a18-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4a18-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a18-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4a18-118">-InputObject</span></span>
<span data-ttu-id="d4a18-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d4a18-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d4a18-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d4a18-120">-Name</span></span>
<span data-ttu-id="d4a18-121">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="d4a18-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4a18-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a18-122">-ResourceGroupName</span></span>
<span data-ttu-id="d4a18-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d4a18-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4a18-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d4a18-124">-SubscriptionId</span></span>
<span data-ttu-id="d4a18-125">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d4a18-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4a18-126">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d4a18-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d4a18-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a18-127">CommonParameters</span></span>
<span data-ttu-id="d4a18-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a18-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a18-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4a18-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a18-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4a18-130">INPUTS</span></span>

### <span data-ttu-id="d4a18-131">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d4a18-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="d4a18-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4a18-132">OUTPUTS</span></span>

### <span data-ttu-id="d4a18-133">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. Api20160501. IUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="d4a18-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="d4a18-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4a18-134">NOTES</span></span>

<span data-ttu-id="d4a18-135">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4a18-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4a18-136">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d4a18-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d4a18-137">Inputobject <IUpdateAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="d4a18-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4a18-138">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="d4a18-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4a18-139">`[ResourceGroupName <String>]`: Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d4a18-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="d4a18-140">`[RunName <String>]`: Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="d4a18-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="d4a18-141">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d4a18-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="d4a18-142">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d4a18-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d4a18-143">`[UpdateLocation <String>]`: Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="d4a18-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="d4a18-144">`[UpdateName <String>]`: Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="d4a18-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="d4a18-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4a18-145">RELATED LINKS</span></span>

