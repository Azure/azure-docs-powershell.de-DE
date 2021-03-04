---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 29a53b49e579ab337c2345a15c86c4c27aaffe8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942571"
---
# <span data-ttu-id="79c72-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="79c72-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="79c72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79c72-102">SYNOPSIS</span></span>
<span data-ttu-id="79c72-103">Löscht eine zentrale IoT-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="79c72-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="79c72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79c72-104">SYNTAX</span></span>

### <span data-ttu-id="79c72-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="79c72-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c72-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79c72-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c72-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="79c72-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79c72-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79c72-108">DESCRIPTION</span></span>
<span data-ttu-id="79c72-109">Löscht eine vorhandene IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="79c72-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="79c72-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79c72-110">EXAMPLES</span></span>

### <span data-ttu-id="79c72-111">Beispiel 1 Delete and IoT Central Application</span><span class="sxs-lookup"><span data-stu-id="79c72-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="79c72-112">Löscht die bereitgestellte IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="79c72-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="79c72-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="79c72-113">PARAMETERS</span></span>

### <span data-ttu-id="79c72-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79c72-114">-AsJob</span></span>
<span data-ttu-id="79c72-115">Führen Sie das Cmdlet als Auftrag im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="79c72-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="79c72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c72-116">-DefaultProfile</span></span>
<span data-ttu-id="79c72-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79c72-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79c72-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79c72-118">-InputObject</span></span>
<span data-ttu-id="79c72-119">Iot Central Application Input Object.</span><span class="sxs-lookup"><span data-stu-id="79c72-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79c72-120">-Name</span><span class="sxs-lookup"><span data-stu-id="79c72-120">-Name</span></span>
<span data-ttu-id="79c72-121">Name der zentralen Anwendungsressource Iot.</span><span class="sxs-lookup"><span data-stu-id="79c72-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c72-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79c72-122">-PassThru</span></span>
<span data-ttu-id="79c72-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="79c72-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="79c72-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c72-124">-ResourceGroupName</span></span>
<span data-ttu-id="79c72-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79c72-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c72-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79c72-126">-ResourceId</span></span>
<span data-ttu-id="79c72-127">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="79c72-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c72-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79c72-128">-Confirm</span></span>
<span data-ttu-id="79c72-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79c72-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c72-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c72-130">-WhatIf</span></span>
<span data-ttu-id="79c72-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79c72-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79c72-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79c72-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c72-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c72-133">CommonParameters</span></span>
<span data-ttu-id="79c72-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c72-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c72-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79c72-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c72-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79c72-136">INPUTS</span></span>

### <span data-ttu-id="79c72-137">System.String</span><span class="sxs-lookup"><span data-stu-id="79c72-137">System.String</span></span>

### <span data-ttu-id="79c72-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="79c72-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="79c72-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79c72-139">OUTPUTS</span></span>

### <span data-ttu-id="79c72-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79c72-140">System.Boolean</span></span>

## <span data-ttu-id="79c72-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="79c72-141">NOTES</span></span>

## <span data-ttu-id="79c72-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="79c72-142">RELATED LINKS</span></span>
