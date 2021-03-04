---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 668b7be0a4c6f9885bf8ebb3a077d58f99b681fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931936"
---
# <span data-ttu-id="330ac-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="330ac-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="330ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="330ac-102">SYNOPSIS</span></span>
<span data-ttu-id="330ac-103">Erstellt eine neue Bestellung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="330ac-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="330ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="330ac-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="330ac-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="330ac-105">DESCRIPTION</span></span>
<span data-ttu-id="330ac-106">Das **Cmdlet New-AzDataBoxEdgeOrder** erstellt eine neue Reihenfolge für ein Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="330ac-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="330ac-107">Eine Data Box Edge-Geräteressource muss zuerst erstellt werden, bevor sie einen Auftrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="330ac-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="330ac-108">Sie können Details wie Kontaktperson, Firmenname, E-Mail, Adresse usw. als Parameter für die Erstellung der Bestellung angeben.</span><span class="sxs-lookup"><span data-stu-id="330ac-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="330ac-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="330ac-109">EXAMPLES</span></span>

### <span data-ttu-id="330ac-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="330ac-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="330ac-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="330ac-111">PARAMETERS</span></span>

### <span data-ttu-id="330ac-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="330ac-112">-AddressLine1</span></span>
<span data-ttu-id="330ac-113">Erste Zeile "Adresse"</span><span class="sxs-lookup"><span data-stu-id="330ac-113">Address first line</span></span>

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

### <span data-ttu-id="330ac-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="330ac-114">-AddressLine2</span></span>
<span data-ttu-id="330ac-115">Adresse der zweiten Zeile</span><span class="sxs-lookup"><span data-stu-id="330ac-115">Address second line</span></span>

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

### <span data-ttu-id="330ac-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="330ac-116">-AddressLine3</span></span>
<span data-ttu-id="330ac-117">Adresse der dritten Zeile</span><span class="sxs-lookup"><span data-stu-id="330ac-117">Address third line</span></span>

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

### <span data-ttu-id="330ac-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="330ac-118">-AsJob</span></span>
<span data-ttu-id="330ac-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="330ac-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="330ac-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="330ac-120">-City</span></span>
<span data-ttu-id="330ac-121">Name der Stadt</span><span class="sxs-lookup"><span data-stu-id="330ac-121">Name of the City</span></span>

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

### <span data-ttu-id="330ac-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="330ac-122">-CompanyName</span></span>
<span data-ttu-id="330ac-123">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="330ac-123">Name of the company</span></span>

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

### <span data-ttu-id="330ac-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="330ac-124">-ContactPerson</span></span>
<span data-ttu-id="330ac-125">Name der Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="330ac-125">Name of the contact person</span></span>

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

### <span data-ttu-id="330ac-126">-Land</span><span class="sxs-lookup"><span data-stu-id="330ac-126">-Country</span></span>
<span data-ttu-id="330ac-127">Name des Landes</span><span class="sxs-lookup"><span data-stu-id="330ac-127">Name of the Country</span></span>

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

### <span data-ttu-id="330ac-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="330ac-128">-DefaultProfile</span></span>
<span data-ttu-id="330ac-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="330ac-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="330ac-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="330ac-130">-DeviceName</span></span>
<span data-ttu-id="330ac-131">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="330ac-131">Resource Name</span></span>

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

### <span data-ttu-id="330ac-132">-E-Mail</span><span class="sxs-lookup"><span data-stu-id="330ac-132">-Email</span></span>
<span data-ttu-id="330ac-133">Liste der E-Mails, die Aktualisierungen erhalten sollen, Akzeptiert maximal 10 E-Mails</span><span class="sxs-lookup"><span data-stu-id="330ac-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="330ac-134">-Phone</span><span class="sxs-lookup"><span data-stu-id="330ac-134">-Phone</span></span>
<span data-ttu-id="330ac-135">Telefonnummer der Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="330ac-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="330ac-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="330ac-136">-PostalCode</span></span>
<span data-ttu-id="330ac-137">Postleitzahl der Adresse</span><span class="sxs-lookup"><span data-stu-id="330ac-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="330ac-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="330ac-138">-ResourceGroupName</span></span>
<span data-ttu-id="330ac-139">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="330ac-139">Resource Group Name</span></span>

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

### <span data-ttu-id="330ac-140">-State</span><span class="sxs-lookup"><span data-stu-id="330ac-140">-State</span></span>
<span data-ttu-id="330ac-141">Name des Bundesstaats</span><span class="sxs-lookup"><span data-stu-id="330ac-141">Name of the State</span></span>

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

### <span data-ttu-id="330ac-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="330ac-142">-Confirm</span></span>
<span data-ttu-id="330ac-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="330ac-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="330ac-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="330ac-144">-WhatIf</span></span>
<span data-ttu-id="330ac-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="330ac-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="330ac-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="330ac-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="330ac-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="330ac-147">CommonParameters</span></span>
<span data-ttu-id="330ac-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="330ac-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="330ac-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="330ac-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="330ac-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="330ac-150">INPUTS</span></span>

### <span data-ttu-id="330ac-151">System.String</span><span class="sxs-lookup"><span data-stu-id="330ac-151">System.String</span></span>

## <span data-ttu-id="330ac-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="330ac-152">OUTPUTS</span></span>

### <span data-ttu-id="330ac-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="330ac-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="330ac-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="330ac-154">NOTES</span></span>

## <span data-ttu-id="330ac-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="330ac-155">RELATED LINKS</span></span>
