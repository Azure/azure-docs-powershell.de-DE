---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: 50708e5faebff03e63b0b6330bac66c2c409adda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651364"
---
# <span data-ttu-id="1c0e7-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="1c0e7-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="1c0e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c0e7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0e7-103">Erstellt einen Dienst unter der angegebenen Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="1c0e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c0e7-104">SYNTAX</span></span>

### <span data-ttu-id="1c0e7-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c0e7-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c0e7-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="1c0e7-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c0e7-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="1c0e7-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c0e7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c0e7-108">DESCRIPTION</span></span>
<span data-ttu-id="1c0e7-109">Das Cmdlet **New-AzDeploymentManagerService** erstellt einen Dienst unter einer Dienst Topologie und gibt ein Objekt zurück, das diesen Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="1c0e7-110">Geben Sie den Dienst nach dem Namen, der Dienst Topologie und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="1c0e7-111">Das Cmdlet gibt ein Dienstobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="1c0e7-112">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerService-Cmdlets Änderungen am Dienst vornehmen.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="1c0e7-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c0e7-113">EXAMPLES</span></span>

### <span data-ttu-id="1c0e7-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c0e7-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="1c0e7-115">Erstellt einen neuen Dienst mit dem Namen ContosoService1 unter Dienst Topologie ContosoServiceTopology in der Ressourcengruppe ContosoResourceGroup, in der zentrale US-Adresse.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="1c0e7-116">Die Zielstandort-Eigenschaft gibt an, dass der Dienst ContosoService1 in der Region East US im angegebenen Abonnement bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="1c0e7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c0e7-117">PARAMETERS</span></span>

### <span data-ttu-id="1c0e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0e7-118">-DefaultProfile</span></span>
<span data-ttu-id="1c0e7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c0e7-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="1c0e7-120">-Location</span></span>
<span data-ttu-id="1c0e7-121">Der Speicherort der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-121">The location of the service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0e7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1c0e7-122">-Name</span></span>
<span data-ttu-id="1c0e7-123">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-123">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0e7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c0e7-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c0e7-125">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0e7-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="1c0e7-126">-ServiceTopologyId</span></span>
<span data-ttu-id="1c0e7-127">Der Dienst Topologie-Ressourcenbezeichner, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-127">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0e7-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="1c0e7-128">-ServiceTopologyName</span></span>
<span data-ttu-id="1c0e7-129">Der Name der Dienst Topologie, zu der dieser Dienst gehört.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-129">The name of the service topology this service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0e7-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="1c0e7-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="1c0e7-131">Das Dienst Topologie-Objekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-131">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0e7-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c0e7-132">-Tag</span></span>
<span data-ttu-id="1c0e7-133">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0e7-134">-Zielstandort</span><span class="sxs-lookup"><span data-stu-id="1c0e7-134">-TargetLocation</span></span>
<span data-ttu-id="1c0e7-135">Bestimmt den Standort, in dem Ressourcen unter dem Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-135">Determines the location where resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0e7-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c0e7-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="1c0e7-137">Bestimmt das Abonnement, für das Ressourcen unter dem Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0e7-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c0e7-138">-Confirm</span></span>
<span data-ttu-id="1c0e7-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c0e7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c0e7-140">-WhatIf</span></span>
<span data-ttu-id="1c0e7-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c0e7-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c0e7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0e7-143">CommonParameters</span></span>
<span data-ttu-id="1c0e7-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0e7-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c0e7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0e7-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c0e7-146">INPUTS</span></span>

### <span data-ttu-id="1c0e7-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1c0e7-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1c0e7-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c0e7-148">OUTPUTS</span></span>

### <span data-ttu-id="1c0e7-149">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="1c0e7-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="1c0e7-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c0e7-150">NOTES</span></span>

## <span data-ttu-id="1c0e7-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c0e7-151">RELATED LINKS</span></span>
