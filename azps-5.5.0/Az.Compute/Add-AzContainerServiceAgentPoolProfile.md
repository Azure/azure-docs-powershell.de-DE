---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 8319a5bc0251e744ee898658b0a0a541f0ce86ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145017"
---
# <span data-ttu-id="4fd6a-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="4fd6a-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="4fd6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd6a-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd6a-103">Fügt ein Containerdienst-Agent-Poolprofil hinzu.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="4fd6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fd6a-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fd6a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4fd6a-105">DESCRIPTION</span></span>
<span data-ttu-id="4fd6a-106">Das **Cmdlet "Add-AzContainerServiceAgentPoolProfile"** fügt einem lokalen Containerdienstdienstobjekt ein Containerdienst-Agent-Poolprofil hinzu.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="4fd6a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4fd6a-107">EXAMPLES</span></span>

### <span data-ttu-id="4fd6a-108">Beispiel 1: Hinzufügen eines Profils</span><span class="sxs-lookup"><span data-stu-id="4fd6a-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="4fd6a-109">Dieser Befehl fügt dem lokalen Containerdienstdienstobjekt ein Containerdienst-Agent-Poolprofil hinzu.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="4fd6a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fd6a-110">PARAMETERS</span></span>

### <span data-ttu-id="4fd6a-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="4fd6a-111">-ContainerService</span></span>
<span data-ttu-id="4fd6a-112">Gibt das Containerdienstobjekt an, dem dieses Cmdlet ein Agentpoolprofil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="4fd6a-113">Verwenden Sie zum Abrufen eines **ContainerService-Objekts** [das Cmdlet "New-AzContainerServiceConfig".](./New-AzContainerServiceConfig.md)</span><span class="sxs-lookup"><span data-stu-id="4fd6a-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="4fd6a-114">-Count</span><span class="sxs-lookup"><span data-stu-id="4fd6a-114">-Count</span></span>
<span data-ttu-id="4fd6a-115">Gibt die Anzahl der Agents an, die Container hosten.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="4fd6a-116">Die zulässigen Werte für diesen Parameter sind: ganze Zahlen zwischen 1 und 100.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="4fd6a-117">Der Standardwert ist "1".</span><span class="sxs-lookup"><span data-stu-id="4fd6a-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd6a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd6a-118">-DefaultProfile</span></span>
<span data-ttu-id="4fd6a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fd6a-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="4fd6a-120">-DnsPrefix</span></span>
<span data-ttu-id="4fd6a-121">Gibt das DNS-Präfix an, mit dem dieses Cmdlet den vollqualifizierten Domänennamen für diesen Agentpool erstellt.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd6a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4fd6a-122">-Name</span></span>
<span data-ttu-id="4fd6a-123">Gibt den Namen des Agentpoolprofils an.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="4fd6a-124">Dieser Wert muss im Kontext des Abonnements und der Ressourcengruppe eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd6a-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="4fd6a-125">-VmSize</span></span>
<span data-ttu-id="4fd6a-126">Gibt die Größe der virtuellen Computer für die Agents an.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd6a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fd6a-127">-Confirm</span></span>
<span data-ttu-id="4fd6a-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd6a-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4fd6a-129">-WhatIf</span></span>
<span data-ttu-id="4fd6a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fd6a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd6a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd6a-132">CommonParameters</span></span>
<span data-ttu-id="4fd6a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd6a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd6a-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fd6a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd6a-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4fd6a-135">INPUTS</span></span>

### <span data-ttu-id="4fd6a-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="4fd6a-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="4fd6a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4fd6a-137">System.String</span></span>

### <span data-ttu-id="4fd6a-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4fd6a-138">System.Int32</span></span>

## <span data-ttu-id="4fd6a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4fd6a-139">OUTPUTS</span></span>

### <span data-ttu-id="4fd6a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="4fd6a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="4fd6a-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4fd6a-141">NOTES</span></span>

## <span data-ttu-id="4fd6a-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4fd6a-142">RELATED LINKS</span></span>

[<span data-ttu-id="4fd6a-143">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="4fd6a-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="4fd6a-144">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="4fd6a-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
