---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: ae4fc80c54aedf7f35ebfc6c0c5f16bb2e5028ee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844860"
---
# <span data-ttu-id="96635-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="96635-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="96635-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96635-102">SYNOPSIS</span></span>
<span data-ttu-id="96635-103">Löschen eines Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="96635-103">Delete a platform image</span></span>

## <span data-ttu-id="96635-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96635-104">SYNTAX</span></span>

### <span data-ttu-id="96635-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="96635-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="96635-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96635-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96635-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96635-107">DESCRIPTION</span></span>
<span data-ttu-id="96635-108">Löschen eines Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="96635-108">Delete a platform image</span></span>

## <span data-ttu-id="96635-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96635-109">EXAMPLES</span></span>

### <span data-ttu-id="96635-110">Beispiel 1: Entfernen eines Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="96635-110">Example 1: Remove a Platform Image</span></span>
```powershell
PS C:\>Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.0.0
```

<span data-ttu-id="96635-111">Ein erfolgreicher Anruf zum Entfernen eines Platt Form Bilds gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="96635-111">A successful call to remove a platform image will not return any output</span></span>

### <span data-ttu-id="96635-112">Beispiel 2: Entfernen eines Platt Form Bilds, das nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="96635-112">Example 2: Remove a Platform Image the Does Not Exist</span></span>
```powershell
PS C:\>  Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.1.6

```

<span data-ttu-id="96635-113">Ein erfolgreicher Anruf zum Entfernen eines nicht vorhandenen Platt Form Bilds gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="96635-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="96635-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="96635-114">PARAMETERS</span></span>

### <span data-ttu-id="96635-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96635-115">-DefaultProfile</span></span>
<span data-ttu-id="96635-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96635-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96635-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="96635-117">-InputObject</span></span>
<span data-ttu-id="96635-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="96635-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96635-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="96635-119">-Location</span></span>
<span data-ttu-id="96635-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="96635-120">Location of the resource.</span></span>

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

### <span data-ttu-id="96635-121">-Angebot</span><span class="sxs-lookup"><span data-stu-id="96635-121">-Offer</span></span>
<span data-ttu-id="96635-122">Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="96635-122">Name of the offer.</span></span>

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

### <span data-ttu-id="96635-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96635-123">-PassThru</span></span>
<span data-ttu-id="96635-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="96635-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="96635-125">-Publisher</span><span class="sxs-lookup"><span data-stu-id="96635-125">-Publisher</span></span>
<span data-ttu-id="96635-126">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="96635-126">Name of the publisher.</span></span>

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

### <span data-ttu-id="96635-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="96635-127">-Sku</span></span>
<span data-ttu-id="96635-128">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="96635-128">Name of the SKU.</span></span>

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

### <span data-ttu-id="96635-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="96635-129">-SubscriptionId</span></span>
<span data-ttu-id="96635-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="96635-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="96635-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="96635-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96635-132">-Version</span><span class="sxs-lookup"><span data-stu-id="96635-132">-Version</span></span>
<span data-ttu-id="96635-133">Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="96635-133">The version of the resource.</span></span>

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

### <span data-ttu-id="96635-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96635-134">-Confirm</span></span>
<span data-ttu-id="96635-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96635-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96635-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96635-136">-WhatIf</span></span>
<span data-ttu-id="96635-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96635-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96635-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96635-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96635-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96635-139">CommonParameters</span></span>
<span data-ttu-id="96635-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96635-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96635-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96635-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96635-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96635-142">INPUTS</span></span>

### <span data-ttu-id="96635-143">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="96635-143">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="96635-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96635-144">OUTPUTS</span></span>

### <span data-ttu-id="96635-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96635-145">System.Boolean</span></span>



## <span data-ttu-id="96635-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="96635-146">NOTES</span></span>

<span data-ttu-id="96635-147">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="96635-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96635-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="96635-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="96635-149">Inputobject <IComputeAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="96635-149">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96635-150">`[DiskId <String>]`: Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="96635-150">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="96635-151">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="96635-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96635-152">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="96635-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="96635-153">`[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="96635-153">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="96635-154">`[Offer <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="96635-154">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="96635-155">`[Publisher <String>]`: Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="96635-155">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="96635-156">`[QuotaName <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="96635-156">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="96635-157">`[Sku <String>]`: Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="96635-157">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="96635-158">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="96635-158">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="96635-159">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="96635-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="96635-160">`[Type <String>]`: Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="96635-160">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="96635-161">`[Version <String>]`: Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="96635-161">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="96635-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96635-162">RELATED LINKS</span></span>

