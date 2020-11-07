---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d39721f1a9ed243242bd08053f9a22f0ed53df30
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827423"
---
# <span data-ttu-id="71539-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="71539-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="71539-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71539-102">SYNOPSIS</span></span>
<span data-ttu-id="71539-103">Fügen Sie ein Bild einer virtuellen Computerplattform aus einer bestimmten Bild Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="71539-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="71539-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71539-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71539-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71539-105">DESCRIPTION</span></span>
<span data-ttu-id="71539-106">Hinzufügen eines Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="71539-106">Add a platform image.</span></span>

## <span data-ttu-id="71539-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71539-107">EXAMPLES</span></span>

### <span data-ttu-id="71539-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="71539-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="71539-109">Fügen Sie ein neues Platt Form Bild hinzu.</span><span class="sxs-lookup"><span data-stu-id="71539-109">Add a new platform image.</span></span>

## <span data-ttu-id="71539-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="71539-110">PARAMETERS</span></span>

### <span data-ttu-id="71539-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71539-111">-AsJob</span></span>
<span data-ttu-id="71539-112">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="71539-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="71539-113">-BillingPartNumber</span></span>
<span data-ttu-id="71539-114">Die Teilenummer wird verwendet, um die Software Kosten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="71539-114">The part number is used to bill for software costs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-115">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="71539-115">-DataDisks</span></span>
<span data-ttu-id="71539-116">Datenträger, die vom Platt Form Bild verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71539-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-117">-Force</span><span class="sxs-lookup"><span data-stu-id="71539-117">-Force</span></span>
<span data-ttu-id="71539-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="71539-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="71539-119">-Location</span></span>
<span data-ttu-id="71539-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="71539-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-121">-Angebot</span><span class="sxs-lookup"><span data-stu-id="71539-121">-Offer</span></span>
<span data-ttu-id="71539-122">Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="71539-122">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="71539-123">-OsType</span></span>
<span data-ttu-id="71539-124">Typ des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="71539-124">Operating system type.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="71539-125">-OsUri</span></span>
<span data-ttu-id="71539-126">Speicherort des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="71539-126">Location of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="71539-127">-Publisher</span></span>
<span data-ttu-id="71539-128">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="71539-128">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="71539-129">-Sku</span></span>
<span data-ttu-id="71539-130">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="71539-130">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-131">-Version</span><span class="sxs-lookup"><span data-stu-id="71539-131">-Version</span></span>
<span data-ttu-id="71539-132">Die Version des Bilds der virtuellen Computerplattform.</span><span class="sxs-lookup"><span data-stu-id="71539-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71539-133">-Confirm</span></span>
<span data-ttu-id="71539-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71539-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71539-135">-WhatIf</span></span>
<span data-ttu-id="71539-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71539-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71539-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71539-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71539-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71539-138">CommonParameters</span></span>
<span data-ttu-id="71539-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71539-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71539-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71539-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71539-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71539-141">INPUTS</span></span>

## <span data-ttu-id="71539-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71539-142">OUTPUTS</span></span>

### <span data-ttu-id="71539-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="71539-143">PlatformImageObject</span></span>

## <span data-ttu-id="71539-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="71539-144">NOTES</span></span>

## <span data-ttu-id="71539-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71539-145">RELATED LINKS</span></span>

