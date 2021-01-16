---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306384"
---
# <span data-ttu-id="ac626-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="ac626-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="ac626-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac626-102">SYNOPSIS</span></span>
<span data-ttu-id="ac626-103">Erstellt einen neuen Databoxauftrag mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="ac626-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="ac626-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac626-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac626-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac626-105">DESCRIPTION</span></span>
<span data-ttu-id="ac626-106">Das **Cmdlet "New-AzDataBoxJob"** wird zum Erstellen eines neuen Databoxauftrags verwendet, indem die für die Erstellung des Auftrags erforderlichen Details angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ac626-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="ac626-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac626-107">EXAMPLES</span></span>

### <span data-ttu-id="ac626-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ac626-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="ac626-109">Das Cmdlet übernimmt alle erforderlichen Parameter und einige optionale Parameter zum Erstellen des Databoxauftrags.</span><span class="sxs-lookup"><span data-stu-id="ac626-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="ac626-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac626-110">PARAMETERS</span></span>

### <span data-ttu-id="ac626-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="ac626-111">-AddressType</span></span>
<span data-ttu-id="ac626-112">Typ der Adresse.</span><span class="sxs-lookup"><span data-stu-id="ac626-112">Type of Address.</span></span> <span data-ttu-id="ac626-113">Verfügbare Werte: AddressType.None (Standard), AddressType.Residential, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="ac626-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac626-114">-Ort</span><span class="sxs-lookup"><span data-stu-id="ac626-114">-City</span></span>
<span data-ttu-id="ac626-115">Name der Stadt.</span><span class="sxs-lookup"><span data-stu-id="ac626-115">Name of the City.</span></span> <span data-ttu-id="ac626-116">Beispiel: San Francisco</span><span class="sxs-lookup"><span data-stu-id="ac626-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="ac626-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="ac626-117">-CompanyName</span></span>
<span data-ttu-id="ac626-118">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="ac626-118">Name of the company</span></span>

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

### <span data-ttu-id="ac626-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="ac626-119">-ContactName</span></span>
<span data-ttu-id="ac626-120">Kontaktname</span><span class="sxs-lookup"><span data-stu-id="ac626-120">Contact Name</span></span>

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

### <span data-ttu-id="ac626-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="ac626-121">-CountryCode</span></span>
<span data-ttu-id="ac626-122">Ländercode.</span><span class="sxs-lookup"><span data-stu-id="ac626-122">Country Code.</span></span> <span data-ttu-id="ac626-123">Beispiel: USA</span><span class="sxs-lookup"><span data-stu-id="ac626-123">Ex: US</span></span>

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

### <span data-ttu-id="ac626-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="ac626-124">-DataBoxType</span></span>
<span data-ttu-id="ac626-125">Der SKU-Typ des Datenfelds.</span><span class="sxs-lookup"><span data-stu-id="ac626-125">Sku type of Databox.</span></span>  <span data-ttu-id="ac626-126">Verfügbare Werte: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="ac626-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac626-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac626-127">-DefaultProfile</span></span>
<span data-ttu-id="ac626-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac626-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac626-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="ac626-129">-EmailId</span></span>
<span data-ttu-id="ac626-130">Eine Liste der E-Mail-Adressen kann bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ac626-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="ac626-131">Atleast one is mandatory</span><span class="sxs-lookup"><span data-stu-id="ac626-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="ac626-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="ac626-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="ac626-133">Für die Reihenfolge von DataBoxDisk ist die Angabe der erwarteten Daten in Terabyte obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ac626-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac626-134">-Location</span><span class="sxs-lookup"><span data-stu-id="ac626-134">-Location</span></span>
<span data-ttu-id="ac626-135">Speicherort des Abonnements</span><span class="sxs-lookup"><span data-stu-id="ac626-135">Location of the subscription</span></span>

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

### <span data-ttu-id="ac626-136">-Name</span><span class="sxs-lookup"><span data-stu-id="ac626-136">-Name</span></span>
<span data-ttu-id="ac626-137">Name des zu erstellende Databoxauftrags</span><span class="sxs-lookup"><span data-stu-id="ac626-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="ac626-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="ac626-138">-PhoneNumber</span></span>
<span data-ttu-id="ac626-139">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="ac626-139">Contact Number</span></span> 

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

### <span data-ttu-id="ac626-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="ac626-140">-PostalCode</span></span>
<span data-ttu-id="ac626-141">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="ac626-141">Postal Code</span></span>

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

### <span data-ttu-id="ac626-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac626-142">-ResourceGroupName</span></span>
<span data-ttu-id="ac626-143">Ressourcengruppenname, unter dem der Datenfeldauftrag erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ac626-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="ac626-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="ac626-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="ac626-145">Geben Sie den Code für Bundesland oder Kanton ein.</span><span class="sxs-lookup"><span data-stu-id="ac626-145">Input the state or province code.</span></span> <span data-ttu-id="ac626-146">Wie CA – Kalifornien; FL – Florida; NY - New York</span><span class="sxs-lookup"><span data-stu-id="ac626-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="ac626-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ac626-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="ac626-148">Liste der Ressourcen-IDs von Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="ac626-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="ac626-149">Zunächst ist eins obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ac626-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac626-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="ac626-150">-StreetAddress1</span></span>
<span data-ttu-id="ac626-151">Straße</span><span class="sxs-lookup"><span data-stu-id="ac626-151">Street Address</span></span>

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

### <span data-ttu-id="ac626-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="ac626-152">-StreetAddress2</span></span>
<span data-ttu-id="ac626-153">Zusätzliche Straße</span><span class="sxs-lookup"><span data-stu-id="ac626-153">Additional Street Address</span></span>

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

### <span data-ttu-id="ac626-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="ac626-154">-StreetAddress3</span></span>
<span data-ttu-id="ac626-155">Zusätzliche Straße</span><span class="sxs-lookup"><span data-stu-id="ac626-155">Additional Street Address</span></span>

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

### <span data-ttu-id="ac626-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac626-156">-Confirm</span></span>
<span data-ttu-id="ac626-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac626-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac626-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ac626-158">-WhatIf</span></span>
<span data-ttu-id="ac626-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac626-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac626-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac626-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac626-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac626-161">CommonParameters</span></span>
<span data-ttu-id="ac626-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac626-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac626-163">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac626-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac626-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac626-164">INPUTS</span></span>

### <span data-ttu-id="ac626-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ac626-165">System.String[]</span></span>

## <span data-ttu-id="ac626-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac626-166">OUTPUTS</span></span>

### <span data-ttu-id="ac626-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="ac626-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="ac626-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ac626-168">NOTES</span></span>

## <span data-ttu-id="ac626-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ac626-169">RELATED LINKS</span></span>
