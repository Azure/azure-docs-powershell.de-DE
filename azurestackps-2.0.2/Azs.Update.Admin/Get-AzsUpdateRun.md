---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: fb36cb0d1be46abb66a1c0cc97165f8eb9cc3913
ms.sourcegitcommit: f7edd4f5c4bebedc139cb01438081edc6ed560bd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2020
ms.locfileid: "94007555"
---
# <span data-ttu-id="7736f-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="7736f-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="7736f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7736f-102">SYNOPSIS</span></span>
<span data-ttu-id="7736f-103">Rufen Sie eine Instanz von Update Run mit der ID ab.</span><span class="sxs-lookup"><span data-stu-id="7736f-103">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="7736f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7736f-104">SYNTAX</span></span>

### <span data-ttu-id="7736f-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7736f-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7736f-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7736f-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7736f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7736f-107">GetViaIdentity</span></span>
```
Get-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7736f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7736f-108">DESCRIPTION</span></span>
<span data-ttu-id="7736f-109">Rufen Sie eine Instanz von Update Run mit der ID ab.</span><span class="sxs-lookup"><span data-stu-id="7736f-109">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="7736f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7736f-110">EXAMPLES</span></span>

### <span data-ttu-id="7736f-111">Beispiel 1: Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="7736f-111">Example 1: Get-AzsUpdateRun</span></span>
```powershell
PS C:\> Get-AzsUpdateRun

cmdlet Get-AzsUpdateRun at command pipeline position 1
Supply values for the following parameters:
UpdateName: Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="7736f-112">Wenn kein Updatename-Wert angegeben wird, werden Get-UpdateRun immer zur Eingabe aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="7736f-112">If a UpdateName value is not specified, Get-UpdateRun will always ask for input.</span></span>
<span data-ttu-id="7736f-113">Nach der Bereitstellung werden alle Instanzen von UpdateRun ausgegeben, die fehlerhaft oder erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="7736f-113">Once provided, it will output all instances of UpdateRun that were Failed or Successful</span></span>

### <span data-ttu-id="7736f-114">Beispiel 2: Get-AzsUpdateRun nach Updatename</span><span class="sxs-lookup"><span data-stu-id="7736f-114">Example 2: Get-AzsUpdateRun By UpdateName</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="7736f-115">Ruft alle UpdateRuns ab, die einem bestimmten Update zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7736f-115">Will retrieve all UpdateRuns associated with a specific Update</span></span>

### <span data-ttu-id="7736f-116">Beispiel 2: Get-AzsUpdateRun nach Name</span><span class="sxs-lookup"><span data-stu-id="7736f-116">Example 2: Get-AzsUpdateRun By Name</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name northwest/Microsoft1.1907.0.10/45aaeb26-805b-495b-9c8c-d5da5542dbf4

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
```

<span data-ttu-id="7736f-117">Ruft alle UpdateRuns ab, die einem bestimmten Update und einem bestimmten Namen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7736f-117">Will retrieve all UpdateRuns associated with a specific Update and a specific Name</span></span>

## <span data-ttu-id="7736f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="7736f-118">PARAMETERS</span></span>

### <span data-ttu-id="7736f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7736f-119">-DefaultProfile</span></span>
<span data-ttu-id="7736f-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7736f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7736f-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7736f-121">-InputObject</span></span>
<span data-ttu-id="7736f-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7736f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7736f-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="7736f-123">-Location</span></span>
<span data-ttu-id="7736f-124">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="7736f-124">The name of the update location.</span></span>

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

### <span data-ttu-id="7736f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7736f-125">-Name</span></span>
<span data-ttu-id="7736f-126">Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="7736f-126">Update run identifier.</span></span>

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

### <span data-ttu-id="7736f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7736f-127">-ResourceGroupName</span></span>
<span data-ttu-id="7736f-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7736f-128">Resource group name.</span></span>

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

### <span data-ttu-id="7736f-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7736f-129">-SubscriptionId</span></span>
<span data-ttu-id="7736f-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7736f-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7736f-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7736f-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7736f-132">-Updatename</span><span class="sxs-lookup"><span data-stu-id="7736f-132">-UpdateName</span></span>
<span data-ttu-id="7736f-133">Der Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="7736f-133">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7736f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7736f-134">CommonParameters</span></span>
<span data-ttu-id="7736f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7736f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7736f-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7736f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7736f-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7736f-137">INPUTS</span></span>

### <span data-ttu-id="7736f-138">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7736f-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="7736f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7736f-139">OUTPUTS</span></span>

### <span data-ttu-id="7736f-140">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="7736f-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="7736f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7736f-141">NOTES</span></span>

<span data-ttu-id="7736f-142">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7736f-142">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7736f-143">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="7736f-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7736f-144">Inputobject <IUpdateAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="7736f-144">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7736f-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="7736f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7736f-146">`[ResourceGroupName <String>]`: Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="7736f-146">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="7736f-147">`[RunName <String>]`: Update Lauf-ID.</span><span class="sxs-lookup"><span data-stu-id="7736f-147">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="7736f-148">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7736f-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="7736f-149">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7736f-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7736f-150">`[UpdateLocation <String>]`: Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="7736f-150">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="7736f-151">`[UpdateName <String>]`: Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="7736f-151">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="7736f-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7736f-152">RELATED LINKS</span></span>

