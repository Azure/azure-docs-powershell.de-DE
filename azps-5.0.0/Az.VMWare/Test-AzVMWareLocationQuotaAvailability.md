---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179469"
---
# <span data-ttu-id="aa36f-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="aa36f-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="aa36f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa36f-102">SYNOPSIS</span></span>
<span data-ttu-id="aa36f-103">Rückgabe Kontingent für Abonnement nach Region</span><span class="sxs-lookup"><span data-stu-id="aa36f-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="aa36f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa36f-104">SYNTAX</span></span>

### <span data-ttu-id="aa36f-105">Überprüfen (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa36f-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aa36f-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aa36f-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aa36f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa36f-107">DESCRIPTION</span></span>
<span data-ttu-id="aa36f-108">Rückgabe Kontingent für Abonnement nach Region</span><span class="sxs-lookup"><span data-stu-id="aa36f-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="aa36f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa36f-109">EXAMPLES</span></span>

### <span data-ttu-id="aa36f-110">Beispiel 1: Überprüfen der Verfügbarkeit von Kontingenten</span><span class="sxs-lookup"><span data-stu-id="aa36f-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="aa36f-111">Überprüfen der Verfügbarkeit von Kontingenten</span><span class="sxs-lookup"><span data-stu-id="aa36f-111">Check quota availability</span></span>

## <span data-ttu-id="aa36f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa36f-112">PARAMETERS</span></span>

### <span data-ttu-id="aa36f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa36f-113">-DefaultProfile</span></span>
<span data-ttu-id="aa36f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa36f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa36f-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa36f-115">-InputObject</span></span>
<span data-ttu-id="aa36f-116">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="aa36f-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa36f-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="aa36f-117">-Location</span></span>
<span data-ttu-id="aa36f-118">Azure-Bereich</span><span class="sxs-lookup"><span data-stu-id="aa36f-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa36f-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="aa36f-119">-SubscriptionId</span></span>
<span data-ttu-id="aa36f-120">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="aa36f-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa36f-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa36f-121">-Confirm</span></span>
<span data-ttu-id="aa36f-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa36f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa36f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa36f-123">-WhatIf</span></span>
<span data-ttu-id="aa36f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa36f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa36f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa36f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa36f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa36f-126">CommonParameters</span></span>
<span data-ttu-id="aa36f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa36f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa36f-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa36f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa36f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa36f-129">INPUTS</span></span>

### <span data-ttu-id="aa36f-130">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="aa36f-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="aa36f-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa36f-131">OUTPUTS</span></span>

### <span data-ttu-id="aa36f-132">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. Api20200320. IQuota</span><span class="sxs-lookup"><span data-stu-id="aa36f-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="aa36f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa36f-133">NOTES</span></span>

<span data-ttu-id="aa36f-134">Aliase</span><span class="sxs-lookup"><span data-stu-id="aa36f-134">ALIASES</span></span>

<span data-ttu-id="aa36f-135">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa36f-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa36f-136">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa36f-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa36f-137">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="aa36f-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa36f-138">Inputobject <IVMWareIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="aa36f-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa36f-139">`[AuthorizationName <String>]`: Name der Express Route-Schaltkreis Autorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="aa36f-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="aa36f-140">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="aa36f-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="aa36f-141">`[HcxEnterpriseSiteName <String>]`: Name der HCx Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="aa36f-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="aa36f-142">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="aa36f-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa36f-143">`[Location <String>]`: Azure-Bereich</span><span class="sxs-lookup"><span data-stu-id="aa36f-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="aa36f-144">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="aa36f-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="aa36f-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa36f-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aa36f-146">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="aa36f-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="aa36f-147">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="aa36f-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="aa36f-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa36f-148">RELATED LINKS</span></span>

