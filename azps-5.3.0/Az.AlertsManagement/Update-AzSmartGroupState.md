---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469080"
---
# <span data-ttu-id="56c11-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="56c11-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="56c11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56c11-102">SYNOPSIS</span></span>
<span data-ttu-id="56c11-103">Aktualisiert den Status intelligenter Gruppen</span><span class="sxs-lookup"><span data-stu-id="56c11-103">Updates smart group state</span></span>

## <span data-ttu-id="56c11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56c11-104">SYNTAX</span></span>

### <span data-ttu-id="56c11-105">ByIdoGroupId (Standard)</span><span class="sxs-lookup"><span data-stu-id="56c11-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56c11-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="56c11-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56c11-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56c11-107">DESCRIPTION</span></span>
<span data-ttu-id="56c11-108">**Das Cmdlet "Update-AzLetsGroupState"** aktualisiert den intelligenten Gruppenzustand.</span><span class="sxs-lookup"><span data-stu-id="56c11-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="56c11-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56c11-109">EXAMPLES</span></span>

### <span data-ttu-id="56c11-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="56c11-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="56c11-111">Dieses Cmdlet aktualisiert den Status der intelligenten Gruppe auf "Acknowleged".</span><span class="sxs-lookup"><span data-stu-id="56c11-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="56c11-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56c11-112">PARAMETERS</span></span>

### <span data-ttu-id="56c11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c11-113">-DefaultProfile</span></span>
<span data-ttu-id="56c11-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56c11-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56c11-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56c11-115">-InputObject</span></span>
<span data-ttu-id="56c11-116">Eingabeobjekt aus pipeline.</span><span class="sxs-lookup"><span data-stu-id="56c11-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56c11-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="56c11-117">-SmartGroupId</span></span>
<span data-ttu-id="56c11-118">Eindeutiger Bezeichner einer intelligenten Gruppe/ResourceId einer intelligenten Gruppe.</span><span class="sxs-lookup"><span data-stu-id="56c11-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56c11-119">-State</span><span class="sxs-lookup"><span data-stu-id="56c11-119">-State</span></span>
<span data-ttu-id="56c11-120">Aktualisierter Status der intelligenten Gruppe</span><span class="sxs-lookup"><span data-stu-id="56c11-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="56c11-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56c11-121">-Confirm</span></span>
<span data-ttu-id="56c11-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56c11-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56c11-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="56c11-123">-WhatIf</span></span>
<span data-ttu-id="56c11-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56c11-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56c11-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56c11-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56c11-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c11-126">CommonParameters</span></span>
<span data-ttu-id="56c11-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c11-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c11-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56c11-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c11-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56c11-129">INPUTS</span></span>

### <span data-ttu-id="56c11-130">Keine</span><span class="sxs-lookup"><span data-stu-id="56c11-130">None</span></span>

## <span data-ttu-id="56c11-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56c11-131">OUTPUTS</span></span>

### <span data-ttu-id="56c11-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PS1Group</span><span class="sxs-lookup"><span data-stu-id="56c11-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="56c11-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="56c11-133">NOTES</span></span>

## <span data-ttu-id="56c11-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="56c11-134">RELATED LINKS</span></span>
