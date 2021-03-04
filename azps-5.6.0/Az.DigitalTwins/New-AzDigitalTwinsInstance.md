---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: 54fdbcfe83dd93101030d92f9f3eec19d1a2564f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935123"
---
# <span data-ttu-id="73903-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="73903-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="73903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73903-102">SYNOPSIS</span></span>
<span data-ttu-id="73903-103">Erstellen oder aktualisieren Sie die Metadaten einer DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="73903-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="73903-104">Das übliche Muster zum Ändern einer Eigenschaft besteht im Abrufen der DigitalTwinsInstance- und Sicherheitsmetadaten, und kombinieren Sie sie dann mit den geänderten Werten in einem neuen Textkörper, um die DigitalTwinsInstance zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="73903-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="73903-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73903-105">SYNTAX</span></span>

### <span data-ttu-id="73903-106">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="73903-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="73903-107">Erstellen</span><span class="sxs-lookup"><span data-stu-id="73903-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="73903-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73903-108">DESCRIPTION</span></span>
<span data-ttu-id="73903-109">Erstellen oder aktualisieren Sie die Metadaten einer DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="73903-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="73903-110">Das übliche Muster zum Ändern einer Eigenschaft besteht im Abrufen der DigitalTwinsInstance- und Sicherheitsmetadaten, und kombinieren Sie sie dann mit den geänderten Werten in einem neuen Textkörper, um die DigitalTwinsInstance zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="73903-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="73903-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73903-111">EXAMPLES</span></span>

### <span data-ttu-id="73903-112">Beispiel 1: Standardmäßig eine AzDigitalTwinsInstance erstellen.</span><span class="sxs-lookup"><span data-stu-id="73903-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="73903-113">Standardmäßiges Erstellen einer AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="73903-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="73903-114">Beispiel 2: Erstellen eines AzDigitalTwinsInstance von AzDigitalTwins-Objekts.</span><span class="sxs-lookup"><span data-stu-id="73903-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="73903-115">Erstellen eines AzDigitalTwinsInstance by AzDigitalTwins-Objekts</span><span class="sxs-lookup"><span data-stu-id="73903-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="73903-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="73903-116">PARAMETERS</span></span>

### <span data-ttu-id="73903-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73903-117">-AsJob</span></span>
<span data-ttu-id="73903-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="73903-118">Run the command as a job</span></span>

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

### <span data-ttu-id="73903-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73903-119">-DefaultProfile</span></span>
<span data-ttu-id="73903-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73903-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73903-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="73903-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="73903-122">Die Beschreibung des DigitalTwins-Diensts.</span><span class="sxs-lookup"><span data-stu-id="73903-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="73903-123">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für DIGITALTWINSCREATE-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="73903-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="73903-124">-Location</span><span class="sxs-lookup"><span data-stu-id="73903-124">-Location</span></span>
<span data-ttu-id="73903-125">Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="73903-125">The resource location.</span></span>

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

### <span data-ttu-id="73903-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="73903-126">-NoWait</span></span>
<span data-ttu-id="73903-127">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="73903-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="73903-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73903-128">-ResourceGroupName</span></span>
<span data-ttu-id="73903-129">Der Name der Ressourcengruppe, die den DigitalTwinsInstance enthält.</span><span class="sxs-lookup"><span data-stu-id="73903-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="73903-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="73903-130">-ResourceName</span></span>
<span data-ttu-id="73903-131">Der Name der DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="73903-131">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="73903-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73903-132">-SubscriptionId</span></span>
<span data-ttu-id="73903-133">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="73903-133">The subscription identifier.</span></span>

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

### <span data-ttu-id="73903-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="73903-134">-Tag</span></span>
<span data-ttu-id="73903-135">Die Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="73903-135">The resource tags.</span></span>

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

### <span data-ttu-id="73903-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73903-136">-Confirm</span></span>
<span data-ttu-id="73903-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73903-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73903-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73903-138">-WhatIf</span></span>
<span data-ttu-id="73903-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73903-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73903-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73903-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73903-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73903-141">CommonParameters</span></span>
<span data-ttu-id="73903-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73903-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73903-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73903-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73903-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73903-144">INPUTS</span></span>

### <span data-ttu-id="73903-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="73903-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="73903-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73903-146">OUTPUTS</span></span>

### <span data-ttu-id="73903-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="73903-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="73903-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="73903-148">NOTES</span></span>

<span data-ttu-id="73903-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="73903-149">ALIASES</span></span>

<span data-ttu-id="73903-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="73903-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73903-151">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="73903-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73903-152">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73903-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73903-153">DIGITALTWINSCREATE <IDigitalTwinsDescription> : Die Beschreibung des DigitalTwins-Diensts.</span><span class="sxs-lookup"><span data-stu-id="73903-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="73903-154">`Location <String>`: Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="73903-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="73903-155">`[Tag <IDigitalTwinsResourceTags>]`: Die Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="73903-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="73903-156">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="73903-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="73903-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="73903-157">RELATED LINKS</span></span>

