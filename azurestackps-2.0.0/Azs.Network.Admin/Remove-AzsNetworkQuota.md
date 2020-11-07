---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842520"
---
# <span data-ttu-id="919c6-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="919c6-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="919c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="919c6-102">SYNOPSIS</span></span>
<span data-ttu-id="919c6-103">Löschen eines Kontingents nach Name</span><span class="sxs-lookup"><span data-stu-id="919c6-103">Delete a quota by name.</span></span>

## <span data-ttu-id="919c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="919c6-104">SYNTAX</span></span>

### <span data-ttu-id="919c6-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="919c6-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="919c6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="919c6-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="919c6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="919c6-107">DESCRIPTION</span></span>
<span data-ttu-id="919c6-108">Löschen eines Kontingents nach Name</span><span class="sxs-lookup"><span data-stu-id="919c6-108">Delete a quota by name.</span></span>

## <span data-ttu-id="919c6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="919c6-109">EXAMPLES</span></span>

### <span data-ttu-id="919c6-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="919c6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="919c6-111">Entfernen eines Netzwerk Kontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="919c6-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="919c6-112">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="919c6-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="919c6-113">Entfernen eines Netzwerk Kontingents mithilfe einer Pipe</span><span class="sxs-lookup"><span data-stu-id="919c6-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="919c6-114">--------------------------Beispiel 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="919c6-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="919c6-115">Entfernen eines Netzwerk Kontingents</span><span class="sxs-lookup"><span data-stu-id="919c6-115">Remove a network quota.</span></span>

## <span data-ttu-id="919c6-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="919c6-116">PARAMETERS</span></span>

### <span data-ttu-id="919c6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="919c6-117">-AsJob</span></span>
<span data-ttu-id="919c6-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="919c6-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="919c6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919c6-119">-DefaultProfile</span></span>
<span data-ttu-id="919c6-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="919c6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="919c6-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="919c6-121">-InputObject</span></span>
<span data-ttu-id="919c6-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="919c6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="919c6-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="919c6-123">-Location</span></span>
<span data-ttu-id="919c6-124">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="919c6-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="919c6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="919c6-125">-Name</span></span>
<span data-ttu-id="919c6-126">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="919c6-126">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="919c6-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="919c6-127">-NoWait</span></span>
<span data-ttu-id="919c6-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="919c6-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="919c6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="919c6-129">-PassThru</span></span>
<span data-ttu-id="919c6-130">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="919c6-130">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="919c6-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="919c6-131">-SubscriptionId</span></span>
<span data-ttu-id="919c6-132">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="919c6-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="919c6-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="919c6-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="919c6-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="919c6-134">-Confirm</span></span>
<span data-ttu-id="919c6-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="919c6-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="919c6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="919c6-136">-WhatIf</span></span>
<span data-ttu-id="919c6-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="919c6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="919c6-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="919c6-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="919c6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919c6-139">CommonParameters</span></span>
<span data-ttu-id="919c6-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919c6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919c6-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="919c6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919c6-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="919c6-142">INPUTS</span></span>

### <span data-ttu-id="919c6-143">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="919c6-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="919c6-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="919c6-144">OUTPUTS</span></span>

### <span data-ttu-id="919c6-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="919c6-145">System.Boolean</span></span>



## <span data-ttu-id="919c6-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="919c6-146">NOTES</span></span>

<span data-ttu-id="919c6-147">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="919c6-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="919c6-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="919c6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="919c6-149">Inputobject <INetworkAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="919c6-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="919c6-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="919c6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="919c6-151">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="919c6-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="919c6-152">`[ResourceName <String>]`: Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="919c6-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="919c6-153">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="919c6-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="919c6-154">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="919c6-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="919c6-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="919c6-155">RELATED LINKS</span></span>

