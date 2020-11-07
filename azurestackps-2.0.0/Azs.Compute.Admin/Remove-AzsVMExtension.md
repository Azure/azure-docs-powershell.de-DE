---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsvmextension
schema: 2.0.0
ms.openlocfilehash: 0b2bca9555b14a391df69acc4abdb2fc8c95017c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844852"
---
# <span data-ttu-id="17fbe-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="17fbe-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="17fbe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="17fbe-103">Löscht das angegebene Image der virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="17fbe-103">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="17fbe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17fbe-104">SYNTAX</span></span>

### <span data-ttu-id="17fbe-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="17fbe-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17fbe-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="17fbe-106">DeleteViaIdentity</span></span>
```
Remove-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17fbe-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17fbe-107">DESCRIPTION</span></span>
<span data-ttu-id="17fbe-108">Löscht das angegebene Image der virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="17fbe-108">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="17fbe-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17fbe-109">EXAMPLES</span></span>

### <span data-ttu-id="17fbe-110">Beispiel 1: Entfernen einer vorhandenen VM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="17fbe-110">Example 1: Remove a VM Extension that Exists</span></span> 
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type MicroExtension -Version 0.1.0
```

<span data-ttu-id="17fbe-111">Ein erfolgreicher Aufruf zum Entfernen eines Compute-Kontingents gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="17fbe-111">A successful call to remove a compute quota will not return any output</span></span>

### <span data-ttu-id="17fbe-112">Beispiel 2: Entfernen einer VM-Erweiterung, die nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="17fbe-112">Example 2: Remove a VM Extension that Does Not Exist</span></span>
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type DoesntExist -Version 9.8.7
```

<span data-ttu-id="17fbe-113">Ein erfolgreicher Anruf zum Entfernen eines nicht vorhandenen Platt Form Bilds gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="17fbe-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="17fbe-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="17fbe-114">PARAMETERS</span></span>

### <span data-ttu-id="17fbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fbe-115">-DefaultProfile</span></span>
<span data-ttu-id="17fbe-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17fbe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17fbe-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="17fbe-117">-InputObject</span></span>
<span data-ttu-id="17fbe-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="17fbe-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="17fbe-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="17fbe-119">-Location</span></span>
<span data-ttu-id="17fbe-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="17fbe-120">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="17fbe-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17fbe-121">-PassThru</span></span>
<span data-ttu-id="17fbe-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="17fbe-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="17fbe-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="17fbe-123">-Publisher</span></span>
<span data-ttu-id="17fbe-124">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="17fbe-124">Name of the publisher.</span></span>

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

### <span data-ttu-id="17fbe-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="17fbe-125">-SubscriptionId</span></span>
<span data-ttu-id="17fbe-126">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="17fbe-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="17fbe-127">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="17fbe-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="17fbe-128">-Typ</span><span class="sxs-lookup"><span data-stu-id="17fbe-128">-Type</span></span>
<span data-ttu-id="17fbe-129">Der Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="17fbe-129">Type of extension.</span></span>

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

### <span data-ttu-id="17fbe-130">-Version</span><span class="sxs-lookup"><span data-stu-id="17fbe-130">-Version</span></span>
<span data-ttu-id="17fbe-131">Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="17fbe-131">The version of the resource.</span></span>

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

### <span data-ttu-id="17fbe-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17fbe-132">-Confirm</span></span>
<span data-ttu-id="17fbe-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17fbe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17fbe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17fbe-134">-WhatIf</span></span>
<span data-ttu-id="17fbe-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17fbe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17fbe-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17fbe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17fbe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fbe-137">CommonParameters</span></span>
<span data-ttu-id="17fbe-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17fbe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fbe-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17fbe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fbe-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17fbe-140">INPUTS</span></span>

### <span data-ttu-id="17fbe-141">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="17fbe-141">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="17fbe-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17fbe-142">OUTPUTS</span></span>

### <span data-ttu-id="17fbe-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17fbe-143">System.Boolean</span></span>



## <span data-ttu-id="17fbe-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="17fbe-144">NOTES</span></span>

<span data-ttu-id="17fbe-145">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17fbe-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17fbe-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="17fbe-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="17fbe-147">Inputobject <IComputeAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="17fbe-147">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="17fbe-148">`[DiskId <String>]`: Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="17fbe-148">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="17fbe-149">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="17fbe-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17fbe-150">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="17fbe-150">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="17fbe-151">`[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="17fbe-151">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="17fbe-152">`[Offer <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="17fbe-152">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="17fbe-153">`[Publisher <String>]`: Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="17fbe-153">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="17fbe-154">`[QuotaName <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="17fbe-154">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="17fbe-155">`[Sku <String>]`: Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="17fbe-155">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="17fbe-156">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="17fbe-156">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="17fbe-157">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="17fbe-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="17fbe-158">`[Type <String>]`: Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="17fbe-158">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="17fbe-159">`[Version <String>]`: Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="17fbe-159">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="17fbe-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17fbe-160">RELATED LINKS</span></span>

