---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471624"
---
# <span data-ttu-id="c77c7-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="c77c7-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="c77c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c77c7-102">SYNOPSIS</span></span>
<span data-ttu-id="c77c7-103">Aktualisiert die Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="c77c7-103">Updates the service topology.</span></span>

## <span data-ttu-id="c77c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c77c7-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c77c7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c77c7-105">DESCRIPTION</span></span>
<span data-ttu-id="c77c7-106">Das **Cmdlet "Set-AzDeploymentManagerServiceTopology"** aktualisiert eine Diensttopologie mit dem angegebenen Diensttopologieobjekt.</span><span class="sxs-lookup"><span data-stu-id="c77c7-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="c77c7-107">Das Cmdlet gibt das aktualisierte Diensttopologieobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c77c7-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="c77c7-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c77c7-108">EXAMPLES</span></span>

### <span data-ttu-id="c77c7-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c77c7-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="c77c7-110">Mit diesem Befehl wird eine Diensttopologie aktualisiert, deren Name und Ressourcengruppe mit den Eigenschaften "Name" bzw. "ResourceGroupName" des $serviceTopologyObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c77c7-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="c77c7-111">Der Befehl gibt das aktualisierte Diensttopologieobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c77c7-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="c77c7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c77c7-112">PARAMETERS</span></span>

### <span data-ttu-id="c77c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c77c7-113">-DefaultProfile</span></span>
<span data-ttu-id="c77c7-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c77c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c77c7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c77c7-115">-InputObject</span></span>
<span data-ttu-id="c77c7-116">Das Diensttopologieobjekt.</span><span class="sxs-lookup"><span data-stu-id="c77c7-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c77c7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c77c7-117">-Confirm</span></span>
<span data-ttu-id="c77c7-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c77c7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c77c7-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c77c7-119">-WhatIf</span></span>
<span data-ttu-id="c77c7-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c77c7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c77c7-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c77c7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c77c7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c77c7-122">CommonParameters</span></span>
<span data-ttu-id="c77c7-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c77c7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c77c7-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c77c7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c77c7-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c77c7-125">INPUTS</span></span>

### <span data-ttu-id="c77c7-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="c77c7-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="c77c7-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c77c7-127">OUTPUTS</span></span>

### <span data-ttu-id="c77c7-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="c77c7-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="c77c7-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c77c7-129">NOTES</span></span>

## <span data-ttu-id="c77c7-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c77c7-130">RELATED LINKS</span></span>
