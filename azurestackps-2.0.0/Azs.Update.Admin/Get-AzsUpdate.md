---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdate
schema: 2.0.0
ms.openlocfilehash: d4acc60a0f5b9acc15efd66187c09ec3acb6cb62
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840959"
---
# <span data-ttu-id="9cb08-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="9cb08-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="9cb08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9cb08-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb08-103">Abrufen eines bestimmten Updates an einem Aktualisierungsspeicherort</span><span class="sxs-lookup"><span data-stu-id="9cb08-103">Get a specific update at an update location.</span></span>

## <span data-ttu-id="9cb08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cb08-104">SYNTAX</span></span>

### <span data-ttu-id="9cb08-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9cb08-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9cb08-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9cb08-106">Get</span></span>
```
Get-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9cb08-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9cb08-107">GetViaIdentity</span></span>
```
Get-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9cb08-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cb08-108">DESCRIPTION</span></span>
<span data-ttu-id="9cb08-109">Abrufen eines bestimmten Updates an einem Aktualisierungsspeicherort</span><span class="sxs-lookup"><span data-stu-id="9cb08-109">Get a specific update at an update location.</span></span>

## <span data-ttu-id="9cb08-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cb08-110">EXAMPLES</span></span>

### <span data-ttu-id="9cb08-111">Beispiel 1: Abrufen aller Updates</span><span class="sxs-lookup"><span data-stu-id="9cb08-111">Example 1: Get All Updates</span></span>
```powershell
PS C:\> Get-AzsUpdate

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="9cb08-112">Ohne Parameter werden Get-AzsUpdate alle Updates auflisten, die der Stempel entdecken kann.</span><span class="sxs-lookup"><span data-stu-id="9cb08-112">Without any parameters, Get-AzsUpdate will list all updates that the stamp can discover</span></span>

### <span data-ttu-id="9cb08-113">Beispiel 2: Abrufen des Updates nach Name</span><span class="sxs-lookup"><span data-stu-id="9cb08-113">Example 2: Get Update by Name</span></span>
```powershell
PS C:\> Get-AzsUpdate -Name Microsoft1.1907.0.10
or
PS C:\> Get-AzsUpdate -Name northwest/Microsoft1.1907.0.10


Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
```

<span data-ttu-id="9cb08-114">Ruft alle Updates ab, die dem angegebenen Namen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9cb08-114">Will retrieve all updates that correspond to the specified Name</span></span>

### <span data-ttu-id="9cb08-115">Beispiel 3: Abrufen aller Updates nach Standort</span><span class="sxs-lookup"><span data-stu-id="9cb08-115">Example 3: Get All Updates by Location</span></span>
```powershell
PS C:\> Get-AzsUpdate -Location northwest

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="9cb08-116">Ruft alle Aktualisierungen innerhalb eines angegebenen Speicherorts ab.</span><span class="sxs-lookup"><span data-stu-id="9cb08-116">Will retrieve all updates within a specified Location.</span></span>
<span data-ttu-id="9cb08-117">Derzeit wird nur ein Standort unterstützt, sodass dies gleichbedeutend mit nur Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="9cb08-117">Currently, only one location is supported so this is the equivalent as just Get-AzsUpdate</span></span>

## <span data-ttu-id="9cb08-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cb08-118">PARAMETERS</span></span>

### <span data-ttu-id="9cb08-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb08-119">-DefaultProfile</span></span>
<span data-ttu-id="9cb08-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9cb08-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb08-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9cb08-121">-InputObject</span></span>
<span data-ttu-id="9cb08-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9cb08-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9cb08-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="9cb08-123">-Location</span></span>
<span data-ttu-id="9cb08-124">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="9cb08-124">The name of the update location.</span></span>

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

### <span data-ttu-id="9cb08-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9cb08-125">-Name</span></span>
<span data-ttu-id="9cb08-126">Der Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="9cb08-126">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9cb08-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb08-127">-ResourceGroupName</span></span>
<span data-ttu-id="9cb08-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9cb08-128">Resource group name.</span></span>

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

### <span data-ttu-id="9cb08-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9cb08-129">-SubscriptionId</span></span>
<span data-ttu-id="9cb08-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9cb08-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9cb08-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9cb08-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9cb08-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb08-132">CommonParameters</span></span>
<span data-ttu-id="9cb08-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb08-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb08-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cb08-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb08-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9cb08-135">INPUTS</span></span>

### <span data-ttu-id="9cb08-136">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9cb08-136">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="9cb08-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9cb08-137">OUTPUTS</span></span>

### <span data-ttu-id="9cb08-138">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. Api20160501. IUpdate</span><span class="sxs-lookup"><span data-stu-id="9cb08-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdate</span></span>



## <span data-ttu-id="9cb08-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="9cb08-139">NOTES</span></span>

<span data-ttu-id="9cb08-140">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9cb08-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9cb08-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="9cb08-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9cb08-142">Inputobject <IUpdateAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9cb08-142">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9cb08-143">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="9cb08-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9cb08-144">`[ResourceGroupName <String>]`: Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9cb08-144">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="9cb08-145">`[RunName <String>]`: Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="9cb08-145">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="9cb08-146">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9cb08-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="9cb08-147">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9cb08-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9cb08-148">`[UpdateLocation <String>]`: Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="9cb08-148">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="9cb08-149">`[UpdateName <String>]`: Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="9cb08-149">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="9cb08-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9cb08-150">RELATED LINKS</span></span>

