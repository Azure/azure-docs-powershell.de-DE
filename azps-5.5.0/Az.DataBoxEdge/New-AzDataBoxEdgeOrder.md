---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148321"
---
# <span data-ttu-id="f8424-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f8424-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="f8424-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8424-102">SYNOPSIS</span></span>
<span data-ttu-id="f8424-103">Erstellt eine neue Bestellung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="f8424-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="f8424-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8424-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8424-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8424-105">DESCRIPTION</span></span>
<span data-ttu-id="f8424-106">Das **Cmdlet "New-AzDataBoxEdgeOrder"** erstellt eine neue Bestellung für ein Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="f8424-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="f8424-107">Eine Datenfeld-Edgegeräteressource muss zuerst erstellt werden, bevor eine Bestellung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f8424-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="f8424-108">Sie können Details wie Kontaktperson, Firmenname, E-Mail-Adresse, Adresse usw. als Parameter für die Erstellung der Bestellung angeben.</span><span class="sxs-lookup"><span data-stu-id="f8424-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="f8424-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8424-109">EXAMPLES</span></span>

### <span data-ttu-id="f8424-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8424-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="f8424-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8424-111">PARAMETERS</span></span>

### <span data-ttu-id="f8424-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="f8424-112">-AddressLine1</span></span>
<span data-ttu-id="f8424-113">Erste Zeile der Adresse</span><span class="sxs-lookup"><span data-stu-id="f8424-113">Address first line</span></span>

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

### <span data-ttu-id="f8424-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="f8424-114">-AddressLine2</span></span>
<span data-ttu-id="f8424-115">Adresse in zweiter Zeile</span><span class="sxs-lookup"><span data-stu-id="f8424-115">Address second line</span></span>

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

### <span data-ttu-id="f8424-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="f8424-116">-AddressLine3</span></span>
<span data-ttu-id="f8424-117">Adresse, dritte Zeile</span><span class="sxs-lookup"><span data-stu-id="f8424-117">Address third line</span></span>

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

### <span data-ttu-id="f8424-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8424-118">-AsJob</span></span>
<span data-ttu-id="f8424-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f8424-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8424-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="f8424-120">-City</span></span>
<span data-ttu-id="f8424-121">Name der Stadt</span><span class="sxs-lookup"><span data-stu-id="f8424-121">Name of the City</span></span>

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

### <span data-ttu-id="f8424-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="f8424-122">-CompanyName</span></span>
<span data-ttu-id="f8424-123">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="f8424-123">Name of the company</span></span>

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

### <span data-ttu-id="f8424-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="f8424-124">-ContactPerson</span></span>
<span data-ttu-id="f8424-125">Name der Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="f8424-125">Name of the contact person</span></span>

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

### <span data-ttu-id="f8424-126">-Country</span><span class="sxs-lookup"><span data-stu-id="f8424-126">-Country</span></span>
<span data-ttu-id="f8424-127">Name des Landes</span><span class="sxs-lookup"><span data-stu-id="f8424-127">Name of the Country</span></span>

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

### <span data-ttu-id="f8424-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8424-128">-DefaultProfile</span></span>
<span data-ttu-id="f8424-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8424-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8424-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f8424-130">-DeviceName</span></span>
<span data-ttu-id="f8424-131">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="f8424-131">Resource Name</span></span>

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

### <span data-ttu-id="f8424-132">-Email</span><span class="sxs-lookup"><span data-stu-id="f8424-132">-Email</span></span>
<span data-ttu-id="f8424-133">Liste der E-Mails zum Empfang von Updates, Maximal 10 E-Mails werden akzeptiert</span><span class="sxs-lookup"><span data-stu-id="f8424-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="f8424-134">-Phone</span><span class="sxs-lookup"><span data-stu-id="f8424-134">-Phone</span></span>
<span data-ttu-id="f8424-135">Telefonnummer der Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="f8424-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="f8424-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="f8424-136">-PostalCode</span></span>
<span data-ttu-id="f8424-137">Postleitzahl der Adresse</span><span class="sxs-lookup"><span data-stu-id="f8424-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="f8424-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8424-138">-ResourceGroupName</span></span>
<span data-ttu-id="f8424-139">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f8424-139">Resource Group Name</span></span>

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

### <span data-ttu-id="f8424-140">-State</span><span class="sxs-lookup"><span data-stu-id="f8424-140">-State</span></span>
<span data-ttu-id="f8424-141">Name des Bundesstaats</span><span class="sxs-lookup"><span data-stu-id="f8424-141">Name of the State</span></span>

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

### <span data-ttu-id="f8424-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8424-142">-Confirm</span></span>
<span data-ttu-id="f8424-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8424-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8424-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f8424-144">-WhatIf</span></span>
<span data-ttu-id="f8424-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8424-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8424-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8424-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8424-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8424-147">CommonParameters</span></span>
<span data-ttu-id="f8424-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8424-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8424-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8424-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8424-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8424-150">INPUTS</span></span>

### <span data-ttu-id="f8424-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f8424-151">System.String</span></span>

## <span data-ttu-id="f8424-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8424-152">OUTPUTS</span></span>

### <span data-ttu-id="f8424-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f8424-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="f8424-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f8424-154">NOTES</span></span>

## <span data-ttu-id="f8424-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f8424-155">RELATED LINKS</span></span>
