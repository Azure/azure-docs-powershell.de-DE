---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: e401755786c8f1aaf967417f526c8a976b333048
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303928"
---
# <span data-ttu-id="e4c99-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e4c99-101">New-AzContainerService</span></span>

## <span data-ttu-id="e4c99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4c99-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c99-103">Erstellt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="e4c99-103">Creates a container service.</span></span>

## <span data-ttu-id="e4c99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4c99-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4c99-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4c99-105">DESCRIPTION</span></span>
<span data-ttu-id="e4c99-106">Das **Cmdlet "New-AzContainerService"** erstellt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="e4c99-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="e4c99-107">Geben Sie ein Containerdienstobjekt an, das Sie mithilfe des cmdlets New-AzContainerServiceConfig können.</span><span class="sxs-lookup"><span data-stu-id="e4c99-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="e4c99-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4c99-108">EXAMPLES</span></span>

### <span data-ttu-id="e4c99-109">Beispiel 1: Erstellen eines Containerdiensts</span><span class="sxs-lookup"><span data-stu-id="e4c99-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="e4c99-110">Der erste Befehl erstellt eine Ressourcengruppe namens "ResourceGroup17" am angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="e4c99-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="e4c99-111">Weitere Informationen finden Sie im New-AzResourceGroup Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c99-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e4c99-112">Der zweite Befehl erstellt einen Container und speichert ihn dann in der $Container Variable.</span><span class="sxs-lookup"><span data-stu-id="e4c99-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="e4c99-113">Weitere Informationen finden Sie im New-AzContainerServiceConfig Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c99-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="e4c99-114">Der letzte Befehl erstellt einen Containerdienst für den Container, der in der $Container.</span><span class="sxs-lookup"><span data-stu-id="e4c99-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="e4c99-115">Der Dienst hat den Namen "csResourceGroup17".</span><span class="sxs-lookup"><span data-stu-id="e4c99-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="e4c99-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4c99-116">PARAMETERS</span></span>

### <span data-ttu-id="e4c99-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4c99-117">-AsJob</span></span>
<span data-ttu-id="e4c99-118">Das Cmdlet "RRun" im Hintergrund und gibt einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="e4c99-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e4c99-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="e4c99-119">-ContainerService</span></span>
<span data-ttu-id="e4c99-120">Gibt ein Containerdienstobjekt an, das die Eigenschaften für den neuen Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="e4c99-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="e4c99-121">Verwenden Sie das **cmdlet New-AzContainerServiceConfig ContainerService,** um ein ContainerService-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e4c99-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="e4c99-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c99-122">-DefaultProfile</span></span>
<span data-ttu-id="e4c99-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4c99-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4c99-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e4c99-124">-Name</span></span>
<span data-ttu-id="e4c99-125">Gibt den Namen des Containerdiensts an, den dieses Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="e4c99-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e4c99-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c99-126">-ResourceGroupName</span></span>
<span data-ttu-id="e4c99-127">Gibt die Ressourcengruppe an, in der der Containerdienst von diesem Cmdlet bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e4c99-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="e4c99-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4c99-128">-Confirm</span></span>
<span data-ttu-id="e4c99-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4c99-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c99-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e4c99-130">-WhatIf</span></span>
<span data-ttu-id="e4c99-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4c99-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c99-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4c99-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c99-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c99-133">CommonParameters</span></span>
<span data-ttu-id="e4c99-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4c99-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c99-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4c99-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c99-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4c99-136">INPUTS</span></span>

### <span data-ttu-id="e4c99-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e4c99-137">System.String</span></span>

### <span data-ttu-id="e4c99-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e4c99-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e4c99-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4c99-139">OUTPUTS</span></span>

### <span data-ttu-id="e4c99-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e4c99-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e4c99-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e4c99-141">NOTES</span></span>

## <span data-ttu-id="e4c99-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e4c99-142">RELATED LINKS</span></span>

[<span data-ttu-id="e4c99-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e4c99-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="e4c99-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="e4c99-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="e4c99-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e4c99-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="e4c99-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e4c99-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


