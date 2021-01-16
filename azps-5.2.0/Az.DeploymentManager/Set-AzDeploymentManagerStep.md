---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294539"
---
# <span data-ttu-id="f95ac-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f95ac-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f95ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f95ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f95ac-103">Aktualisiert den Schritt.</span><span class="sxs-lookup"><span data-stu-id="f95ac-103">Updates the step.</span></span>

## <span data-ttu-id="f95ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f95ac-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f95ac-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f95ac-105">DESCRIPTION</span></span>
<span data-ttu-id="f95ac-106">Das **Cmdlet "Set-AzDeploymentManagerStep"** aktualisiert einen Schritt mit dem angegebenen Schrittobjekt.</span><span class="sxs-lookup"><span data-stu-id="f95ac-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="f95ac-107">Das Cmdlet gibt das aktualisierte Schrittobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f95ac-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="f95ac-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f95ac-108">EXAMPLES</span></span>

### <span data-ttu-id="f95ac-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f95ac-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="f95ac-110">Mit diesem Befehl wird ein Schritt aktualisiert, dessen Name und Ressourcengruppe den Eigenschaften "Name" bzw. "ResourceGroupName" des $stepObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f95ac-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="f95ac-111">Der Schritt wird auf die eigenschaften aktualisiert, die in der Liste $stepObject.</span><span class="sxs-lookup"><span data-stu-id="f95ac-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="f95ac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f95ac-112">PARAMETERS</span></span>

### <span data-ttu-id="f95ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95ac-113">-DefaultProfile</span></span>
<span data-ttu-id="f95ac-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f95ac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f95ac-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f95ac-115">-InputObject</span></span>
<span data-ttu-id="f95ac-116">Das Schrittobjekt.</span><span class="sxs-lookup"><span data-stu-id="f95ac-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ac-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f95ac-117">-Confirm</span></span>
<span data-ttu-id="f95ac-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f95ac-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95ac-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f95ac-119">-WhatIf</span></span>
<span data-ttu-id="f95ac-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f95ac-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f95ac-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f95ac-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95ac-122">CommonParameters</span></span>
<span data-ttu-id="f95ac-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95ac-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f95ac-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95ac-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f95ac-125">INPUTS</span></span>

### <span data-ttu-id="f95ac-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f95ac-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f95ac-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f95ac-127">OUTPUTS</span></span>

### <span data-ttu-id="f95ac-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f95ac-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f95ac-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f95ac-129">NOTES</span></span>

## <span data-ttu-id="f95ac-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f95ac-130">RELATED LINKS</span></span>
