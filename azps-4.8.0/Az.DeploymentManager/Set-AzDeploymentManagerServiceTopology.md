---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008530"
---
# <span data-ttu-id="42b96-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="42b96-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="42b96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42b96-102">SYNOPSIS</span></span>
<span data-ttu-id="42b96-103">Aktualisiert die Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="42b96-103">Updates the service topology.</span></span>

## <span data-ttu-id="42b96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42b96-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42b96-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42b96-105">DESCRIPTION</span></span>
<span data-ttu-id="42b96-106">Das Cmdlet " **Satz-AzDeploymentManagerServiceTopology** " aktualisiert eine Dienst Topologie mit dem angegebenen Dienst Topologie-Objekt.</span><span class="sxs-lookup"><span data-stu-id="42b96-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="42b96-107">Das Cmdlet gibt das aktualisierte Dienst Topologie-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="42b96-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="42b96-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42b96-108">EXAMPLES</span></span>

### <span data-ttu-id="42b96-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42b96-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="42b96-110">Mit diesem Befehl wird eine Dienst Topologie aktualisiert, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $serviceTopologyObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="42b96-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="42b96-111">Der Befehl gibt das aktualisierte Dienst Topologie-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="42b96-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="42b96-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="42b96-112">PARAMETERS</span></span>

### <span data-ttu-id="42b96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b96-113">-DefaultProfile</span></span>
<span data-ttu-id="42b96-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42b96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42b96-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42b96-115">-InputObject</span></span>
<span data-ttu-id="42b96-116">Das Service Topology-Objekt.</span><span class="sxs-lookup"><span data-stu-id="42b96-116">The service topology object.</span></span>

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

### <span data-ttu-id="42b96-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42b96-117">-Confirm</span></span>
<span data-ttu-id="42b96-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42b96-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42b96-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42b96-119">-WhatIf</span></span>
<span data-ttu-id="42b96-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42b96-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42b96-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42b96-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42b96-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b96-122">CommonParameters</span></span>
<span data-ttu-id="42b96-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b96-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b96-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42b96-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b96-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42b96-125">INPUTS</span></span>

### <span data-ttu-id="42b96-126">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="42b96-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="42b96-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42b96-127">OUTPUTS</span></span>

### <span data-ttu-id="42b96-128">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="42b96-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="42b96-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="42b96-129">NOTES</span></span>

## <span data-ttu-id="42b96-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42b96-130">RELATED LINKS</span></span>
