---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472433"
---
# <span data-ttu-id="45b22-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="45b22-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="45b22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45b22-102">SYNOPSIS</span></span>
<span data-ttu-id="45b22-103">Löscht eine IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="45b22-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="45b22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45b22-104">SYNTAX</span></span>

### <span data-ttu-id="45b22-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="45b22-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b22-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45b22-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b22-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="45b22-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45b22-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45b22-108">DESCRIPTION</span></span>
<span data-ttu-id="45b22-109">Löscht eine vorhandene IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="45b22-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="45b22-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45b22-110">EXAMPLES</span></span>

### <span data-ttu-id="45b22-111">Beispiel 1 Delete and IoT Central Application</span><span class="sxs-lookup"><span data-stu-id="45b22-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="45b22-112">Löscht die bereitgestellte IoT-Zentralanwendung.</span><span class="sxs-lookup"><span data-stu-id="45b22-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="45b22-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45b22-113">PARAMETERS</span></span>

### <span data-ttu-id="45b22-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45b22-114">-AsJob</span></span>
<span data-ttu-id="45b22-115">Führen Sie das Cmdlet als Aufgabe im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="45b22-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="45b22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b22-116">-DefaultProfile</span></span>
<span data-ttu-id="45b22-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45b22-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45b22-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45b22-118">-InputObject</span></span>
<span data-ttu-id="45b22-119">Iot Central Application Input Object.</span><span class="sxs-lookup"><span data-stu-id="45b22-119">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="45b22-120">-Name</span><span class="sxs-lookup"><span data-stu-id="45b22-120">-Name</span></span>
<span data-ttu-id="45b22-121">Name der zentralen Anwendungsressource "Iot".</span><span class="sxs-lookup"><span data-stu-id="45b22-121">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="45b22-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45b22-122">-PassThru</span></span>
<span data-ttu-id="45b22-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="45b22-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="45b22-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b22-124">-ResourceGroupName</span></span>
<span data-ttu-id="45b22-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="45b22-125">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="45b22-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45b22-126">-ResourceId</span></span>
<span data-ttu-id="45b22-127">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="45b22-127">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="45b22-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45b22-128">-Confirm</span></span>
<span data-ttu-id="45b22-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45b22-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b22-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="45b22-130">-WhatIf</span></span>
<span data-ttu-id="45b22-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45b22-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45b22-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45b22-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b22-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b22-133">CommonParameters</span></span>
<span data-ttu-id="45b22-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b22-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b22-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45b22-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b22-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45b22-136">INPUTS</span></span>

### <span data-ttu-id="45b22-137">System.String</span><span class="sxs-lookup"><span data-stu-id="45b22-137">System.String</span></span>

### <span data-ttu-id="45b22-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="45b22-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="45b22-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45b22-139">OUTPUTS</span></span>

### <span data-ttu-id="45b22-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45b22-140">System.Boolean</span></span>

## <span data-ttu-id="45b22-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45b22-141">NOTES</span></span>

## <span data-ttu-id="45b22-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45b22-142">RELATED LINKS</span></span>
