---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467771"
---
# <span data-ttu-id="1c3dd-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="1c3dd-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="1c3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3dd-103">Erstellen oder aktualisieren Sie die Metadaten einer DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="1c3dd-104">Das übliche Muster zum Ändern einer Eigenschaft besteht im Abrufen der Metadaten "DigitalTwinsInstance" und der Sicherheitsmetadaten, die dann mit den geänderten Werten in einem neuen Textkörper kombiniert werden, um "DigitalTwinsInstance" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="1c3dd-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c3dd-105">SYNTAX</span></span>

### <span data-ttu-id="1c3dd-106">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c3dd-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c3dd-107">Erstellen</span><span class="sxs-lookup"><span data-stu-id="1c3dd-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c3dd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c3dd-108">DESCRIPTION</span></span>
<span data-ttu-id="1c3dd-109">Erstellen oder aktualisieren Sie die Metadaten einer DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="1c3dd-110">Das übliche Muster zum Ändern einer Eigenschaft besteht im Abrufen der Metadaten "DigitalTwinsInstance" und der Sicherheitsmetadaten, die dann mit den geänderten Werten in einem neuen Textkörper kombiniert werden, um "DigitalTwinsInstance" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="1c3dd-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1c3dd-111">EXAMPLES</span></span>

### <span data-ttu-id="1c3dd-112">Beispiel 1: Standardmäßig wird eine AzDigitalTwinsInstance erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="1c3dd-113">Standardmäßiges Erstellen einer AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="1c3dd-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="1c3dd-114">Beispiel 2: Erstellen eines AzDigitalTwinsInstance von AzDigitalTwins-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="1c3dd-115">Erstellen eines AzDigitalTwinsInstance von AzDigitalTwins-Objekt</span><span class="sxs-lookup"><span data-stu-id="1c3dd-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="1c3dd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c3dd-116">PARAMETERS</span></span>

### <span data-ttu-id="1c3dd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c3dd-117">-AsJob</span></span>
<span data-ttu-id="1c3dd-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1c3dd-118">Run the command as a job</span></span>

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

### <span data-ttu-id="1c3dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3dd-119">-DefaultProfile</span></span>
<span data-ttu-id="1c3dd-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c3dd-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="1c3dd-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="1c3dd-122">Die Beschreibung des DigitalTwins-Diensts.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="1c3dd-123">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für "DIGITALTWINSCREATE"-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c3dd-124">-Location</span><span class="sxs-lookup"><span data-stu-id="1c3dd-124">-Location</span></span>
<span data-ttu-id="1c3dd-125">Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3dd-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1c3dd-126">-NoWait</span></span>
<span data-ttu-id="1c3dd-127">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1c3dd-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1c3dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="1c3dd-129">Der Name der Ressourcengruppe, die "DigitalTwinsInstance" enthält.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3dd-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1c3dd-130">-ResourceName</span></span>
<span data-ttu-id="1c3dd-131">Der Name von "DigitalTwinsInstance".</span><span class="sxs-lookup"><span data-stu-id="1c3dd-131">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3dd-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c3dd-132">-SubscriptionId</span></span>
<span data-ttu-id="1c3dd-133">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-133">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3dd-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c3dd-134">-Tag</span></span>
<span data-ttu-id="1c3dd-135">Die Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-135">The resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3dd-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c3dd-136">-Confirm</span></span>
<span data-ttu-id="1c3dd-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c3dd-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1c3dd-138">-WhatIf</span></span>
<span data-ttu-id="1c3dd-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c3dd-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c3dd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3dd-141">CommonParameters</span></span>
<span data-ttu-id="1c3dd-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3dd-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c3dd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3dd-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1c3dd-144">INPUTS</span></span>

### <span data-ttu-id="1c3dd-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="1c3dd-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="1c3dd-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1c3dd-146">OUTPUTS</span></span>

### <span data-ttu-id="1c3dd-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="1c3dd-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="1c3dd-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1c3dd-148">NOTES</span></span>

<span data-ttu-id="1c3dd-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1c3dd-149">ALIASES</span></span>

<span data-ttu-id="1c3dd-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1c3dd-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c3dd-151">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c3dd-152">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c3dd-153">DIGITALTWINSCREATE <IDigitalTwinsDescription> : Die Beschreibung des DigitalTwins-Diensts.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="1c3dd-154">`Location <String>`: Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="1c3dd-155">`[Tag <IDigitalTwinsResourceTags>]`: Die Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="1c3dd-156">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="1c3dd-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1c3dd-157">RELATED LINKS</span></span>

