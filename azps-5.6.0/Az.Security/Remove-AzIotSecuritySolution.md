---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: da98138060b0c06e09a56b375c64f530ea8e51f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934659"
---
# <span data-ttu-id="1c1fe-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="1c1fe-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="1c1fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="1c1fe-103">Löschen der IoT-Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="1c1fe-103">Delete IoT security solution</span></span>

## <span data-ttu-id="1c1fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c1fe-104">SYNTAX</span></span>

### <span data-ttu-id="1c1fe-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c1fe-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c1fe-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c1fe-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c1fe-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1c1fe-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c1fe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c1fe-108">DESCRIPTION</span></span>
<span data-ttu-id="1c1fe-109">Das Remove-AzIotSecuritySolution-Cmdlet löscht eine bestimmte iot-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="1c1fe-110">Die IoT-Sicherheitslösung sammelt Sicherheitsdaten und -Ereignisse von iot-Geräten und iot-Hubs, um Bedrohungen zu verhindern und zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="1c1fe-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1c1fe-111">EXAMPLES</span></span>

### <span data-ttu-id="1c1fe-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c1fe-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="1c1fe-113">Löschen der IoT-Sicherheitslösung "MySample" mit der Ressourcengruppe "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="1c1fe-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="1c1fe-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1c1fe-114">PARAMETERS</span></span>

### <span data-ttu-id="1c1fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c1fe-115">-DefaultProfile</span></span>
<span data-ttu-id="1c1fe-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c1fe-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c1fe-117">-InputObject</span></span>
<span data-ttu-id="1c1fe-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1fe-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1c1fe-119">-Name</span></span>
<span data-ttu-id="1c1fe-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1fe-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c1fe-121">-PassThru</span></span>
<span data-ttu-id="1c1fe-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="1c1fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c1fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c1fe-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1fe-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c1fe-125">-ResourceId</span></span>
<span data-ttu-id="1c1fe-126">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1fe-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c1fe-127">-Confirm</span></span>
<span data-ttu-id="1c1fe-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c1fe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c1fe-129">-WhatIf</span></span>
<span data-ttu-id="1c1fe-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c1fe-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c1fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c1fe-132">CommonParameters</span></span>
<span data-ttu-id="1c1fe-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c1fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c1fe-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c1fe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c1fe-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1c1fe-135">INPUTS</span></span>

### <span data-ttu-id="1c1fe-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1c1fe-136">System.String</span></span>

### <span data-ttu-id="1c1fe-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="1c1fe-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="1c1fe-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1c1fe-138">OUTPUTS</span></span>

### <span data-ttu-id="1c1fe-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1c1fe-139">System.Boolean</span></span>

## <span data-ttu-id="1c1fe-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1c1fe-140">NOTES</span></span>

## <span data-ttu-id="1c1fe-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1c1fe-141">RELATED LINKS</span></span>
