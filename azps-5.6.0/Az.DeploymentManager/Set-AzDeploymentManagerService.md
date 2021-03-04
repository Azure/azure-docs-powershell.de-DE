---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: 4c33ba2bd87e1f6103454740529c5570ef04ea17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925747"
---
# <span data-ttu-id="88127-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="88127-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="88127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88127-102">SYNOPSIS</span></span>
<span data-ttu-id="88127-103">Aktualisiert den Dienst.</span><span class="sxs-lookup"><span data-stu-id="88127-103">Updates the service.</span></span>

## <span data-ttu-id="88127-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88127-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88127-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88127-105">DESCRIPTION</span></span>
<span data-ttu-id="88127-106">Das **Cmdlet Set-AzDeploymentManagerService** aktualisiert einen Dienst mit dem angegebenen Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="88127-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="88127-107">Das Cmdlet gibt das aktualisierte Dienstobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="88127-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="88127-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88127-108">EXAMPLES</span></span>

### <span data-ttu-id="88127-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="88127-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="88127-110">Mit diesem Befehl wird ein Dienst aktualisiert, dessen Name, Diensttopologiename und Ressourcengruppe den Eigenschaften Name, ServiceTopologyName und ResourceGroupName des $serviceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="88127-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="88127-111">Der Dienst wird auf die eigenschaften aktualisiert, die in der Liste $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="88127-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="88127-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="88127-112">PARAMETERS</span></span>

### <span data-ttu-id="88127-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88127-113">-DefaultProfile</span></span>
<span data-ttu-id="88127-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88127-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88127-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88127-115">-InputObject</span></span>
<span data-ttu-id="88127-116">Das Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="88127-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88127-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88127-117">-Confirm</span></span>
<span data-ttu-id="88127-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88127-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88127-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88127-119">-WhatIf</span></span>
<span data-ttu-id="88127-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88127-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88127-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88127-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88127-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88127-122">CommonParameters</span></span>
<span data-ttu-id="88127-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88127-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88127-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88127-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88127-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88127-125">INPUTS</span></span>

### <span data-ttu-id="88127-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="88127-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="88127-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88127-127">OUTPUTS</span></span>

### <span data-ttu-id="88127-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="88127-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="88127-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="88127-129">NOTES</span></span>

## <span data-ttu-id="88127-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="88127-130">RELATED LINKS</span></span>
