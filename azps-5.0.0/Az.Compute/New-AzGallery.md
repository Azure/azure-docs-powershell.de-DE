---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176449"
---
# <span data-ttu-id="22073-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="22073-101">New-AzGallery</span></span>

## <span data-ttu-id="22073-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22073-102">SYNOPSIS</span></span>
<span data-ttu-id="22073-103">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="22073-103">Create a gallery.</span></span>

## <span data-ttu-id="22073-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22073-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22073-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22073-105">DESCRIPTION</span></span>
<span data-ttu-id="22073-106">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="22073-106">Create a gallery.</span></span>

## <span data-ttu-id="22073-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22073-107">EXAMPLES</span></span>

### <span data-ttu-id="22073-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22073-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="22073-109">Erstellen eines Katalogs</span><span class="sxs-lookup"><span data-stu-id="22073-109">Create a gallery.</span></span>

## <span data-ttu-id="22073-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22073-110">PARAMETERS</span></span>

### <span data-ttu-id="22073-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22073-111">-AsJob</span></span>
<span data-ttu-id="22073-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="22073-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22073-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22073-113">-DefaultProfile</span></span>
<span data-ttu-id="22073-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22073-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22073-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22073-115">-Description</span></span>
<span data-ttu-id="22073-116">Die Beschreibung der Katalog Ressource.</span><span class="sxs-lookup"><span data-stu-id="22073-116">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22073-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="22073-117">-Location</span></span>
<span data-ttu-id="22073-118">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="22073-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22073-119">-Name</span><span class="sxs-lookup"><span data-stu-id="22073-119">-Name</span></span>
<span data-ttu-id="22073-120">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="22073-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22073-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22073-121">-ResourceGroupName</span></span>
<span data-ttu-id="22073-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="22073-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="22073-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="22073-123">-Tag</span></span>
<span data-ttu-id="22073-124">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="22073-124">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22073-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="22073-125">-Confirm</span></span>
<span data-ttu-id="22073-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22073-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22073-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22073-127">-WhatIf</span></span>
<span data-ttu-id="22073-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22073-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22073-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22073-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22073-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22073-130">CommonParameters</span></span>
<span data-ttu-id="22073-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22073-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22073-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22073-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22073-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22073-133">INPUTS</span></span>

### <span data-ttu-id="22073-134">System. String</span><span class="sxs-lookup"><span data-stu-id="22073-134">System.String</span></span>

### <span data-ttu-id="22073-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22073-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22073-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22073-136">OUTPUTS</span></span>

### <span data-ttu-id="22073-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="22073-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="22073-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="22073-138">NOTES</span></span>

## <span data-ttu-id="22073-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22073-139">RELATED LINKS</span></span>
