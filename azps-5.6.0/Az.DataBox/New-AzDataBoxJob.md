---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 2c78f8b40621ba58b84169f2bd9022399fce80b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942976"
---
# <span data-ttu-id="9395f-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="9395f-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="9395f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9395f-102">SYNOPSIS</span></span>
<span data-ttu-id="9395f-103">Erstellt einen neuen Databoxauftrag mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="9395f-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="9395f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9395f-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9395f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9395f-105">DESCRIPTION</span></span>
<span data-ttu-id="9395f-106">Das **Cmdlet New-AzDataBoxJob** wird zum Erstellen eines neuen Databoxauftrags verwendet, indem die details angegeben werden, die für die Erstellung des Auftrags erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9395f-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="9395f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9395f-107">EXAMPLES</span></span>

### <span data-ttu-id="9395f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9395f-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="9395f-109">Das Cmdlet verwendet alle erforderlichen Parameter und einige optionale Parameter, um den Databoxauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9395f-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="9395f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9395f-110">PARAMETERS</span></span>

### <span data-ttu-id="9395f-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="9395f-111">-AddressType</span></span>
<span data-ttu-id="9395f-112">Typ der Adresse.</span><span class="sxs-lookup"><span data-stu-id="9395f-112">Type of Address.</span></span> <span data-ttu-id="9395f-113">Verfügbare Werte: AddressType.None (Standard), AddressType.Residential, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="9395f-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="9395f-114">-Ort</span><span class="sxs-lookup"><span data-stu-id="9395f-114">-City</span></span>
<span data-ttu-id="9395f-115">Name der Stadt.</span><span class="sxs-lookup"><span data-stu-id="9395f-115">Name of the City.</span></span> <span data-ttu-id="9395f-116">Beispiel: San Francisco</span><span class="sxs-lookup"><span data-stu-id="9395f-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="9395f-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="9395f-117">-CompanyName</span></span>
<span data-ttu-id="9395f-118">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="9395f-118">Name of the company</span></span>

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

### <span data-ttu-id="9395f-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="9395f-119">-ContactName</span></span>
<span data-ttu-id="9395f-120">Kontaktname</span><span class="sxs-lookup"><span data-stu-id="9395f-120">Contact Name</span></span>

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

### <span data-ttu-id="9395f-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="9395f-121">-CountryCode</span></span>
<span data-ttu-id="9395f-122">Ländercode.</span><span class="sxs-lookup"><span data-stu-id="9395f-122">Country Code.</span></span> <span data-ttu-id="9395f-123">Beispiel: USA</span><span class="sxs-lookup"><span data-stu-id="9395f-123">Ex: US</span></span>

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

### <span data-ttu-id="9395f-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="9395f-124">-DataBoxType</span></span>
<span data-ttu-id="9395f-125">Sku-Typ von Databox.</span><span class="sxs-lookup"><span data-stu-id="9395f-125">Sku type of Databox.</span></span>  <span data-ttu-id="9395f-126">Verfügbare Werte: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="9395f-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="9395f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9395f-127">-DefaultProfile</span></span>
<span data-ttu-id="9395f-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9395f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9395f-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="9395f-129">-EmailId</span></span>
<span data-ttu-id="9395f-130">Eine Liste der E-Mail-Ids kann bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9395f-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="9395f-131">Atleast one is mandatory</span><span class="sxs-lookup"><span data-stu-id="9395f-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="9395f-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="9395f-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="9395f-133">Für die Reihenfolge von DataBoxDisk ist die Angabe der erwarteten Daten in Terabytes obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="9395f-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="9395f-134">-Location</span><span class="sxs-lookup"><span data-stu-id="9395f-134">-Location</span></span>
<span data-ttu-id="9395f-135">Speicherort des Abonnements</span><span class="sxs-lookup"><span data-stu-id="9395f-135">Location of the subscription</span></span>

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

### <span data-ttu-id="9395f-136">-Name</span><span class="sxs-lookup"><span data-stu-id="9395f-136">-Name</span></span>
<span data-ttu-id="9395f-137">Name des zu erstellende Databoxauftrags</span><span class="sxs-lookup"><span data-stu-id="9395f-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="9395f-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="9395f-138">-PhoneNumber</span></span>
<span data-ttu-id="9395f-139">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="9395f-139">Contact Number</span></span> 

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

### <span data-ttu-id="9395f-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="9395f-140">-PostalCode</span></span>
<span data-ttu-id="9395f-141">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="9395f-141">Postal Code</span></span>

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

### <span data-ttu-id="9395f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9395f-142">-ResourceGroupName</span></span>
<span data-ttu-id="9395f-143">Ressourcengruppenname, unter dem der Datenfeldauftrag erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="9395f-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="9395f-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="9395f-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="9395f-145">Geben Sie den Landes- oder Kantonscode ein.</span><span class="sxs-lookup"><span data-stu-id="9395f-145">Input the state or province code.</span></span> <span data-ttu-id="9395f-146">Wie CA – Kalifornien; FL – Florida; NY - New York</span><span class="sxs-lookup"><span data-stu-id="9395f-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="9395f-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9395f-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="9395f-148">Liste der Ressourcen-Ids von Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="9395f-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="9395f-149">Atleast one is mandatory.</span><span class="sxs-lookup"><span data-stu-id="9395f-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="9395f-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="9395f-150">-StreetAddress1</span></span>
<span data-ttu-id="9395f-151">Adresse der Straße</span><span class="sxs-lookup"><span data-stu-id="9395f-151">Street Address</span></span>

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

### <span data-ttu-id="9395f-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="9395f-152">-StreetAddress2</span></span>
<span data-ttu-id="9395f-153">Zusätzliche Anschrift</span><span class="sxs-lookup"><span data-stu-id="9395f-153">Additional Street Address</span></span>

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

### <span data-ttu-id="9395f-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="9395f-154">-StreetAddress3</span></span>
<span data-ttu-id="9395f-155">Zusätzliche Anschrift</span><span class="sxs-lookup"><span data-stu-id="9395f-155">Additional Street Address</span></span>

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

### <span data-ttu-id="9395f-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9395f-156">-Confirm</span></span>
<span data-ttu-id="9395f-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9395f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9395f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9395f-158">-WhatIf</span></span>
<span data-ttu-id="9395f-159">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9395f-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9395f-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9395f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9395f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9395f-161">CommonParameters</span></span>
<span data-ttu-id="9395f-162">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9395f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9395f-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9395f-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9395f-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9395f-164">INPUTS</span></span>

### <span data-ttu-id="9395f-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9395f-165">System.String[]</span></span>

## <span data-ttu-id="9395f-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9395f-166">OUTPUTS</span></span>

### <span data-ttu-id="9395f-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="9395f-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="9395f-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9395f-168">NOTES</span></span>

## <span data-ttu-id="9395f-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9395f-169">RELATED LINKS</span></span>
