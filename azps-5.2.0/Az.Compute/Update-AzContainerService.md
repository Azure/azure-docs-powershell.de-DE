---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372432"
---
# <span data-ttu-id="e7c61-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e7c61-101">Update-AzContainerService</span></span>

## <span data-ttu-id="e7c61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7c61-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c61-103">Aktualisiert den Zustand eines Containerdiensts.</span><span class="sxs-lookup"><span data-stu-id="e7c61-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="e7c61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7c61-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7c61-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7c61-105">DESCRIPTION</span></span>
<span data-ttu-id="e7c61-106">Das **Cmdlet "Update-AzContainerService"** aktualisiert den Zustand eines Containerdiensts, um einer lokalen Instanz des Diensts zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e7c61-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="e7c61-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7c61-107">EXAMPLES</span></span>

### <span data-ttu-id="e7c61-108">Beispiel 1: Aktualisieren eines Containerdiensts</span><span class="sxs-lookup"><span data-stu-id="e7c61-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="e7c61-109">Dieser Befehl ruft den Containerdienst mit dem Namen CSResourceGroup17 mithilfe des Get-AzContainerService-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="e7c61-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="e7c61-110">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators Remove-AzContainerServiceAgentPoolProfile an das Remove-AzContainerServiceAgentPoolProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7c61-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e7c61-111">**Remove-AzContainerServiceAgentPoolProfile** entfernt das Profil mit dem Namen "AgentPool01".</span><span class="sxs-lookup"><span data-stu-id="e7c61-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="e7c61-112">Der Befehl übergibt das Ergebnis an das Add-AzContainerServiceAgentPoolProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7c61-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="e7c61-113">**Add-AzContainerServiceAgentPoolProfile** fügt ein Profil mit dem Namen "AgentPool01" und den angegebenen Eigenschaften hinzu.</span><span class="sxs-lookup"><span data-stu-id="e7c61-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="e7c61-114">Der Befehl übergibt das Ergebnis an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7c61-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="e7c61-115">Das aktuelle Cmdlet aktualisiert den Containerdienst entsprechend den Änderungen, die in diesem Befehl vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="e7c61-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="e7c61-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7c61-116">PARAMETERS</span></span>

### <span data-ttu-id="e7c61-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7c61-117">-AsJob</span></span>
<span data-ttu-id="e7c61-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e7c61-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7c61-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="e7c61-119">-ContainerService</span></span>
<span data-ttu-id="e7c61-120">Gibt ein lokales **ContainerService-Objekt** an, das Änderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="e7c61-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c61-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c61-121">-DefaultProfile</span></span>
<span data-ttu-id="e7c61-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7c61-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7c61-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e7c61-123">-Name</span></span>
<span data-ttu-id="e7c61-124">Gibt den Namen des Containerdiensts an, der von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e7c61-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="e7c61-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7c61-125">-ResourceGroupName</span></span>
<span data-ttu-id="e7c61-126">Gibt die Ressourcengruppe des Containerdiensts an, der von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e7c61-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c61-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7c61-127">-Confirm</span></span>
<span data-ttu-id="e7c61-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7c61-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c61-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e7c61-129">-WhatIf</span></span>
<span data-ttu-id="e7c61-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7c61-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7c61-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7c61-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c61-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c61-132">CommonParameters</span></span>
<span data-ttu-id="e7c61-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c61-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c61-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7c61-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c61-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7c61-135">INPUTS</span></span>

### <span data-ttu-id="e7c61-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e7c61-136">System.String</span></span>

### <span data-ttu-id="e7c61-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e7c61-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e7c61-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7c61-138">OUTPUTS</span></span>

### <span data-ttu-id="e7c61-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e7c61-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e7c61-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e7c61-140">NOTES</span></span>

## <span data-ttu-id="e7c61-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e7c61-141">RELATED LINKS</span></span>

[<span data-ttu-id="e7c61-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e7c61-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="e7c61-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e7c61-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="e7c61-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e7c61-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="e7c61-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e7c61-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="e7c61-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e7c61-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


