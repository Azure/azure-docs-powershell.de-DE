---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165033"
---
# <span data-ttu-id="07cf8-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="07cf8-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="07cf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="07cf8-103">Generiert einen Zugriffsschlüssel für einen SignalR-Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="07cf8-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="07cf8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07cf8-104">SYNTAX</span></span>

### <span data-ttu-id="07cf8-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="07cf8-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07cf8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07cf8-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07cf8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07cf8-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07cf8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07cf8-108">DESCRIPTION</span></span>
<span data-ttu-id="07cf8-109">Generiert einen Zugriffsschlüssel für einen SignalR-Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="07cf8-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="07cf8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07cf8-110">EXAMPLES</span></span>

### <span data-ttu-id="07cf8-111">Neuererieren des Primärschlüssels</span><span class="sxs-lookup"><span data-stu-id="07cf8-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="07cf8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07cf8-112">PARAMETERS</span></span>

### <span data-ttu-id="07cf8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07cf8-113">-DefaultProfile</span></span>
<span data-ttu-id="07cf8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07cf8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07cf8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07cf8-115">-InputObject</span></span>
<span data-ttu-id="07cf8-116">Das SignalR-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="07cf8-116">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07cf8-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="07cf8-117">-KeyType</span></span>
<span data-ttu-id="07cf8-118">Der Schlüsseltyp, entweder "Primär" oder "Sekundär".</span><span class="sxs-lookup"><span data-stu-id="07cf8-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cf8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="07cf8-119">-Name</span></span>
<span data-ttu-id="07cf8-120">Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="07cf8-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cf8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07cf8-121">-PassThru</span></span>
<span data-ttu-id="07cf8-122">Gibt "true" zurück, wenn die Begnung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="07cf8-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="07cf8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07cf8-123">-ResourceGroupName</span></span>
<span data-ttu-id="07cf8-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="07cf8-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cf8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07cf8-125">-ResourceId</span></span>
<span data-ttu-id="07cf8-126">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="07cf8-126">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07cf8-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07cf8-127">-Confirm</span></span>
<span data-ttu-id="07cf8-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07cf8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07cf8-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="07cf8-129">-WhatIf</span></span>
<span data-ttu-id="07cf8-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07cf8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07cf8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07cf8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07cf8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07cf8-132">CommonParameters</span></span>
<span data-ttu-id="07cf8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07cf8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07cf8-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07cf8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07cf8-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07cf8-135">INPUTS</span></span>

### <span data-ttu-id="07cf8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="07cf8-136">System.String</span></span>
### <span data-ttu-id="07cf8-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="07cf8-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="07cf8-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07cf8-138">OUTPUTS</span></span>

### <span data-ttu-id="07cf8-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07cf8-139">System.Boolean</span></span>
## <span data-ttu-id="07cf8-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="07cf8-140">NOTES</span></span>

## <span data-ttu-id="07cf8-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="07cf8-141">RELATED LINKS</span></span>
