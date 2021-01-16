---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298499"
---
# <span data-ttu-id="f0860-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="f0860-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="f0860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0860-102">SYNOPSIS</span></span>
<span data-ttu-id="f0860-103">Erstellen Sie einen neuen Azure DevSpaces-Controller.</span><span class="sxs-lookup"><span data-stu-id="f0860-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="f0860-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0860-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0860-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0860-105">DESCRIPTION</span></span>
<span data-ttu-id="f0860-106">Erstellen Sie einen neuen Azure DevSpaces-Controller.</span><span class="sxs-lookup"><span data-stu-id="f0860-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="f0860-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0860-107">EXAMPLES</span></span>

### <span data-ttu-id="f0860-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0860-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="f0860-109">Erstellen Sie einen DevSpaces-Controller in der Ressourcengruppe devSpaceResourceGroup mit einem Namen "devSpaceName".</span><span class="sxs-lookup"><span data-stu-id="f0860-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="f0860-110">Verwenden Sie clusterName Cluster als Ziel für diesen Controller.</span><span class="sxs-lookup"><span data-stu-id="f0860-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="f0860-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0860-111">PARAMETERS</span></span>

### <span data-ttu-id="f0860-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0860-112">-AsJob</span></span>
<span data-ttu-id="f0860-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f0860-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0860-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0860-114">-DefaultProfile</span></span>
<span data-ttu-id="f0860-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0860-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0860-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f0860-116">-Name</span></span>
<span data-ttu-id="f0860-117">DevSpaces-Controllername.</span><span class="sxs-lookup"><span data-stu-id="f0860-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0860-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0860-118">-ResourceGroupName</span></span>
<span data-ttu-id="f0860-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f0860-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0860-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0860-120">-Tag</span></span>
<span data-ttu-id="f0860-121">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f0860-121">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0860-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="f0860-122">-TargetClusterName</span></span>
<span data-ttu-id="f0860-123">Name des Zielclusters.</span><span class="sxs-lookup"><span data-stu-id="f0860-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0860-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0860-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="f0860-125">Name der Zielressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0860-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0860-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0860-126">-Confirm</span></span>
<span data-ttu-id="f0860-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0860-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0860-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f0860-128">-WhatIf</span></span>
<span data-ttu-id="f0860-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0860-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0860-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0860-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0860-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0860-131">CommonParameters</span></span>
<span data-ttu-id="f0860-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0860-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0860-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0860-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0860-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0860-134">INPUTS</span></span>

### <span data-ttu-id="f0860-135">Keine</span><span class="sxs-lookup"><span data-stu-id="f0860-135">None</span></span>

## <span data-ttu-id="f0860-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0860-136">OUTPUTS</span></span>

### <span data-ttu-id="f0860-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="f0860-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="f0860-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f0860-138">NOTES</span></span>

## <span data-ttu-id="f0860-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f0860-139">RELATED LINKS</span></span>
