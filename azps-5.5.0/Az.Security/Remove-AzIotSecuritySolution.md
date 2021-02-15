---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174236"
---
# <span data-ttu-id="d1156-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d1156-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="d1156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1156-102">SYNOPSIS</span></span>
<span data-ttu-id="d1156-103">Löschen der Sicherheitslösung für IoT</span><span class="sxs-lookup"><span data-stu-id="d1156-103">Delete IoT security solution</span></span>

## <span data-ttu-id="d1156-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1156-104">SYNTAX</span></span>

### <span data-ttu-id="d1156-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1156-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1156-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1156-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1156-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d1156-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1156-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1156-108">DESCRIPTION</span></span>
<span data-ttu-id="d1156-109">Das Remove-AzIotSecuritySolution cmdlet löscht eine bestimmte iot-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="d1156-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="d1156-110">Die Sicherheitslösung für das Internet (IoT) sammelt Sicherheitsdaten und Ereignisse von iot-Geräten und dem iot-Hub, um Bedrohungen zu verhindern und zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="d1156-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="d1156-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d1156-111">EXAMPLES</span></span>

### <span data-ttu-id="d1156-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1156-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d1156-113">Löschen der IoT-Sicherheitslösung "MySample" mit der Ressourcengruppe "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="d1156-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="d1156-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1156-114">PARAMETERS</span></span>

### <span data-ttu-id="d1156-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1156-115">-DefaultProfile</span></span>
<span data-ttu-id="d1156-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1156-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1156-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1156-117">-InputObject</span></span>
<span data-ttu-id="d1156-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="d1156-118">Input Object.</span></span>

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

### <span data-ttu-id="d1156-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d1156-119">-Name</span></span>
<span data-ttu-id="d1156-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d1156-120">Resource name.</span></span>

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

### <span data-ttu-id="d1156-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1156-121">-PassThru</span></span>
<span data-ttu-id="d1156-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="d1156-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d1156-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1156-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1156-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d1156-124">Resource group name.</span></span>

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

### <span data-ttu-id="d1156-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1156-125">-ResourceId</span></span>
<span data-ttu-id="d1156-126">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="d1156-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d1156-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1156-127">-Confirm</span></span>
<span data-ttu-id="d1156-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1156-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1156-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d1156-129">-WhatIf</span></span>
<span data-ttu-id="d1156-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1156-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1156-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1156-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1156-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1156-132">CommonParameters</span></span>
<span data-ttu-id="d1156-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1156-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1156-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1156-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1156-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d1156-135">INPUTS</span></span>

### <span data-ttu-id="d1156-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d1156-136">System.String</span></span>

### <span data-ttu-id="d1156-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d1156-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="d1156-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d1156-138">OUTPUTS</span></span>

### <span data-ttu-id="d1156-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1156-139">System.Boolean</span></span>

## <span data-ttu-id="d1156-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d1156-140">NOTES</span></span>

## <span data-ttu-id="d1156-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d1156-141">RELATED LINKS</span></span>
