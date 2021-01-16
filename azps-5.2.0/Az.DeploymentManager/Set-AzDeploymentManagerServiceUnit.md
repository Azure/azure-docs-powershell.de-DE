---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294550"
---
# <span data-ttu-id="39a73-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="39a73-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="39a73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39a73-102">SYNOPSIS</span></span>
<span data-ttu-id="39a73-103">Aktualisiert die Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="39a73-103">Updates the service unit.</span></span>

## <span data-ttu-id="39a73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39a73-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39a73-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39a73-105">DESCRIPTION</span></span>
<span data-ttu-id="39a73-106">Das **Cmdlet "Set-AzDeploymentManagerServiceUnit"** aktualisiert eine Diensteinheit mit dem angegebenen Diensteinheitsobjekt.</span><span class="sxs-lookup"><span data-stu-id="39a73-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="39a73-107">Das Cmdlet gibt das aktualisierte Diensteinheitsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="39a73-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="39a73-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39a73-108">EXAMPLES</span></span>

### <span data-ttu-id="39a73-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39a73-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="39a73-110">Mit diesem Befehl wird eine Diensteinheit aktualisiert, deren Name, Dienstname, Name der Diensttopologie und Ressourcengruppe mit den Eigenschaften "Name", "ServiceName", "ServiceTopologyName" bzw. "ResourceGroupName" der $serviceUnitObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="39a73-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="39a73-111">Der Befehl gibt das aktualisierte Diensteinheitsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="39a73-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="39a73-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39a73-112">PARAMETERS</span></span>

### <span data-ttu-id="39a73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a73-113">-DefaultProfile</span></span>
<span data-ttu-id="39a73-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39a73-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39a73-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39a73-115">-InputObject</span></span>
<span data-ttu-id="39a73-116">Das Diensteinheitsobjekt.</span><span class="sxs-lookup"><span data-stu-id="39a73-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39a73-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39a73-117">-Confirm</span></span>
<span data-ttu-id="39a73-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39a73-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39a73-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="39a73-119">-WhatIf</span></span>
<span data-ttu-id="39a73-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39a73-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39a73-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39a73-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39a73-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a73-122">CommonParameters</span></span>
<span data-ttu-id="39a73-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39a73-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a73-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39a73-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a73-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39a73-125">INPUTS</span></span>

### <span data-ttu-id="39a73-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="39a73-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="39a73-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39a73-127">OUTPUTS</span></span>

### <span data-ttu-id="39a73-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="39a73-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="39a73-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39a73-129">NOTES</span></span>

## <span data-ttu-id="39a73-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39a73-130">RELATED LINKS</span></span>
