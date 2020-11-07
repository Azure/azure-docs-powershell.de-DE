---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0390c3f55c444b4a0e37e25c93536b60d10bc7b1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827488"
---
# <span data-ttu-id="c52a2-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="c52a2-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="c52a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c52a2-102">SYNOPSIS</span></span>
<span data-ttu-id="c52a2-103">Erstellen Sie ein neues Abbild der virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="c52a2-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="c52a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c52a2-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c52a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c52a2-105">DESCRIPTION</span></span>
<span data-ttu-id="c52a2-106">Erstellen Sie ein Bild für eine Virtual Machine-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c52a2-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="c52a2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c52a2-107">EXAMPLES</span></span>

### <span data-ttu-id="c52a2-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c52a2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="c52a2-109">Fügen Sie eine neue Plattform-Bild Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="c52a2-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="c52a2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c52a2-110">PARAMETERS</span></span>

### <span data-ttu-id="c52a2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c52a2-111">-AsJob</span></span>
<span data-ttu-id="c52a2-112">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c52a2-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c52a2-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="c52a2-113">-ComputeRole</span></span>
<span data-ttu-id="c52a2-114">Der Typ der Rolle, IaaS oder PaaS, die von dieser Erweiterung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c52a2-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="c52a2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c52a2-115">-Force</span></span>
<span data-ttu-id="c52a2-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c52a2-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c52a2-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="c52a2-117">-IsSystemExtension</span></span>
<span data-ttu-id="c52a2-118">Gibt an, ob die Erweiterung für das System gilt.</span><span class="sxs-lookup"><span data-stu-id="c52a2-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="c52a2-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="c52a2-119">-Location</span></span>
<span data-ttu-id="c52a2-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c52a2-120">Location of the resource.</span></span>

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

### <span data-ttu-id="c52a2-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c52a2-121">-Publisher</span></span>
<span data-ttu-id="c52a2-122">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="c52a2-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="c52a2-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="c52a2-123">-SourceBlob</span></span>
<span data-ttu-id="c52a2-124">Erweiterungspaket für URI-zu-Virtual-Machine</span><span class="sxs-lookup"><span data-stu-id="c52a2-124">URI to virtual machine extension package.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a2-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="c52a2-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="c52a2-126">True, wenn mehrere Erweiterungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c52a2-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="c52a2-127">-Typ</span><span class="sxs-lookup"><span data-stu-id="c52a2-127">-Type</span></span>
<span data-ttu-id="c52a2-128">Der Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c52a2-128">Type of extension.</span></span>

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

### <span data-ttu-id="c52a2-129">-Version</span><span class="sxs-lookup"><span data-stu-id="c52a2-129">-Version</span></span>
<span data-ttu-id="c52a2-130">Die Version der vritual-Computerabbild Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c52a2-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="c52a2-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="c52a2-131">-VmOsType</span></span>
<span data-ttu-id="c52a2-132">Der für die Bereitstellung des Erweiterungs Handlers erforderliche Betriebssystemtyp des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c52a2-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="c52a2-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="c52a2-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="c52a2-134">Wert, der angibt, ob die Erweiterung für die Unterstützung von Skalierungs Sätzen für virtuelle Maschinen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c52a2-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="c52a2-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c52a2-135">-Confirm</span></span>
<span data-ttu-id="c52a2-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c52a2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c52a2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c52a2-137">-WhatIf</span></span>
<span data-ttu-id="c52a2-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c52a2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c52a2-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c52a2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c52a2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52a2-140">CommonParameters</span></span>
<span data-ttu-id="c52a2-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c52a2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52a2-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c52a2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52a2-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c52a2-143">INPUTS</span></span>

## <span data-ttu-id="c52a2-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c52a2-144">OUTPUTS</span></span>

### <span data-ttu-id="c52a2-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="c52a2-145">VmExtensionObject</span></span>

## <span data-ttu-id="c52a2-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="c52a2-146">NOTES</span></span>

## <span data-ttu-id="c52a2-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c52a2-147">RELATED LINKS</span></span>

