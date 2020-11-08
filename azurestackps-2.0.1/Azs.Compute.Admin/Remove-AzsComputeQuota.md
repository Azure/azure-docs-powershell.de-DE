---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005574"
---
# <span data-ttu-id="3cd7a-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="3cd7a-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="3cd7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cd7a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd7a-103">Löschen eines vorhandenen Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="3cd7a-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="3cd7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cd7a-104">SYNTAX</span></span>

### <span data-ttu-id="3cd7a-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cd7a-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3cd7a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3cd7a-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3cd7a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cd7a-107">DESCRIPTION</span></span>
<span data-ttu-id="3cd7a-108">Löschen eines vorhandenen Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="3cd7a-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="3cd7a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cd7a-109">EXAMPLES</span></span>

### <span data-ttu-id="3cd7a-110">Beispiel 1: Entfernen eines Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="3cd7a-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="3cd7a-111">Ein erfolgreicher Aufruf zum Entfernen eines Compute-Kontingents gibt keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="3cd7a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cd7a-112">PARAMETERS</span></span>

### <span data-ttu-id="3cd7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd7a-113">-DefaultProfile</span></span>
<span data-ttu-id="3cd7a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cd7a-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3cd7a-115">-InputObject</span></span>
<span data-ttu-id="3cd7a-116">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3cd7a-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="3cd7a-117">-Location</span></span>
<span data-ttu-id="3cd7a-118">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-118">Location of the resource.</span></span>

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

### <span data-ttu-id="3cd7a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3cd7a-119">-Name</span></span>
<span data-ttu-id="3cd7a-120">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-120">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3cd7a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cd7a-121">-PassThru</span></span>
<span data-ttu-id="3cd7a-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="3cd7a-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3cd7a-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="3cd7a-123">-SubscriptionId</span></span>
<span data-ttu-id="3cd7a-124">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3cd7a-125">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3cd7a-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cd7a-126">-Confirm</span></span>
<span data-ttu-id="3cd7a-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cd7a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cd7a-128">-WhatIf</span></span>
<span data-ttu-id="3cd7a-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cd7a-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cd7a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd7a-131">CommonParameters</span></span>
<span data-ttu-id="3cd7a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd7a-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cd7a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd7a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cd7a-134">INPUTS</span></span>

### <span data-ttu-id="3cd7a-135">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3cd7a-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="3cd7a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cd7a-136">OUTPUTS</span></span>

### <span data-ttu-id="3cd7a-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3cd7a-137">System.Boolean</span></span>



## <span data-ttu-id="3cd7a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cd7a-138">NOTES</span></span>

<span data-ttu-id="3cd7a-139">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3cd7a-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3cd7a-141">Inputobject <IComputeAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="3cd7a-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3cd7a-142">`[DiskId <String>]`: Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="3cd7a-143">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="3cd7a-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3cd7a-144">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3cd7a-145">`[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="3cd7a-146">`[Offer <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="3cd7a-147">`[Publisher <String>]`: Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="3cd7a-148">`[QuotaName <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3cd7a-149">`[Sku <String>]`: Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="3cd7a-150">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3cd7a-151">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3cd7a-152">`[Type <String>]`: Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="3cd7a-153">`[Version <String>]`: Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3cd7a-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="3cd7a-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cd7a-154">RELATED LINKS</span></span>

