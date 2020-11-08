---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: a39986404e0969de2db4a2b58e0d275e102799cf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003276"
---
# <span data-ttu-id="75633-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="75633-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="75633-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75633-102">SYNOPSIS</span></span>
<span data-ttu-id="75633-103">Erstellt eine neue Reihenfolge für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="75633-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="75633-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75633-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75633-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75633-105">DESCRIPTION</span></span>
<span data-ttu-id="75633-106">Das Cmdlet **New-AzStackEdgeOrder** erstellt eine neue Reihenfolge für ein Stack-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="75633-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="75633-107">Vor dem Erstellen einer Bestellung muss zuerst eine Stack-Edge-Geräteressource erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="75633-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="75633-108">Sie können Details wie Kontaktperson, Firmenname, e-Mail-Adresse, Anschrift usw. als Parameter für die Erstellung des Auftrags angeben.</span><span class="sxs-lookup"><span data-stu-id="75633-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="75633-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75633-109">EXAMPLES</span></span>

### <span data-ttu-id="75633-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75633-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="75633-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="75633-111">PARAMETERS</span></span>

### <span data-ttu-id="75633-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="75633-112">-AddressLine1</span></span>
<span data-ttu-id="75633-113">Erste Zeile der Adresse</span><span class="sxs-lookup"><span data-stu-id="75633-113">Address first line</span></span>

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

### <span data-ttu-id="75633-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="75633-114">-AddressLine2</span></span>
<span data-ttu-id="75633-115">Zweite Zeile der Adresse</span><span class="sxs-lookup"><span data-stu-id="75633-115">Address second line</span></span>

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

### <span data-ttu-id="75633-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="75633-116">-AddressLine3</span></span>
<span data-ttu-id="75633-117">Adresse dritte Zeile</span><span class="sxs-lookup"><span data-stu-id="75633-117">Address third line</span></span>

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

### <span data-ttu-id="75633-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75633-118">-AsJob</span></span>
<span data-ttu-id="75633-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="75633-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75633-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="75633-120">-City</span></span>
<span data-ttu-id="75633-121">Name des Orts</span><span class="sxs-lookup"><span data-stu-id="75633-121">Name of the City</span></span>

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

### <span data-ttu-id="75633-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="75633-122">-CompanyName</span></span>
<span data-ttu-id="75633-123">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="75633-123">Name of the company</span></span>

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

### <span data-ttu-id="75633-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="75633-124">-ContactPerson</span></span>
<span data-ttu-id="75633-125">Name der Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="75633-125">Name of the contact person</span></span>

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

### <span data-ttu-id="75633-126">-Land</span><span class="sxs-lookup"><span data-stu-id="75633-126">-Country</span></span>
<span data-ttu-id="75633-127">Name des Landes</span><span class="sxs-lookup"><span data-stu-id="75633-127">Name of the Country</span></span>

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

### <span data-ttu-id="75633-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75633-128">-DefaultProfile</span></span>
<span data-ttu-id="75633-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75633-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75633-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="75633-130">-DeviceName</span></span>
<span data-ttu-id="75633-131">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="75633-131">Resource Name</span></span>

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

### <span data-ttu-id="75633-132">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="75633-132">-Email</span></span>
<span data-ttu-id="75633-133">Liste der e-Mails für den Empfang von Updates, akzeptiert maximal 10 e-Mails</span><span class="sxs-lookup"><span data-stu-id="75633-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="75633-134">-Telefon</span><span class="sxs-lookup"><span data-stu-id="75633-134">-Phone</span></span>
<span data-ttu-id="75633-135">Telefonnummer der Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="75633-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="75633-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="75633-136">-PostalCode</span></span>
<span data-ttu-id="75633-137">Postleitzahl der Adresse</span><span class="sxs-lookup"><span data-stu-id="75633-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="75633-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75633-138">-ResourceGroupName</span></span>
<span data-ttu-id="75633-139">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="75633-139">Resource Group Name</span></span>

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

### <span data-ttu-id="75633-140">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="75633-140">-State</span></span>
<span data-ttu-id="75633-141">Name des Bundesstaats</span><span class="sxs-lookup"><span data-stu-id="75633-141">Name of the State</span></span>

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

### <span data-ttu-id="75633-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75633-142">-Confirm</span></span>
<span data-ttu-id="75633-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75633-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75633-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75633-144">-WhatIf</span></span>
<span data-ttu-id="75633-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75633-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75633-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75633-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75633-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75633-147">CommonParameters</span></span>
<span data-ttu-id="75633-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75633-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75633-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75633-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75633-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75633-150">INPUTS</span></span>

### <span data-ttu-id="75633-151">System. String</span><span class="sxs-lookup"><span data-stu-id="75633-151">System.String</span></span>

## <span data-ttu-id="75633-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75633-152">OUTPUTS</span></span>

### <span data-ttu-id="75633-153">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="75633-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="75633-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="75633-154">NOTES</span></span>

## <span data-ttu-id="75633-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75633-155">RELATED LINKS</span></span>
