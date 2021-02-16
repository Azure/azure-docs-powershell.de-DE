---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163740"
---
# <span data-ttu-id="85105-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="85105-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="85105-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85105-102">SYNOPSIS</span></span>
<span data-ttu-id="85105-103">Aktualisiert den Dienst.</span><span class="sxs-lookup"><span data-stu-id="85105-103">Updates the service.</span></span>

## <span data-ttu-id="85105-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85105-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85105-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85105-105">DESCRIPTION</span></span>
<span data-ttu-id="85105-106">Das **Cmdlet "Set-AzDeploymentManagerService"** aktualisiert einen Dienst mit dem angegebenen Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="85105-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="85105-107">Das Cmdlet gibt das aktualisierte Dienstobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="85105-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="85105-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85105-108">EXAMPLES</span></span>

### <span data-ttu-id="85105-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85105-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="85105-110">Mit diesem Befehl wird ein Dienst aktualisiert, dessen Name, Name der Diensttopologie und Ressourcengruppe mit den Eigenschaften "Name", "ServiceTopologyName" und "ResourceGroupName" der $serviceObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="85105-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="85105-111">Der Dienst wird auf die eigenschaften aktualisiert, die in der Liste $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="85105-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="85105-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85105-112">PARAMETERS</span></span>

### <span data-ttu-id="85105-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85105-113">-DefaultProfile</span></span>
<span data-ttu-id="85105-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85105-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85105-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85105-115">-InputObject</span></span>
<span data-ttu-id="85105-116">Das Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="85105-116">The service object.</span></span>

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

### <span data-ttu-id="85105-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85105-117">-Confirm</span></span>
<span data-ttu-id="85105-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85105-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85105-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="85105-119">-WhatIf</span></span>
<span data-ttu-id="85105-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85105-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85105-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85105-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85105-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85105-122">CommonParameters</span></span>
<span data-ttu-id="85105-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85105-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85105-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85105-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85105-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85105-125">INPUTS</span></span>

### <span data-ttu-id="85105-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="85105-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="85105-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85105-127">OUTPUTS</span></span>

### <span data-ttu-id="85105-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="85105-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="85105-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85105-129">NOTES</span></span>

## <span data-ttu-id="85105-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85105-130">RELATED LINKS</span></span>
