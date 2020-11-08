---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174801"
---
# <span data-ttu-id="8de68-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="8de68-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="8de68-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8de68-102">SYNOPSIS</span></span>
<span data-ttu-id="8de68-103">Erstellt einen neuen DataBox-Auftrag unter Verwendung der angegebenen Parameter</span><span class="sxs-lookup"><span data-stu-id="8de68-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="8de68-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8de68-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de68-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8de68-105">DESCRIPTION</span></span>
<span data-ttu-id="8de68-106">Das Cmdlet **New-AzDataBoxJob** wird zum Erstellen eines neuen DataBox-Auftrags verwendet, indem die für die Erstellung des Auftrags erforderlichen Details angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8de68-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="8de68-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8de68-107">EXAMPLES</span></span>

### <span data-ttu-id="8de68-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8de68-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="8de68-109">Das Cmdlet akzeptiert alle erforderlichen Parameter und einige optionale Parameter zum Erstellen des DataBox-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="8de68-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="8de68-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8de68-110">PARAMETERS</span></span>

### <span data-ttu-id="8de68-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="8de68-111">-AddressType</span></span>
<span data-ttu-id="8de68-112">Art der Adresse.</span><span class="sxs-lookup"><span data-stu-id="8de68-112">Type of Address.</span></span> <span data-ttu-id="8de68-113">Verfügbare Werte: AddressType. None (Standard), AddressType. Residential, AddressType. Commercial</span><span class="sxs-lookup"><span data-stu-id="8de68-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="8de68-114">-Ort</span><span class="sxs-lookup"><span data-stu-id="8de68-114">-City</span></span>
<span data-ttu-id="8de68-115">Name des Orts.</span><span class="sxs-lookup"><span data-stu-id="8de68-115">Name of the City.</span></span> <span data-ttu-id="8de68-116">Ex: San Francisco</span><span class="sxs-lookup"><span data-stu-id="8de68-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="8de68-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="8de68-117">-CompanyName</span></span>
<span data-ttu-id="8de68-118">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="8de68-118">Name of the company</span></span>

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

### <span data-ttu-id="8de68-119">-Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="8de68-119">-ContactName</span></span>
<span data-ttu-id="8de68-120">Name des Kontakts</span><span class="sxs-lookup"><span data-stu-id="8de68-120">Contact Name</span></span>

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

### <span data-ttu-id="8de68-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="8de68-121">-CountryCode</span></span>
<span data-ttu-id="8de68-122">Landesvorwahl.</span><span class="sxs-lookup"><span data-stu-id="8de68-122">Country Code.</span></span> <span data-ttu-id="8de68-123">Ex: US</span><span class="sxs-lookup"><span data-stu-id="8de68-123">Ex: US</span></span>

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

### <span data-ttu-id="8de68-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="8de68-124">-DataBoxType</span></span>
<span data-ttu-id="8de68-125">SKU-Typ von DataBox.</span><span class="sxs-lookup"><span data-stu-id="8de68-125">Sku type of Databox.</span></span>  <span data-ttu-id="8de68-126">Verfügbare Werte: DataBoxDisk, DataBox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="8de68-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="8de68-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de68-127">-DefaultProfile</span></span>
<span data-ttu-id="8de68-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8de68-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8de68-129">-E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="8de68-129">-EmailId</span></span>
<span data-ttu-id="8de68-130">Eine Liste der EmailIds kann bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8de68-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="8de68-131">Mindestens eine ist obligatorisch</span><span class="sxs-lookup"><span data-stu-id="8de68-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="8de68-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="8de68-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="8de68-133">Für DataBoxDisk-Reihenfolge ist die Angabe der erwarteten Daten in Terabyte obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="8de68-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="8de68-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="8de68-134">-Location</span></span>
<span data-ttu-id="8de68-135">Standort des Abonnements</span><span class="sxs-lookup"><span data-stu-id="8de68-135">Location of the subscription</span></span>

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

### <span data-ttu-id="8de68-136">-Name</span><span class="sxs-lookup"><span data-stu-id="8de68-136">-Name</span></span>
<span data-ttu-id="8de68-137">Name des zu erstellende DataBox-Auftrags</span><span class="sxs-lookup"><span data-stu-id="8de68-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="8de68-138">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="8de68-138">-PhoneNumber</span></span>
<span data-ttu-id="8de68-139">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="8de68-139">Contact Number</span></span> 

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

### <span data-ttu-id="8de68-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="8de68-140">-PostalCode</span></span>
<span data-ttu-id="8de68-141">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="8de68-141">Postal Code</span></span>

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

### <span data-ttu-id="8de68-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de68-142">-ResourceGroupName</span></span>
<span data-ttu-id="8de68-143">Der Ressourcengruppen Name, unter dem der DataBox-Auftrag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8de68-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="8de68-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="8de68-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="8de68-145">Geben Sie den Code für Bundesland oder Kanton ein.</span><span class="sxs-lookup"><span data-stu-id="8de68-145">Input the state or province code.</span></span> <span data-ttu-id="8de68-146">Wie CA-Kalifornien; FL-Florida; NY-New York</span><span class="sxs-lookup"><span data-stu-id="8de68-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="8de68-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8de68-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="8de68-148">Liste der Ressourcen-IDs von Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="8de68-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="8de68-149">Mindestens eine ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="8de68-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="8de68-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="8de68-150">-StreetAddress1</span></span>
<span data-ttu-id="8de68-151">Straßenanschrift</span><span class="sxs-lookup"><span data-stu-id="8de68-151">Street Address</span></span>

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

### <span data-ttu-id="8de68-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="8de68-152">-StreetAddress2</span></span>
<span data-ttu-id="8de68-153">Zusätzliche Anschrift</span><span class="sxs-lookup"><span data-stu-id="8de68-153">Additional Street Address</span></span>

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

### <span data-ttu-id="8de68-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="8de68-154">-StreetAddress3</span></span>
<span data-ttu-id="8de68-155">Zusätzliche Anschrift</span><span class="sxs-lookup"><span data-stu-id="8de68-155">Additional Street Address</span></span>

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

### <span data-ttu-id="8de68-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8de68-156">-Confirm</span></span>
<span data-ttu-id="8de68-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8de68-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de68-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de68-158">-WhatIf</span></span>
<span data-ttu-id="8de68-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8de68-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8de68-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8de68-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de68-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de68-161">CommonParameters</span></span>
<span data-ttu-id="8de68-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de68-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de68-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8de68-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de68-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8de68-164">INPUTS</span></span>

### <span data-ttu-id="8de68-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="8de68-165">System.String[]</span></span>

## <span data-ttu-id="8de68-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8de68-166">OUTPUTS</span></span>

### <span data-ttu-id="8de68-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="8de68-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="8de68-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="8de68-168">NOTES</span></span>

## <span data-ttu-id="8de68-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8de68-169">RELATED LINKS</span></span>
