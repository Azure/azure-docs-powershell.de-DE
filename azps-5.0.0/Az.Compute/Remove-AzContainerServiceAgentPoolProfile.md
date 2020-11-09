---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302073"
---
# <span data-ttu-id="df43c-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="df43c-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="df43c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df43c-102">SYNOPSIS</span></span>
<span data-ttu-id="df43c-103">Entfernt ein Profil eines Agenten Pools aus einem Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="df43c-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="df43c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df43c-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df43c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df43c-105">DESCRIPTION</span></span>
<span data-ttu-id="df43c-106">Das Cmdlet **Remove-AzContainerServiceAgentPoolProfile** entfernt ein Agenten Pool Profil aus einem Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="df43c-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="df43c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df43c-107">EXAMPLES</span></span>

### <span data-ttu-id="df43c-108">Beispiel 1: Entfernen eines Profils aus einem Containerdienst</span><span class="sxs-lookup"><span data-stu-id="df43c-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="df43c-109">Der erste Befehl ruft einen Containerdienst mit dem Namen CSResourceGroup17 mithilfe des Get-AzContainerService-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="df43c-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="df43c-110">Der Befehl speichert den Dienst in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="df43c-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="df43c-111">Der zweite Befehl entfernt das Profil mit dem Namen AgentPool01 aus dem Containerdienst in $Container.</span><span class="sxs-lookup"><span data-stu-id="df43c-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="df43c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="df43c-112">PARAMETERS</span></span>

### <span data-ttu-id="df43c-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="df43c-113">-ContainerService</span></span>
<span data-ttu-id="df43c-114">Gibt das Containerdienst Objekt an, aus dem dieses Cmdlet ein Agenten Pool Profil entfernt.</span><span class="sxs-lookup"><span data-stu-id="df43c-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="df43c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df43c-115">-DefaultProfile</span></span>
<span data-ttu-id="df43c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df43c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df43c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="df43c-117">-Name</span></span>
<span data-ttu-id="df43c-118">Gibt den Namen des Agenten Pool Profils an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="df43c-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="df43c-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df43c-119">-Confirm</span></span>
<span data-ttu-id="df43c-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df43c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df43c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df43c-121">-WhatIf</span></span>
<span data-ttu-id="df43c-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df43c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df43c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df43c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df43c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df43c-124">CommonParameters</span></span>
<span data-ttu-id="df43c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df43c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df43c-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df43c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df43c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df43c-127">INPUTS</span></span>

### <span data-ttu-id="df43c-128">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="df43c-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="df43c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="df43c-129">System.String</span></span>

## <span data-ttu-id="df43c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df43c-130">OUTPUTS</span></span>

### <span data-ttu-id="df43c-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="df43c-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="df43c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="df43c-132">NOTES</span></span>

## <span data-ttu-id="df43c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df43c-133">RELATED LINKS</span></span>

[<span data-ttu-id="df43c-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="df43c-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="df43c-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="df43c-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


