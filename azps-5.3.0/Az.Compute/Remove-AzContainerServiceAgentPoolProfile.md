---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470855"
---
# <span data-ttu-id="54408-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="54408-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="54408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54408-102">SYNOPSIS</span></span>
<span data-ttu-id="54408-103">Entfernt ein Agentpoolprofil aus einem Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="54408-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="54408-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54408-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54408-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54408-105">DESCRIPTION</span></span>
<span data-ttu-id="54408-106">Das **Cmdlet "Remove-AzContainerServiceAgentPoolProfile"** entfernt ein Agentpoolprofil aus einem Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="54408-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="54408-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54408-107">EXAMPLES</span></span>

### <span data-ttu-id="54408-108">Beispiel 1: Entfernen eines Profils aus einem Containerdienst</span><span class="sxs-lookup"><span data-stu-id="54408-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="54408-109">Der erste Befehl ruft einen Containerdienst namens CSResourceGroup17 mithilfe des Get-AzContainerService-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="54408-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="54408-110">Der Befehl speichert den Dienst in der $Container Variable.</span><span class="sxs-lookup"><span data-stu-id="54408-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="54408-111">Der zweite Befehl entfernt das Profil mit dem Namen "AgentPool01" aus dem Containerdienst in $Container.</span><span class="sxs-lookup"><span data-stu-id="54408-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="54408-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54408-112">PARAMETERS</span></span>

### <span data-ttu-id="54408-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="54408-113">-ContainerService</span></span>
<span data-ttu-id="54408-114">Gibt das Containerdienstobjekt an, aus dem dieses Cmdlet ein Agentpoolprofil entfernt.</span><span class="sxs-lookup"><span data-stu-id="54408-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54408-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54408-115">-DefaultProfile</span></span>
<span data-ttu-id="54408-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54408-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54408-117">-Name</span><span class="sxs-lookup"><span data-stu-id="54408-117">-Name</span></span>
<span data-ttu-id="54408-118">Gibt den Namen des Agentpoolprofils an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="54408-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54408-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54408-119">-Confirm</span></span>
<span data-ttu-id="54408-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54408-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54408-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="54408-121">-WhatIf</span></span>
<span data-ttu-id="54408-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54408-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54408-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54408-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54408-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54408-124">CommonParameters</span></span>
<span data-ttu-id="54408-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54408-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54408-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54408-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54408-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54408-127">INPUTS</span></span>

### <span data-ttu-id="54408-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="54408-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="54408-129">System.String</span><span class="sxs-lookup"><span data-stu-id="54408-129">System.String</span></span>

## <span data-ttu-id="54408-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54408-130">OUTPUTS</span></span>

### <span data-ttu-id="54408-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="54408-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="54408-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54408-132">NOTES</span></span>

## <span data-ttu-id="54408-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54408-133">RELATED LINKS</span></span>

[<span data-ttu-id="54408-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="54408-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="54408-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="54408-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


