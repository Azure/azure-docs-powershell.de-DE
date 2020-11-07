---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842571"
---
# <span data-ttu-id="6032e-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="6032e-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="6032e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6032e-102">SYNOPSIS</span></span>
<span data-ttu-id="6032e-103">Löschen eines bestimmten Katalogelements</span><span class="sxs-lookup"><span data-stu-id="6032e-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="6032e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6032e-104">SYNTAX</span></span>

### <span data-ttu-id="6032e-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="6032e-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6032e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6032e-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6032e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6032e-107">DESCRIPTION</span></span>
<span data-ttu-id="6032e-108">Löschen eines bestimmten Katalogelements</span><span class="sxs-lookup"><span data-stu-id="6032e-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="6032e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6032e-109">EXAMPLES</span></span>

### <span data-ttu-id="6032e-110">Beispiel 1: Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="6032e-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="6032e-111">Löscht TestUbuntu. Test. 1.0.0 aus dem Azure Stack-Katalog.</span><span class="sxs-lookup"><span data-stu-id="6032e-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="6032e-112">Beispiel 2: Remove-AzsGalleryItem-through-Pipeline</span><span class="sxs-lookup"><span data-stu-id="6032e-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="6032e-113">Löscht TestUbuntu. Test. 1.0.0 durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6032e-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="6032e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6032e-114">PARAMETERS</span></span>

### <span data-ttu-id="6032e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6032e-115">-DefaultProfile</span></span>
<span data-ttu-id="6032e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6032e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6032e-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6032e-117">-InputObject</span></span>
<span data-ttu-id="6032e-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6032e-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6032e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6032e-119">-Name</span></span>
<span data-ttu-id="6032e-120">Die Identität des Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="6032e-120">Identity of the gallery item.</span></span>
<span data-ttu-id="6032e-121">Enthält den Namen des Herausgebers, den Elementnamen und kann die durch das Perioden Zeichen getrennte Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="6032e-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6032e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6032e-122">-PassThru</span></span>
<span data-ttu-id="6032e-123">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="6032e-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6032e-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6032e-124">-SubscriptionId</span></span>
<span data-ttu-id="6032e-125">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6032e-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6032e-126">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="6032e-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6032e-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6032e-127">-Confirm</span></span>
<span data-ttu-id="6032e-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6032e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6032e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6032e-129">-WhatIf</span></span>
<span data-ttu-id="6032e-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6032e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6032e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6032e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6032e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6032e-132">CommonParameters</span></span>
<span data-ttu-id="6032e-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6032e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6032e-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6032e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6032e-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6032e-135">INPUTS</span></span>

### <span data-ttu-id="6032e-136">Microsoft. Azure. PowerShell. Cmdlets. Gallery. Models. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="6032e-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="6032e-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6032e-137">OUTPUTS</span></span>

### <span data-ttu-id="6032e-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6032e-138">System.Boolean</span></span>



## <span data-ttu-id="6032e-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="6032e-139">NOTES</span></span>

<span data-ttu-id="6032e-140">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6032e-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6032e-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="6032e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6032e-142">Inputobject <IGalleryIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="6032e-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6032e-143">`[GalleryItemName <String>]`: Identität des Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="6032e-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="6032e-144">Enthält den Namen des Herausgebers, den Elementnamen und kann die durch das Perioden Zeichen getrennte Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="6032e-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="6032e-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="6032e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6032e-146">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6032e-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6032e-147">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="6032e-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6032e-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6032e-148">RELATED LINKS</span></span>

