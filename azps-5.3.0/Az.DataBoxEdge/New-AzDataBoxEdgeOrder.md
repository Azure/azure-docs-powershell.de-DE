---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472719"
---
# <span data-ttu-id="b37a2-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="b37a2-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="b37a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b37a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b37a2-103">Erstellt eine neue Bestellung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="b37a2-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="b37a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b37a2-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b37a2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b37a2-105">DESCRIPTION</span></span>
<span data-ttu-id="b37a2-106">Das **Cmdlet "New-AzDataBoxEdgeOrder"** erstellt eine neue Bestellung für ein Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="b37a2-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="b37a2-107">Eine Datenfeld-Edgegeräteressource muss zuerst erstellt werden, bevor eine Bestellung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b37a2-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="b37a2-108">Sie können Details wie Kontaktperson, Firmenname, E-Mail-Adresse, Adresse usw. als Parameter für die Erstellung der Bestellung angeben.</span><span class="sxs-lookup"><span data-stu-id="b37a2-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="b37a2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b37a2-109">EXAMPLES</span></span>

### <span data-ttu-id="b37a2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b37a2-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="b37a2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b37a2-111">PARAMETERS</span></span>

### <span data-ttu-id="b37a2-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="b37a2-112">-AddressLine1</span></span>
<span data-ttu-id="b37a2-113">Erste Zeile der Adresse</span><span class="sxs-lookup"><span data-stu-id="b37a2-113">Address first line</span></span>

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

### <span data-ttu-id="b37a2-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="b37a2-114">-AddressLine2</span></span>
<span data-ttu-id="b37a2-115">Adresse in zweiter Zeile</span><span class="sxs-lookup"><span data-stu-id="b37a2-115">Address second line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b37a2-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="b37a2-116">-AddressLine3</span></span>
<span data-ttu-id="b37a2-117">Adresse, dritte Zeile</span><span class="sxs-lookup"><span data-stu-id="b37a2-117">Address third line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b37a2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b37a2-118">-AsJob</span></span>
<span data-ttu-id="b37a2-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b37a2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b37a2-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="b37a2-120">-City</span></span>
<span data-ttu-id="b37a2-121">Name der Stadt</span><span class="sxs-lookup"><span data-stu-id="b37a2-121">Name of the City</span></span>

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

### <span data-ttu-id="b37a2-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="b37a2-122">-CompanyName</span></span>
<span data-ttu-id="b37a2-123">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="b37a2-123">Name of the company</span></span>

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

### <span data-ttu-id="b37a2-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="b37a2-124">-ContactPerson</span></span>
<span data-ttu-id="b37a2-125">Name der Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="b37a2-125">Name of the contact person</span></span>

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

### <span data-ttu-id="b37a2-126">-Country</span><span class="sxs-lookup"><span data-stu-id="b37a2-126">-Country</span></span>
<span data-ttu-id="b37a2-127">Name des Landes</span><span class="sxs-lookup"><span data-stu-id="b37a2-127">Name of the Country</span></span>

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

### <span data-ttu-id="b37a2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b37a2-128">-DefaultProfile</span></span>
<span data-ttu-id="b37a2-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b37a2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b37a2-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b37a2-130">-DeviceName</span></span>
<span data-ttu-id="b37a2-131">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="b37a2-131">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b37a2-132">-Email</span><span class="sxs-lookup"><span data-stu-id="b37a2-132">-Email</span></span>
<span data-ttu-id="b37a2-133">Liste der E-Mails zum Empfang von Updates, Maximal 10 E-Mails werden akzeptiert</span><span class="sxs-lookup"><span data-stu-id="b37a2-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b37a2-134">-Phone</span><span class="sxs-lookup"><span data-stu-id="b37a2-134">-Phone</span></span>
<span data-ttu-id="b37a2-135">Telefonnummer der Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="b37a2-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="b37a2-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="b37a2-136">-PostalCode</span></span>
<span data-ttu-id="b37a2-137">Postleitzahl der Adresse</span><span class="sxs-lookup"><span data-stu-id="b37a2-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="b37a2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b37a2-138">-ResourceGroupName</span></span>
<span data-ttu-id="b37a2-139">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b37a2-139">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b37a2-140">-State</span><span class="sxs-lookup"><span data-stu-id="b37a2-140">-State</span></span>
<span data-ttu-id="b37a2-141">Name des Bundesstaats</span><span class="sxs-lookup"><span data-stu-id="b37a2-141">Name of the State</span></span>

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

### <span data-ttu-id="b37a2-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b37a2-142">-Confirm</span></span>
<span data-ttu-id="b37a2-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b37a2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b37a2-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b37a2-144">-WhatIf</span></span>
<span data-ttu-id="b37a2-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b37a2-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b37a2-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b37a2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b37a2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b37a2-147">CommonParameters</span></span>
<span data-ttu-id="b37a2-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b37a2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b37a2-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b37a2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b37a2-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b37a2-150">INPUTS</span></span>

### <span data-ttu-id="b37a2-151">System.String</span><span class="sxs-lookup"><span data-stu-id="b37a2-151">System.String</span></span>

## <span data-ttu-id="b37a2-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b37a2-152">OUTPUTS</span></span>

### <span data-ttu-id="b37a2-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="b37a2-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="b37a2-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b37a2-154">NOTES</span></span>

## <span data-ttu-id="b37a2-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b37a2-155">RELATED LINKS</span></span>
